# V1 API

## About the V1 API

(Original: https://docs.snyk.io/snyk-api/v1-api#about-the-v1-api)

The Snyk API is available only for Enterprise plans.

For more information, see [Plans and pricing](https://snyk.io/plans).

The V1 API will be deprecated eventually, as further Snyk developments are now focused on the REST API.

The V1 API enables you to test a package for issues as they are defined by Snyk, and to automate Snyk processes to accomplish your specific workflows. Customers and partners can perform functions including:

* Accessing vulnerability data
* Scanning Projects and applications
* Receiving remediation advice
* Viewing user data to build custom security solutions

The V1 API endpoints are available in the [Reference](https://docs.snyk.io/snyk-api/reference).

***

## API URLs

(Original: https://docs.snyk.io/snyk-api/v1-api#api-urls)

Snyk is hosted in the following regions. Each region has its own base URL.

| Region     | Base URL                     |
| ---------- | ---------------------------- |
| SNYK-US-01 | `https://api.snyk.io/v1/`    |
| SNYK-US-02 | `https://api.us.snyk.io/v1/` |
| SNYK-EU-01 | `https://api.eu.snyk.io/v1/` |
| SNYK-AU-01 | `https://api.au.snyk.io/v1/` |

This API is available only over HTTPS. Calling the API over HTTP will yield a 404 for all requests.

***

## Authorization

(Original: https://docs.snyk.io/snyk-api/v1-api#authorization)

To use this API, you must get your token from Snyk. You can find the token in your [personal account settings](https://snyk.io/account/) after you register with Snyk and log in. For details, see [Authentication for API](https://docs.snyk.io/snyk-api/authentication-for-api).

Provide the token in an `Authorization` header with the token, preceded by `token`:

```http
Authorization: token API_KEY
```

If the token is not provided or is invalid, a 401 "Unauthorized" response will be returned:

```http
HTTP/1.1 401 Unauthorized

{
    "code": 401,
    "error": "Not authorised",
    "message": "Not authorised"
}
```

***

## Rate limiting

(Original: https://docs.snyk.io/snyk-api/v1-api#rate-limiting)

Snyk limits the requests to the V1 API to help provide a stable experience for customers.

The V1 API has a default rate limit of **2,000 requests per minute**, but some specific endpoints have lower limits. Refer to the reference docs for each endpoint to see the rate limits.

If you exceed the rate limit, you will receive a `429` error response.

***

## Errors

(Original: https://docs.snyk.io/snyk-api/v1-api#errors)

The V1 API uses standard HTTP error codes for error responses. Example 404-style error body:

```json
{
    "code": 404,
    "message": "Org 39db46b1-ad57-47e6-a87d-e34f6968030b was not found or you may not have the correct permissions to access the org.",
    "error": "Org 39db46b1-ad57-47e6-a87d-e34f6968030b was not found or you may not have the correct permissions to access the org."
}
```

The error reference is also supplied in the `x-error-reference` header in the server reply.

Example `500` response headers:

```http
HTTP/1.1 500 Internal Server Error
x-error-reference: a45ec9c1-065b-4f7b-baf8-dbd1552ffc9f
Content-Type: application/json; charset=utf-8
Content-Length: 1848
Vary: Accept-Encoding
Date: Sun, 10 Sep 2017 06:48:40 GMT
```

***

Last updated: 9 months ago

Was this helpful?
