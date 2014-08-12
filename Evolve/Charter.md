# openAgile Evolve Charter

The openAgile Evolve team will swarm around a few primary themes, and this document will serve to provide a high-level outline of those themes and what is involved in each.

## Subversion Exodus

Many integrations continue to be locked within the V1 internal Subversion repo, and following our desire to move to a much more open-source model, those integrations need to be migrated to GitHub.

* Identify the integrations to be migrated, and the integrations to be abandoned
* Analyze the integrations for common dependencies, break them out into their own GitHub projects and if needed, make them available in NuGet/Maven
* Overhaul the Config Tool (may require work from openSprint Team)
* Overhaul ServiceHost (refactor as V1 Integration Service?)
* Provide consistent documentation for integrations (mix of GitHub and Dev Community site?)

## Integration Maintenance

Related to the Subversion Exodus, this theme is focused on binging existing integrations up-to-date with the dependencies and versions of their target systems.

* Bring projects up to latest IDE/Framework versions (Visual Studio 2013/.NET Framework 4.5 & Eclipse Luna/JDK 8)
* Bring integrations up to latest target system version
* Ensure all integrations are OAuth enabled
* Expand unit test coverage to 80% using mocking frameworks
* Create hosted dev/test environments
* Create automated end-to-end integration test coverage for major workflows using hosted environments
* Create two Jenkins build jobs for each integration:
	* Automatic build for code checkins to compile and run unit tests
	* On-demand build for integration tests, package and deployment
* Create installer packages (Chocolatey, WIX, Installshield, ZIP?)
* Review and maintain AppCatalog

## Developer Community

Another theme is that of developer community which involves engaging our developer customers to ensuring their success using our development platform and integrations, and supporting their contributions to our open-source code base.

* Monitor and react to GitHub repo forks, issues, and pull requests
* "Own" the developer community website, assist openAgile Sprint with new documentation
* Create blog post on relevant topics
* Assist Services in developer oriented offerings (API training, integration customization, etc.)
* Engage internal teams for developer customer feedback (Customer Success, Services, Support, Product Specialists)
* Attend relevant developer oriented events, stay close to the community

## Developer Support

The final theme is that of developer support which is closely related to developer community, but is more reactive in nature.

* Work with Support to establish consistent ticket shepherding process
* Bring support "closer" by educating and paring with them on platform and integrations tickets 
* Serve as escalation route for developer oriented tickets
* Monitor Zendesk, StackOverflow, and Google Dev Group for new issues and bring into backlog as necessary
* Strive to reduce ticket cycle time and number of tickets submitted
