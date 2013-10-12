# Stop the Line

## Why? The Purpose of the Ceremony

We want to follow W. Edwards Deming's idea, "Quality is everyone's responsibility." 

* Focus on quality at all times.
* Identify recurrent, systemic problems so they are solved once and for all.
* Make everyone aware of the problem so anyone who can help, can contribute to fixing it.

## Who? The Participants

Team.

## When? Frequency and Timing

A stoptheline is raised when:

* A build is failing (it doesn't compile or pass unit tests).
* A WIP Limit is exceeded on our [Kanban Board](KanbanBoard.md).
* A problem prevents manual testing to be performed.

## What? The Artifacts we Review and Update

What we stop:

* Accepting Pull Requests, except those expected to fix the problem.
* Promoting cards, except the one with the stoptheline.

How we fix it:

* Whole team works on the issue until it is resolved.

How we prevent it from recurring:

* Root cause analysis.

# Where? How We Get Together

* Determined as needed.

# Thoughts

* Seems like we need an issue type for stoptheline so that we have a record of it even after it has been fixed.
* If stoptheline is an issue, can we automate creating one from Jenkins and Huboard?
* How can we make it obvious to all? HipChat?

# References

* [Stop the line: 5 c's for improving processes](http://www.slideshare.net/onimproving/stop-the-line-5-cs-for-improving-processes)
* [Stop the line & Stop Feature Development practices](http://www.slideshare.net/agilespain/presentation-cas2011-18102011)
