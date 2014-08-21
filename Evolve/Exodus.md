# openAgile Evolve Exodus Plan

An primary goal of the Evolve Team is to unlock legacy integrations from the internal Subversion repository, update and refactor them, then make them available in GitHub as open source solutions.  

## Integrations Slated for Exodus

We will unlock the following integrations, order of exodus TBD:

* **Subversion**: Source code already in the [VersionOne.Integration.Subversion](https://github.com/versionone/VersionOne.Integration.Subversion) repo. Needs cleanup and verification.
* **JIRA**: 
* **Quality Center**: 
* **Bugzilla**: 
* **CruiseControl (Java version)**: 
* **ElectricCommander**: 
* **Git**: 
* **Hudson**: 
* Jenkins
* Innovation Games (BuyAFeature)
* LDAP Provisioning
* Perforce
* TeamCity
* TFS

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
</table>


## Pre-Exodus Actions

Prior to moving integrations into their own GitHub repositories, there are a few actions that we will need to take:

1. Purge the [ServiceHost GitHub Repo](https://github.com/versionone/ServiceHost) of sunset integrations
2. Run the [VS Solution Dependency Visualizer](http://www.devio.at/index.php/vsslndepvis) to understand all dependencies
3. 
 
