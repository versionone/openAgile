# openAgile Evolve Maintain Plan

Once an integration has completed the [Exodus](https://github.com/versionone/openAgile/blob/master/Evolve/Exodus.md), the Evolve team will then enter the Maintain phase. In this phase, the integrations will be brought up-to-date to target the latest version of the systems that they integrate with, will get expanded unit testing, and will get automate integration testing so that we may better ensure their integrity. This may include removing and/or enhancing their functionality.

## Integrations Slated for Maintain

Based on the [Integration Checklist: Summer 2014](http://confluence/display/V1Integrations/Integration+Checklist+2014+%283%29+Summer), the following is the list of integrations that the Evolve team will maintain:

<table border="1" width="100%">
	<tr>
		<th>Name</th>
		<th>Type</th>
		<th>Repo</th>
	</tr>
	<tr>
		<td>Bugzilla</td>
		<td>.NET (ServiceHost + Perl scripts)</td>
		<td>https://github.com/versionone/VersionOne.Integration.Bugzilla</td>
	</tr>
	<tr>
		<td>Clarity PPM</td>
		<td>Java</td>
		<td>https://github.com/versionone/VersionOne.Integration.ClarityPPM</td>
	</tr>
	<tr>
		<td>CruiseControl</td>
		<td>Java</td>
		<td>https://github.com/versionone/VersionOne.Integration.CruiseControl</td>
	</tr>
	<tr>
		<td>Hudson</td>
		<td>Java</td>
		<td>https://github.com/versionone/VersionOne.Integration.Hudson</td>
	</tr>
	<tr>
		<td>Innovation Games</td>
		<td>.NET (ServiceHost)</td>
		<td>https://github.com/versionone/VersionOne.Integration.Buy-A-Feature</td>
	</tr>
	<tr>
		<td>Jenkins</td>
		<td>Java</td>
		<td>https://github.com/versionone/VersionOne.Integration.Jenkins</td>
	</tr>
	<tr>
		<td>JIRA</td>
		<td>.NET (ServiceHost)</td>
		<td>https://github.com/versionone/VersionOne.Integration.JIRA</td>
	</tr>
	<tr>
		<td>LDAP Provisioning</td>
		<td>.NET</td>
		<td>https://github.com/versionone/VersionOne.Provisioning.LDAP</td>
	</tr>
	<tr>
		<td>Perforce</td>
		<td>.NET (ServiceHost)</td>
		<td>https://github.com/versionone/VersionOne.Integration.Perforce</td>
	</tr>
	<tr>
		<td>Quality Center</td>
		<td>.NET (ServiceHost)</td>
		<td>https://github.com/versionone/VersionOne.Integration.QualityCenter</td>
	</tr>
	<tr>
		<td>Salesforce</td>
		<td>SFDC Apex</td>
		<td>https://github.com/versionone/VersionOne.Integration.Salesforce</td>
	</tr>
	<tr>
		<td>Subversion</td>
		<td>.NET (ServiceHost)</td>
		<td>https://github.com/versionone/VersionOne.Integration.Subversion</td>
	</tr>
	<tr>
		<td>TeamCity</td>
		<td>Java</td>
		<td>https://github.com/versionone/VersionOne.Integration.TeamCity</td>
	</tr>
	<tr>
		<td>TFS</td>
		<td>.NET</td>
		<td>https://github.com/versionone/VersionOne.Integration.VSTFS</td>
	</tr>
</table>

## Pre-Maintain Actions

Prior to beginning to work on integration maintenance, there are a few actions that we will need to take:

* Refactor ServiceHost Configuration Tool (may require work from openAgile Sprint Team)
* Refactor ServiceHost
* Refactor additional shared dependencies (i.e. WorkitemServices, ServerConnector, etc.)
* Refactor OAuth enablement approach (client.secrets and stored.credentials file dependency)

## Maintain Actions Checklist

As we move each integration into maintenance mode, there is a common set of actions that we will need to take:

1. Create hosted test environment (Azure VMs) with current target system version
2. Ensure that integration compiles and works with current target system version
3. Update integration to use only OAuth for V1 authentication
4. Triage related GitHub issues and add to backlog as needed
5. Expand unit test coverage using mocking frameworks as needed
6. Create automated integration test coverage for major workflows using hosted test environment
7. Create installer package (Chocolatey|WIX|Installshield)
8. Update integration documentation
9. Update integration AppCatalog entries
10. Develop transition plan for integration monitoring

> The goal of all of this is to make integration maintenance uniform and consistent so that some other team can take ownership of verifying their integrity. Should the other team find issues with an integration, the openAgile team will still own the development work.