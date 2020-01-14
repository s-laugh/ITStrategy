<!--markdownlint-disable MD033-->
# Working in the Open

**SSC Learn Architecture**, January 22 2020

Gabriel Cossette, Senior Advisor<br>
Employment and Social Development Canada

---

## What

--

Your workspace (or part of it) is public and participatory.

Note:

- Public and Participatory - [Mozilla - Working Open](https://wiki.mozilla.org/Working_open)

--

People can find your workspace and read its content

Note:

- Documents, including drafts
- Planning
- Tasks
- Notes
- Source code

--

It's not just "working out loud"

You need to enable and encourage contributions!

Note:

- Not just sharing one way
  - Promoting, Sharing, Communicating what you are working on
- With entire department (and GC!), not just your branch or your team
- Open Source
  - Thousands of people working together
  - Various levels of contributions
- Do not force collaboration (see [HBR Collaborative Overload](https://hbr.org/2016/01/collaborative-overload))
  - It has to come organically (people interested, similar issues, etc.)
  - Can be sporadic or more involved (simple fixes, no commitments)

--

It's also a cultural thing

- Humility
  - Willingness to learn and improve
- Inclusiveness
- Trust

Note:

- Humility, being humble
  - "I don't know everything. And it's okay because I want to learn and improve."
  - "You may have a better answer than me even though I don't know you."
- Inclusiveness and accessibility
  - No discrimination
  - Encourage participation of everyone, actively looking for people from a diverse background and community
- Trust
  - You trust your team
  - You trust this is good for the public
  - The public should trust the government
    - [Accountability](https://product-guide.18f.gov/working-in-a-way-that-reflects-our-values/working-in-the-open/)

---

## Why

--

### 1. It makes your work discoverable

According to [DORA DevOps Report 2019](https://cloud.google.com/devops/state-of-devops/) (page 62):
> Internal and External search capabilities are key enablers for **productivity** AND **job satisfaction**

Note:

- It's hard to look for something you don't know exists
  - If it's in the open, it can at least be found
- Create opportunities for a community
  - E.g. [Open Resource Exchange](https://canada-ca.github.io/ore-ero/en/index.html) with Canadian municipalities

--

### 2. Avoid duplication of work

MANY problems are already solved

Note:

- Lots of redundancies across teams, branches and departments
- Because it's discoverable, you may find an already existing solution
- Adapt instead of building from scratch (or buying something!)

--

### 3. Economies of scale

For your organization and outside

Note:

- Many solutions can be useful to problems/people you haven't thought of
- Contribute to the project so that everyone benefit from it
- With a community, team is bigger than number of people you can hire

--

### 4. Early Feedback Loop

To be agile in an unpredictable world

- Early course correction to avoid waste
- Peer review is very valuable

--

### 5. Increase Quality of Work

> when other people can see your work, you tend to raise your game
United Kingdom Government Digital Service [blog post](https://gds.blog.gov.uk/2017/09/04/the-benefits-of-coding-in-the-open/)

Note:

- Encourages good practice (people will see your work!)
  - In software development, improve security, accountability and sustainability (see [Working in the Open from 18F Product Guide](https://product-guide.18f.gov/working-in-a-way-that-reflects-our-values/working-in-the-open/))
- Makes collaboration easier (more organic, less rigid)
- Helps others learn from your own work

---

## When

--

As soon as possible. Now.

Don't wait until it's perfect, it never will be

Note:

- Don't wait until you had all your committee reviews done
- Start your drafts in the open (improve the way you write)
- It's a lot harder to open up at the end
- [Policy on Service and Digital 4.3](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=32603#cla4.3)
  - Open and strategic management of information
  - 4.3.2.8 Maximizing the release of departmental information and data as an open resource, discoverable through the Government of Canada open government portal designated by the Treasury Board of Canada Secretariat, while respecting information security, privacy, and legal considerations.

---

## How

---

### Responsibilities

--

#### Copyright

Your work is under Crown Copyright

> Copyright (c) Her Majesty the Queen in Right of Canada, as represented by `<Department Name>`, `<Date>`

Source: [Crown Copyright Request](https://www.canada.ca/en/canadian-heritage/services/crown-copyright-request.html)

--

#### Licence

If possible and applicable, release it under an open licence:

- [Open Source Licence](https://opensource.org/licenses) - for source code
- [Open Government Licence – Canada](https://open.canada.ca/en/open-government-licence-canada) - for data, information, content

Note:

- Need approval from proper delegated authority (varies by department)
- Existing OSS licence is preferable for source code
  - Industry is more familiar with these licences
  - Easier to have people contribute back to your project

--

#### Notice

Include a notice with the mention of the licence and trademark

--

Licence:

> Unless otherwise noted, the source code of this project is covered under Crown Copyright, Government of Canada, and is distributed under the MIT License.

--

Trademark:

> The Canada wordmark and related graphics associated with this distribution are protected under trademark law and copyright law. No permission is granted to use them outside the parameters of the Government of Canada's corporate identity program. For more information, see Federal identity requirements.

--

#### Security Classification

Include only unclassified material

From recently published [GC OSS Guidance](https://www.canada.ca/en/government/system/digital-government/open-source-software/guide-for-publishing-open-source-code.html#toc03)

> Keep sensitive data such as credentials secure and separate from source code.
> Leverage tools and services to automate finding known security vulnerabilities, possible secret keys and personally identifiable information.

Note:

- Also, don't include personally identifiable information, or information related to procurement processes

--

#### Public Scrutiny

Write like the newspaper is going to publish your content

Note:

- Again, increase quality of your work
- You KNOW people can come and see it; you should think twice before posting something
- If you're not comfortable at a personal level, ask for help!
- Bigger picture, you may want to ask why you're working on this if you're not comfortable sharing

--

#### Control

It's still your work, you need to maintain it

- Single source of truth
- You control incoming contributions
- And if you don't control anymore, it continues to live

Note:

- Not a clone of your internal workspace
- Contributions are welcome but you decide what goes into your work or not

--

#### Community Management

> Warning: A community may coalesce

Manage the community for your own benefit... and everyone's

- Set expectations
  - "We usually respond within 48 hours"
  - "We don't take contributions at this point, but happy to have you submit suggestions"
  - "Use these templates for contributions"

Note:

- Manage your community, you will benefit greatly from it (incl. personnally)
- Stephen Walli - "It's all about software engineering economics"
- If your work is interesting, people might find it
- People may submit recommendations and modifications to you

--

#### Help newcomers

Be kind, Be patient, Be inclusive

Note:

- Some people are new at this
- Welcome people from everywhere
- Set a Code of Conduct
  - Should include a link to the Public Servant's Values and Ethics

--

![oh-my-zsh Contributions](assets/images/oss-zsh.png)

---

### Tools

Note:

- If the following tools are blocked, lets chat.
- The DA, TBS and many other teams across departments may be able to help

--

#### Community Management

- [GCmessage (pilot)](https://message.gccollab.ca/home)
- [Slack](https://slack.com/) to a certain extent (closed communities)
- [GCcollab](https://gccollab.ca/splash/)
  - Communities of Practice

--

#### Workspace

- [GitHub](https://github.com)
- [GitLab](https://gitlab.com)

- [GCpedia](https://www.gcpedia.gc.ca)
- [GCcollab Wiki](https://wiki.gccollab.ca/)

--

#### Planning

- [GitHub - Projects](https://github.com/features/project-management/)
- [GitLab - Boards](https://about.gitlab.com/product/issueboard/)
- [Trello](https://trello.com/)
- [Taiga](https://taiga.io)

--

#### Version Control

- [GitLab](https://gitlab.com/)
- [GitHub](https://github.com/)
- [Bitbucket](https://bitbucket.org/)
- [GCcode](https://gccode.ssc-spc.gc.ca/) (internal)

--

#### Communications

- [Twitter](https://twitter.com/)
- Intranet News and Sites
- [Open Resource Exchange](https://canada-ca.github.io/ore-ero/)

---

## Demo of our team workspace

--

# GitHub Workspace

![GitHub Workspace](assets/images/github-workspace.png)

--

# Team website (automatically generated from Workspace)

![GitHub Workspace](assets/images/github-workspace.png)

--

# Kanban board for Planning

![Kanban](assets/images/kanban.png)

--

# Pull Request

![GitHub Workspace](assets/images/pullrequest.png)

--

# Feedback in Pull Request

![GitHub Workspace](assets/images/pullrequest-feedback.png)

--

# Text Editor (Visual Studio Code - free open source)

![GitHub Workspace](assets/images/vscode.png)

--

# View changes in text editor

![GitHub Workspace](assets/images/vscode-changes.png)

---

## Examples

Note:

Of projects in the open

--

[Open Resource Exchange](https://github.com/canada-ca/ore-ero)

--

[Algorithmic Impact Assessment](https://github.com/canada-ca/aia-eia-js)

--

[Web Experience Toolkit (WET)](https://wet-boew.github.io/wet-boew/docs/ref/accolades-en.html)

--

[Drupal-WXT](http://drupalwxt.org)

--

[Linux Kernel](https://github.com/torvalds/linux)

![Linux Kernel Contributors](assets/images/oss-linux.png)

---

# References

5 principles from article ["Working in the Open: lessons from open source on building innovation networks in education"](https://www.emerald.com/insight/content/doi/10.1108/OTH-05-2016-0025/full/html):

- Public storytelling and context setting
- Enabling community contribution
- Rapid prototyping “in the wild”
- Public reflection and documentation
- Creating remixable work products