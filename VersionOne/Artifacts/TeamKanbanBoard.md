# Caution: WIP

Kanban, as applied to software development, is not a perfect discipline. 

It's meant to be adopted gradually, and evolved from a team's experience. [Learn the basics here](http://en.wikipedia.org/wiki/Kanban_\(development\)).

## Four basic principles

* Start with what you do now
* Agree to pursue incremental, evolutionary change
* Respect the current process, roles, responsibilities & titles
* Leadership at all levels

## Six core practices

David Anderson's six core practices for using Kanban with software development:

### **Visualise** 

> The workflow of knowledge work is inherently invisible, so make it visible!

### **Limit WIP**

> Limiting work-in-process implies that a pull system is implemented on parts or all of the workflow.

### **Manage flow** 

> The flow of work through each state in the workflow should be monitored, measured and reported.

### **Make policies explicit**

> Until the mechanism of a process is made explicit it is often hard or impossible to hold a discussion about improving it.

### **Implement feedback loops** 

> Collaboration to review flow of work and demand versus capability measures, metrics and indicators coupled with anecdotal narrative explaining notable events is vital to enabling evolutionary change.

### **Improve collaboratively, evolve experimentally**

> Use models and the scientific method to pursue small, continuous, incremental and evolutionary changes that stick. 

# Practicing the practices

## Visualise: The Kanban Board

TODO: move this to LIMIT WIP section: WIP Limit = 9 Cards (derived from 1.5 x team size).

## Issue States

Ideally, the fundamental states of the issue (open and closed) represent the issuer's perspective, while the lanes on the Kanban Board are internal "sub-states" useful to organizing the work of the team.

### Open

Any one can open a new card. The default lane for new items is unprioritized. A card is considered open until it has been [resolved](Resolutions.md).

### Closed

The Product Owner closes cards. Cards are removed from the Kanban Board when they are closed. The Product Owner provides a [resolution](Resolutions.md) to signal the outcome as completed or not.

## Lanes

### 0 - Unprioritized

All cards enter the board as unprioritized work. Cards may be entered by anyone, though usually they are entered in collaboration with the Product Owner.

Before the Product Owner will move a card from **Unprioritized** to **Prioritized**, the card must meet these criteria:

* Has a **descritive and specific title**.
* Has a description from the **user perspective**.
* Has been **tagged** as enhancement, defect, or question.

TODO revise this: WIP Limit = 18 cards (yesterday's weather for cards worked in 2 weeks). Not subject to board WIP Limit.

### 1 - Prioritized

Cards that are in this state have been prioritized by the Product Owner. The prioritization process is not done **in an ivory tower** without the team or other important people participating, but ultimately it is the Product Owner's doing to move the card.

TODO: WIP Limit = None. Subject to board WIP Limit.

### In Progress

A team member pulls a card out of the **Prioritzed** queue and into the **In Progress** lane.

When a card is **In Progress**, all kinds of collaborative activities happen that are specific and necessary for that card. The exact activities will **vary from card to card, and that's why it is a collaborative process, not a throw-over-the-wall process**. 

#### In Progress activities:

* **[Having Three Amigos sessions](../Ceremonies/ThreeAmigos.md)** -- typically best if done as close to pulling as possible, and done throughout the **In Progress** state when necessary for further collaboration and understanding
* **Writing Acceptance Criteria** -- expressions of what is needed to consider the card DONE
* **Creating and refining Specifications** -- 
  * If the card is an enhancement, it has a **scenarios** in a feature file (hyperlinked).
  * If the card is a sufficiently complex enhancement to UI, it has a **mockup** (hyperlinked).
  * If the card is a defect:
    * It has **steps to reproduce**.
    * It includes an **error message or screen shot** of the invalid state.
* **Designing 'spikes' and higher fidelity prototypes**
* **Exploratory and usability testing of spikes**
* **Developing the 'real' feature in collaboration with the tester and users** 

### Ready to Test

### In Test

### Tested

## Delivered


# NOTE: old

### 2 - Speced

The team decides which cards from to pull from the prioritized cards. To exit this lane, the card must meet the following criteria:

* Has been coded.
* Has unit tests.
* Has issued a Pull Request.

WIP Limit = None. Subject to board WIP Limit.

### 3 - Coded

The team decides which cards to pull from the coded cards. To exit this lane, the card must meet the following criteria:

* Has been tested.
* Has been tagged with a **[resolution](Resolutions.md)**.

WIP Limit = None. Subject to board WIP Limit.

### 4 - Tested

The Product Owner decides when to close tested cards. This provides an opportunity to decide what to demo during iteration review (tagged as `demo`) and what should be in the release notes (tagged as `noteworthy`).

WIP Limit = None. Not subject to board WIP Limit.

## Thoughts

* Are some issues just tasks? How does a task fit with spec, code, and test? For example, Issue #27 on Three Amigos.
* For readability, is it better to have entry or exit criteria?
* Can we really distinguish between a defect and an enhancement, if there is no specification? Do we care about the difference in the execution of our workflow?
* What about questions and documentation? How does speced, coded, and tested fit with questions or documentation?
* Should we demo everything we put into release notes? If so, can't we just collapse the tag space to `noteworthy`?
* Where does "support certification" fit?
* Should we hold items in tested until they are published in a release? Can Jenkins close items as part of the promotion job? Should it?
* How do we account for stoptheline? Is it a feature of the Kanban Board or something more (signals in HipChat, email, etc)?
* GitHub considers Pull Requests as Issues. How can we better account for this? Unsolicited Pull Requests are work. But most of ours are in context of an existing issue. Do we need to account for this on the board?
* What about estimates? If we need them, I suggest estimates are part of prioirization, so should be exit criteria for `prioritized`.
