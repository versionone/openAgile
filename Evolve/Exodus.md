# openAgile Evolve Exodus Plan

An primary goal of the Evolve Team is to unlock legacy integrations from the internal SVN repository, update and refactor them, then make them available in GitHub as open source solutions. As discussed in the [openAgile Evolve Charter](Chater.md), the team will focus on the following tasks for the Exodus:

## Integrations Slated for Exodus

We will Exodus the following integrations, order TBD:

<table border="1" width="100%">
	<tr>
		<th>Name</th>
		<th>Repo</th>
		<th>Notes</th>
	</tr>
	<tr>
		<td>Innovation Games</td>
		<td>https://github.com/versionone/VersionOne.Integration.Buy-A-Feature</td>
		<td>Repo contains documentation only.</td>
	</tr>
	<tr>
		<td>JIRA</td>
		<td>https://github.com/versionone/VersionOne.Integration.JIRA</td>
		<td>Repo contains documentation only.</td>
	</tr>
	<tr>
		<td>Perforce</td>
		<td>https://github.com/versionone/VersionOne.Integration.Perforce</td>
		<td>Repo contains documentation only.</td>
	</tr>
	<tr>
		<td>Quality Center</td>
		<td>https://github.com/versionone/VersionOne.Integration.QualityCenter</td>
		<td>Repo contains documentation only.</td>
	</tr>
	<tr>
		<td>Subversion</td>
		<td>https://github.com/versionone/VersionOne.Integration.Subversion</td>
		<td>Source code is in repo, buts needs cleanup and verification.</td>
	</tr>
</table>

## Shared Components

A key aspect of the Exodus is to find common dependencies and break them out as individual projects, cleanup and verify them, then put them into their own GitHub repositories to be referenced by the integration projects. Where it makes sense, we will extrapolate the components into a public repository such as MyGet/NuGet.

<table border="1" width="100%">
	<tr>
		<th>Name</th>
		<th>Repo</th>
		<th>Notes</th>
	</tr>
	<tr>
		<td>ServiceHost.Core</td>
		<td>https://github.com/versionone/VersionOne.ServiceHost.Core</td>
		<td>Source code is in repo, buts needs cleanup and verification.</td>
	</tr>
	<tr>
		<td>ServiceHost.ConfigurationTool</td>
		<td>REPO DOES NOT EXIST</td>
		<td>Needs cleanup and verification.</td>
	</tr>
</table>

## Pre-Exodus Actions

Prior to moving integrations into their own GitHub repositories, there are a few actions that we will need to take:

1. Purge the [ServiceHost GitHub Repo](https://github.com/versionone/ServiceHost) of sunset integrations
2. Run the [VS Solution Dependency Visualizer](http://www.devio.at/index.php/vsslndepvis) to understand all dependencies
3. Break out common dependencies into shared components
4. Create Jenkins build job using psake tools for each shared component
4. Publish the common dependencies in MyGet/NuGet as needed
 
## Exodus Actions Checklist

As we Exodus each integration, there is a common set of actions that we will need to take:

1. Detangle integration from ServiceHost solution, put it in its own GitHub repo
2. Bring solution/project files up to latest IDE/Framework versions (Visual Studio 2013/.NET Framework 4.5.1 & Eclipse Luna/JDK 8)
3. Remove unnecessary dependencies (tool?)
4. Remove dead/commented out code (tool?)
5. Set all dependencies to use MyGet
6. Create new unit test project/package, pull in any existing usable tests
7. For .NET projects, refactor unit tests using MSTest
8. Bring integrations up to latest V1 SDK versions (.NET and Java API clients)
9. Research target system dependencies, make note of newer versions
10. Rename integration executable and config file to match integration name (not ServiceHost.exe)
11. Ensure that project compiles
12. Ensure the existing unit tests pass
13. Create Jenkins job for CI builds/unit test runs of integration
14. Confirm availability of integration documentation
15. Verify auto-population and accuracy of AppCatalog entries (staging)
16. Hold post-mortem to review lessons learned

> As we work through each integration, we'll look for problem areas and log them as GitHub issues. We will not be fixing those issues during the Exodus as our focus is to modernize and ensure that the current code compiles and functions. We will address issues during the [Maintain](https://github.com/versionone/openAgile/blob/master/Evolve/Maintain.md) phase.