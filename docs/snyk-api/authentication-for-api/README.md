# Authentication for API

To use the Snyk API, you must be an Enterprise plan customer and have a token from Snyk.

Use the URL for your region when calling an API. See https://docs.snyk.io/snyk-api/rest-api/about-the-rest-api#api-urls

Enterprise users have access to a personal token under their profile (https://docs.snyk.io/snyk-api/authentication-for-api#how-to-obtain-your-personal-token) and to service account tokens. The personal API token is associated with your Snyk Account and not with a specific Organization. Service accounts are associated with an Organization or a Group. For more information, see https://docs.snyk.io/implementation-and-setup/enterprise-setup/service-accounts

{% hint style="warning" %}
Enterprise users should use a service account to authenticate for any kind of automation. This includes, but is not limited to, CI/CD scanning with the CLI or build system plugins and any automation, including automation with the API.
{% endhint %}

{% hint style="info" %}
Enterprise users should use the personal token under their user profile for:

* Running the CLI locally on their machine; for details, see https://docs.snyk.io/developer-tools/snyk-cli/authenticate-to-use-the-cli
* Authenticating with the IDE manually
* Running API calls one time, for example, to test something
{% endhint %}

Note that for free and team plan users, the personal token does not have access to the API and may be used for authenticating to IDE, CLI, and CI/CD integrations only. For details, see https://docs.snyk.io/discover-snyk/getting-started#obtain-and-use-your-snyk-api-token

For additional information, see https://docs.snyk.io/snyk-api/authentication-for-api/snyk-api-token-permissions-users-can-control

***

## How to obtain your personal token

You can find your personal API token in your personal account settings: https://app.snyk.io/account after you register with Snyk and log in. In the **key** field, Click to show. Then highlight and copy the API key.

If you want a new API token, select **Revoke & Regenerate.** This will make the previous API token invalid. For details, see https://docs.snyk.io/snyk-api/authentication-for-api/revoke-and-regenerate-a-snyk-api-token

***

## Authenticating with a personal API token

When using the API directly, provide the API token in an `Authorization: token` header. Example (replace `API_TOKEN` with your token):

```bash
curl --request GET \
--url "https://api.snyk.io/rest/self?version=2024-06-10" \
--header "Content-Type: application/vnd.api+json" \
--header "Authorization: token API_TOKEN"
```

***

## Authenticating for Snyk Apps

If you are using the Snyk Apps APIs (https://docs.snyk.io/snyk-api/using-specific-snyk-apis/snyk-apps-apis), provide the `access_token` in an `Authorization: bearer` header as follows (replace `API_TOKEN` with your token):

```bash
curl --request GET \
--url "https://api.snyk.io/rest/self?version=2024-06-10" \
--header "Content-Type: application/vnd.api+json" \
--header "Authorization: bearer API_TOKEN"
```

Otherwise, a `401 Unauthorized` error will be returned.

***

Related:

* Previous: https://docs.snyk.io/snyk-api/v1-api
* Next: https://docs.snyk.io/snyk-api/authentication-for-api/snyk-api-token-permissions-users-can-control

Last updated 8 months ago.
