# Node.js Project Assessment

## About the project
From [nodejs.org](https://nodejs.org/en/):
> Node.js® is a JavaScript runtime built on Chrome's V8 JavaScript engine.

From [Wikipedia](https://en.wikipedia.org/wiki/Node.js):
> Node.js is an open-source, cross-platform, JavaScript runtime environment that executes JavaScript code outside a web browser. Node.js lets developers use JavaScript to write command line tools and for server-side scripting—running scripts server-side to produce dynamic web page content before the page is sent to the user's web browser. Consequently, Node.js represents a "JavaScript everywhere" paradigm, unifying web-application development around a single programming language, rather than different languages for server- and client-side scripts. [...] The Node.js distributed development project was previously governed by the Node.js Foundation, and has now merged with the JS Foundation to form the OpenJS Foundation, which is facilitated by the Linux Foundation's Collaborative Projects program. Corporate users of Node.js software include GoDaddy, Groupon, IBM, LinkedIn, Microsoft, Netflix, PayPal, Rakuten, SAP, Voxer, Walmart, and Yahoo!.

## Project governance
Understanding the Node.js governance model becomes easier when one understand's the project's history:
- Ryan Dahl first created Node.js in 2009. In November 2010, he announced that he had reached an agreement with Joyent to handle its governance.
- In December 2014, due to an internal conflict over Joyent's governance, a group of developers decided fork Node.js and release it as io.js. io.js was created as an open governance alternative with a separate technical committee. Unlike Node.js, the authors planned to keep io.js up to date with the latest releases of the Google V8 JavaScript engine.
- In February 2015, the intent to form a neutral Node.js Foundation was announced. By June 2015, the Node.js and io.js communities voted to work together under the Node.js Foundation.
- In September 2015, Node.js v0.12 and io.js v3.3 merged into Node v4.0. This released introduced the project's governance model to the average to the average Node.js user.
- In 2019, the JS Foundation and Node.js Foundation merged to form the OpenJS Foundation. Under the OpenJS Foundation, Node.js is one of many projects (30 at last count). It is listed as one of their six "Impact Projects." The over five are: Appium, jQuery, Dojo, Electron, and webpack.

### Governance model
The Node.js project operates with [a hybrid governance model](https://nodejs.org/en/about/governance/): one part foundation-backed, one part electoral.

The [OpenJS Foundation](https://openjsf.org/) (a Linux Foundation project) oversees business, legal, and technical aspects of the project, and operates through a [Technical Steering Committee](https://github.com/nodejs/TSC/blob/master/TSC-Charter.md) (TSC) that runs its own [electoral processes](https://github.com/nodejs/TSC/blob/master/TSC-Charter.md#section-6-elections). The TSC is the ultimate arbiter of the Node.js project.

The Node.js [Community Committee](https://nodejs.org/en/about/community/) (or "CommComm"), "[an autonomous committee that collaborates alongside the TSC](https://github.com/nodejs/community-committee#governance-and-current-members) and whose governance was strongly influenced by the TSC's example," oversees implementation of TSC's decisions regarding both technical and non-technical aspects of the project. It also operates [through elections](https://github.com/nodejs/community-committee/blob/master/Community-Committee-Charter.md#section-6-elections).

The CommComm is further divided into [various working groups](https://nodejs.org/en/about/working-groups/), each dedicated to a different aspect of project management.

### Decision-making processes
The TSC makes decisions both through [lazy consensus and votes requiring simple majority](https://github.com/nodejs/TSC/blob/master/TSC-Charter.md#section-7-voting). The CommComm's process differs slighty (at least [as described](https://github.com/nodejs/community-committee/blob/master/CONTRIBUTING.md#the-commcomm-process)):
> The group tries to find a resolution that has no open objections among the CommComm members. If a consensus cannot be reached that has no objections then a majority wins vote is called. It is also expected that the majority of decisions made by the CommComm are via a consensus seeking process and that voting is only used as a last-resort. Resolution may involve returning the issue to collaborators with suggestions on how to move forward towards a consensus. It is not expected that a meeting of the CommComm will resolve all issues on its agenda during that meeting and may prefer to continue the discussion happening among the collaborators.

The CommComm gathers twice per month for synchronous meetings (Observers, of course, are also in attendance).

### Community roles and responsibilities
The Node.js project features four principal roles participants can play:

- Contributor 
- Collaborator
- Observer
- Member

According to the project's [governance documents](https://nodejs.org/en/about/community/):
> A **Contributor** is any individual creating or commenting on an issue or pull request. A **Collaborator** is a contributor who has been given write access to the repository. An **Observer** is any individual who has requested or been requested to attend a CommComm meeting. It is also the first step to becoming a Member. A **Member** is a collaborator with voting rights who has met the requirements of participation and voted in by the CommComm voting process.

Additional detail is available in [a GitHub repository](https://github.com/nodejs/community-committee/tree/master/governance).

Node.js seems to have a reputation as a project with a "[liberal contribution model](https://medium.com/the-node-js-collection/healthy-open-source-967fa8be7951)" (as noted above, the community considers a "contributor" anyone who has done so much as left a comment or opened an issue). Much of its project infrastructure is therefore accessible to a majority of project participants.

## Infrastructure audit
| Activity | Tool Used | Tool Location | Target Project Role | Notes |
| -------- | --------- | ------------- | ------------------- | ----- |
| Bug reports and feature requests | GitHub Issues | https://github.com/nodejs/node/issues | All | Bugs / Features are all maintained in GitHub Issues and separated via labels. |
| Secuirty | HackerOne | https://hackerone.com/nodejs https://nodejs.org/en/security/ | | For security related issues, the Node.JS requests using HackerOne. Use of this tool and feeback is outlined on the [website](https://nodejs.org/en/security/). |
| Documentation | GitHub Flavored Markdown & Website | https://github.github.com/gfm/ https://github.com/nodejs/node/tree/master/doc https://nodejs.org/en/docs/ | Collaborator, Observer, Member (Contributors welcome to leave comments or open a request) | Documentation is maintained using GFM and accessed by most users via the [website](https://nodejs.org/dist/latest-v14.x/docs/api/). |
| Team communication | IRC | Freenode | All | Located in ``#node.js`` on ``irc.freenode.net`` |
| Team communication | Discord | https://discordapp.com/invite/vUsrbjd | All (?) | Seems to be reserved primarily for "backend developers" |
| Localization | Crowdin | https://crowdin.com/project/nodejs-website | | Moving to Crowdin seems like [a relatively recent infrastructural decision](https://github.com/nodejs/nodejs.org/blob/master/TRANSLATION.md) |
| Project website | Metalsmith | https://metalsmith.io/ | Collaborator, Observer, Member (specifically on [website working group](https://github.com/nodejs/nodejs.dev)) | The Node.JS website is created using a tool that runs in Node.JS |
| Governance | GitHub | https://github.com/nodejs/community-committee | Members | The Community Committee (or "CommComm") is a principal governing body in Node.js; it appears to conduct most of its work via GitHub |
| Community outreach | Slack | https://www.nodeslackers.com/ | All | "Anyone with any amount of interest in Node.js is welcome to join." |
| News and marketing | Medium | https://medium.com/the-node-js-collection | Collaborator, Observer, Member (specifically on [evangelism working group](https://nodejs.org/en/about/working-groups/#evangelism)) | |
| News and marketing | Twitter | https://twitter.com/nodejs | Collaborator, Observer, Member (specifically on [evangelism working group](https://nodejs.org/en/about/working-groups/#evangelism)) | |
