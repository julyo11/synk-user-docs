# Apply security and license policies

Policies define how Snyk behaves when identifying issues. Policies give you a quick and automated way to identify, prioritize, and triage issues. This saves valuable development time and allows developers to take more responsibility and ownership for security, reducing the “noise” level.

See [Policies](/broken/pages/pSMvTbvxFhevQiQSH13s) for more details.

## Security policies

Group administrators can define security policies, thus providing an automated way to identify certain issues or types of issues, and apply actions like changing the severity or ignoring the issue based on your conditions.

* Configure policies to increase priority or decrease it as needed.
* Create ignores where needed

See [Security policies](/broken/pages/KhkVNMIq6t3wsULtc2Xq) for more details.

## License policies

Group administrators can set license policies to define Snyk behavior for treating license issues. For example, you can allow or disallow packages with certain license types, to avoid using packages containing incompatible licenses.

By default, Snyk determines the severity of licenses in the following way:

* High severity - licenses that definitely present issues for commercial software.
* Medium severity - licenses that have clauses that may be of concern and should be reviewed.

Configure policies to match your requirements.

See [Snyk License Compliance Management](/broken/pages/S9I60Saqp9wV8hPyp2JV) for more details.

## Asset policies

Policies can be created using the Policy Editor to:

* Notify user(s) using Slack or email when a condition is met
* create a Jira ticket
* Set classification using policy
* Set tags using policy
* Specify coverage policies, for example, scan not performed within a specified number of days
* For more information, navigate to the [Assets policies](/broken/pages/2bOYG0BUPNve8C912nBT) page.
