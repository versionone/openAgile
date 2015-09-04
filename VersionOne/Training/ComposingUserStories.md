# Composing User Stories Notes

Notes from team training on https://elearning.industriallogic.com/gh/submit?Action=PageAction&album=composingUserStories&path=composingUserStories/invest/nQuiz&devLanguage=None

## Chartering

* This is a positive practice
  * Keep charter notes into an Epic
* VersionOne site: http://www.agilesherpa.org/agile_coach/product_planning/chartering/
* Example from Core project: http://confluence/display/prod/Community+of+Practice
* http://guide.agilealliance.org/guide/project-chartering.html

## What is a user story?

* Break them into user-focused chunks
* Try to find language that speaks to some user ROLE, not just "the user"
* "Virtual users" are a real thing, they are agents that access your system
  * You can model stories from the perspective of the "agent", not necessarily a human agent
    * However, ideally you can trace this further back to a human user's needs

## Ambiguity

* Keep in mind the "three levels"
  * Feature (Product team meetings, Customers)
  * Headline (Shawn Marie often focuses here first)
  * Headline + Details + Discussion + Key Tests
* Appropriate for diff audiences  

## An Example Story

* Deliberately simple
* Simple narrative

## Role-Action-Context

* Think about these in CS, DevOps context

## Good Headings

* When a heading contains OR, AND, or IF, you just might be able to break it up.
* If you struggle to find a good heading, or you need complex phrases or sentences to summarize the story in the heading, the story's scope probably needs to be more constrained.

## Story Formats

* We typically do As a Role - so that - goal
* Free form on bugs

## Details

* More mockups and hand-drawn pictures please :-D
* Shawn Marie: More details the better for error-handling (message, status codes, points-of-faliure)
  * Example: "html_url": when it's missing, BOOM
* A User Story is a promissory note for a conversation.” —Alistair Cockburn  
* "Defer decisions until the last responsible moment."
  * However, when deferring decisions, we need to **communicate** with each other, especially Shawn Marie!

## Not all projects are Greenfield, some of BROWNFIELD

* See https://en.wikipedia.org/wiki/Brownfield_(software_development)  
* Ira: this shit is TOXIC

## Card, Conversation, Confirmation

* Don't have confirmations without having had the CONVERSATION

# INVEST

* READ THIS: http://alistair.cockburn.us/Are+iterations+hazardous+to+your+project%3F

## INVEST Notes

*  Shawn Marie: Independent is most important
  * Non-independent example: API coming before UI. The UI story Depends On the API.

### Negotiable

* Be aware when it's negotiation versus NEW STORY
* DEVS inform Shawn Marie about NEW TESTS or CHANGES

### Valuable

* Technical work is PART Of implementing Stories, but is not itself a "User Story"
	* Technical work, refactoring, unit tests, etc are the foundations of the ABILITY to DELIVER ANYTHING OF VALUE
		* Therefore, DO NOT fall prey to tendency to accuse those of doing technical work as "not contributing to a User Story"
## Summary

* Apply the INVEST guidelines to help you, not box you into a rigid frame.

# Great User Stories

## Essential

* Helps you focus on what charter and sponsors want

## What About Developer Needs?

* TODO: deep dive this one more

## External Stories

* User Stories that are external to a System Boundary focus on organizational and business concerns rather than technical ones
* Example: CS API

## Instantaneous Stories

* A great story describes an instantaneous event
* Ex: System Sends Daily Summary Email
* Ex: Customer Selects Report
