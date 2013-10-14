# Stop the Line

## Why? The Purpose of the Ceremony

We want to follow [W. Edwards Deming's](http://en.wikipedia.org/wiki/W._Edwards_Deming) idea, **"Quality is everyone's responsibility."** [(More Demming quotes)](http://www.brainyquote.com/quotes/authors/w/w_edwards_deming.html)

* Focus on quality at all times.
* Identify recurrent, systemic problems so they are solved once and for all.
* Make everyone aware of the problem so anyone who can help, can contribute to fixing it.

If it helps you to remember, pretend that he's looking at you over there in the corner and bubbling that quote out of his head, like this:

![Quality is everyone's responsibility](http://100qualityquotes.files.wordpress.com/2013/02/dr_w_edwards_deming.jpg)

### Goal: Implement the Demming Cycle (PDSA)

Agile and Lean are heavily influenced by Demming's popularization of the Shewhart cycle, becoming popularly known 
as The Demming Cycle or the [Plan-Do-Study-Act process](http://en.wikipedia.org/wiki/PDCA):

![Plan Do Study Act](http://upload.wikimedia.org/wikipedia/commons/thumb/a/a8/PDCA_Process.png/800px-PDCA_Process.png)

**NOTE:** It's commonly known as **Plan-Do-Check-Act**, but Demming himself began to refer to it as [**Plan-Do-Study-Act**](http://www.bizmanualz.com/blog/how-are-pdca-cycles-used-inside-iso-9001.html) because
he felt that **check** emphasized ***inspection*** over the more important goal of **analysis**.

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
