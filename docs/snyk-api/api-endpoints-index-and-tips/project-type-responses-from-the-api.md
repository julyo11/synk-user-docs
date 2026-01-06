# Project type responses from the API

The Snyk Project type, defined in the V1 API only as `the package manager of the project`, is returned from the [API v1 Projects endpoints](https://docs.snyk.io/snyk-api/reference/projects-v1) and from the endpoint [List all Projects for an Org with the given Org ID](https://docs.snyk.io/snyk-api/reference/projects#orgs-org_id-projects).

The following is a list of the possible `type` values that may be returned:

* `apk`
* `armconfig`
* `cloudformationconfig`
* `cocoapods`
* `composer`
* `cpp`
* `deb`
* `dockerfile`
* `golang`
* `golangdep`
* `gomodules`
* `gradle`
* `govendor`
* `helmconfig`
* `hex`
* `k8sconfig`
* `linux`
* `maven`
* `npm`
* `nuget`
* `paket`
* `pip`
* `poetry`
* `rpm`
* `rubygems`
* `sast`
* `sbt`
* `terraformconfig`
* `terraformplan`
* `yarn`
* `yarn-workspace`

Last updated 9 months ago

For related endpoints see:

* [API v1 Projects endpoints](https://docs.snyk.io/snyk-api/reference/projects-v1)
* [List all Projects for an Org with the given Org ID](https://docs.snyk.io/snyk-api/reference/projects#orgs-org_id-projects)
