# Node.js Project Assessment

## About the project
From [nodejs.org](https://nodejs.org/en/):
> Node.js® is a JavaScript runtime built on Chrome's V8 JavaScript engine.

From [Wikipedia](https://en.wikipedia.org/wiki/Node.js):
> Node.js is an open-source, cross-platform, JavaScript runtime environment that executes JavaScript code outside a web browser. Node.js lets developers use JavaScript to write command line tools and for server-side scripting—running scripts server-side to produce dynamic web page content before the page is sent to the user's web browser. Consequently, Node.js represents a "JavaScript everywhere" paradigm, unifying web-application development around a single programming language, rather than different languages for server- and client-side scripts. [...] The Node.js distributed development project was previously governed by the Node.js Foundation, and has now merged with the JS Foundation to form the OpenJS Foundation, which is facilitated by the Linux Foundation's Collaborative Projects program. Corporate users of Node.js software include GoDaddy, Groupon, IBM, LinkedIn, Microsoft, Netflix, PayPal, Rakuten, SAP, Voxer, Walmart, and Yahoo!.

## Project governance

### Governance model
The Node.js project operates with [a hybrid governance model](https://www.redhat.com/en/resources/guide-to-open-source-project-governance-models-overview?source=resourcelisting&f%5B0%5D=taxonomy_topic%3AOpen+source+communities): one part foundation-backed, one part electoral. The [OpenJS Foundation](https://openjsf.org/) (a Linux Foundation project) oversees business and legal aspects of the project, and operates through a [Technical Steering Committee](https://github.com/nodejs/TSC/blob/master/TSC-Charter.md) (TSC) that runs its own [electoral processes](https://github.com/nodejs/TSC/blob/master/TSC-Charter.md#section-6-elections); the [Community Committee](https://github.com/nodejs/community-committee/blob/master/Community-Committee-Charter.md#community-committee-charter) (or "CommComm"), which operates [through elections](https://github.com/nodejs/community-committee/blob/master/Community-Committee-Charter.md#section-6-elections) overseas technical aspects of the project.

### Decision-making processes
The TSC makes decisions both through [lazy consensus and votes requiring simple majority](https://github.com/nodejs/TSC/blob/master/TSC-Charter.md#section-7-voting).

### Community roles and responsibilities
The Node.js project features four principal roles participants can play:

- Contributor
- Collaborator
- Observer
- Member

According to the project's [governance documents](https://nodejs.org/en/about/community/):
> A **Contributor** is any individual creating or commenting on an issue or pull request. A **Collaborator** is a contributor who has been given write access to the repository. An **Observer** is any individual who has requested or been requested to attend a CommComm meeting. It is also the first step to becoming a Member. A **Member** is a collaborator with voting rights who has met the requirements of participation and voted in by the CommComm voting process.

Additional detail is available in [a GitHub repository](https://github.com/nodejs/community-committee/tree/master/governance).

## Infrastructure audit
| Activity | Tool Used | Tool Location | Target Project Role | Notes |
| -------- | --------- | ------------- | ------------------- | ----- |
| Bug reports & Feature requests | GitHub Issues | https://github.com/nodejs/node/issues | All | Bugs / Features are all maintained in GitHub Issues and separated via labels. |
| Secuirty | HackerOne | https://hackerone.com/nodejs https://nodejs.org/en/security/ | Users, contributors, and project maintainers | For security related issues, the Node.JS requests using HackerOne. Use of this tool and feeback is outlined on the [website](https://nodejs.org/en/security/). |
| Documentation | GitHub Flavored Markdown & Website| https://github.github.com/gfm/ https://github.com/nodejs/node/tree/master/doc https://nodejs.org/en/docs/ | Users, contributors, and project maintainers | Documentation is maintained using GFM and accessed by most users via the [website](https://nodejs.org/dist/latest-v14.x/docs/api/). |
| Team communication | IRC | Freenode | Users, current and prospective contributors | Located in ``#node.js`` on ``irc.freenode.net`` |
| Team communication | Discord | https://discordapp.com/invite/vUsrbjd | Users, current and prospective contributors | Seems to be reserved primarily for "backend developers" |
| Localization | Crowdin | https://crowdin.com/project/nodejs-website | International community members and the localization team | Moving to Crowdin seems like [a relatively recent infrastructural decision](https://github.com/nodejs/nodejs.org/blob/master/TRANSLATION.md) |
| Project website | Metalsmith | https://metalsmith.io/ | Current and potential users, and website steering committee | The Node.JS website is created using a tool that runs in Node.JS |
| Governance | GitHub | https://github.com/nodejs/community-committee | [Contributors](https://nodejs.org/en/about/community/#contributors-and-collaborators) and [project members](https://nodejs.org/en/about/community/#observers-and-membership) | The Community Committee (or "CommComm") is a principal governing body in Node.js; it appears to conduct most of its work via GitHub |
| Community outreach | Slack | https://www.nodeslackers.com/ | Users, current and prospective contributors |  |
| News & marketing | Medium | https://medium.com/the-node-js-collection | Users and potential contributors |  |
| News & marketing | Twitter | https://twitter.com/nodejs | Users and potential contributors |  |
