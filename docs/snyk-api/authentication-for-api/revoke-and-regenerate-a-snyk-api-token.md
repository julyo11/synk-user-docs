# Revoke and regenerate a Snyk API token

{% hint style="warning" %}
When an API token is revoked, all integrations using that key immediately stop working. Proceed with caution!

If you suspect an API token has been leaked, it is good practice to revoke that token and generate a new one to use in its place.
{% endhint %}

{% stepper %}
{% step %}
### Go to your account settings

Navigate to your personal General Account Settings in the Snyk Web UI at https://app.snyk.io/account.
{% endstep %}

{% step %}
### Revoke & regenerate the token

Click the **Revoke & Regenerate** button to revoke your API token. A new one will be generated in its place.
{% endstep %}

{% step %}
### Update your integrations

Copy the newly generated API token and update any integrations that used the old token so they continue to work.
{% endstep %}
{% endstepper %}

![](../../.gitbook/assets/image)

API token screen, Revoke & Regenerate button

For more details on API token permissions, see: https://docs.snyk.io/snyk-api/authentication-for-api/snyk-api-token-permissions-users-can-control
