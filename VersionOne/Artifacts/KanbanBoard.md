# Kanban Board

## Board

WIP Limit = 9 Cards (derived from 1.5 x team size).

## Issue States

Ideally, the fundamental states of the issue (open and closed) represent the issuer's perspective, while the lanes on the Kanban Board are internal "sub-states" useful to organizing the work of the team.

### Open

Any one can open a new card. The default lane for new items is unprioritized. A card is considered open until it has been [resolved](Resolutions.md).

### Closed

The Product Owner closes cards. Cards are removed from the Kanban Board when they are closed. The Product Owner provides a [resolution](Resolutions.md) to signal the outcome as completed or not.

## Lanes

### 0 - Unprioritized

All cards enter the board as unprioritized work. To exit this lane, the card must meet the following criteria:

* Has a *descritive and specific title*.
* Has a description from the *user perspective*.
* Has been *tagged* as enhancement, defect, or question.

WIP Limit = 18 cards (yesterday's weather for cards worked in 2 weeks). Not subject to board WIP Limit.

### 1 - Prioritized

The Product Owner decides which cards are prioritized for the team to work next. To exit this lane, the card must meet the following criteria:

* Has been the subject of a *[Three Amigos](../Ceremonies/ThreeAmigos.md)* discussion.
* Has appropriate *specifications*.
  * If it is an enhancement, it has a *scenarios* in a feature file (hyperlinked).
  * If it is a sufficiently complex enhancement to UI, it has a *mockup* (hyperlinked).
  * If it is a defect, it has *steps to reproduce*.
  * If it is a defect, it includes an *error message or screen shot* of the invalid state.

WIP Limit = None. Subject to board WIP Limit.

### 2 - Speced

The team decides which cards from to pull from the prioritized cards. To exit this lane, the card must meet the following criteria:

* Has been coded.
* Has unit tests.
* Has issued a Pull Request.

WIP Limit = None. Subject to board WIP Limit.

### 3 - Coded

The team decides which cards to pull from the coded cards. To exit this lane, the card must meet the following criteria:

* Has been tested.
* Has been tagged with a [resolution](Resolutions.md).

WIP Limit = None. Subject to board WIP Limit.

### 4 - Tested

The Product Owner decides when to close tested cards. This provides an opportunity to decide what to demo during iteration review (tagged as "demo") and what should be in the release notes (tagged as "noteworthy").

WIP Limit = None. Not subject to board WIP Limit.

## Thoughts

* Can we assume unprioritized means "Needs Review"?
* Are some issue just tasks? How does a task fit with spec, code, and test? For example, Issue #27 on Three Amigos.
* There's a conflict for some items that are currently coded but not tested. Issue #7 and #47 both have "Needs Test Spec". Does this indicate a flaw in the workflow? Or just a consequence of retro-actively applying the workflow? In other words, does speced mean a Test Spec (steps to reproduce and an error message)?
* I realize many Kanban boards have progressive tense (like "developing" or "testing"). I assert that progressive tense leads to sloppy definition of a state (defining it by the activity rather than the result) so I prefer past tense to express more clearly distinguishable states. Does that work for the team?
* For readability, is it better to have entry or exit criteria?
* Can we really distinguish between a defect and an enhancement, if there is no specification? Do we care about the difference in the execution of our workflow?
* What about questions and documentation? How does speced, coded, and tested fit with questions or documentation?
* Should we demo everything we put into release notes? If so, can't we just collapse the tag space to "noteworthy"?
* Where does "support certification" fit?
* Should we hold items in tested until they are published in a release? Can Jenkins close items as part of the promotion job? Should it?
* How do we account for stoptheline? Is it a feature of the Kanban Board or something more (signals in HipChat, email, etc)?
* GitHub considers Pull Requests as Issues. How can we better account for this? Unsolicited Pull Requests are work. But most of ours are in context of an existing issue. Do we need to account for this on the board?