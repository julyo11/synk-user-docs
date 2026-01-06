# Scenarios for using the Snyk API

The Snyk API scenarios identify procedures you can use to accomplish tasks with Snyk applications using the API. The scenarios listed here are grouped by Snyk processes and provided in a repository or on the user docs site. Links are included.

If you have issues when using these procedures, contact your Technical Success Manager or Solutions Engineer, or submit a ticket to Snyk support: https://support.snyk.io/

Last updated: 8 months ago

Manage Snyk Organization structure

Create multiple new Organizations that all have the same settings in a given Group

* Scenario: create-multiple-orgs-and-copy-settings (complete procedure)\
  https://github.com/snyk-playground/cx-tools/blob/main/scripts/create-multiple-orgs-and-copy-settings.md
* Endpoints used:
  * Create a new organization: https://docs.snyk.io/snyk-api/reference/organizations-v1#org
  * View organization settings: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-settings-1
  * Update organization settings: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-settings
  * Clone an integration with settings and credentials: https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-integrationid-clone

Assign all users in a given list to all the Organizations a company has (all Organizations in a Group)

* Scenario: assign-users-to-all-orgs (complete procedure)\
  https://github.com/snyk-playground/cx-tools/blob/main/scripts/assign-users-to-all-orgs.md
* Endpoints used:
  * List all members in a group: https://docs.snyk.io/snyk-api/reference/groups-v1#group-groupid-members
  * Invite users: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-invite

Add users to organizations at scale ahead of the first login

* Scenario: Provision users to Orgs via API\
  https://docs.snyk.io/snyk-platform-administration/user-management-with-the-api/provision-users-to-organizations-using-the-api
* Endpoint used:
  * Provision a user to the organization: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-provision

Import and set up Snyk Projects

Identify and import new repositories only

* Scenario: Identify-and-import-new-repos (complete procedure)\
  https://github.com/snyk-playground/cx-tools/blob/main/scripts/Identify-and-import-new-repos.md
* Endpoints used:
  * Get targets by org ID: https://docs.snyk.io/snyk-api/reference/targets#orgs-org\_id-targets
  * Import targets: https://docs.snyk.io/snyk-api/reference/import-projects-v1#org-orgid-integrations-integrationid-import

Import fresh container images

* Scenario: import-new-container-images (complete procedure)\
  https://github.com/snyk-playground/cx-tools/blob/main/scripts/import-new-container-images.md
* Endpoints used:
  * List all projects for an Org with the given Org ID: https://docs.snyk.io/snyk-api/reference/projects#orgs-org\_id-projects
  * Import targets: https://docs.snyk.io/snyk-api/reference/import-projects-v1#org-orgid-integrations-integrationid-import
  * Get import job details: https://docs.snyk.io/snyk-api/reference/import-projects-v1#org-orgid-integrations-integrationid-import-jobid
  * Delete a project: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-2

Detect new Projects (files) in repositories and import them into a Target in Snyk on a regular basis

* Scenario: Identify-and-import-new-repos (complete procedure)\
  https://github.com/snyk-playground/cx-tools/blob/main/scripts/Identify-and-import-new-repos.md
* Endpoints used:
  * Get targets by org ID: https://docs.snyk.io/snyk-api/reference/targets#orgs-org\_id-targets
  * Import targets: https://docs.snyk.io/snyk-api/reference/import-projects-v1#org-orgid-integrations-integrationid-import

Manage Snyk Projects

Tag all Projects in Snyk

* Scenario: Tag projects in Snyk (complete procedure)\
  https://github.com/snyk-playground/cx-tools/blob/main/scripts/tag-snyk-projects.md
* Endpoints used:
  * List all Projects for an Org with the given Org ID: https://docs.snyk.io/snyk-api/reference/projects#orgs-org\_id-projects

Move Projects from one Organization to another

* Scenario: Move projects between organizations (complete procedure)\
  https://github.com/snyk-playground/cx-tools/blob/main/scripts/move-projects.md
* Notes:
  * The API token used must have Group Admin access.
  * If moving between Organizations in different Groups, use a personal API token with Group Admin permissions in both Groups. Service Accounts cannot move projects between Organizations in different Groups.
  * Historical data for reporting will be lost.
* Endpoints used:
  * Move project to a different organization: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-move

Integrate with SCMs

Rotate or change your Broker token for any reason

* Scenario: Broker-token-rotation (complete procedure)\
  https://github.com/snyk-playground/cx-tools/blob/main/scripts/broker-token-rotation.md
* Endpoints used:
  * List all the organizations a user belongs to (group admin only): https://docs.snyk.io/snyk-api/reference/organizations-v1#orgs
  * Add new integration: https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations
  * Update existing integration (to enable Broker): https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-integrationid

For a specific event or time, disable all interactions (pull requests, tests) from Snyk to the code base (source control management repository)

* Scenario: disable-all-interaction-from-snyk (complete procedure)\
  https://github.com/snyk-playground/cx-tools/blob/main/scripts/disable-all-interaction-from-snyk.md
* Endpoints used (alternative 1: update integration settings):
  * List integrations: https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-1
  * Update integration settings: https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-integrationid-settings
  * Update existing integration: https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-integrationid
* Endpoints used (alternative 2: webhooks approach):
  * List webhooks: https://docs.snyk.io/snyk-api/reference/webhooks-v1#org-orgid-webhooks-1
  * Delete a webhook: https://docs.snyk.io/snyk-api/reference/webhooks-v1#org-orgid-webhooks-webhookid-1
  * Create a webhook: https://docs.snyk.io/snyk-api/reference/webhooks-v1#org-orgid-webhooks

Retrieve and manage issues

Retrieve a Project snapshot for every Project in a given Group

* Scenario: Retrieve-project-snapshots (complete procedure)\
  https://github.com/snyk-playground/cx-tools/blob/main/scripts/retrieve-projects-snapshots.md
* Endpoints used:
  * List all organizations in a group: https://docs.snyk.io/snyk-api/reference/groups-v1#group-groupid-orgs
  * Get list of latest issues: https://docs.snyk.io/snyk-api/reference/reporting-api-v1#reporting-issues-latest

Find all Projects affected by a vulnerability

* Scenario: find-all-projects-affected-by-a-vuln.md (complete procedure)\
  https://github.com/snyk-playground/cx-tools/blob/main/scripts/find-all-projects-affected-by-a-vuln.md
* Endpoints used:
  * Get list of issues: https://docs.snyk.io/snyk-api/reference/reporting-api-v1#reporting-issues
  * List all organizations in a group: https://docs.snyk.io/snyk-api/reference/groups-v1#group-groupid-orgs
  * List all projects for an Org with the given Org ID: https://docs.snyk.io/snyk-api/reference/projects#orgs-org\_id-projects

Bulk ignore issues

* Scenario: bulk-ignore-issues (complete procedure)\
  https://github.com/snyk-playground/cx-tools/blob/main/scripts/bulk-ignore-issues.md
* Endpoints used:
  * List all projects for an Org with the given Org ID: https://docs.snyk.io/snyk-api/reference/projects#orgs-org\_id-projects
  * Get list of latest issues (To get all issues but Code): https://docs.snyk.io/snyk-api/reference/reporting-api-v1#reporting-issues-latest
  * Get issues by org ID (To get all Code issues): https://docs.snyk.io/snyk-api/reference/issues#orgs-org\_id-issues

List all issues including Snyk Code issues in all the Projects in an Organization

* Scenario: list-all-issues-for-a-snyk-org (complete procedure)\
  https://github.com/snyk-playground/cx-tools/blob/main/scripts/list-all-issues-for-a-snyk-org.md
* Endpoints used:
  * List all projects for an Org with the given Org ID: https://docs.snyk.io/snyk-api/reference/projects#orgs-org\_id-projects
  * List all aggregated issues (no Code): https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-aggregated-issues
  * Get issues by org ID: https://docs.snyk.io/snyk-api/reference/issues#orgs-org\_id-issues
    * Note: As of April 2025, you can retrieve Snyk Code issues using this endpoint. It includes the primary file path and primary region in the `source_location` data in `representations` in `coordinates` for an issue.
  * REST experimental - Get a Snyk Code issue by its ID: https://apidocs.snyk.io/?version=2022-04-06%7Eexperimental#get-/orgs/-org\_id-/issues/detail/code/-issue\_id-
  * Retrieve ignore: https://docs.snyk.io/snyk-api/reference/ignores-v1#org-orgid-project-projectid-ignore-issueid-2

Related

* Solutions for specific use cases: https://docs.snyk.io/snyk-api/api-endpoints-index-and-tips/solutions-for-specific-use-cases
* Issue IDs in Snyk APIs: https://docs.snyk.io/snyk-api/api-endpoints-index-and-tips/issue-ids-in-snyk-apis

Was this helpful?
