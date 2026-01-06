# GitLab

{% include "../../../../../.gitbook/includes/pilot-guide-toc.md" %}

Review the steps below to configure the GitLab integration with Snyk. For more details about setting up the GitHub integration, contact your Snyk account team.

## Generate a GitLab PAT

Generate a GitHub PAT with the following permissions enabled:\\

* `api`
* `read_api`
* `read_repository`

{% hint style="info" %}
Save the PAT details since the PAT is required in two places, at the Group-level integration and the Organization-level integration.
{% endhint %}

## Configure the Group-level integration

Configure the Group-level integration by following these steps:

* Open the Snyk Web UI
* Navigate to the Group-level
* Open **Integrations**, then **Add integration**

<figure><img src="../../../../../.gitbook/assets/image (307) (1).png" alt=""><figcaption></figcaption></figure>

* Search and select the GitHub integration
* Configure the integration and populate all mandatory fields, including the PAT details. For more details, see the [Integrate GitLab using Snyk Essentials](/broken/pages/UKTPvn5HlySjNsbjp4xE#gitlab-integrate-using-snyk-apprisk) page.
* If relevant, you can also include the Backstage catalog. See the [Backstage file for SCM integrations](/broken/pages/02qFHiSuRZqcR8LYBBEs#backstage-file-for-scm-integrations) page for more details.

{% hint style="info" %}
After the integration is configured, the Group-level integration shifts to a **Partially connected** status. During the next synchronization, it will transition to the connected state, and the Inventory view will be filled with data from the GitHub source.
{% endhint %}

## Configure the Organization-level integration

Configure the Organization-level integration by following these steps:

* Open the Snyk Web UI
* Navigate to the Organization-level
* Open **Integrations**
* Search and select the GitLab integration
* Configure the integration and populate all mandatory fields, including the PAT details. For more details, see the [GitLab integration settings](/broken/pages/D90VmGS53dWUzau2JSyJ) page.

<figure><img src="../../../../../.gitbook/assets/image (303).png" alt=""><figcaption></figcaption></figure>

The Organization-level integration is immediately available to import repositories and begin scanning.

\
\\
