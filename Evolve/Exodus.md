# openAgile Evolve Exodus Plan

An primary goal of the Evolve Team is to unlock legacy integrations from the internal SVN repository, update and refactor them, then make them available in GitHub as open source solutions.

## Integrations Slated for Exodus

We will Exodus the following integrations, order TBD:

<table border="1" width="100%">
	<tr>
		<th>Name</th>
		<th>Repo</th>
		<th>Dependencies</th>
		<th>Notes</th>
	</tr>
	<tr>
		<td>Innovation Games (BuyAFeatureServices)</td>
		<td>https://github.com/versionone/VersionOne.Integration.Buy-A-Feature</td>
		<td>VersionOne.BuyAFeature</br>VersionOne.ServerConnector</br>VersionOne.ServiceHost.Core</br>Microsoft.Practices</br>Ninject</td>
		<td>Repo contains documentation only.</td>
	</tr>
	<tr>
		<td>Innovation Games (BuyAFeature)</td>
		<td></td>
		<td>VersionOne.ServiceHost.Core</br>Microsoft.Practices</td>
		<td>Repo contains documentation only.</td>
	</tr>
	<tr>
		<td>JIRA (JiraServices)</td>
		<td>https://github.com/versionone/VersionOne.Integration.JIRA</td>
		<td>VersionOne.Jira.Proxy/Connector</br>VersionOne.SDK.APIClient</br>VersionOne.ServerConnector</br>VersionOne.ServiceHost.Core</br>VersionOne.ServiceHost.WorkitemServices</br>Ninject</td>
		<td>Repo contains documentation only.</td>
	</tr>
	<tr>
		<td>JIRA (JiraConnector)</td>
		<td></td>
		<td>VersionOne.ServiceHost.WorkitemServices</td>
		<td>Repo contains documentation only.</td>
	</tr>
	<tr>
		<td>Perforce</td>
		<td>https://github.com/versionone/VersionOne.Integration.Perforce</td>
		<td>VersionOne.ServiceHost.Core</br>VersionOne.ServiceHost.SourceServices</br>Ninject</br>p4api</br>p4dn</td>
		<td>Repo contains documentation only.</td>
	</tr>
	<tr>
		<td>Quality Center</td>
		<td>https://github.com/versionone/VersionOne.Integration.QualityCenter</td>
		<td>VersionOne.ServiceHost.Core</br>VersionOne.ServiceHost.TestServices</br>VersionOne.ServiceHost.WorkitemServices</br>Interop.TDAPIOLEib</br>Ninject</td>
		<td>Repo contains documentation only.</td>
	</tr>
	<tr>
		<td>Subversion</td>
		<td>https://github.com/versionone/VersionOne.Integration.Subversion</td>
		<td>VersionOne.SDK.APIClient</br>VersionOne.ServiceHost.Core</br>log4net</br>Newtonsoft.Json</br>Ninject</br>OAuth2Client</br>SharpSvn</br>SharpSvn.UI</br>FSharp.Data</br>FSharp.Data.DesignTime</td>
		<td>Source code is in repo, buts needs cleanup and verification.</td>
	</tr>
	<tr>
		<td>Bugzilla (Services)</td>
		<td>https://github.com/versionone/VersionOne.Integration.Bugzilla</td>
		<td>VersionOne.Bugzilla.XmlRpcProxy</br>VersionOne.ServiceHost.Core</br>VersionOne.ServiceHost.WorkitemServices</br>Ninject</td>
		<td>Perl scripts code is in repo, but ServiceHost code is not.</td>
	</tr>
	<tr>
		<td>Bugzilla (XmlRpcProxy)</td>
		<td></td>
		<td>CookComuting.XmlRpcV2</td>
		<td>Perl scripts code is in repo, but ServiceHost code is not.</td>
	</tr>
</table>

## Shared Components

A key aspect of the Exodus is to find common dependencies and break them out as individual projects, cleanup and verify them, then put them into their own GitHub repositories. In addition, each component will have its own Jenkins job for compiling, running unit tests, and publishing to MyGet.

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
		<td>ServiceHost.ServerConnector</td>
		<td>https://github.com/versionone/Platform.V1.ServerConnector</td>
		<td>Need to change repo name.</td>
	</tr>
	<tr>
		<td>ServiceHost.WorkitemServices</td>
		<td>REPO DOES NOT EXIST</td>
		<td></td>
	</tr>
	<tr>
		<td>ServiceHost.TestServices</td>
		<td>REPO DOES NOT EXIST</td>
		<td></td>
	</tr>
	<tr>
		<td>ServiceHost.ChangesetServices</td>
		<td>REPO DOES NOT EXIST</td>
		<td></td>
	</tr>
	<tr>
		<td>ServiceHost.ConfigurationTool</td>
		<td>REPO DOES NOT EXIST</td>
		<td></td>
	</tr>
</table>

## Packaging, Deployment, and Versioning

An important aspect of Exodusing the integrations is the use of a consistent process for build, test, package, and deployment. In this regard we will:

* Place all integration Jenkins jobs in the "Integrations" folder
* Ensure that we use a consistent naming scheme for all Jenkins jobs using a "GitHub repo name-branch-phase" naming pattern
	* GitHub repo name: Should be consistent to group make it easier to find related projects
	* Branch: In most cases will be "master", but may use other branches as needed
	* Phases:
		* **Build**: Triggered from GutHub commits, compiles and executes unit tests
		* **Test**: Executes integration/end-to-end tests
		* **Deploy**: Packages and deploys to a public (beta) repository such as MyGet/Artifactory
		* **Release**: Deploys to a public (release) repository such as NuGet/Maven Central
		* **Sandbox**: Creates the test VM used for the integration
* Ensure that we follow a consistent [versioning policy](https://github.com/versionone/openAgile/blob/master/VersionOne/Artifacts/VersioningPolicy.md)


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
7. For .NET projects, refactor unit tests using MSTest (see [Comparing the MSTest and Nunit Frameworks](http://blogs.msdn.com/b/nnaderi/archive/2007/02/01/mstest-vs-nunit-frameworks.aspx))
8. Bring integrations up to latest V1 SDK versions (.NET and Java API clients)
9. Research target system dependencies, make note of newer versions
10. Rename integration executable and config file to match integration name (not ServiceHost.exe)
11. Ensure that project compiles (debug and release)
12. Ensure that existing unit tests pass
13. Create Jenkins "build" job for build/unit test runs
14. Create Jenkins "deploy" job for MyGet deployment
14. Confirm availability of integration documentation
15. Verify auto-population and accuracy of AppCatalog entries (staging)
16. Hold post-mortem to review lessons learned

> As we work through each integration, we'll look for problem areas and log them as GitHub issues. We will not be fixing those issues during the Exodus as our focus is to modernize and ensure that the current code compiles and functions. We will address issues during the [Maintain](https://github.com/versionone/openAgile/blob/master/Evolve/Maintain.md) phase.