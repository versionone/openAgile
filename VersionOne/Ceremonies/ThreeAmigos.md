# Three Amigos

![http://upload.wikimedia.org/wikipedia/en/8/87/Three_amigos_ver2.jpg](http://upload.wikimedia.org/wikipedia/en/8/87/Three_amigos_ver2.jpg)

## Why? The Purpose of the Ceremony

Three Amigos is a [collaborative approach to specification](http://www.stickyminds.com/sitewide.asp?Function=edetail&ObjectType=COL&ObjectId=17232). The purpose is to:

* Build shared understanding across the team
* Write testable specifications in a [human readable form](http://martinfowler.com/bliki/BusinessReadableDSL.html) using concrete and specific examples

### General Ground Rules from the StickyMinds article:

> The Three Amigos are the essential stakeholders of the system being developed: The business (or product owner, in Scrum terms), the developer, and the tester. These three represent the viewpoints of what the system is intended to do, what can and cannot be implemented, and what might go wrong or be misunderstood.

> Don't limit yourself to just three stakeholders, however.

> May need to pull in: UX Designers, System Operators, Service Technicians, Sales Team Members, Security Team, etc.

> Only include people who have a stake in the success of the system. Many times there will be multiple programmers and testers on the team. Don't include all the developers and testers in each meeting, as that dilutes the sense of responsibility.

### How to use Three Amigos at different parts of the "Agile Lifecycle":

#### During Backlog Grooming 

> The Three Amigos need to collaborate to define what needs to be done, how they'll know when it's done, and that it's done correctly. After implementation, the Three Amigos need to review the work to make sure it’s still correct from everyone's point of view. In between these two points, a well-functioning Three Amigos will continue the dialog so that any misunderstandings will be discovered and corrected early, and so any new insights can be incorporated to everyone’s advantage.

> The goal is to come up with examples that cover all of the important scenarios and to boil them down to the essence of the functionality.

#### During Planning Meeting

> When we get together to plan the next increment of development work, such as the sprint planning meeting in Scrum, the Three Amigos will use these examples to communicate the intent to the full development team. The content of the examples will give the full team a reasonably good idea of what will be involved to implement the user story. The number of those examples will give team members a good idea of its size. If the story is split into multiple stories, the examples clearly indicate which functionality is assigned to which story. This is a big timesaver in my experience. I've seen team discussions go round and round, with some members thinking the story is a small slice and others thinking it includes many other scenarios. If you're estimating the size of stories, the explicit nature of the examples makes it much easier.

> Turning the examples into automated tests should be a pretty easy chore, depending on how you've expressed those examples and the tools you're using. This is best done prior to implementing the story, but might also be done as work begins on the story. Hooking the example up to drive the code under development may have to wait until the story is a little further along. That's OK. Just hook it up as soon as there's an appropriate place to connect it. This work is often a collaboration between tester and programmer.

#### During Exploratory Testing

> As each bit of functionality becomes available, you'll want to take a look at it. Does it fulfill the original intent of the functionality? Does it seem reasonable? Does the functionality still seem desirable when you see it in operation? Does the system suggest unintended ways it might be used? If so, do these unintended operations work in a reasonable fashion and give correct answers?

Passing the acceptance tests does not necessarily mean the software is acceptable. That's just the first hurdle to acceptance. The example scenarios envisioned by the Three Amigos before development should cover the expected functionality pretty well, but no one has perfect foresight. It's always best to bring critical thinking to bear after development, also.

## Who? The Participants

The product owner, a developer, and a tester.

## When? Frequency and Timing

The meeting is called before starting a new user story.

## What? The Artifacts we Review and Update

* Feature files in the Gherkin syntax (regardless of test automation)
* Other examples such as example data sets (JSON, XML, etc)

# Where? How We Get Together

* Determined as needed.
