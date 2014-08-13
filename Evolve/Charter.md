# openAgile Evolve Charter

The charter of the openAgile Evolve team is to understand and improve the state and maintainability of all the integrations owned by VersionOne, and to improve VersionOne platform developer engagement and support. The Evolve team will be short-lived as it will exist only as long as needed to complete and/or transition ownership of the major themes that the team was created to address.

The Evolve team will swarm around the following themes:

* **Exodus**: Move legacy integrations from internal Subversion repository to GitHub, cleaning up and modernizing in the process.
* **Maintain**: Create automated process for ensuring integration integrity and support.
* **Engage**: Reorganize and enhance platform and integration documentation, establish processes for better developer engagement and support.
* **Support**: Own escalations of platform support, work with V1 support to improve response cycle times and processes.

## Exodus

Many of our integrations continue to be locked within the V1 internal Subversion repository, and following our desire to move to a much more open-source model, those integrations need to be migrated to GitHub. Over time, many of these legacy integrations have accumulated technical debt, and have fallen behind the current versions of the systems that they target.

* Identify integrations to be maintained or retired (sunset).
* Analyze the integrations for common dependencies, break them out into shared components
* Bring integration projects up to latest IDE/Framework versions (Visual Studio 2013/.NET Framework 4.5 & Eclipse Luna/JDK 8)
* Remove unnecessary dependencies
* Refactor Configuration Tool (may require work from openAgile Labs Team)
* Refactor ServiceHost (V1IntegrationService?)
* Create hosted dev/test environments (Azure VMs)
* Ensure that integrations compile and work with last tested target system versions
* Review and triage related GitHub issues

### Exit Criteria:

* 

## Maintain

Related to the Subversion Exodus, this theme is focused on bringing existing integrations up-to-date with the dependencies and versions of their target systems, looking for areas in which they can be improved, and ensuring that we have an automated process for testing them.

* Bring integrations up to latest target system versions
* Ensure all integrations use OAuth for V1 authentication
* Expand unit test coverage using mocking frameworks as needed
* Create automated end-to-end integration test coverage for major workflows using hosted environments
* Create installer packages (Chocolatey, WIX, Installshield)
* Create two Jenkins build jobs for each integration for compile, test, and packaging
* Update and maintain AppCatalog
* Update and maintain integration documentation (GitHub, Dev Community)

### Exit Criteria:

*

## Engage

Another theme is that of developer community which involves engaging our developer customers to ensuring their success using our development platform and integrations, and supporting their contributions to our open-source code base.

* Monitor and react to GitHub repo forks, issues, and pull requests
* "Own" the developer community website, assist openAgile Sprint with new documentation
* Create blog post on relevant topics
* Assist Services in developer oriented offerings (API training, integration customization, etc.)
* Engage internal teams for developer customer feedback (Customer Success, Services, Support, Product Specialists)
* Attend relevant developer oriented events, stay close to the community

### Exit Criteria:

*

## Support

The final theme is that of developer support which is closely related to developer community, but is more reactive in nature.

* Establish consistent ticket triage and shepherding process
* Bring support "closer" by educating and paring with them on platform and integrations tickets (build a bridge) 
* Involve support in decisions
* Serve as escalation route for developer oriented tickets
* Monitor Zendesk, StackOverflow, and Google Dev Group for new issues and bring into backlog as necessary
* Strive to reduce ticket cycle time and number of tickets submitted

### Exit Criteria:

*
