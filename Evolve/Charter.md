# openAgile Evolve Charter

The charter of the openAgile Evolve team is to improve the integrity and maintainability of all the integrations owned by VersionOne, and to improve VersionOne platform developer engagement and support. The Evolve team will be short-lived as it will exist only as long as needed to complete and/or transition ownership of the areas that the team was created to address. The Evolve team will dissolve once all exit criteria have been met.

The Evolve team will swarm around the following themes:

* **Exodus**: Move legacy integrations from internal Subversion repository to GitHub, cleaning up and modernizing in the process
* **Maintain**: Create automated process for ensuring integration integrity and support
* **Engage**: Reorganize and enhance platform and integration documentation, establish processes for better developer engagement and support
* **Support**: Own escalations of platform support, work with V1 support to improve response cycle times and processes
* **Fuse**: Serve as the technology partner for external vendors that create integrations with VersionOne.

> While the focus of the team is on the themes listed above, the team will operate in an agile and opportunistic fashion - much of our work will be on-demand in response to external events. As a result, our work will be both planned and interrupt driven.

## Exodus

Many of our integrations continue to be locked within the V1 internal SVN repository, and continuing our move to an open-source model, those integrations need to be cleaned up, verified, and migrated to GitHub.

* Identify integrations to be maintained or retired (sunset)
* Purge deprecated integrations from current ServiceHost solution
* Analyze the integrations for common dependencies
* Break out the common dependencies into shared components (EX: ServiceHost.Core)
* Ensure that shared components are available in MyGet, NuGet, or Maven Central
* Detangle individual integrations from ServiceHost solution, create each in its own GitHub repo
* Bring integrations up to latest IDE/Framework versions (Visual Studio 2013/.NET Framework 4.5 & Eclipse Luna/JDK 8)
* Bring integrations up to latest V1 SDK versions (.NET and Java API)
* Change EXE and config file name from ServiceHost to integration name???
* Remove unnecessary dependencies
* Remove dead/commented out code
* Create hosted test environments (Azure VMs) with last tested target system versions
* Ensure that integrations compile and work with last tested target system versions
* Ensure that integrations have unit test project and that all current tests pass
* Create Jenkins build job for each integration
* Verify integration documentation
* Verify auto-population and accuracy of AppCatalog entries
* Triage related GitHub issues and add to backlog as needed

> View the [Exodus Plan](Exodus.md) for more details.

### Exit Criteria:

* All integrations have a Jenkins build job
* All integrations have a hosted test environment
* All integrations are publicly available in GitHub
* All integrations use shared components
* Separate unit tests into each integration's project
* All integrations documentation is current
* All integrations AppCatalog entries are current
* List of integrations and status available in Dev Community site

## Maintain

Following completion of the integration exodus, we'll next focus on bringing the integrations up-to-date with the versions of their target systems, looking for areas in which they can be improved, and ensuring that we have an automated process for validating their integrity.

* Refactor ConfigurationTool (may require work from openAgile Labs Team)
* Refactor ServiceHost (may require work from openAgile Labs Team)
* Create hosted test environments (Azure VMs) with current target system versions
* Ensure that integrations compile and work with current target system versions
* Ensure all integrations use OAuth for V1 authentication
* Expand unit test coverage using mocking frameworks as needed
* Create automated integration test coverage for major workflows using hosted test environments
* Create installer packages (Chocolatey|WIX|Installshield)
* Update integration documentation
* Update integration AppCatalog entries
* Develop transition plan for integration monitoring

> View the [Maintain Plan](Maintain.md) for more details.

### Exit Criteria:

* ConfigurationTool refactored
* ServiceHost refactored
* All integrations have a current version hosted test environment
* All integrations use OAuth
* All integrations have improved code coverage
* All integrations have automated integration tests
* All integrations have an installer package
* All integrations documentation is current
* All integrations AppCatalog entries are current
* Transition plan is executed

## Engage

Another theme is that of developer community which involves engaging our developer customers to ensure their success using our development platform and integrations, and supporting their contributions to our open-source code base.

* Monitor and react to GitHub repo forks, issues, and pull requests
* "Own" the developer community website, assist openAgile Sprint with new documentation
* Create blog post on relevant topics
* Assist Services in developer oriented offerings (API training, integration customization, etc.)
* Engage internal teams for developer customer feedback (Customer Success, Services, Support, Product Specialists)
* Attend relevant developer oriented events, stay close to the community
* Monitor and react to API traffic usage (analyzed with SumoLogic)

> View the [Engage Plan](Engage.md) for more details.

### Exit Criteria:

* TBD

## Support

The final theme is that of developer support which is a component of engaging the developer community, but is more reactive in nature. A key part of our support effort will be reacting to each support incident to drive down the number of incidents.

* Establish a consistent incident lifecycle
* Establish an automated ticket response process using Zendesk Macros
* Establish a process for reacting to support incidents
* Establish a process for V1 support to escalate Zendesk tickets to us
* Bring support "closer" by educating and paring with them on platform and integrations tickets (build a bridge) 
* Automate the process for monitoring support channels for new issues and bringing into our backlog
* Strive to reduce ticket cycle time and number of incidents
* Reduce support channels by deprecating Dev-Google Group in lieu of StackOverflow
* Consistently evangelize StackOverflow as the first and best choice for platform questions

> View the [Support Plan](Support.md) for more details.

### Exit Criteria:

* Incident lifecycle defined and put in use
* Zendesk macros defined and put in use
* Incident reaction process defined and put in use
* V1 support knows the escalation process
* V1 support fields all 1st level platform support tickets
* Have an automated process for monitoring support channels and adding to our backlog
* Support incidents and their cycle time measurably reduced from current levels
* Decrease in Google Group activity
* Increase in StackOverflow activity

## Fuse
TBD

### Exit Criteria:

* TBD