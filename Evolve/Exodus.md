# openAgile Evolve Exodus Plan

An primary goal of the Evolve Team is to unlock legacy integrations from the internal SVN repository, update and refactor them, then make them available in GitHub as open source solutions.

## Integrations Slated for Exodus

We will Exodus the following integrations, order TBD:

<table border="1" width="100%">
	<tr>
		<th>Name</th>
		<th>Repo</th>
		<th>Status</th>
		<th>Notes</th>
	</tr>
	<tr>
		<td>Innovation Games (BuyAFeatureServices)</td>
		<td>https://github.com/versionone/VersionOne.Integration.Buy-A-Feature</td>
		<td>Not Started</td>
		<td>Repo contains documentation only.</td>
	</tr>
	<tr>
		<td>JIRA (JiraServices)</td>
		<td>https://github.com/versionone/VersionOne.Integration.JIRA</td>
		<td>Started, needs to use shared components</td>
		<td></td>
	</tr>
	<tr>
		<td>Perforce</td>
		<td>https://github.com/versionone/VersionOne.Integration.Perforce</td>
		<td>Not Started</td>
		<td>Repo contains documentation only.</td>
	</tr>
	<tr>
		<td>Quality Center</td>
		<td>https://github.com/versionone/VersionOne.Integration.QualityCenter</td>
		<td>Not Started</td>
		<td>Repo contains documentation only.</td>
	</tr>
	<tr>
		<td>Subversion</td>
		<td>https://github.com/versionone/VersionOne.Integration.Subversion</td>
		<td>Started, needs to use shared components</td>
		<td>Source code is in repo, buts needs cleanup and verification.</td>
	</tr>
	<tr>
		<td>Bugzilla (Services)</td>
		<td>https://github.com/versionone/VersionOne.Integration.Bugzilla</td>
		<td>Started, needs to use shared components</td>
		<td>.</td>
	</tr>
	<tr>
		<td>TeamCity</td>
		<td>https://github.com/versionone/VersionOne.Integration.TeamCity</td>
		<td>Not started</td>
		<td></td>
	</tr>
</table>

## Shared Components

A key aspect of the Exodus is to find common dependencies and break them out as individual projects, cleanup and verify them, then put them into their own GitHub repositories. In addition, each component will have its own Jenkins job for compiling, running unit tests, and publishing to MyGet.

<table border="1" width="100%">
	<tr>
		<th>Name</th>
		<th>Repo</th>
		<th>Version</th>
	</tr>
	<tr>
		<td>ServiceHost.Core</td>
		<td>https://github.com/versionone/VersionOne.ServiceHost.Core</td>
		<td>Was 1.0.14247.228, reset to 1.1.0.0</td>
	</tr>
	<tr>
		<td>ServiceHost.ServerConnector</td>
		<td>https://github.com/versionone/VersionOne.ServiceHost.ServerConnector</td>
		<td>1.0.0.0</td>
	</tr>
	<tr>
		<td>ServiceHost.WorkitemServices</td>
		<td>https://github.com/versionone/VersionOne.ServiceHost.WorkitemServices</td>
		<td>1.0.0.0</td>
	</tr>
	<tr>
		<td>ServiceHost.TestServices</td>
		<td>https://github.com/versionone/VersionOne.ServiceHost.TestServices</td>
		<td>1.0.0.0</td>
	</tr>
	<tr>
		<td>ServiceHost.ChangesetServices</td>
		<td>https://github.com/versionone/VersionOne.ServiceHost.ChangesetServices</td>
		<td>1.0.0.0</td>
	</tr>
	<tr>
		<td>ServiceHost.ConfigurationTool</td>
		<td>REPO DOES NOT EXIST</td>
		<td>1.0.0.0</td>
	</tr>
</table>

## Packaging, Deployment, and Versioning

An important aspect of Exodusing the integrations is the use of a consistent process for build, test, package, and deployment. In this regard we will:

* Place all integration Jenkins jobs in the "Integrations" tab view
* Place all SDK Jenkins jobs in the "Platform" tab view
* Ensure that we use a consistent naming scheme for all Jenkins jobs using a "GitHub repo name-branch-phase" naming pattern
	* GitHub repo name: Should be consistent to group make it easier to find related projects
	* Branch: In most cases will be "master", but may use other branches as needed
	* Phases:
		* **Sandbox**: Triggered on demand, creates the test VM used for the integration
		* **Build**: Triggered from GutHub commits, compiles, executes unit tests
		* **Verify**: Triggered to run nightly, executes integration/end-to-end tests
		* **Deploy**: Triggered on demand, pachages then deploys to a public (release) repository such as NuGet/Maven Central, updates documentation and AppCatalog entries
* Ensure that we follow a consistent [versioning policy](https://github.com/versionone/openAgile/blob/master/VersionOne/Artifacts/VersioningPolicy.md)


## Pre-Exodus Actions

Prior to moving integrations into their own GitHub repositories, there are a few actions that we will need to take:

1. Purge the [ServiceHost GitHub Repo](https://github.com/versionone/ServiceHost) of sunset integrations
2. Run the [VS Solution Dependency Visualizer](http://www.devio.at/index.php/vsslndepvis) to understand all dependencies
3. Break out common dependencies into shared components
4. Create Jenkins build jobs using psake tools for each shared component
4. Publish the shared components in MyGet
 
## Exodus Actions Checklist

As we Exodus each integration, there is a common set of actions that we will need to take:

1. Detangle integration from ServiceHost solution, put it in its own GitHub repo
2. Check repo description, .gitignore, and Markdown files
3. Ensure that repo publishes commits to HipChat
2. Bring solution/project files up to latest IDE/Framework versions (Visual Studio 2013/.NET Framework 4.5.1)
3. Bring integration up to latest V1 API Client version
3. Remove unnecessary dependencies (tool?)
4. Remove dead/commented out code (tool?)
5. Update all dependencies to use MyGet/NuGet as appropriate
6. Review and refactor project build events
6. Create new unit test project, pull in any existing usable tests refactor using MSTest (see [Comparing the MSTest and NUnit Frameworks](http://blogs.msdn.com/b/nnaderi/archive/2007/02/01/mstest-vs-nunit-frameworks.aspx))
10. Rename integration executable and config file to match integration name (not ServiceHost.exe)
11. Ensure that project compiles (debug and release)
12. Ensure that existing unit tests pass
13. Create Jenkins "build" job for build/unit test runs, triggered from GitHub commit
14. Ensure Jenkins "build" job publishes success/failures to HipChat
15. Ensure Jenkins "build" job publishes MSTest results
14. Create Jenkins "deploy" job for MyGet deployment
15. Ensure Jenkins "deploy" job publishes success/failures to HipChat
14. Confirm availability of integration documentation
15. Verify auto-population and accuracy of AppCatalog entries (staging)
16. Hold post-mortem to review lessons learned

> As we work through each integration, we'll look for problem areas and log them as GitHub issues. We will not be fixing those issues during the Exodus as our focus is to modernize and ensure that the current code compiles and functions. We will address issues during the [Maintain](https://github.com/versionone/openAgile/blob/master/Evolve/Maintain.md) phase.