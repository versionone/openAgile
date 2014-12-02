## Setting Up Clean VM

- We have a TFS sandbox in Azure, built from a Jenkins job  
- Includes and installation of the integration  
- Need to have a VM with everything except the integration itself  
	- Base OS
	- Database (should include full text search (for V1)
	- Target system (EX: TFS)
	- VersionOne: BASIC, NTLM, OAuth (future), proxy?
		- Can silent install set to NTLM?
- Should be created from a Jenkins job


## Documenting Test Cases

- Step-by-step document to start with
- Maybe move to V1 regression tests once we have it sorted out
- Needs to include testing the documentation  
- Start with MD docs in each integration's repo (TEST_CASES.MD)  

## What should we test?

- Documentation
- System requirements validation (WIX validation?)
	- .NET Framework
	- Database
	- IIS
	- Target application (EX: TFS)
- Installation and configuration
- Ensuring connections with BASIC, NTLM, OAuth (future), proxy?
- Log files (creation and being written to) 
- Main workflows (varies with integration, happy path only)
- Uninstallation

## If/when to automate

- When it gets too painful
- Monitor and iterate