# About the REST API

The Snyk REST API is based on the [JSON:API standard](https://jsonapi.org/), defined in [OpenAPI 3.0.3](https://spec.openapis.org/oas/v3.0.3.html), and represents an evolutionary approach to API development, with each endpoint versioned. For more information, see the [Versioning](about-the-rest-api.md#versioning) section.

## API URLs

Snyk is hosted in the following regions. Each region has its own base URL. Use the URL for your region when calling an API.

| Region     | Base URL                      |
| ---------- | ----------------------------- |
| SNYK-US-01 | `https://api.snyk.io/rest`    |
| SNYK-US-02 | `https://api.us.snyk.io/rest` |
| SNYK-EU-01 | `https://api.eu.snyk.io/rest` |
| SNYK-AU-01 | `https://api.au.snyk.io/rest` |

{% hint style="warning" %}
This API is available only over HTTPS. Calling this API over HTTP will yield a 404 for all requests.
{% endhint %}

## JSON:API Content-Type header

The Snyk REST API generally adheres to the [JSON:API standard](https://jsonapi.org/), with some [caveats](https://github.com/snyk/sweater-comb/blob/main/docs/principles/jsonapi.md). When using the REST API, send all requests which contain data with the header:

```http
Content-Type: application/vnd.api+json
```

Otherwise a 400 "Bad Request" response will be returned. Example response:

```http
HTTP/1.1 400 Bad Request

{
    "errors": [
        {
            "status": "400",
            "detail": "Client request did not conform to OpenAPI specification",
            ...
        }
    ]
}
```

## Versioning

### Using versions dated on or after 2024-10-15

The API Reference examples include `?version=text` as a placeholder, where `text` represents the required date-formatted version string. Snyk recommends using `2024-10-15` for the version number unless you are using an earlier version for a specific reason. You can use the current day's date; this will call the most recent version of the API. The format for the date is `YYYY-MM-DD`.

### Using versions dated prior to 2024-10-15

The following applies to calling versions earlier than 2024-10-15. The Snyk REST API has per-endpoint version contracts. For information about differences in GA versions, see the [API Changelog](https://docs.snyk.io/snyk-api/changelog). Each endpoint can have its own release and support lifecycle, independent of other endpoints.

In its most explicit form, the endpoint version number includes a date and stability tree, for example:

```
2023-11-27~beta
```

This version number indicates that the requested endpoint should be at stability level `2023-11-27` or older `beta`. The possible stability levels are:

* `ga` — Generally Available, the default. Snyk will support these for at least six months after the next GA release.
* `beta` — Beta. Snyk will support these for at least three months after the next beta or GA release.
* `experimental` — Experimental. An experimental endpoint should be considered unstable and regarded as a tech preview. Experimental versions may introduce breaking changes and may be discontinued at any time.

In the default case of Generally Available, there is no stability level specified in the version number itself (only the date), for example:

```
2023-11-27
```

This means the requested endpoint should be 2023-11-27 or older on the Generally Available stability tree.

When the requested endpoint is at a specific stability level, Snyk serves the latest version released on or before the requested date, or that stability or higher. For example, if an endpoint has a beta version at `2023-09-29` and GA version at `2024-01-23`, and the requested endpoint is after `2024-01-23~beta`, Snyk resolves to the GA version.

After an endpoint is marked as deprecated, it will contain a `Sunset` header indicating the date at which that endpoint contract will no longer be supported. For example:

```http
Sunset: "2021-11-11"
```

## Pagination

All endpoints in the Snyk REST API are paginated using cursor-based pagination. Cursor-based pagination helps prevent inconsistent results when collections are modified while being iterated. However, it does not completely prevent inconsistent results (for example, if an item is inserted in a prior page based on the requested sort order after a request is made).

To mitigate inconsistent results, by default Snyk sorts by insertion order, so it is not possible to have items inserted on a prior page. If you specify the `sort` parameter, consistent pagination is no longer guaranteed. If you see inconsistent results, submit a new request. If consistent pagination is important, use the default insertion sort order.

API responses include appropriate links in the body for pagination, for example:

```json
{
    "data": [ ... ],
    "links": {
        "prev": "/orgs/123-abc-def-456/projects?version=2024-06-10&ending_before=v1.eyJpZCI6Mz1zODQyMH0%3D",
        "next": "/orgs/123-abc-def-456/projects?version=2024-06-10&starting_after=v1.eyJpZCI6Mz1zODQyMH0%3D"
    }
}
```

These links contain pre-defined parameters to make pagination easy. The parameters are:

* `starting_after`: an opaque Snyk internal blob that tells Snyk the last record you have seen and that you want records after this last one
* `ending_before`: an opaque Snyk internal blob that tells Snyk the first record you have seen and that you want records before this first one
* `limit`: the number of records per page

## Errors

Errors conform to the JSON:API specification and include path-based information to indicate the root cause. Example:

```json
{
    "errors": [
        {
            "id": "0418e907-a89e-4736-9a5b-91a2022e0899",
            "detail": "Unknown query parameter 'unknown'",
            "status": "400",
            "source": {
                "parameter": "unknown"
            }
        }
    ]
}
```

## Rate limiting

There is a limit of 1620 requests per minute, per API key. All requests above the limit will receive status code `429` — Too Many Requests — until requests stop for the duration of the rate-limiting interval (one minute).

From time to time, Snyk may introduce new rate limits to maintain overall system health. This is not considered a breaking change. All clients are expected to handle `429` responses correctly; such requests can be retried later safely.
