# Snyk release process

{% hint style="info" %}
Not all features follow all these stages, and timelines for each feature vary.
{% endhint %}

## Feature release stages

Snyk features are provided to users in the following release stages.

<table><thead><tr><th>Stage</th><th width="195.8680419921875">Description</th><th>Available to</th><th>Access</th><th>Docs</th></tr></thead><tbody><tr><td>Alpha</td><td>Internal release only</td><td>Snyk internal users, potentially some design partners</td><td>Controlled</td><td>No documentation provided</td></tr><tr><td>Closed Beta</td><td>The first customer-facing rollout of a feature</td><td>A preselected group of users</td><td>Invitation only</td><td>Provided but not public</td></tr><tr><td>Early Access</td><td>Feature is tested and ready for use, but not available by default. See <a href="snyk-release-process.md#early-access-features">Early Access features</a></td><td>All users on an opt-in basis. This may include some additional purchase costs</td><td>Opt-in: on request through Snyk account team, or using Snyk Preview</td><td>Public documentation</td></tr><tr><td>General Availability</td><td>Feature is fully enabled</td><td>All users, subject to standard feature availability</td><td>Available by default</td><td>Public documentation</td></tr></tbody></table>

## Feature lifecycle stages

<table><thead><tr><th>Stage</th><th>Description</th><th width="131.5997314453125">Available to</th><th>Access</th><th>Docs</th></tr></thead><tbody><tr><td>Deprecated</td><td>The feature is available, but use is discouraged. See <a href="snyk-release-process.md#deprecated-features">Deprecated features</a></td><td>Active users only</td><td>Available by default</td><td>Public documentation, with the Release status at the top of the page</td></tr><tr><td>End of support</td><td>No new support tickets will be answered. See <a href="snyk-release-process.md#end-of-support-features">End of support features</a></td><td>Active users only</td><td>Available by default</td><td>Public documentation, with the Release status at the top of the page</td></tr><tr><td>End of Life</td><td>The feature is no longer available</td><td>No users</td><td>Not available</td><td>No documentation available</td></tr></tbody></table>

## Brownouts

Brownouts occur when Snyk temporarily suspends an API endpoint or a feature, making it unavailable for use. This situation indicates that the resource or service is still operational, but its performance is reduced compared to its normal or expected capacity.

## Features status

### Early Access features

* [Snyk GitHub Cloud App](/broken/pages/mAsNuoNuZyD3AM0hMELI)
* [Automatically created Project collections](/broken/pages/xooIFeWjfseW9mDxUubU)
* [Fix code vulnerabilities automatically](/broken/pages/pEZ1aw9qJSIj3NddeyoQ)
* Risk Management
  * [Risk Score](/broken/pages/pf9Z3Rqd97IAaA4P12rU)
  * [Reachability analysis](/broken/pages/KomNA2dYi3p7VjqA6HB8)
* Universal Broker
* Language support
  * [Improved .NET scanning](../../supported-languages/supported-languages-list/.net/improved-.net-scanning.md)
  * [Snyk CLI pnpm support](../../supported-languages/supported-languages-list/javascript/#support-for-pnpm)
  * [Improved Gradle SCM scanning](../../supported-languages-package-managers-and-frameworks/java-and-kotlin/git-repositories-with-maven-and-gradle.md#improved-gradle-scm-scanning)
* Reports
  * [Repositories tested in CI/CD report](/broken/pages/fLpYTxz79MgYV44FXKoS)
  * [PCI-DSS v4.0.1 report](/broken/pages/fLpYTxz79MgYV44FXKoS#pci-dss-v4.0.1-report)

### Deprecated features

Deprecated features are outdated and will be removed in the future. The documentation page will announce the transition of a feature to Deprecated six months before its start date.

* Snyk Code Quality is deprecated.
* Snyk Code Local Engine is deprecated.
* Apps API has the following deprecated endpoints:
  * **Revoke app bot authorization** endpoint
    * The [Revoke app bot authorization](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#deprecated-revoke-app-bot-authorization) endpoint is deprecated.
    * Use the [Revoke app authorization for a Snyk Group with install ID](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#revoke-app-authorization-for-a-snyk-group-with-install-id) endpoint.
  * **Create a new app for an organization** endpoint
    * The [Create a new app for an organization](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#deprecated-create-a-new-app-for-an-organization) endpoint is deprecated.
    * Use the [Create a new Snyk App for an organization](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#create-a-new-snyk-app-for-an-organization) endpoint.
  * **Get a list of apps created by an organization** endpoint
    * The [Get a list of apps created by an organization](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#deprecated-get-a-list-of-apps-created-by-an-organization) endpoint is deprecated.
    * Use the new [Get a list of apps created by an organization](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#get-a-list-of-apps-created-by-an-organization) endpoint.
  * **Update app attributes that are name, redirect URIs, and access token time to live** endpoint
    * The [Update app attributes that are name, redirect URIs, and access token time to live](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#deprecated-update-app-attributes-that-are-name-redirect-uris-and-access-token-time-to-live) endpoint is deprecated.
    * Use the [Update app creation attributes such as name, redirect URIs, and access token time to live using the App ID](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#update-app-creation-attributes-such-as-name-redirect-uris-and-access-token-time-to-live-using-the-ap) endpoint.
  * **Get an app by client id** endpoint
    * The [Get an app by client id](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#deprecated-get-an-app-by-client-id) endpoint is deprecated.
    * Use the [Get a Snyk App by its App ID](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#get-a-snyk-app-by-its-app-id) endpoint.
  * **Delete an app** endpoint
    * The [Delete an app](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#deprecated-delete-an-app) endpoint is deprecated.
    * Use the [Delete a Snyk App by its App ID](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#delete-an-app-by-its-app-id) endpoint.
  * **Manage client secrets for an app** endpoint
    * The [Manage client secrets for an app](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#deprecated-manage-client-secrets-for-an-app) endpoint is deprecated.
    * Use the [Manage client secret for non-interactive Snyk App installations](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#manage-client-secret-for-non-interactive-snyk-app-installations) endpoint.
  * **Get a list of app bots authorized to an organization** endpoint
    * The [Get a list of app bots authorized to an organization](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#deprecated-get-a-list-of-app-bots-authorized-to-an-organization) endpoint is deprecated.
    * Use the [Get a list of apps installed for an organization](/broken/pages/Wr8Smn99fRYSVtJ6VuIg#get-a-list-of-apps-installed-for-an-organization) endpoint.
  * [Integration with Google Container Registry (GCR)](/broken/pages/CohqSf3CDfwDGyLdT9us) is deprecated.

### End of support features

When a feature transitions to an end-of-support stage, both development and support work are terminated.

The documentation page will announce the transition of a feature to End of Support six months before its start date.

### End of Life features

A feature can also be the subject of an end-of-life event, meaning that the feature or capability impacted by this process ceases to exist and is removed from the product and public documentation.

API endpoints have a dedicated section for the end of life process and also provide details about the migration steps. Navigate to the [API End of Life process and migration guides](/broken/pages/pNbLzJmwQBwdyu1Emsu6) for more details.
