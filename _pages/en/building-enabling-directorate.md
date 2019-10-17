---
layout: default
title: Building Nested Enabling Teams
ref: mandate
lang: en
status: posted
categories: Work In Progress
permalink: /building-enabling-directorate.html
---

## {{ page.title }}

### Problem Statement

In [Team Topologies](https://itrevolution.com/book/team-topologies/) they write that organizations should organize themselves by nesting the four team definitions.

- Value Stream Aligned Teams
- Platform Teams
- Enabling Teams
- Complex Subsystem Teams

In our particular case, to use it as an example, the IT Strategy team is an enabling team.
We are under a director who considers the directorate to be an enabling team.
Therefore the IT Strategy team is an enabling team within an enabling team, and has other sibling teams that are also enabling teams.
That being the case, how would one synchronize activities of the entire directorate? Say the director was to offer their services to a team elsewhere in the organization.
How best to manage and coordinate the work between the series of sub-enabling teams? That is the question this document is intending to answer.

### Proposal

#### Organizational

##### Internal Interactions

The teams may remain in their present functional structure for now, which aligns well with the governments expected structure for the sake of processes such as the Public Service Performance Management (PSPM).
In our particular case, the teams will be as follows:

- IT Strategy
- IT Service Management
- Software Vendor Management
- Hardware Vendor Management

Each team has its own set of responsibilities for which they are responsible.
The teams will collaborate regularly both via regular meetings and open collaboration tools (where possible and appropriate).
For example, in addition to e-mail, tools such as Slack or Skype messenger should be used for regular informal communications and kanban boards should be open by default enabling each team to follow the progress of one another.

###### Time Management

Teams should not be fully allocated to their enabling function.

Firstly, each team must resolve time for the continuous self-improvement, which should be equal to, or strictly greater than, 20% of their teams available work time.

Secondly, teams are free to self organize under the condition that they are able to meet the needs of the directorate’s priorities.
For example, a team within the directorate may accept to fulfill an enabling function for another team within the organization.

Thirdly, an enabling team need not commit all of their time to being an enabling team.
For example, in the case of the IT Strategy team they are also responsible for setting the IT vision for the department, and thus cannot dedicate 100%(-20%) of their time to their enabling function.
In this particular case, for example, we recommend that the IT Strategy spend a maximum of (100-20)/2 percent of their time on enabling other teams.

##### External Interactions

This is an initial proposal and is intended to allow for iterations to refine and modify the process as needed.

###### Interactions

The book Team Topologies, referenced below, recommends that Enabling Teams work with other teams for a period (potentially a few months) [TO-DO: Quote needed] in order to assist them with onboarding new technologies and approaches, and improving their existing processes and procedures.
The goal is to ensure the interactions are brief enough that the teams being enabled do not become dependent on the enabling teams.
The process improvements should stand on their own, and should not involve [toil](https://landing.google.com/sre/sre-book/chapters/eliminating-toil/).
That is to say, the new processes and procedures should aim to automate or improve the existing processes, not lend temporary person-power to the teams
Given the short and iterative nature of the interactions between the teams (duration of interactions should be defined by number of sprints) the enabling teams must identify quick wins -- the amount of automation that could be done within the limited time frame that would result in the greatest amount of automated work.

###### Tooling

[TO-DO: Quote from Team Topologies regarding varying levels of team communication]

The amount of collaboration between the enabling teams and the enabled teams should vary significantly during the time which the enabling team is paired with the enabled team
As such, collaboration tools that allow for the rapid creation and disintegration should be leveraged
An example of a viable tool for such a requirement would be Slack, where groups can be created and disposed of with relative ease.

#### Process

##### Teams Iterative Process

- All teams within the directorate have synchronized sprints
- Representatives from each enabling team within the enabling directorate meet prior to the synchronized sprint planning for the director to set directorate-level priorities
- During the synchronized sprint planning meetings, ensure directorate-level priorities are broken down into manageable tasks

##### Engaging the Enabling Teams

- Potential teams to be enabled should contact the enabling teams
- An item is created on the kanban board of the enabling team
- Representative from an enabling team meets with potential client team to prioritize work
- Work is planned and prioritized by the enabling team during sprint planning

*Note: It is important that the enabling teams have open kanban boards so that teams who have requested their attention can see where their tasks have been prioritized relative to others, or can see work in progress as the interaction takes place between the two teams.*

### References

[Team Topologies](https://itrevolution.com/book/team-topologies/)