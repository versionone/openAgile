# openAgile Evolve Exodus Plan

An primary goal of the Evolve Team is to unlock legacy integrations from the internal Subversion repository, update and refactor them, then make them available in GitHub as open source solutions.  

## Integrations Slated for Exodus

We will unlock the following integrations, order of exodus TBD:

<table border="1" width="100%">
	<tr>
		<th>Name</th>
		<th>Repo</th>
		<th>Notes</th>
	</tr>
	<tr>
		<td>Subversion</td>
		<td>https://github.com/versionone/VersionOne.Integration.Subversion</td>
		<td>Source code is in repo, buts needs cleanup and verification.</td>
	</tr>
	<tr>
		<td>JIRA</td>
		<td>https://github.com/versionone/VersionOne.Integration.JIRA</td>
		<td>Repo contians documentation only.</td>
	</tr>
	<tr>
		<td>Quality Center</td>
		<td>https://github.com/versionone/VersionOne.Integration.QualityCenter</td>
		<td>Repo contians documentation only.</td>
	</tr>
	<tr>
		<td>Bugzilla</td>
		<td>https://github.com/versionone/VersionOne.Integration.Bugzilla</td>
		<td>Source code is in repo, buts needs cleanup and verification.</td>
	</tr>
	<tr>
		<td>CruiseControl</td>
		<td>https://github.com/versionone/VersionOne.Integration.CruiseControl</td>
		<td>Source code is in repo, buts needs cleanup and verification.</td>
	</tr>
	<tr>
		<td>ElectricCommander</td>
		<td>https://github.com/versionone/VersionOne.Integration.ElectricCommander</td>
		<td>Repo contians documentation only.</td>
	</tr>
	<tr>
		<td>Git</td>
		<td>https://github.com/versionone/VersionOne.Integration.GitSCM</td>
		<td>Source code is in repo, buts needs cleanup and verification.</td>
	</tr>
	<tr>
		<td>Hudson</td>
		<td>https://github.com/versionone/VersionOne.Integration.Hudson</td>
		<td>Empty repo.</td>
	</tr>
	<tr>
		<td>Jenkins</td>
		<td>https://github.com/versionone/VersionOne.Integration.Jenkins</td>
		<td>Source code is in repo, buts needs cleanup and verification.</td>
	</tr>
	<tr>
		<td>Innovation Games</td>
		<td>https://github.com/versionone/VersionOne.Integration.Buy-A-Feature</td>
		<td>Repo contians documentation only.</td>
	</tr>
	<tr>
		<td>LDAP Provisioning</td>
		<td>https://github.com/versionone/VersionOne.Provisioning.LDAP</td>
		<td>Source code is in repo, buts needs cleanup and verification.</td>
	</tr>
	<tr>
		<td>Perforce</td>
		<td>https://github.com/versionone/VersionOne.Integration.Perforce</td>
		<td>Repo contians documentation only.</td>
	</tr>
	<tr>
		<td>TeamCity</td>
		<td>https://github.com/versionone/VersionOne.Integration.TeamCity</td>
		<td>Source code is in repo, buts needs cleanup and verification.</td>
	</tr>
	<tr>
		<td>TFS</td>
		<td>https://github.com/versionone/VersionOne.Integration.VSTFS</td>
		<td>Source code is in repo, buts needs cleanup and verification.</td>
	</tr>
</table>


## Pre-Exodus Actions

Prior to moving integrations into their own GitHub repositories, there are a few actions that we will need to take:

1. Purge the [ServiceHost GitHub Repo](https://github.com/versionone/ServiceHost) of sunset integrations
2. Run the [VS Solution Dependency Visualizer](http://www.devio.at/index.php/vsslndepvis) to understand all dependencies
3. 
 
