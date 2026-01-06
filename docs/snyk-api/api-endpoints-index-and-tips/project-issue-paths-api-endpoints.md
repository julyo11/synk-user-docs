# Project issue paths API endpoints

This page provides additional details for the API endpoints:

* List all project issue paths: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-issue-issueid-paths
* List all project snapshot issue paths: https://docs.snyk.io/snyk-api/reference/snapshots-v1#org-orgid-project-projectid-history-snapshotid-issue-issueid-paths

The `paths` endpoints return details of the paths through which an issue has been introduced.

## Requests

* Method: GET
* Endpoints:
  * Latest project test:
    * `https://api.snyk.io/v1/org/<orgId>/project/<projectId>/issue/<issueId>/paths`
    * (See: https://docs.snyk.io/snyk-api/reference/projects-v1#org-orgid-project-projectid-issue-issueid-paths)
  * Specific project snapshot:
    * `https://api.snyk.io/v1/org/<orgId>/project/<projectId>/history/<snapshotId>/issue/<issueId>/paths`
    * (See: https://docs.snyk.io/snyk-api/reference/snapshots-v1#org-orgid-project-projectid-history-snapshotid-issue-issueid-paths)

Both endpoints accept a query string for pagination, for example:

* `?page=2&perPage=500`

Defaults and limits:

* By default the first page of 100 results is returned.
* You can request up to 1,000 results per page.

## Response structure

A typical response has this structure:

{% code title="response.json" %}
```json
{
  "snapshotId": "6d5813be-7e6d-4ab8-80c2-1e3e2a454553",
  "paths": [...],
  "total": 193,
  "links": {
    "prev": "<https://snyk.io/>...",
    "next": "<https://snyk.io/>...",
    "last": "<https://snyk.io/>..."
  }
}
```
{% endcode %}

Field descriptions:

* `snapshotId`: ID of the Project snapshot from which the paths were returned.
* `paths`: An array where each element is a path through the dependency tree (see example below).
* `total`: Total number of paths for the issue in the snapshot.
* `links`: Convenience links for navigating pages. `links.next` and `links.prev` are included only if such pages exist (e.g., the last page will not include `next`).

### Paths format

Each element in `paths` is itself an array of package descriptors. Example:

{% code title="paths-example.json" %}
```json
{
  "paths": [
    [
      { "name": "lodash", "version": "4.17.4", "fixVersion": "4.17.20" }
    ],
    [
      { "name": "babel-template", "version": "6.26.0", "fixVersion": "6.26.0" },
      { "name": "lodash", "version": "4.17.10" }
    ]
  ]
}
```
{% endcode %}

Notes on this example and general rules:

* The example shows the issue introduced through two different versions of `lodash`. One is a direct dependency; the other is an indirect dependency via `babel-template`.
* Paths are ordered with the shortest path first.
* If an issue applies to the Project itself, the single element in the path will be the Project.
* For dependency issues, each path starts with a direct dependency.
* The `fixVersion` attribute appears on the first element of a path when that path is upgradable.
  * If `version` and `fixVersion` are the same, the upgrade involves re-locking transitive dependencies rather than changing the direct dependency version.

## Related

* Previous: Organization and Group identification for Projects using the API\
  https://docs.snyk.io/snyk-api/api-endpoints-index-and-tips/organization-and-group-identification-for-projects-using-the-api
* Next: Project type responses from the API\
  https://docs.snyk.io/snyk-api/api-endpoints-index-and-tips/project-type-responses-from-the-api

Last updated 1 year ago

Privacy note: This site uses cookies. By browsing this site you accept the privacy policy: https://snyk.io/policies/privacy/
