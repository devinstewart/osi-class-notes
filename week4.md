# Final project
Open Source Workflow and Infrastructure
Braideis University (FA20)
Devin Stewart
Bryan Behrenshausen

## Introduction: Meet Node2020
Node.js, "[a JavaScript runtime built on Chrome's V8 JavaScript engine](https://nodejs.org/en/)," is a [popular open source project](https://nodesource.com/blog/enterprise-node-js-adoption-increases/) with an active, vibrant development community and a rich, [decade-long history](https://en.wikipedia.org/wiki/Node.js).

But what if the project were launching today? And what if Node.js creator Ryan Dahl sought advice from Team 2 of Brandeis University's Open Source Workflow and Infrastructure course as he established a infrastructural foundation that best ensured the project's success and sustainability?

What might the Node.js project look like if it launched *tomorrow*?

Call it Node2020. Here's how we'd recommend architecting it.

## Priorities and parameters
Our infrastructural recommendations aim to respect the following project priorities and parameters.

**Respect foundation-backed governance.** The Node.js project's [history](https://en.wikipedia.org/wiki/Node.js#History) is complicated and winding. But it culminates in an interseting [hybrid governance model](https://www.redhat.com/en/resources/guide-to-open-source-project-governance-models-overview) involving support from a sponsoring foundation, the [OpenJS Foundation](https://openjsf.org/). Node.js features twin governing bodies: the [Technical Steering Committee (TSC)](https://github.com/nodejs/TSC/blob/master/TSC-Charter.md), ulimate arbiter of Node.js overseeing business, legal, and technical aspects of the project, and the [Community Committee (CommComm)](https://nodejs.org/en/about/community/), which oversees implementation of the TSC's decisions regarding both technical and non-technical aspects of the project. Each of these groups establishes its own [initiatives](https://github.com/nodejs/community-committee#contributing) and [priorities](https://github.com/nodejs/TSC/blob/master/Strategic-Initiatives.md). Participants select the initiatives to which they'd like to contribute, forming working groups on a largely ad-hoc basis. Infrastructural recommendations for Node2020 presuppose this governance model. Note that this document does *not* address `npm`, as a completely different community with its own governance is responsible for the `npm` CLI.

**Maintain the liberal contribution model.** Node.js prides itself on its "[liberal contribution model](https://medium.com/the-node-js-collection/healthy-open-source-967fa8be7951)." This model—more like a guiding spirit or project ethos—fosters continual infusion of new contributors to Node.js, and is critical to  ensuring project health and longevity. Node.js considers anyone who so much as comments on an outstanding project issue, opens a pull request, or participates in a conversation to be a project "[Contributor](https://nodejs.org/en/about/community/)." Becoming a contributor is the first step toward occupying additional roles (which grant additional permissions) in Node.js. Project infrastructure for Node2020 should sustain this spirit of liberal contribution, eliminanting potential hurdles to participation wherever possible.

## Infrastructural recommendations
Our recommendations distinguish between infrastructural components that accomplish both technical and social ends. Any successful open source *project* requires tooling that facilitates distributed collaboration on technical work; any successful open source *community* requires tooling that facilitates communicating about work, coordinating efforts, sharing accomplishments, and recruiting new contributors.

### Technical infrastructure overview
| Activity | Recommended Tool |
| - | - |
| Source code management | [GitHub](github.com/) |
| Issue tracking | [GitHub](github.com/) |
| Documentation | [GitHub](github.com/) |
| Build tools | A yet to be invented CI/CD system |
| Security | [HackerOne](https://www.hackerone.com/) |
| Project website | [Metalsmith](https://metalsmith.io/) |

### GitHub for source code management, issue tracking, and documentation
Node.js has taken an "all in on GitHub" approach. The project uses it for source code management, issue tracking, and documentation. The community even goes as far as conducting basic governance via GitHub, asking that all suggestions for modifications to project policy and procedurebe initiated via a GitHub pull request. Node2020 should stay this course, as it has served the project well to date. While this approach does raise the concern that Node2020 might become beholden to GitHub's whims, two notes relax our concerns here. First, Node.js was born in the GitHub age, and has modeled its governance around the platform's abilities. Second, the scale at which Node.js has grown cannot be dismissed. That scale (and the influence it provides) would benefit Node2020 should the project want to suggest changes to the GitHub platform. Moreover, as [the NPM default repository](https://https://www.npmjs.com/) is now part of GitHub, we assume assume the Node project would have even more leverage at GitHub, should it require implementation of a new feature.

### A net-new CI/CD tool for builds
Node.js uses Jenkins for its CI/CD build tool, because more friendly software-as-a-service solutions such as Travis CI or Circle CI just can't create binaries in all the different shapes and sizes that Node.js requires. That said, Jenkins is an aging technology missing many of the bells and whistles the more modern solutions provide. It also works in a "core-with-lots-of-plugins" model. In fact, a look at [CI documentation](https://ci.nodejs.org/) shows Node.js is *behind* a version on its implementation of Jenkins core (as well as a handlful of plugins). This is why Node2020 would use some *yet to be built* CI/CD solution along the lines of Circle CI, with all the features Node.js requires. These solutions, when finally available,are often free of charge for open source projects.

### HackerOne for security
When determining the Node.js project's [essential tooling](https://github.com/devinstewart/osi-class-notes/blob/master/node_js_assessment.md), Team 2 listed security as a *recommended* component. This was not to imply that security was *optional*, only to mark a distinction in the way security bugs get reported, relative to other types of bugs (perhaps even critical ones). Node2020 would continue to use HackerOne, just as Node.js does today. The reason for this is not so much the availability of bounties, but rather the ability to verify bug reports and access a controlled and defined system for announcement, risk assessment, liability, and recomended actions at their appropriate times.

### Metalsmith for project website
Metalsmith is a static site generator built on Node.js. Node2020 should utilize the same technology for building a fast and lightweight project website. This not only allows project participants to develop the site the same way they develop Node.js itself (on GitHub), but also allows the community to continuously improve a project that builds on its work, strengthening the Node project ecosystem.

### Social infrastructure overview
| Activity | Recommended Tool |
| - | - |
| Development chat and synchronous collaboration | [Matrix](https://matrix.org/) |
| Support and asynchronous collaboration | [Discourse](https://www.discourse.org/) |
| Community outreach | [Discourse](https://www.discourse.org/) |
| News and marketing | [Metalsmith](https://metalsmith.io/) |

### Matrix for development chat and synchronous collaboration
Developers collaborating on an open source project often require some means of real-time chat via text, audio, and/or video, especially when collaborating synchronously on a new feature or collectively assessing a security issue. Node.js [recommends](https://nodejs.org/en/get-involved/#community-discussion) developers connect to "the OpenJS Foundation Slack or IRC" to conduct development conversations. Node2020 should adopt a unified chat platform for developer communication, one built on the open source Matrix protocol, to better connect its developers and erode barriers to participating in development conversations. Access to the platform could be a perk of achieving "[Collaborator]((https://nodejs.org/en/about/community/))" status in the project. (We do recognize a significant [Node.js presence on Gitter](https://gitter.im/nodejs/home), and [Matrix just acquired Gitter](https://matrix.org/blog/2020/09/30/welcoming-gitter-to-matrix), so perhaps Node.js is already planning a move to this platform.) Node2020 could host and maintain its own Matrix infrastructure or subscribe to hosted service.

### Discourse for support and asynchronous communication
Node.js featured a fractured and disparate ecosystem of communication platforms for connecting with and supporting users, one that encompased familiar channels like Slack, Discord, Reddit, IRC, and more. Interstingly enough, while these platforms facilitate synchronous communication, the project (and its various working groups) utilized them largely for posting announcements (without invitation for further discussion) or addressing support requests (even those that didn't necessary unfold in real time). Node2020 should adopt a single paltform for community engagement, announcements, and support, one built on the open source Discourse tool. Adopting Discourse benefits Node2020 by offering a singular point of community support and engagement, enabling greater control over asynchronous communications tooling (Discourse features fine-grained access and moderation controls), and facilitating the construction of a robust knowledge commons, where questions and answers are more usefully logged and archived (rather than spread across platforms like [Stack Overflow](https://stackoverflow.com/questions/tagged/node.js) or lost in a Slack stream). Node2020 could host and maintain its own Discourse infrastructure or subscribe to hosted service.

### Discourse for community outreach
Once again, Discourse could serve Node2020 by functioning as a platform for community outreach and recruitment. Project members could (finally?) point would-be contributors to a single source for community conversation and assistance getting started with the project. Discourse's fine-grained access controls allow project members to make certain documentation available even to visitors who haven't yet created accounts or formally joined the project.

### Metalsmith for news and marketing
Curiously, Node.js utilizes a magazine-style [publication on Medium](https://medium.com/the-node-js-collection) for relaying stories about its community members and their successes. (The project's blog is [a purely technical changelog](https://nodejs.org/en/blog/).) Node2020 should relocate this publication to the project's flagship website, jettisoning a proprietary platform and instead availing itself of the same Node-based backend technology that powers the community's other web properties. On a Metalsmith-backed platform, publication authors could enjoy the same Markdown-based syntax they used on Medium. This syntax also allows for greater collaboration with other members of the project; collaboration on article drafts could proceed via GitHub issues and pull requests.
