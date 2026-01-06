---
cover: .gitbook/assets/docs-banner-nov25.webp
coverY: 0
---

# What's new?

The most recent updates include significant changes to the user docs, such as features added or removed, structure changes that affect how you find relevant information, and other improvements aimed at enhancing your interaction with the Snyk knowledge base.

## November 2025

### **Snyk Container**

* The list of [operated distribution systems supported by Snyk Container](/broken/pages/MgFrePnlbvurSaWmgk1R) has been updated with support for Chisel.

### **Snyk CLI**

* The latest [Snyk CLI version](/broken/pages/KUVsQmktSlBzw3LlQdio) available is v1.1301.0.
* The [CLI help](/broken/pages/KomNA2dYi3p7VjqA6HB8#using-reachability-analysis-with-snyk-cli) has been updated with commands for reachability analysis.

### Snyk IDE

* The Automated Org Selection feature uses repository context to choose an Organization. Manual configuration overrides this automated selection. If the selection fails, Snyk defaults to your preferred Organization setting. The feature is available for the [Eclipse plugin](/broken/pages/mqxg1cr48TyLIGEXxmu5), the [JetBrains plugin](/broken/pages/xZWNucBR2H4G33qoVoud), the [Visual Studio extension](/broken/pages/J4ScfzSVbLAXvPiWOYbl), and the [Visual Studio Code extension](/broken/pages/BBc5cBakd9hQ7HPx262L).

### **Snyk integrations**

* The Amazon Q guide for Snyk Studio now includes [updated instructions](/broken/pages/eJBYJXQPTqQVRtRS9z8P#install-the-snyk-mcp-server-in-the-amazon-q-ide-extension) for configuring the Snyk MCP Server in VS Code and JetBrains.

### **Other updates**

* [Reachabilty analysis](/broken/pages/KomNA2dYi3p7VjqA6HB8) has been updated with instructions on how it works and how to use it in both the Snyk Web UI and the Snyk CLI and clear support for specific languages and package managers.
* The [Pre-defined roles](/broken/pages/XNksHYxr70heqewL6k3D#role-types) documentation has been updated to communicate that the Organization Admin role and associated permissions supersede any Group Member role restrictions.
* The [severity condition](/broken/pages/s2zov366HHPZl22L6nxb) is now available in Group-level policies. Use this feature to create more granular policies for Snyk Code and Snyk Open Source findings, for example, ignoring a finding or changing its severity.

## October 2025

### **Snyk API**

* A new [API migration guide](/broken/pages/mKJap8nBgonqVXAhBJt2) is available to help you migrate from the v1 Reporting API to the REST Exporting API.
* The Export API has been improved with the option to [limit the link expiration](/broken/pages/gCHWZEjDuqlvCr0zFNRD#data-retention).

### **Snyk Broker**

* The [Universal Broker](/broken/pages/jFEfCFusEEKxY5YoKQAw) release status has transitioned to Generally Available.
* The page [Upgrade an Organization from Classic Broker to Universal Broker](implementation-and-setup/enterprise-setup/snyk-broker/universal-broker/upgrade-an-organization-integration-from-classic-broker-to-universal-broker.md#migrating-multiple-organizations) has been updated with steps to migrate multiple Organizations at a time.

### **Snyk CLI**

* Snyk CLI now supports uploading files and folders for Snyk Code scanning. The command [`code-test`](/broken/pages/pqfZxIVWZpuyzLm0epnx) has been updated with options reflecting these capabilities.
* The latest [Snyk CLI version](/broken/pages/KUVsQmktSlBzw3LlQdio) available is v1.1300.2.

### **Snyk integrations**

* The list of Snyk MCP quick guides now includes [Devin guide](/broken/pages/FbKZViyg7daUvj94dJqp), [Factory guide](/broken/pages/oOJrR8tewOtbF86Z7iVM), [Factory terminal guide](/broken/pages/2Ye90ZW9YqTs6SyazT4Y).
* The Snyk MCP Server has been rebranded as [Snyk Studio](/broken/pages/ZXX8R1Mwg3ejaKXdm5iy).
* [SCM integration support for Python](supported-languages/supported-languages-list/python/scm-integrations-and-python.md) has been updated with support for Python 3.14.

### **Other updates**

* The [Operating system distributions supported by Snyk Container](/broken/pages/MgFrePnlbvurSaWmgk1R#minimus) has been updated to include include support for Minimus, Ubuntu 25.10 - Questing Quokka, and Ubuntu 25.04 - Plucky Puffin.
* For [Ruby](supported-languages/supported-languages-list/ruby.md), versions 2.3.X are no longer supported. The Ruby-specific versions have been updated to include more version patches.
* PR Check report was added as Early Access to the available reports to identify Snyk PR check locations, increase adoption, and pinpoint common failure impacts on developer workflows.
* You can now label your assets with metadata on repository assets and build artifacts, helping tag, manage security, and group items by features. An asset label differs from an asset tag, which enables key-value tags for structured metadata, allowing for granular filtering, policy creation, and improved system alignment.
* [JavaScript for open source](supported-languages/supported-languages-list/javascript/#javascript-for-snyk-open-source) has been updated to include full support for pnpm Projects.

## September 2025

### **Snyk Container**

* The instructions for [installing the Snyk Controller on Amazon Elastic Kubernetes Service (Amazon AKS)](/broken/pages/Pa2LsQjWVP7fAtA5vWdL#create-an-eks-node-role-for-your-node-group-and-add-the-trust-relationship-for-the-iam-role) have been updated with details for configuring trust relationships for the IAM role.
* The list of [operating system distributions supported by Snyk Container](/broken/pages/MgFrePnlbvurSaWmgk1R) has been updated to include SUSE Linux Enterprise Server 15.7 and Rocky Linux 10.

### **Snyk integrations**

* The SCM integration for Bitbucket Data Center/Server now supports the Required Builds feature for granular control over pull requests. To learn more, visit [Required Builds](/broken/pages/bbJXoUXuzIFdCJ5H6NEc#required-builds).
* [GitLab](/broken/pages/W8wAyxeVYWAz1fKExTVO#gitlab) is supported for PR check results. This feature blocks merge requests with security issues when the "Pipelines must succeed" setting is enabled.
* The Snyk MCP quick guides list has been enriched with the following guides: [Claude Code](/broken/pages/etd50TrOct4hdbvHeIIr), [Continue](/broken/pages/kcMQZTJCAsVNqyuq4VpK), [JetBrains AI Assistant](/broken/pages/I5Sh6AacFhWVPxw2jHFa), [JetBrains Junie](/broken/pages/d0KjRrKbYE9lf7jfeZHB)

### **Other updates**

* For Java and Kotlin, the list of [supported Gradle versions](supported-languages-package-managers-and-frameworks/java-and-kotlin/#supported-package-managers-and-package-registries) now includes Gradle 9.
* For [Ruby](supported-languages/supported-languages-list/ruby.md), an end-of-support notice has been added to say that starting Oct 1, 2025, Fix PRs are no longer supported for Projects using Ruby versions 3.1.x and lower. The table of supported Ruby versions has also been updated.
* For Javascript, [support for pnpm Projects](supported-languages/supported-languages-list/javascript/#support-for-pnpm) has been added.
* `Raise Support Community Cases` and `View Support Community Cases` Tenant level permissions have been added. To learn more about which Tenant roles these permissions apply to, visit Pre-defined roles, [Tenant-level permissions](/broken/pages/XNksHYxr70heqewL6k3D#tenant-level-permissions).
* The [Analytics](/broken/pages/BMi0F0SumchUc2wiIH5v) menu now updates its data daily instead of hourly.
* Learn how to resolve duplicated and unenriched assets discovered outside Group and Organization-level SCM integrations.
* You can now [exclude specific values](/broken/pages/n3TechyZbEmvCh4okzNQ) when you filter your reports.

## August 2025

### **Snyk API**

* The [Export API](/broken/pages/1kmTPh7zLAD2U3qzA9GD) has been enhanced with the project\_target\_file field.
* A new dataset for usage events has been added to the [Export API.](/broken/pages/1kmTPh7zLAD2U3qzA9GD)

### **Snyk CLI**

* [Experimental builds ](/broken/pages/6Vhte2N6l1KsI6DbEfoJ#experimental-builds)information is now available for the CLI releases and channels.
* The [AI-BOM](/broken/pages/dseBHiQAm7kTvA2faDaw) Snyk CLI command is now available with any stable CLI release.
* A new Snyk CLI analytics page is now available, providing information about [Essential Operational Analytics](/broken/pages/VbKV6nbUXWWduqSlhHw9#essential-operational-analytics) and [Optional Usage Analytics](/broken/pages/VbKV6nbUXWWduqSlhHw9#optional-usage-analytics).

### **Snyk integrations**

* You can now add the Snyk MCP server to [Goose CLI](/broken/pages/CoeHokByMdTvdmbpmiU3) to secure code generated with agentic workflows through an LLM.
* You can now integrate Akamai with the Snyk API & Web to discover and scan your API. See the [API Security](/broken/pages/9naKDoxJTj9b7DJzIoUg#api-security) section under Partner integrations page for more details.
* The [Jira Cloud documentation](/broken/pages/8zCHQCjwscqIhLGGE5SN) has been updated for parity with the current version.

### **Other updates**

* A new [Risk exposure report](/broken/pages/fLpYTxz79MgYV44FXKoS#risk-exposure-report) has been released, providing you with a single, consolidated view of your security risks.
* The rollout to General Availability has started for the [Pull Request Experience](/broken/pages/4EzfnLftlTPRtCBeIOIN).
* The [Operating system distributions supported by Snyk Container](/broken/pages/MgFrePnlbvurSaWmgk1R) now includes Debian 14 - Forky.
* Snyk now supports [Ruby versions](supported-languages/supported-languages-list/ruby.md#technical-specifications) 3.3 \[3.3.9] and 3.4 \[3.4.5]. If the Ruby version is not specified in the gemfile, it will default to version 3.1.

## July 2025

### **Snyk API**

* The [Export API](/broken/pages/1kmTPh7zLAD2U3qzA9GD) is now available as GA.
* The Assets API is now available as Early Access.

### **Snyk CLI**

* MCP updates:
  * [Updated the list of supported Snyk security tools into an AI system](/broken/pages/ZXX8R1Mwg3ejaKXdm5iy#snyk-studio-tools).
  * Updated release status from experimental to [Early access](discover-snyk/getting-started/snyk-release-process.md#early-access-features) and removed the experimental flag.
  * Added [Cursor](/broken/pages/fQ3PUe4HVKQO5VrTW1h4) as a new supported agentic IDE for MCP.
* PAT updates:
  * Added PAT support for [Snyk CLI](/broken/pages/XurLzUfRULfzMIxjt6Jy).
  * Added PAT support for Snyk CI/CD integrations ([CircleCI](/broken/pages/UjviiOUN6MEqawzrMb95), [Jenkins](/broken/pages/CF0Nlmgc3znbmQI1T8bz), [Maven](/broken/pages/8PRxnyu6tYwbw5JhwcMN)).

### **Snyk Code**

* Support for Python, JavaScript and Typescript now includes more frameworks.

### **Snyk Container**

[Operating system distributions supported by Snyk Container](/broken/pages/MgFrePnlbvurSaWmgk1R) has been updated to include: SUSE Linux Enterprise (SLE) 15.3+, Red Hat Enterprise Linux 10, and Oracle Linux 10.

### **Snyk IDE**

* Added PAT support for all [Snyk IDE](/broken/pages/OWQNUoqm7FrjlbC3vcXP) plugins and extensions.
* Added an [IDE Plugin Compatibility Matrix](/broken/pages/HgUkS14JmBImjHHYhP1M) for all supported versions.

### **Snyk integrations**

* [Snyk Agent Fix in the PR](/broken/pages/4EzfnLftlTPRtCBeIOIN#snyk-agent-fix-in-the-pr) has added support for Bitbucket integrations, still in Early Access.
* The [minimum version](/broken/pages/ayI25YDO7XOf8qjt9t4C) of Bitbucket Server and Bitbucket Data Center required to use the integrations with PR checks has been updated to 7.4 and 8 respectively.

### **Snyk Open Source**

[Scan open-source libraries and licenses](/broken/pages/xgyzAquFW2LGS1zwIGer), [Snyk License Compliance Management](/broken/pages/S9I60Saqp9wV8hPyp2JV), and [Fix your vulnerabilities](/broken/pages/2u7V4rIWmsExCtH82Qqe) have been updated with the new **Issues** tab layout.

### **Other updates**

* A new architecture for user documentation on developer tools is now available. This update groups the main developer tools into a single section and distinctly separates them from the integrations documentation.
* [Analytics](/broken/pages/ispZPc0rVpOSK18BekCl) has a fresh new look.
* Added [Snyk Assist](discover-snyk/snyk-learn/snyk-assist.md) documentation.
* The [Developer IDE and CLI usage](/broken/pages/fLpYTxz79MgYV44FXKoS#developer-ide-and-cli-usage) report has been improved with MCP-related data to provide better visibility into MCP usage.
* [Okta custom mapping documentation](implementation-and-setup/enterprise-setup/single-sign-on-sso-for-authentication-to-snyk/custom-mapping/examples-setting-up-custom-mapping-for-idps/example-setting-up-custom-mapping-for-okta.md#construct-a-value-expression-that-creates-a-roles-array-to-be-sent-to-snyk) has been updated to clarify handling of the `Arrays.flatten(appuser.snyk_orgs)` value during setup.

## June 2025

### **Snyk Broker**

* Updated the Snyk Broker documentation to include distinct steps for setting up the [Container Registry Agent with Docker](implementation-and-setup/enterprise-setup/snyk-broker/snyk-broker-container-registry-agent/#configuring-and-running-the-container-registry-agent), whether using the Classic or Universal Broker.
* Updated the [Using the API to set up Universal Broker](implementation-and-setup/enterprise-setup/snyk-broker/universal-broker/using-the-api-to-set-up-universal-broker/) documentation with a Prerequisites section and clarified that the Snyk Broker App ID differs for each [region](/broken/pages/JSacA44jLZg6roCCprQQ#broker-client-urls).
* Snyk Learn courses have been integrated into the [Universal Broker](enterprise-setup/snyk-broker/universal-broker/) pages.

### **Other updates**

* [Usage settings](/broken/pages/gfMN3CV44C1OcuCHHpjj) has been updated with the new **Billing and Usage** dashboard, available with the new Snyk Platform Access plan.
* [Snyk Platform Access credits](/broken/pages/vGaYgIHWWPcywR2AUF3F) has been added with brief information on the new Snyk Platform Access plan.
* The troubleshooting sections for all [Snyk IDE plugins](/broken/pages/OWQNUoqm7FrjlbC3vcXP), have been updated to include clear steps for working with the Logs details, which are available across all plugins.
* A new feature, the [Snyk Agent Fix in the PR](/broken/pages/4EzfnLftlTPRtCBeIOIN#snyk-agent-fix-in-the-pr), has been released, enabling the user to interact with inline comments by requesting an initial fix or a different suggestion, or by applying a specific fix by using the `@snyk /apply #` command.
* [Consistent Ignores](/broken/pages/3O1axcZQqxWZ7SfDBWU2) for Snyk Code now fully supports CLI Upload.
* The page on Docker Desktop Extension integration has been removed, due to the end of support.

## May 2025

### **Snyk CLI**

* The `--platform` option was added to the [`container sbom`](/broken/pages/Mx5qgK8sIAuIxfP2xdSM) command.
* The MCP information was expanded to [Developer guardrails for agentic workflows](/broken/pages/ZXX8R1Mwg3ejaKXdm5iy).

### **IDE plugins and extensions**

* Information was added to the [JetBrains plugin troubleshooting](/broken/pages/Hqnce9hdeDZBE2Y3DR3H).
* Region information was updated on all [IDE pages](/broken/pages/OWQNUoqm7FrjlbC3vcXP).

### **Snyk Code**

* Legacy ignores can be converted using [bulk ignore conversion](/broken/pages/EFPTP3vtdsXoXywwvMPG#bulk-ignore-conversion).
* DeepCode AI Fix has a new name: [Snyk Agent Fix](/broken/pages/pEZ1aw9qJSIj3NddeyoQ).

### **Snyk Container**

[Configure the integration with Docker Hub](/broken/pages/OxSpeBNrMgzF4MOKhDQD) has been updated to state that Snyk does not support Organization Access Tokens (OAT).

### **Snyk Integrations**

The [Bitbucket Cloud App](/broken/pages/qf5A2ekieSDaNixdGv08) and [Jira App](/broken/pages/8zCHQCjwscqIhLGGE5SN) integrations are now available in the `SNYK-US-02` environment.

### **Other updates**

* For [SCM integrations with Python](supported-languages/supported-languages-list/python/scm-integrations-and-python.md), the list of dependencies that are not supported has been updated to include `pip` for Python 2.7 and 3.7.
* [Python dependency filtering results](supported-languages/supported-languages-list/python/scm-integrations-and-python.md) have been updated to clarify the conditions in which certain packages and configurations are skipped by SCM scans.
* The list of supported package managers has been updated to include `conan`. See [C/C++](supported-languages/supported-languages-list/c-c++/), [SBOM test](/broken/pages/nZleIPs8JENYElpbSLR5), [Test an SBOM document for vulnerabilities](/broken/pages/6qyuMaW3fgI5zskPfPpb).
* [Instructions for upgrading an Organization integration from Classic Broker to Universal Broker](implementation-and-setup/enterprise-setup/snyk-broker/universal-broker/upgrade-an-organization-integration-from-classic-broker-to-universal-broker.md) were clarified.

## April 2025

### **Snyk API**

* Several APIs have been updated; see the [Changelog](/broken/pages/sPPk40XEPFC4MSDJ62DO).
* The navigation in the API section now reflects the use of Authentication and the Changelog for both the V1 and REST APIs.
* The [Authentication for API](/broken/pages/sZnVmeZvNLxOL4uHy3Wx) page has been updated with region information and clarity on using the bearer token.
* The [API endpoints index and tips](/broken/pages/Wr8Smn99fRYSVtJ6VuIg) page now has a note about how to find your `org_id`.

### **Snyk Essentials**

* [The Inventory Overview tab](/broken/pages/VMCKJe3yElYb8cTQrSXf) is now available to provide insights and prescriptive guidance to improve your application security.
* [The Visibility column](/broken/pages/pFNNg6FMwP7rLqEUdmun#visibility) has been added to show the visibility status of your repositories.

### **Snyk Broker**

Additional updates have been made to the [Universal Broker](/broken/pages/jFEfCFusEEKxY5YoKQAw) documentation to clarify the instructions and add details about the use of the APIs.

### **Snyk CLI**

Information has been added about Snyk support for the Model Context Protocol (MCP) through the [`snyk mcp` experimental CLI command](/broken/pages/eyZvPk292ErICLAFFXaS).

### **Snyk Code**

* [Consistent Ignores ](/broken/pages/3O1axcZQqxWZ7SfDBWU2)is now available in Early Access. Your development teams can create ignores that are consistently respected regardless of how and where the test is run and what branch is being tested.
* Snyk Code supports gRPC libraries.

### **Snyk Container**

* [Using Custom Base Image Recommendation](/broken/pages/PDxBJ7rfWc64PZSWCaNO) has been updated with clarifications on how Snyk recommends images.
* The list of [Operating system distributions supported by Snyk Container](/broken/pages/MgFrePnlbvurSaWmgk1R) has been updated to include Alpine Linux 3.21, Ubuntu 25.04 - Plucky Puffin, and Ubuntu 24.10 - Oracular Oriole.
* The section describing the automated integration process for Amazon Elastic Container Registry (ECR) has been removed, as Snyk no longer supports this method.

### **Snyk Integrations**

* For the [Jira integration](/broken/pages/vjOMCauWUJDcqNW5wkXK#prerequisites-for-jira-integration-with-snyk), Snyk now supports Jira versions 5 to 10.
* For [SCM integrations with Gradle](supported-languages-package-managers-and-frameworks/java-and-kotlin/git-repositories-with-maven-and-gradle.md), Snyk now supports `allprojects` and `subprojects` blocks, as well as Spring Boot plugins BOMs.

### **Other updates**

* DAST scanning is now available with [Snyk API & Web](/broken/pages/guZhuC4o4zRSvnScRTiT#select-scanning-methods), enabling users to discover and test the security of their APIs and web apps, including AI-generated ones.
* PR Checks is now available with a General Availability release status.

## March 2025

### **Snyk Broker**

* The Snyk Broker section has been divided into [Universal Broker](enterprise-setup/snyk-broker/universal-broker/) and [Classic Broker](implementation-and-setup/enterprise-setup/snyk-broker/classic-broker/) documentation and the [main page](implementation-and-setup/enterprise-setup/snyk-broker/) has been updated.
* The Classic Broker installation instructions now include the command to set the `BROKER_SERVER_URL` for [Docker](enterprise-setup/snyk-broker/classic-broker/install-and-configure-snyk-broker/install-and-configure-broker-using-docker.md) and the `brokerServerUrl` for [Helm](enterprise-setup/snyk-broker/classic-broker/install-and-configure-snyk-broker/install-and-configure-broker-using-helm.md).

### **Snyk API**

* The [V1 API overview](/broken/pages/gpPn1NS3mzF7BKKBBZnI) and [reference](/broken/pages/ECyJAJMN5IqcBO66xEja) are now on the user docs site only. Additional details from Apiary have been added to the V1 reference on the user docs site. The API reference has been removed from the V1 API Apiary site.
* A section has been added for [pages that explain how to use specific APIs in depth](/broken/pages/12g7wDANR4EdBT2njlaC).

### **Snyk CLI, CI/CD, IDE**

* [Advanced use of Snyk Container CLI](/broken/pages/Qu8aHBy6xgNy0wZg2pjW) now includes support for scanning Kaniko image archives.
* The [support policy for the CI/CD plugins](/broken/pages/pRDRUD7zlzkFwSnoufwe#support-policy) was updated to align with the CLI support policy.
* The Net new issues feature was added to the IDE documentation for [Eclipse](/broken/pages/Y66SCByA2uEgCz8ulzfZ#net-new-issues-versus-all-issues), [JetBrains](/broken/pages/FEYe0UcKeceUbZLdspk1#net-new-issues-versus-all-issues), [Visual Studio](/broken/pages/c8WBSW46AOQwUajgrpWx#net-new-issues-versus-all-issues), and [Visual Studio Code](/broken/pages/GMXfvr0fEjYw4WIiY2kM#net-new-issues-versus-all-issues), and [troubleshooting information](/broken/pages/32MAaVq3ZsxFQW70bixg) was added.

### **Snyk Code**

* The Generated Pull Requests report is now available in Early Access. This report provides an overview of how Fix, Backlog, and Upgrade PRs are used and highlights the efficiency of PR merges.
* [The Pull Request Experience](/broken/pages/4EzfnLftlTPRtCBeIOIN) now supports GitLab and Azure Repos SCM integrations, with a few [limitations](/broken/pages/4EzfnLftlTPRtCBeIOIN#inline-comments).
* New Snyk Code filters and columns were added to [Snyk Reports](/broken/pages/yXnlgY8PW3vOTtDuLKkc#issue-characteristics) and [Snowflake Data Share](/broken/pages/JsCDBJ7iHuf2FmEK7PtX): File Path, Code Region, and Asset Finding ID.
* Snyk Code now supports [Rust](supported-languages/supported-languages-list/rust.md) and [Groovy](supported-languages/supported-languages-list/groovy.md) available in Early Access and accessible from Snyk Preview.

### Snyk Essentials

* A new feature is now available in Snyk Essentials, introducing a new type of [asset tag](/broken/pages/2bOYG0BUPNve8C912nBT#asset-tagging) known as GitHub custom properties.
* [Asset tags](/broken/pages/pFNNg6FMwP7rLqEUdmun#tags) have been redefined and are now clearly separated into system tags and user-defined tags.

### **Snyk Integrations**

* The [GitHub Server App](/broken/pages/ERFI3bAU1nLD7EoT4pTe) has moved into General Availability.
* The [Jira integration documentation](/broken/pages/vjOMCauWUJDcqNW5wkXK#prerequisites-for-jira-integration-with-snyk) has been updated to state that Snyk supports version 5 to version 9.

### **Other updates**

* The [PCI-DSS v4.0.1 report](/broken/pages/fLpYTxz79MgYV44FXKoS#pci-dss-v4.0.1-report) is now available in Early Access. This report leverages Snyk scan results to assess, prove, and improve readiness for PCI-DSS AppSec compliance regarding SCA and SAST vulnerabilities.
* The [Repositories Tested in CI/CD report](/broken/pages/fLpYTxz79MgYV44FXKoS#repositories-tested-in-ci-cd-report) is available in Early Access. This report tracks Snyk CI/CD testing to prevent vulnerable production deployments.
* [Severity levels](/broken/pages/JhnKMHkgiHwuiqrPYCEb#why-are-there-multiple-cvss-scores-for-the-same-vulnerability) now provide more details about the CVSS v4.0.

## February 2025

### Snyk Essentials

* The Integrations UI at the Group level has been enhanced to improve readability and actionability and provide inline instructions and inline profile helpers.
* Group-level [Integrations documentation](/broken/pages/xwry3aDtePANCG1oKbgw#integrations-syncing-time) has been updated with new, more accurate sync times.
* The [asset filter](/broken/pages/4Xks0gPRz2QeZafju1Tw) documentation has been consolidated into one section, and it now links to all relevant areas, such as Inventory and Asset Policy filters.
* [Issues Analytics](/broken/pages/0NAoz3x5XZZVmWqGvOVy) is now available with a General Availability release status.

### Other updates

* A new [Automated Provisioning guide](implementation-and-setup/enterprise-setup/auto-provisioning-guide.md) has been created for **Pilot** and **Enterprise** **users**, detailing the steps of the auto-provisioning process for new and existing user accounts.
* [Snyk Code PR Checks](/broken/pages/ayI25YDO7XOf8qjt9t4C#configure-for-code-analysis-click-to-expand) are in General Availability.

## December 2024 and January 2025

### **Snyk Container**

* Page "Integrate with Docker Desktop Extension" has been updated to include an end-of-support notice. Effective June 20, 2025, the integration with Docker Desktop will no longer receive updates or technical support.

### **Snyk CLI and IDEs**

* [Eclipse IDE](/broken/pages/j7AOvFyfxRPzSjhsBNUq) major update
* [Visual Studio IDE](/broken/pages/uZcKqI9uJub1vgh6ORJd) major update
* Region configuration update for [IDEs](/broken/pages/OWQNUoqm7FrjlbC3vcXP)
* [Snyk images EOL policy updated](/broken/pages/VGq4kZMQv4FKZKEC5GfJ)
* [`snyk container test`](/broken/pages/amAv5P52XqPzbw5Vfpwj) and [`snyk container monitor`](/broken/pages/hHmY0Y3otsm00e5f66Ap) option `--exclude-node-modules` added

### **Other updates**

* [Snyk Admin](/broken/pages/MXicuilyieYCoMggeNgj) pages have been updated to reflect the addition of [Tenants](/broken/pages/YCvtOyrXkSg1d2tj0Ux8) in the Snyk hierarchy, including a new infographic to illustrate the Tenant position in the [hierarchy](/broken/pages/bNgd7bJkGk7MGdumvqYR#the-snyk-hierarchy).

## November 2024

### **Snyk Essentials**

### **Snyk Container**

* The list of [operating system distributions supported by Snyk Container](/broken/pages/MgFrePnlbvurSaWmgk1R) has been updated to include Ubuntu 24.10 - Oracular Oriole and Ubuntu 24.04 - Noble Numbat 04.
* [How Snyk Container works](/broken/pages/Yo3ugnNhE0xY00SxPOx4) has been updated with details on the logic Snyk applies when providing public base image recommendations.

### **Other updates**

* The Pull Request Checks section has been updated to include the new [Pull Request Experience](/broken/pages/4EzfnLftlTPRtCBeIOIN) for PR Checks.
* The [Supported languages](supported-languages/supported-languages-package-managers-and-frameworks.md) page has been reorganized to provide detailed information about language availability for each Snyk product. Additionally, it provides a list of package managers, frameworks, and features for each supported language.
* A service account using OAuth 2.0 can now be [created through the Snyk Web UI](implementation-and-setup/enterprise-setup/service-accounts/service-accounts-using-oauth-2.0.md#create-oauth-service-accounts-through-the-ui).
* The [API index ](/broken/pages/Wr8Smn99fRYSVtJ6VuIg)now includes entries for each endpoint mentioned in the Snyk user docs.
* The[ Developer IDE and CLI usage](/broken/pages/fLpYTxz79MgYV44FXKoS#developer-ide-and-cli-usage) report has been enhanced with additional functionalities: **Developer email address** and **PDF export**.
* The [Vulnerabilities Detail](/broken/pages/fLpYTxz79MgYV44FXKoS#vulnerabilities-detail-report) report has been enhanced with additional functionalities, such as **Target indication** and **Column picker**.

## October 2024

### **Snyk API**

* [Asset inventory components](/broken/pages/pFNNg6FMwP7rLqEUdmun#clusters) has been updated to include details on clusters.

### **Snyk CLI and IDEs**

* The [CLI authentication page](/broken/pages/XurLzUfRULfzMIxjt6Jy) has been updated for the OAuth 2.0 protocol.
* The page [Debugging the Snyk CLI](/broken/pages/itq6lWS45pWG8dvsWQAh) has been added.
* [CLI standalone executables](/broken/pages/KUVsQmktSlBzw3LlQdio#install-with-standalone-executables) have been updated to include Alpine Arm64.
* IDE Eclipse[ plugin](/broken/pages/j7AOvFyfxRPzSjhsBNUq) and [JetBrains plugin ](/broken/pages/Zh1Cr8JwIgs2j19UcaKh)documentation pages have been updated.
* [Authentication information](/broken/pages/OWQNUoqm7FrjlbC3vcXP) has been updated for all IDEs.

### **Snyk Integrations**

* [Snowflake Data Share](/broken/pages/EPtJutHgCG40vHc8x9q6) is now in [GA](discover-snyk/getting-started/snyk-release-process.md).
* [Snyk SCM integrations](/broken/pages/LNOXZ05NnHPVVNO7KcJH) has been updated with additional notices relating to repository retrieval and permission or scope modifications after initial configuration.
* GitHub Cloud App has been added to feature support notices for Fix, Backlog, and Upgrade PRs.
* Snyk SCM integrations has been updated to include a table detailing the [permissions and scopes](/broken/pages/2QJhLf5QB0qPBznNl9TE#github-cloud-app-permission-requirements) required for the GitHub Cloud App.

### **Other updates**

* [Getting started](discover-snyk/getting-started/) has been updated to centralize content related to everything you need to know before using Snyk.
* Scanning methods have been added for the [Dart and Flutter](supported-languages/supported-languages-list/dart-and-flutter.md) languages.

## September 2024

### Snyk API

* A prerequisites section has been added to the Group level of [GitHub integration](/broken/pages/nyteKuwjuiougUcOmurw#prerequisites), and more details about the [Pull personal repositories](/broken/pages/ZvXMfSTsBxBdsrDJezQZ) option have been added to the same documentation page.
* The [Set up Insights](/broken/pages/a1GmeqRNHZ3tJN3c2ULH) section was updated to emphasize the risk factors availability for each integration option.
* The Snyk Runtime Sensor has been updated to reflect the importance of adopting it to achieve the most effective integration and to access its continuously expanded set of features.

### Snyk Broker

The Universal Broker feature is now available in Early Access. The Universal Broker separates deployment and container concerns from connection concerns. It allows for a smaller or a single deployment to support numerous connections of varied types.

### Snyk CLI

* The [CLI commands and options summary](/broken/pages/4ipsV5z7ecuTQbH6s3oW) was updated.
* [Authentication](/broken/pages/XurLzUfRULfzMIxjt6Jy) has been updated.
* Configuration has been updated: Environment variables for Snyk CLI, [`snyk config`](/broken/pages/UPIFDPxwach4UFaSrLKd) help, [`snyk config environment`](/broken/pages/En6bzvVfwK3fyPsLE6b8) help.

### Snyk Integrations

The Snowflake Data Share section has been updated to include a [Data Share Dictionary](/broken/pages/JsCDBJ7iHuf2FmEK7PtX), designed to help you navigate and build your dataset.

### Other updates

* The updated [Regional hosting and data residency](/broken/pages/JSacA44jLZg6roCCprQQ) page was published.
* [Glossary](discover-snyk/getting-started/glossary.md) terms were updated for SCA, SAST, DAST, and IAST as well as Software Composition Analysis.
* [Early Access](discover-snyk/getting-started/snyk-release-process.md#early-access) release status notices were updated.

## August 2024

### Snyk API

* Links in the API reference docs have been updated.
* The [API endpoints index and notes](/broken/pages/Wr8Smn99fRYSVtJ6VuIg) have been updated.

### Snyk Essentials

### Snyk CLI

* [`snyk auth`](/broken/pages/vGilzhqiXuKYn8yDsCOu) command help updated to reflect OAuth default.
* [CLI authentication](/broken/pages/XurLzUfRULfzMIxjt6Jy) instructions updated for OAuth default and improved flow.
* [`snyk config environment`](/broken/pages/En6bzvVfwK3fyPsLE6b8) command help has been added.
* CLI [support for pnpm added](supported-languages/supported-languages-list/javascript/#support-for-pnpm).

### Snyk IDE

* [CLI authentication](/broken/pages/XurLzUfRULfzMIxjt6Jy) instructions updated for IDE.
* IDE authentication instructions updated: [Eclipse](/broken/pages/RynrPZ3Z4FNVhd7c4Nzo), [Jetbrains](/broken/pages/gv166yFwTNpRom7Q0TEf), [VS extension](/broken/pages/BWYVd0qtChBn9OlOcGbg), [VS Code extension](/broken/pages/iReTz6ORYp76RFyf4DNE)

### **Snyk Integrations**

* Git repository cloning has been renamed [Workspaces for SCM integrations](/broken/pages/TuZEhC7XyJEPG00DiKD2) to better reflect its functionality. Additional detail on [enablement](/broken/pages/TuZEhC7XyJEPG00DiKD2#manage-workspaces) has been added.
* The [relationship](/broken/pages/mAsNuoNuZyD3AM0hMELI#how-to-set-up-the-github-cloud-app) between GitHub organizations and Snyk Organizations when integrating with the GitHub Cloud App has been clarified.

## July 2024

### **Snyk API**

* The API documentation now provides the API Reference and explanatory documentation in the [API section](/broken/pages/WJR3UthqfOfZZs4uhhwu).
* The [API End of Life (EOL) process and migration guides](/broken/pages/pNbLzJmwQBwdyu1Emsu6) are now published and updated to support the process, which began in July.
* [Asset inventory filtering](/broken/pages/pFNNg6FMwP7rLqEUdmun#asset-tabs) describes the new, simplified view that provides an improved experience of filtering the assets.
* The [Asset inventory layouts](/broken/pages/VMCKJe3yElYb8cTQrSXf) have been renamed to better reflect their functionality.
* Four new SCM integrations are now available for Snyk:
  * [Atlassian Compass](/broken/pages/02qFHiSuRZqcR8LYBBEs#atlassian-compass)
  * [Harness](/broken/pages/02qFHiSuRZqcR8LYBBEs#harness)
  * [OpsLevel](/broken/pages/02qFHiSuRZqcR8LYBBEs#opslevel)
  * [Datadog Service Catalog](/broken/pages/02qFHiSuRZqcR8LYBBEs#datadog-service-catalog)

### Snyk Integrations

* A comparison of the GitHub and GitHub Enterprise integrations functions now resides on the [SCM, IDE, and CI/CD integrations](/broken/pages/ciKBZ9UfhCVJ7g5uFCdB#github-vs-github-enterprise) page.
* Steps for [migrating from the GitHub integration to the GitHub Enterprise integration](/broken/pages/nPkWomOTKXA861LP8KTp#migrate-to-the-github-enterprise-integration) now reside on the GitHub integration page.
* The [Snyk SCM Integrations](/broken/pages/LNOXZ05NnHPVVNO7KcJH) page now contains information critical to using these integrations successfully in your SDLC. This includes:
  * [Git repository cloning](/broken/pages/TuZEhC7XyJEPG00DiKD2) details
  * [Deployment recommendations](/broken/pages/1NYL0m6HKnOghItgEC2t) for Enterprise customers
  * [User permissions and access scope requirements](/broken/pages/2QJhLf5QB0qPBznNl9TE) for each SCM integration
  * Instructions on how to generate [integrated SCM tokens for Snyk Broker](/broken/pages/jodE68LTzW7LBttN35iN#integrated-scm-tokens-for-classic-broker)

### **Other updates**

* **Snyk Reports:** The [issue column dictionary](/broken/pages/yXnlgY8PW3vOTtDuLKkc#issue-vulnerability-details) includes new filters and columns for Jira (JIRA ISSUES LIST, LATEST JIRA ISSUE) and EPSS (EPSS SCORE, EPSS PERCENTILE). This allows you to manage your work with Jira and to include EPSS in your prioritization steps.
* **Snyk Security:** Snyk has improved the prioritization workflow and risk assessment by adopting [CVSS V4.0](/broken/pages/JhnKMHkgiHwuiqrPYCEb#severity-levels-and-cvss) as the default evaluation for new vulnerabilities.
* **Fix code vulnerabilities automatically:** [DeepCode AI Fix](/broken/pages/pEZ1aw9qJSIj3NddeyoQ#snyk-agent-fix-language-support) is now available in AWS Environments and JetBrains IDEs. If you use AWS multi-tenant environments, turn on the Snyk Preview [Snyk Code Fix Suggestions](/broken/pages/pEZ1aw9qJSIj3NddeyoQ#enable-snyk-agent-fix) and retest with Snyk in your IDE.
