# Getting started with the REST API

{% stepper %}
{% step %}
### Log in

Log in to [Snyk](https://snyk.io/).
{% endstep %}

{% step %}
### Choose an Organization

In your account, use the left navigation to find an **Organization** where you have Projects you can list.
{% endstep %}

{% step %}
### Get your Organization ID

Navigate to your **Organization Settings**, and on the **General** settings page, find your **Organization ID** and copy the value.
{% endstep %}

{% step %}
### Get your API token

Navigate to your personal [General Account Settings](https://app.snyk.io/account/) and copy your **API Token**. For instructions, see [Authentication for API](https://docs.snyk.io/snyk-api/authentication-for-api).
{% endstep %}

{% step %}
### Make the API request with curl

Replace `{orgId}` and `API_TOKEN` with your **Organization ID** and **API Token**, respectively. Snyk recommends using `2024-10-15` for the `version` query parameter unless you are using an earlier version for a specific reason. Using the current day's date will call the most recent version of the API.

{% code title="curl command" %}
```bash
curl --request GET \
--url "https://api.snyk.io/rest/orgs/{orgId}/projects?version=2024-10-15" \
--header "Content-Type: application/vnd.api+json" \
--header "Authorization: token API_TOKEN"
```
{% endcode %}
{% endstep %}
{% endstepper %}

{% hint style="info" %}
The API URL varies by region. For a complete list, see [API URLs](about-the-rest-api.md#api-urls).
{% endhint %}

As an example, the SNYK-US-02 region API URLs are:

* **API V1:** https://api.us.snyk.io/v1/
* **REST API:** https://api.us.snyk.io/rest/

{% hint style="warning" %}
If you use the `target-reference` parameter, you must URL-encode its value.
{% endhint %}

If you have any problems or questions, contact [Snyk support](https://support.snyk.io/).
