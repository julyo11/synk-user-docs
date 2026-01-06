# API endpoints index and tips

Log in to Snyk, navigate to your Organization, and then to your Settings > General. The Organization ID is on the General settings page, and you can copy it.

This index and notes section provides, in addition to this index, solutions for specific use cases, scenarios for using Snyk APIs, and pages with detailed information about using Snyk API endpoints:

* [Solutions for specific use cases](solutions-for-specific-use-cases.md)
* [Scenarios for using Snyk APIs](scenarios-for-using-the-snyk-api.md)
* [Organization and Group identification for Projects using the API](organization-and-group-identification-for-projects-using-the-api.md)
* [Project issue paths V1 API endpoints](project-issue-paths-api-endpoints.md)
* [Project type responses from the API](project-type-responses-from-the-api.md)

For additional information, see the API support articles: https://support.snyk.io/s/topic/0TOPU00000BgWMv4AN/snyk-api&#x20;

This index includes categories and names of REST GA and beta and V1 API endpoints, with a reference URL for each endpoint and links to related information where available. REST is the default and GA is the status unless beta is noted. V1 API is specified where applicable.

***

## AccessRequests (beta)

* Get access requests (beta): https://apidocs.snyk.io/?beta=\&version=2024-10-15#get-/self/access\_requests

## Apps

More information: https://docs.snyk.io/snyk-api/using-specific-snyk-apis/snyk-apps-apis

* Get a list of apps that act on your behalf: https://docs.snyk.io/snyk-api/reference/apps#self-apps
* Revoke an app: https://docs.snyk.io/snyk-api/reference/apps#self-apps-app\_id
* Get a list of active OAuth sessions for the app: https://docs.snyk.io/snyk-api/reference/apps#self-apps-app\_id-sessions
* Revoke an active user app session: https://docs.snyk.io/snyk-api/reference/apps#self-apps-app\_id-sessions-session\_id
* Get a list of apps installed for a user: https://docs.snyk.io/snyk-api/reference/apps#self-apps-installs
* Revoke access for an app by install ID: https://docs.snyk.io/snyk-api/reference/apps#self-apps-installs-install\_id
  * Replaces: DEPRECATED Revoke app bot authorization
* DEPRECATED: Create a new app for an organization: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps
  * Replaced by: Create a new Snyk App for an organization
  * More information: https://docs.snyk.io/snyk-api/using-specific-snyk-apis/snyk-apps-apis/create-a-snyk-app-using-the-snyk-api
* Get a list of apps created by an organization: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps-1
  * Replaces: DEPRECATED Get a list of apps created by an organization
  * More information: https://docs.snyk.io/snyk-api/using-specific-snyk-apis/snyk-apps-apis/manage-app-details
* DEPRECATED: Update app attributes (name, redirect URIs, access token TTL): https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps-client\_id
  * Replaced by: Update app creation attributes using the App ID
* DEPRECATED: Get an app by client id: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps-client\_id-1
  * Replaced by: Get a Snyk App by its App ID
* DEPRECATED: Delete an app: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps-client\_id-2
  * Replaced by: Delete a Snyk App by its App ID
* DEPRECATED: Manage client secrets for an app: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps-client\_id-secrets
  * Replaced by: Manage client secret for non-interactive Snyk App installations
* Install a Snyk App to this organization: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps-installs
* Get a list of apps installed for an organization: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps-installs-1
  * Replaces: DEPRECATED Get a list of app bots authorized to an organization
  * More information (Slack app / Jira integration): https://docs.snyk.io/integrations/jira-and-slack-integrations/slack-app
* Revoke app authorization for a Snyk organization: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps-installs-install\_id
  * See also: Revoke app authorization for a Snyk Group with install ID
* Manage client secret for non-interactive Snyk App installations: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps-installs-install\_id-secrets
  * More information: https://docs.snyk.io/snyk-api/using-specific-snyk-apis/snyk-apps-apis/manage-app-details
* Create a new Snyk App for an organization: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps-creations
  * Replaces: DEPRECATED Create a new app for an organization
  * More information: https://docs.snyk.io/snyk-api/using-specific-snyk-apis/snyk-apps-apis/create-a-snyk-app-using-the-snyk-api
* Get a Snyk APP by its App ID: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps-creations-app\_id
  * Replaces: DEPRECATED Get an app by client id
* Delete an app by its App ID: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps-creations-app\_id-2
  * Replaces: DEPRECATED Delete an app
  * More information: https://docs.snyk.io/snyk-api/using-specific-snyk-apis/snyk-apps-apis/manage-app-details
* Manage client secret for the Snyk App: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-apps-creations-app\_id-secrets
  * More information: https://docs.snyk.io/snyk-api/using-specific-snyk-apis/snyk-apps-apis/manage-app-details
* DEPRECATED: Get a list of app bots authorized to an organization: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-app\_bots
  * Replaced by: Get a list of apps installed for an organization (https://apidocs.snyk.io/?#get-/orgs/-org\_id-/apps/installs)
  * More information: Slack app for Jira integration: https://docs.snyk.io/integrations/jira-and-slack-integrations/slack-app
* DEPRECATED: Revoke app bot authorization: https://docs.snyk.io/snyk-api/reference/apps#orgs-org\_id-app\_bots-bot\_id
  * Replaced by: Revoke app authorization for a Snyk Group with install ID
  * See also: Revoke access for an app by install: https://apidocs.snyk.io/?#delete-/self/apps/installs/-install\_id-
* Install a Snyk App to this group: https://docs.snyk.io/snyk-api/reference/apps#groups-group\_id-apps-installs
* Get a list of apps installed for a group: https://docs.snyk.io/snyk-api/reference/apps#groups-group\_id-apps-installs-1
* Revoke app authorization for a Snyk Group with install ID: https://docs.snyk.io/snyk-api/reference/apps#groups-group\_id-apps-installs-install\_id
* Manage client secret for non-interactive Snyk App installations (group): https://docs.snyk.io/snyk-api/reference/apps#groups-group\_id-apps-installs-install\_id-secrets
  * Replaces: DEPRECATED Manage client secrets for an app

## Audit Logs

More information:

* Retrieve audit logs: https://docs.snyk.io/snyk-platform-administration/user-management-with-the-api/retrieve-audit-logs-of-user-initiated-activity-by-api-for-an-org-or-group
* AWS CloudTrail Lake integration: https://docs.snyk.io/integrations/event-forwarding/aws-cloudtrail-lake
* Search Organization audit logs: https://docs.snyk.io/snyk-api/reference/audit-logs#orgs-org\_id-audit\_logs-search
* Search Group audit logs: https://docs.snyk.io/snyk-api/reference/audit-logs#groups-group\_id-audit\_logs-search
  * More information: https://updates.snyk.io/filter-through-your-audit-logs-more-efficiently-with-the-new-ga-rest-version-of-the-audit-logs-api-and-api-access-is-now-opt-in-291850

## Audit logs (v1)

* Group level audit logs: Use https://docs.snyk.io/snyk-api/reference/audit-logs#groups-group\_id-audit\_logs-search
* Organization level audit logs: Use https://docs.snyk.io/snyk-api/reference/audit-logs#orgs-org\_id-audit\_logs-search

## Cloud (beta)

* List Environments: https://apidocs.snyk.io/?beta=\&version=2024-10-15#get-/orgs/-org\_id-/cloud/environments
* Create New Environment: https://apidocs.snyk.io/?beta=\&version=2024-10-15#post-/orgs/-org\_id-/cloud/environments
* Delete Environment: https://apidocs.snyk.io/?beta=\&version=2024-10-15#delete-/orgs/-org\_id-/cloud/environments/-environment\_id-
* Update Environment: https://apidocs.snyk.io/?beta=\&version=2024-10-15#patch-/orgs/-org\_id-/cloud/environments/-environment\_id-
* Generate Cloud Provider Permissions: https://apidocs.snyk.io/?beta=\&version=2024-10-15#post-/orgs/-org\_id-/cloud/permissions
* List Resources: https://apidocs.snyk.io/?beta=\&version=2024-10-15#get-/orgs/-org\_id-/cloud/resources
  * See Snyk IaC: https://docs.snyk.io/scan-with-snyk/snyk-iac
* List Scans: https://apidocs.snyk.io/?beta=\&version=2024-10-15#get-/orgs/-org\_id-/cloud/scans
* Create Scan: https://apidocs.snyk.io/?beta=\&version=2024-10-15#post-/orgs/-org\_id-/cloud/scans
* Get scan: https://apidocs.snyk.io/?beta=\&version=2024-10-15#get-/orgs/-org\_id-/cloud/scans/-scan\_id-

## Collection

* The View Project History permission is needed to use this API.
* More information: https://docs.snyk.io/snyk-platform-administration/snyk-projects/project-collections-groupings
* Create a collection: https://docs.snyk.io/snyk-api/reference/collection#orgs-org\_id-collections
* Get collections: https://docs.snyk.io/snyk-api/reference/collection#orgs-org\_id-collections-1
* Edit a collection: https://docs.snyk.io/snyk-api/reference/collection#orgs-org\_id-collections-collection\_id
* Get a collection: https://docs.snyk.io/snyk-api/reference/collection#orgs-org\_id-collections-collection\_id-1
* Delete a collection: https://docs.snyk.io/snyk-api/reference/collection#orgs-org\_id-collections-collection\_id-2
* Add projects to a collection: https://docs.snyk.io/snyk-api/reference/collection#orgs-org\_id-collections-collection\_id-relationships-projects
* Get projects from the specified collection: https://docs.snyk.io/snyk-api/reference/collection#orgs-org\_id-collections-collection\_id-relationships-projects-1
* Remove projects from a collection: https://docs.snyk.io/snyk-api/reference/collection#orgs-org\_id-collections-collection\_id-relationships-projects-2

## ContainerImage

* List instances of container image: https://docs.snyk.io/snyk-api/reference/containerimage#orgs-org\_id-container\_images
* Get instance of container image: https://docs.snyk.io/snyk-api/reference/containerimage#orgs-org\_id-container\_images-image\_id
* List instances of image target references for a container image: https://docs.snyk.io/snyk-api/reference/containerimage#orgs-org\_id-container\_images-image\_id-relationships-image\_target\_refs

## Custom Base Images

More information: https://docs.snyk.io/scan-with-snyk/snyk-container/use-snyk-container/use-custom-base-image-recommendations

* Create a Custom Base Image from an existing container project: https://docs.snyk.io/snyk-api/reference/custom-base-images#custom\_base\_images
  * More: Mark the created Project as a custom base image; versioning schema: https://docs.snyk.io/scan-with-snyk/snyk-container/use-snyk-container/use-custom-base-image-recommendations#mark-the-created-project-as-a-custom-base-image
* Get a custom base image collection: https://docs.snyk.io/snyk-api/reference/custom-base-images#custom\_base\_images-1
* Update a custom base image: https://docs.snyk.io/snyk-api/reference/custom-base-images#custom\_base\_images-custombaseimage\_id
* Get a custom base image: https://docs.snyk.io/snyk-api/reference/custom-base-images#custom\_base\_images-custombaseimage\_id-1
* Delete a custom base image: https://docs.snyk.io/snyk-api/reference/custom-base-images#custom\_base\_images-custombaseimage\_id-2

## Dependencies (v1)

* List all dependencies: https://docs.snyk.io/snyk-api/reference/dependencies-v1

## Entitlements (v1)

* List all entitlements: https://docs.snyk.io/snyk-api/reference/entitlements-v1#org-orgid-entitlements
* Get an organization's entitlement value: https://docs.snyk.io/snyk-api/reference/entitlements-v1#org-orgid-entitlement-entitlementkey

## Groups (beta)

* Get all groups: https://apidocs.snyk.io/?version=2024-10-15#get-/groups
* Get a group: https://apidocs.snyk.io/?version=2024-10-15#get-/groups/-group\_id-
  * More information: https://docs.snyk.io/snyk-api/api-endpoints-index-and-tips/organization-and-group-identification-for-projects-using-the-api
* Get all SSO connections for a group: https://apidocs.snyk.io/?version=2024-10-15#get-/groups/-group\_id-/sso\_connections
* Get all users using a given SSO connection: https://apidocs.snyk.io/?version=2024-10-15#get-/groups/-group\_id-/sso\_connections/-sso\_id-/users
* Delete a user from a Group SSO connection: https://apidocs.snyk.io/?version=2024-10-15#delete-/groups/-group\_id-/sso\_connections/-sso\_id-/users/-user\_id-
  * More: Remove members from Groups and Orgs using the API; Retrieve audit logs for Org or Group

## Groups (v1)

* List all tags in a group: https://docs.snyk.io/snyk-api/reference/groups-v1#group-groupid-tags
  * More information: https://docs.snyk.io/snyk-platform-administration/snyk-projects/project-tags
* Delete tag from group: https://docs.snyk.io/snyk-api/reference/groups-v1#group-groupid-tags-delete
* Update group settings: https://docs.snyk.io/snyk-api/reference/groups-v1#group-groupid-settings
* View group settings: https://docs.snyk.io/snyk-api/reference/groups-v1#group-groupid-settings-1
* List all roles in a group: https://docs.snyk.io/snyk-api/reference/groups-v1#group-groupid-roles
  * More information: Update member roles using the API; Manage service accounts using the Snyk API
* List all organizations in a group: https://docs.snyk.io/snyk-api/reference/groups-v1#group-groupid-orgs
  * More information and scenarios: see links in original doc
* Add a member to an organization within a group: https://docs.snyk.io/snyk-api/reference/groups-v1#group-groupid-org-orgid-members
* List all members in a group: https://docs.snyk.io/snyk-api/reference/groups-v1#group-groupid-members

## Groups

* Get a list of org memberships of a group user: https://docs.snyk.io/snyk-api/reference/groups#groups-group\_id-org\_memberships
* Create a group membership for a user with role: https://docs.snyk.io/snyk-api/reference/groups#groups-group\_id-memberships
* Get all memberships of the group: https://docs.snyk.io/snyk-api/reference/groups#groups-group\_id-memberships-1
* Update a role from a group membership: https://docs.snyk.io/snyk-api/reference/groups#groups-group\_id-memberships-membership\_id
* Delete a membership from a group: https://docs.snyk.io/snyk-api/reference/groups#groups-group\_id-memberships-membership\_id-1

## IacSettings

* Update the Infrastructure as Code Settings for an org: https://docs.snyk.io/snyk-api/reference/groups-v1#group-groupid-org-orgid-members
  * More information: Use a remote IaC custom rules bundle
* Get the Infrastructure as Code Settings for an org: https://docs.snyk.io/snyk-api/reference/iacsettings#orgs-org\_id-settings-iac-1
* Update the Infrastructure as Code Settings for a group: https://docs.snyk.io/snyk-api/reference/iacsettings#groups-group\_id-settings-iac
* Get the Infrastructure as Code Settings for a group: https://docs.snyk.io/snyk-api/reference/iacsettings#groups-group\_id-settings-iac-1

## Ignores (v1)

* List all ignores: https://docs.snyk.io/snyk-api/reference/ignores-v1#org-orgid-project-projectid-ignores
* Replace ignores: https://docs.snyk.io/snyk-api/reference/ignores-v1#org-orgid-project-projectid-ignore-issueid
* Add ignore: https://docs.snyk.io/snyk-api/reference/ignores-v1#org-orgid-project-projectid-ignore-issueid-1
* Retrieve ignore: https://docs.snyk.io/snyk-api/reference/ignores-v1#org-orgid-project-projectid-ignore-issueid-1
* Delete ignores: https://docs.snyk.io/snyk-api/reference/ignores-v1#org-orgid-project-projectid-ignore-issueid-3

## Import Projects (v1)

Projects can be Git repositories, Docker images, containers, configuration files, and more. More information: https://docs.snyk.io/snyk-platform-administration/snyk-projects

A typical import flow:

* Use Import targets to request a target to be processed: https://docs.snyk.io/snyk-api/reference/import-projects-v1#org-orgid-integrations-integrationid-import
* Poll Import job details for completion: https://docs.snyk.io/snyk-api/reference/import-projects-v1#org-orgid-integrations-integrationid-import-jobid

Notes:

* target.owner is case-sensitive.
* If Import targets fails, use Get import job details to determine why.
  * Failures include repository rejected for processing (e.g., repo does not exist, unreachable, invalid token, no default branch) or accepted but no projects detected/failed (e.g., no supported manifests, archived repo, manifest processing errors).
* Poll results return a message per manifest: success: true or success: false.

More info and tools:

* api-import creating import targets data: https://docs.snyk.io/scan-with-snyk/snyk-tools/tool-snyk-api-import/creating-import-targets-data-for-import-command
* api-import kicking off an import: https://docs.snyk.io/scan-with-snyk/snyk-tools/tool-snyk-api-import/kicking-off-an-import
* Configure integrations (Enterprise guide): https://docs.snyk.io/implementation-and-setup/team-implementation-guide/phase-2-configure-your-organization/configure-integrations
* Import Projects (Enterprise guide): https://docs.snyk.io/implementation-and-setup/team-implementation-guide/phase-3-gain-visibility/import-projects

## Integrations (v1)

* Add new integration: https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations
* List integrations: https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-1
* Get existing integration by type: https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-type
* Update existing integration: https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-integrationid
* Update (settings): https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-integrationid-settings
* Retrieve: https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-integrationid-settings-1
* Clone an integration (settings and credentials): https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-integrationid-clone
* Delete credentials: https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-integrationid-authentication
* Switch between broker tokens: https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-integrationid-authentication-switch-token
* Provision new broker token: https://docs.snyk.io/snyk-api/reference/integrations-v1#org-orgid-integrations-integrationid-authentication-provision-token

## Invites

* Invite a user to an organization: https://docs.snyk.io/snyk-api/reference/invites#orgs-org\_id-invites
* List pending user invitation to an organization: https://docs.snyk.io/snyk-api/reference/invites#orgs-org\_id-invites-1
* Cancel a pending user invitation to an organization: https://docs.snyk.io/snyk-api/reference/invites#orgs-org\_id-invites-invite\_id

## Issues

* List issues for a package: https://docs.snyk.io/snyk-api/reference/issues#orgs-org\_id-packages-purl-issues
* List issues for a given set of packages (limited availability): https://docs.snyk.io/snyk-api/reference/issues#orgs-org\_id-packages-issues
* Get issues by org ID: https://docs.snyk.io/snyk-api/reference/issues#orgs-org\_id-issues
  * As of April 2025, Snyk Code issues are retrievable here with source\_location data.
* Get an issue (Organization): https://docs.snyk.io/snyk-api/reference/issues#orgs-org\_id-issues-issue\_id
* Get issues by group ID: https://docs.snyk.io/snyk-api/reference/issues#orgs-org\_id-issues-issue\_id
  * Remedies are not included; Snyk Code issues available as noted above.
* Get an issue (Group): https://docs.snyk.io/snyk-api/reference/issues#groups-group\_id-issues-issue\_id

## Jira (v1)

* List all Jira issues: https://docs.snyk.io/snyk-api/reference/jira-v1#org-orgid-project-projectid-jira-issues
* Create Jira issue: https://docs.snyk.io/snyk-api/reference/jira-v1#org-orgid-project-projectid-issue-issueid-jira-issuev

## Licenses (v1)

* List all licenses: https://docs.snyk.io/snyk-api/reference/licenses-v1

## Monitor (v1)

* Monitor Dep Graph: https://docs.snyk.io/snyk-api/reference/monitor-v1

## Organizations (v1)

* Webhooks events and payloads: https://docs.snyk.io/snyk-api/using-specific-snyk-apis/webhooks-apis/webhooks
* List all the organizations a user belongs to: https://docs.snyk.io/snyk-api/reference/organizations-v1#orgs
* Create a new organization: https://docs.snyk.io/snyk-api/reference/organizations-v1#org
* Remove organization: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid
* Update organization settings: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid
  * Only editable attribute: requestAccess
* View organization settings: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-settings-1
* Provision a user to the organization: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-provision
* List pending user provisions: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-provision-1
* Delete pending user provision: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-provision-2
* Set notification settings: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-notification-settings
* Get organization notification settings: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-notification-settings-1
* List members: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-members
* Update a member in the organization: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-members-userid
* Remove a member from the organization: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-members-userid-1
* Update a member's role in the organization: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-members-update-userid
* Invite users: https://docs.snyk.io/snyk-api/reference/organizations-v1#org-orgid-invite

## Orgs (GA and beta)

* List accessible organizations: https://docs.snyk.io/snyk-api/reference/orgs#orgs
* Update organization: https://docs.snyk.io/snyk-api/reference/orgs#orgs-org\_id
* Create a org membership for a user with role: https://docs.snyk.io/snyk-api/reference/orgs#orgs-org\_id-memberships
* Get all memberships of the org: https://docs.snyk.io/snyk-api/reference/orgs#orgs-org\_id-memberships-1
* Update a org membership for user with role: https://docs.snyk.io/snyk-api/reference/orgs#orgs-org\_id-memberships-membership\_id
* List all organizations in a group: https://docs.snyk.io/snyk-api/reference/orgs#groups-group\_id-orgs
* Get an ORG (beta): https://apidocs.snyk.io/?version=2024-10-15#get-/orgs/-org\_id-

## Projects (v1)

More information: Project type responses from API; Webhooks events and payloads

* Update a project: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid
* Retrieve a single project: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-1
* Delete a project: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-2
* Add a tag to a project: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-tags
* Remove a tag from a project: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-tags-remove
* Update project settings: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-settings
* List project settings: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-settings-1
* Delete project settings: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-settings-2
* Move project to a different organization: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-move
* List all project issue paths: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-issue-issueid-paths
* Get Project dependency graph: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-dep-graph
* Deactivate (a project): https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-deactivate
* Applying project attributes: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-attributes
  * Flow to set attributes after import is described in original doc
* List all Aggregated (Project) issues: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-aggregated-issues
* Activate (a project): https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-activate

## Projects

* List all Projects for an Org with the given Org ID: https://docs.snyk.io/snyk-api/reference/projects#orgs-org\_id-projects
* Updates project by project ID: https://docs.snyk.io/snyk-api/reference/projects#orgs-org\_id-projects-project\_id
* Get project by project ID: https://docs.snyk.io/snyk-api/reference/projects#orgs-org\_id-projects-project\_id-1
* Delete project by project ID: https://docs.snyk.io/snyk-api/reference/projects#orgs-org\_id-projects-project\_id-2

## Pull request templates

* Create or update pull request template for group: https://docs.snyk.io/snyk-api/reference/pull-request-templates#groups-group\_id-settings-pull\_request\_template
* Get pull request template for group: https://docs.snyk.io/snyk-api/reference/pull-request-templates#groups-group\_id-settings-pull\_request\_template-1
* Delete pull request template for group: https://docs.snyk.io/snyk-api/reference/pull-request-templates#groups-group\_id-settings-pull\_request\_template-2

## Reporting API (v1)

Notes:

* V1 Reporting supports only legacy reporting. Not available in single-tenant implementations or multi-tenant regions US-02, EU, AU. Use Issues REST API in those regions.
* V1 reporting use cases: counts for issues/tests/projects.
* Rate limit: up to 70 requests/minute per user. Exceeding returns 429. More information: Legacy reports, Dependencies and licenses
* Get list of issues: https://docs.snyk.io/snyk-api/reference/reporting-api-v1#reporting-issues
* Get list of latest issues: https://docs.snyk.io/snyk-api/reference/reporting-api-v1#reporting-issues-latest
* Get test counts: https://docs.snyk.io/snyk-api/reference/reporting-api-v1#reporting-counts-tests
* Get project counts: https://docs.snyk.io/snyk-api/reference/reporting-api-v1#reporting-counts-projects
* Get latest project counts: https://docs.snyk.io/snyk-api/reference/reporting-api-v1#reporting-counts-projects-latest
* Get issue counts: https://docs.snyk.io/snyk-api/reference/reporting-api-v1#reporting-counts-issues
* Get latest issue counts: https://docs.snyk.io/snyk-api/reference/reporting-api-v1#reporting-counts-issues-latest

## SBOM (GA and beta)

* Get a project’s SBOM document: https://docs.snyk.io/snyk-api/reference/sbom
* Create an SBOM test run (beta): https://apidocs.snyk.io/?version=2024-10-15#post-/orgs/-org\_id-/sbom\_tests
* Get an SBOM test run status (beta): https://apidocs.snyk.io/?version=2024-10-15#get-/orgs/-org\_id-/sbom\_tests/-job\_id-
* Get an SBOM test run result (beta): https://apidocs.snyk.io/?version=2024-10-15#get-/orgs/-org\_id-/sbom\_tests/-job\_id-/results

## SastSettings

* Enable/Disable the Snyk Code settings for an org: https://docs.snyk.io/snyk-api/reference/sastsettings#orgs-org\_id-settings-sast
* Retrieve the SAST settings for an org: https://docs.snyk.io/snyk-api/reference/sastsettings#orgs-org\_id-settings-sast-1

## ServiceAccounts

More information: Manage service accounts using the Snyk API; Choose a service account type

* Create a service account for an organization: https://docs.snyk.io/snyk-api/reference/serviceaccounts#orgs-org\_id-service\_accounts
* Get a list of organization service accounts: https://docs.snyk.io/snyk-api/reference/serviceaccounts#orgs-org\_id-service\_accounts-1
* Update an organization service account: https://docs.snyk.io/snyk-api/reference/serviceaccounts#orgs-org\_id-service\_accounts-serviceaccount\_id
* Get an organization service account: https://docs.snyk.io/snyk-api/reference/serviceaccounts#orgs-org\_id-service\_accounts-serviceaccount\_id-1
* Delete a service account in an organization: https://docs.snyk.io/snyk-api/reference/serviceaccounts#orgs-org\_id-service\_accounts-serviceaccount\_id-2
* Manage an organization service account’s client secret: https://docs.snyk.io/snyk-api/reference/serviceaccounts#orgs-org\_id-service\_accounts-serviceaccount\_id-secrets
* Create a service account for a group: https://docs.snyk.io/snyk-api/reference/serviceaccounts#groups-group\_id-service\_accounts
* Get a list of group service accounts: https://docs.snyk.io/snyk-api/reference/serviceaccounts#groups-group\_id-service\_accounts-1
* Update a group service account: https://docs.snyk.io/snyk-api/reference/serviceaccounts#groups-group\_id-service\_accounts-serviceaccount\_id
* Get a group service account: https://docs.snyk.io/snyk-api/reference/serviceaccounts#groups-group\_id-service\_accounts-serviceaccount\_id-1
* Delete a group service account: https://docs.snyk.io/snyk-api/reference/serviceaccounts#groups-group\_id-service\_accounts-serviceaccount\_id
* Manage a group service account’s client secret: https://docs.snyk.io/snyk-api/reference/serviceaccounts#groups-group\_id-service\_accounts-serviceaccount\_id-secrets

## SlackSettings

More information: Slack app (for Jira integration)

* Create new Slack notification default settings: https://docs.snyk.io/snyk-api/reference/slacksettings#orgs-org\_id-slack\_app-bot\_id
* Get Slack integration default notification settings: https://docs.snyk.io/snyk-api/reference/slacksettings#orgs-org\_id-slack\_app-bot\_id-1
* Remove the given Slack App integration: https://docs.snyk.io/snyk-api/reference/slacksettings#orgs-org\_id-slack\_app-bot\_id-2
* Slack notification settings override for projects: https://docs.snyk.io/snyk-api/reference/slacksettings#orgs-org\_id-slack\_app-bot\_id-projects
* Create a new Slack settings override for a given project: https://docs.snyk.io/snyk-api/reference/slacksettings#orgs-org\_id-slack\_app-bot\_id-projects-project\_id
* Update Slack notification settings for a project: https://docs.snyk.io/snyk-api/reference/slacksettings#orgs-org\_id-slack\_app-bot\_id-projects-project\_id-1
* Remove Slack settings override for a project: https://docs.snyk.io/snyk-api/reference/slacksettings#orgs-org\_id-slack\_app-bot\_id-projects-project\_id-2

## Slack

* Get a list of Slack channels: https://docs.snyk.io/snyk-api/reference/slack#orgs-org\_id-slack\_app-tenant\_id-channels
* Get Slack Channel name by Slack Channel ID: https://docs.snyk.io/snyk-api/reference/slack#orgs-org\_id-slack\_app-tenant\_id-channels-channel\_id

## Snapshots (v1)

* List all project snapshots: https://docs.snyk.io/snyk-api/reference/snapshots-v1#org-orgid-project-projectid-history
* List all project snapshot issue paths: https://docs.snyk.io/snyk-api/reference/snapshots-v1#org-orgid-project-projectid-history-snapshotid-issue-issueid-paths
* List all project snapshot aggregated issues: https://docs.snyk.io/snyk-api/reference/snapshots-v1#org-orgid-project-projectid-history-snapshotid-aggregated-issues

## Targets

* Get targets by org ID: https://docs.snyk.io/snyk-api/reference/targets#orgs-org\_id-targets
* Get target by target ID: https://docs.snyk.io/snyk-api/reference/targets#orgs-org\_id-targets-target\_id
* Delete target by target ID: https://docs.snyk.io/snyk-api/reference/targets#orgs-org\_id-targets-target\_id-1

## Test (v1)

More information: guidance for languages and scanning

* Test package.json & yarn-lock file: https://docs.snyk.io/snyk-api/reference/test-v1#test-yarn
* Test sbt file: https://docs.snyk.io/snyk-api/reference/test-v1#test-sbt
* sbt\_Test for issues in a public package by group id, artifact id and version: https://docs.snyk.io/snyk-api/reference/test-v1#test-sbt-groupid-artifactid-version
* Test gemfile.lock file: https://docs.snyk.io/snyk-api/reference/test-v1#test-rubygems
* Test for issues in a public gem by name and version: https://docs.snyk.io/snyk-api/reference/test-v1#test-rubygems-gemname-version
* Test requirements.txt file (pip): https://docs.snyk.io/snyk-api/reference/test-v1#test-pip
* Pip\_Test for issues in a public pip package by name and version: https://docs.snyk.io/snyk-api/reference/test-v1#test-pip-packagename-version
* Test package.json & package-lock.json file: https://docs.snyk.io/snyk-api/reference/test-v1#test-npm
* Test for issues in a public package by name and version (npm): https://docs.snyk.io/snyk-api/reference/test-v1#test-npm-packagename-version
* Test maven file: https://docs.snyk.io/snyk-api/reference/test-v1#test-maven
* Test for issues in a public package by group id, artifact id and version (Maven): https://docs.snyk.io/snyk-api/reference/test-v1#test-maven-groupid-artifactid-version
* Test gradle file: https://docs.snyk.io/snyk-api/reference/test-v1#test-gradle
* Test for issues in a public package by group, name and version (Gradle): https://docs.snyk.io/snyk-api/reference/test-v1#test-gradle-group-name-version
* Test vendor.json file: https://docs.snyk.io/snyk-api/reference/test-v1#test-govendor
* Test Gopkg.toml & Gopkg.lock File: https://docs.snyk.io/snyk-api/reference/test-v1#test-golangdep
* Test Dep Graph: https://docs.snyk.io/snyk-api/reference/test-v1#test-dep-graph
* Test composer.json & composer.lock file: https://docs.snyk.io/snyk-api/reference/test-v1#test-composer

## Users (v1)

* Get user details: https://docs.snyk.io/snyk-api/reference/users-v1#user-userid
* Get My Details: https://docs.snyk.io/snyk-api/reference/users-v1#user-me
* Modify organization notification settings (user): https://docs.snyk.io/snyk-api/reference/users-v1#user-me-notification-settings-org-orgid
* Get organization notification settings (user): https://docs.snyk.io/snyk-api/reference/users-v1#user-me-notification-settings-org-orgid-1
* Modify project notification settings (user): https://docs.snyk.io/snyk-api/reference/users-v1#user-me-notification-settings-org-orgid-project-projectid
* Get project notification settings (user): https://docs.snyk.io/snyk-api/reference/users-v1#user-me-notification-settings-org-orgid-project-projectid-1

## Users

* My User Details: https://docs.snyk.io/snyk-api/reference/users
* Update a user’s role in a group (beta): https://apidocs.snyk.io/?version=2024-10-15#patch-/groups/-group\_id-/users/-id-
* Get user by ID (beta): https://apidocs.snyk.io/?version=2024-10-15#get-/orgs/-org\_id-/users/-id-

## Webhooks (v1)

* Create a webhook: https://docs.snyk.io/snyk-api/reference/webhooks-v1#org-orgid-webhooks
* List webhooks: https://docs.snyk.io/snyk-api/reference/webhooks-v1#org-orgid-webhooks-1
* Retrieve a webhook: https://docs.snyk.io/snyk-api/reference/webhooks-v1#org-orgid-webhooks-webhookid
* Delete a webhook: https://docs.snyk.io/snyk-api/reference/webhooks-v1#org-orgid-webhooks-webhookid-1
* Ping a webhook: https://docs.snyk.io/snyk-api/reference/webhooks-v1#org-orgid-webhooks-webhookid-ping

***

More scenarios and related pages referenced throughout:

* Solutions for specific use cases: https://docs.snyk.io/snyk-api/api-endpoints-index-and-tips/solutions-for-specific-use-cases
* Scenarios for using the Snyk API: https://docs.snyk.io/snyk-api/api-endpoints-index-and-tips/scenarios-for-using-the-snyk-api
* API support articles: https://support.snyk.io/s/topic/0TOPU00000BgWMv4AN/snyk-api

Last updated: (as in source)

Was this helpful?
