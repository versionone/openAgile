# openAgile Team Streams

As a result of working with Dave Laribee in July, 2014, we recognized the need to, at least temporarily, divide our backlog into two major streams:

## Team 1: openAgile Evolve

Purpose: TODO

Backlog owner: @aceybunch

Team charter: [openAgile Evolve Charter](https://github.com/versionone/openAgile/blob/master/Evolve/Charter.md)

## Team 2: openAgile Labs

Purpose: TODO

Backlog owner: @ibuchanan

Team charter: TODO

# Background

The older document [BigPicture.md](https://github.com/versionone/openAgile/blob/master/VersionOne/Artifacts/BigPicture.md) outlines the major factors that have led to this split. You can learn more about how we've progressed in the respective Charter links above. 

In brief, openAgile has been doing the following:

* Maintaining and upgrading around two dozen existing third-party integrations, most of which you can find with this [search for VersionOne.Integration](https://github.com/versionone?page=2&query=VersionOne.Integration)
* Responding to emergent request in GitHub, StackOverflow, ZenDesk, Google Groups, email, face-to-face requests
* Building new platform features to advance the state-of-the-art in integration capabilities, such as query.v1, OAuth2, and the nascent CommitStream
* Supporting internal DevOps efforts and producing open source tools and libaries under the [openAgile organization](http://www.github.com/openAgile) on GitHub
* TODO what else?


# Prototyping this change

We've met several times to prototype how this will work. Here are some sketches / diagrams:

## Josh's sketch

![Josh's Sketch](https://s3.amazonaws.com/uploads.hipchat.com/12722/130235/M5wJrLZtn4tDrF6/upload.png)

# Serve the needs of individuals and teams, starting with V1 employees and teams

As the sketches above depict, openAgile's major directive is to improve our product integration capabilities. This starts with serving the needs of our own individuals and teams first and foremost. **When our open platform serves our own employees' needs well, it will serve the larger and external community of developers integrating with VersionOne.**

## Value streams between VersionOne teams

Let's envision the flow as a series of requests and responses:

* Request: openAgile Evolve asks, ***"ServiceHost is so tightly coupled! Can we break this project into smaller parts for better testability, extensibility, and maintainability?"***
 * Response: openAgile Labs says, ***"Totally. Check out the ideas here about [creating a modular architecture in .NET with MEF the same way Visual Studio itself works! Then let's collaborate in the next iteration on this.](https://github.com/JogoShugh/ModularAspNetMvc/blob/master/new/Programming-with-Modules-MEF-CSharp.md)."***
* Request: Both V1 Services and Ops lament, ***"Customers like Ventyx and CapitalOne are using thousands and thousands of API calls to rest-1.v1 API! How do we use query.v1 to reduce those calls?"***
 * Response 1: openAgile Evolve responds, ***"Glad you asked. Watch this video Laureano did about how he reduced the API calls, data traffic, and response time all by more than 90%! Let's collaborate on that next week."***
  <a href="http://www.youtube.com/watch?feature=player_embedded&v=G_3ukdxhw2Q
" target="_blank"><img src="http://img.youtube.com/vi/G_3ukdxhw2Q/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>
 * Response 2: VersionOne Services' Matt Badgley says, ***"Hey check out what I did with query.v1 with Dashing.io! I'd like to participate in that collaboration. Here's a screen shot of V1Dashing:"*** 
 ![V1Dashing](https://s3.amazonaws.com/uploads.hipchat.com/12722/130235/LC52QBJzyVhyjqA/upload.png)
* TODO: add more

