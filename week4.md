# Final project
Open Source Workflow and Infrastructure  
Braideis University (FA20)  
Devin Stewart  
Bryan Behrenshausen

## Introduction: Meet Node2020
Node.js, "[a JavaScript runtime built on Chrome's V8 JavaScript engine](https://nodejs.org/en/)," is a [popular open source project](https://nodesource.com/blog/enterprise-node-js-adoption-increases/) with an active, vibrant development community and a rich, [decade-long history](https://en.wikipedia.org/wiki/Node.js).

But what if the project were launching today? And what if Node.js creator Ryan Dahl sought advice from Group 2 of Brandeis University's Open Source Workflow and Infrastructure course as he established a infrastructural foundation that best ensured the project's success and sustainability?

What might the Node.js project look like if it launched *tomorrow*?

Call it Node2020. Here's how we'd recommend architecting it.

## Priorities and parameters
Our infrastructural recommendations aim to respect the following project priorities and parameters.

**Respect foundation-backed governance.** The Node.js project's [history](https://en.wikipedia.org/wiki/Node.js#History) is complicated and winding. But it culminates in an interseting [hybrid governance model](https://www.redhat.com/en/resources/guide-to-open-source-project-governance-models-overview) involving support from a sponsoring foundation, the [OpenJS Foundation](https://openjsf.org/). Node.js features twin governing bodies: the [Technical Steering Committee (TSC)](https://github.com/nodejs/TSC/blob/master/TSC-Charter.md), ulimate arbiter of Node.js overseeing business, legal, and technical aspects of the project, and the [Community Committee (CommComm)](https://nodejs.org/en/about/community/), which oversees implementation of the TSC's decisions regarding both technical and non-technical aspects of the project. Each of these groups establishes its own [initiatives](https://github.com/nodejs/community-committee#contributing) and [priorities](https://github.com/nodejs/TSC/blob/master/Strategic-Initiatives.md). Participants select the initiatives to which they'd like to contribute, forming working groups on a largely ad-hoc basis. Infrastructural recommendations for Node2020 presuppose this governance model.

**Maintain the liberal contribution model.** Node.js prides itself on its "[liberal contribution model](https://medium.com/the-node-js-collection/healthy-open-source-967fa8be7951)." This model—more like a guiding spirit or project ethos—fosters continual infusion of new contributors to Node.js, and is critical to  ensuring project health and longevity. Node.js considers anyone who so much as comments on an outstanding project issue, opens a pull request, or participates in a conversation to be a project "[Contributor](https://nodejs.org/en/about/community/)." Becoming a contributor is the first step toward occupying additional roles (which grant additional permissions) in Node.js. Project infrastructure for Node2020 should sustain this spirit of liberal contribution, eliminanting potential hurdles to participation wherever possible.

## Infrastructural recommendations
Our recommendations distinguish between infrastructural components that accomplish both technical and social ends. Any successful open source *project* requires tooling that facilitates distributed collaboration on technical work; any successful open source *community* requires tooling that facilitates communicating about work, coordinating efforts, sharing accomplishments, and recruiting new contributors.

### Technical infrastructure overview
| Activity | Recommended Tool |
| - | - |
| Source code management (SCM) |  |
| Issue tracking |  |
| Documentation |  |
| Build tools |  |
| Security |  |
| Project website |  |

### Social infrastructure overview
| Activity | Recommended Tool |
| - | - |
| Development chat and synchronous collaboration | [Matrix](https://matrix.org/) |
| Support and asynchronous collaboration | [Discourse](https://www.discourse.org/) |
| Community outreach | [Discourse](https://www.discourse.org/) |
| News and marketing | [Metalsmith](https://metalsmith.io/) |

### Matrix for development chat and synchronous collaboration
Developers collaborating on an open source project often require some means of real-time chat via text, audio, and/or video, especially when collaborating synchronously on a new feature or collectively assessing a security issue. Node.js did not seem to mandate (or publicize) a tool or channel for synchronous development activity, instead seeming to defer to the preferences of individual working groups and initiatives. Node2020 should adopt a unified chat platform for developer communication, one built on the open source Matrix protocol, to better connected the its developers. Access to the platform could be a perk of achieving "[Collaborator]((https://nodejs.org/en/about/community/))" status in the project. (We do recognize a significant [Node.js presence on Gitter](https://gitter.im/nodejs/home), and [Matrix just acquired Gitter](https://matrix.org/blog/2020/09/30/welcoming-gitter-to-matrix), so perhaps Node.js is already planning a move to this platform.) Node2020 could host and maintain its own Matrix infrastructure or subscribe to hosted service.

### Discourse for support and asynchronous communication
Node.js featured a fractured and disparate ecosystem of communication platforms for connecting with and supporting users, one that encompased familiar channels like Slack, Discord, Reddit, IRC, and more. Interstingly enough, while these platforms facilitate synchronous communication, the project (and its various working groups) utilized them largely for posting announcements (without invitation for further discussion) or addressing support requests (even those that didn't necessary unfold in real time). Node2020 should adopt a single paltform for community engagement, announcements, and support, one built on the open source Discourse tool. Adopting Discourse benefits Node2020 by offering a singular point of community support and engagement, enabling greater control over asynchronous communications tooling (Discourse features fine-grained access and moderation controls), and facilitating the construction of a robust knowledge commons, where questions and answers are more usefully logged and archived (rather than spread across platforms like [Stack Overflow](https://stackoverflow.com/questions/tagged/node.js) or lost in a Slack stream). Node2020 could host and maintain its own Discourse infrastructure or subscribe to hosted service.

### Discourse for community outreach
Once again, Discourse could serve Node2020 by functioning as a platform for community outreach and recruitment. Project members could (finally?) point would-be contributors to a single source for community conversation and assistance getting started with the project. Discourse's fine-grained access controls allow project members to make certain documentation available even to visitors who haven't yet created accounts or formally joined the project.

### Metalsmith for news and marketing
Curiously, Node.js utilizes a magazine-style [publication on Medium](https://medium.com/the-node-js-collection) for relaying stories about its community members and their successes. (The project's blog is [a purely technical changelog](https://nodejs.org/en/blog/).) Node2020 should relocate this publication to the project's flagship website, jettisoning a proprietary platform and instead availing itself of the same Node-based backend technology that powers the community's other web properties. On a Metalsmith-backed platform, publication authors could enjoy the same Markdown-based syntax they used on Medium. This syntax also allows for greater collaboration with other members of the project; collaboration on article drafts could proceed via GitHub issues and pull requests.
