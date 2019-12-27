---
layout: post
title: "Engineering Organizations"
ref: engineering-organizations
lang: en
author: "Jayson McIntosh, IT Strategy Team"
date: "2019-12-27"
last_modified: "2019-12-27"
excerpt_separator: <!--more-->
---

### Preamble

Given that I am writing this as a member of the IT Strategy team from ESDC, I will be speaking largely to government organizational structures, though I would imagine many of the content would apply to many large organizations that have existed long enough to acquire the dreaded and inevitable technnical and organizational debt (for a more indepth discussion of organizational debt I would suggest giving [Brave New Work](https://www.bravenewwork.com/) a read).

## Introduction

In [Brave New Work](https://www.bravenewwork.com/) author [Aaron Dignan](http://www.aarondignan.com/#intro) remarks in the opening chapters how the org chart hasn't changed in decades. He calls showing organizations an organizational chart and asks them, roughly what year do they think it is from? It so happens that in this case it was from the late 1800s. The point being made here is that while the world has changed around us our organizations have remained stagnant. Is it the case that organizations have not needed to change, or is it the case that our organizational transformations are indeed lagging behind other forms of innovation? By the end of this article a case will be made for the latter.

## Current Situation

> The older way of thinking about risk is by planning and thinking through things in great detail. This will work well in a situation where things don't change much, but that just isn't the situation we have. Every day I walk into work, something surprises me. Even in government, in immigration, things changed all the time. Technology changes all the time and new things become possible and demanded by users. Relying on a plan to mitigate risk is not going to work.

- [War & Peace & IT](https://itrevolution.com/war-and-peace-and-it/) by Mark Schwartz

Often in large organizations the following set of events is common place

1. We identify a problem
2. Create team X to rectify said problem, and said team becomes "responsible" for ensuring "compliance"
3. Team X creates a process to steamline their approach to solving said problem
4. Henceforth, all teams must go through team X in order to ensure said process is followed for consistency

Often when digging through process documentation one may find phrases something akin to "this process is intended such that all requests must go through it in order to ensure create a deterministic and consistent process". That sounds like a good thing, right?

The trick with change, and this only worsens as the change is procrastinated over time which makes the leap that much greater, is that sometimes something intuitive can be wrong. To make things worse, the intuitive answer was probably right at some point or another, though with the advent of new tools new possibilities are uncovered. Back five or ten years ago I recall hearing colleagues joke about 'doing it live' while logging on to a production server to fix an issue, something that was known to be somewhat of a cowboy move as it often resulted in even larger issues being caused, given that proper testing had not taken place to test the change. Someone who began their career in this kind of environment may have difficulty accepting the new model there situations as follows are promoted

> ... one of the most surprising elements of this story is that TurboTax performed production experiments during their peak traffic seasons. For decades, especially in retailing, the risk of revenue-impacting outages during the holiday season were so high that we would often put into place a change freeze from mid-October to mid-January. However, by making software deployments and releases fast and safe, the TurboTax team made online user experimentation and any required production changes a low-risk activity that could be performed during the highest traffic and revenue generating periods.

- [The DevOps Handbook](https://www.amazon.ca/dp/B01M9ASFQ3/ref=dp-kindle-redirect?_encoding=UTF8&btkr=1)

Another example would the Chaos Monkey, from Netflix. Everyone who has worked in an operational environment knows how fragile a production environment can be. We have teams of people to separate responsibilities in order to ensure the proper _processes_ are followed, ensuring checks at every turn, and entire teams dedicated to a given step in the process to ensure care and repeatability. In less desirable situations, I have worked on teams where once something enters production it is never touched or changed. Ever. If you want a new version of whatever is in production you just host _the_best_app_ever_v2.sh_ and then people have the option of using whichever version they require. In any case, production is fragile and protected at all costs to reduce the chances of outages. Someone who developed their skillset in this environment may not find it intuitive then that leading IT companies such as Netflix runs software like Chaos Monkey on their production networks.

> ... in addition to implementing these architectural patterns, they also built and had been running a surprising and audacious service called Chaos Monkey, which simulated AWS failures by constantly and randomly killing production servers. They did so because they wanted all “engineering teams to be used to a constant level of failure in the cloud” so that services could “automatically recover without any manual intervention.”

- [The DevOps Handbook](https://www.amazon.ca/dp/B01M9ASFQ3/ref=dp-kindle-redirect?_encoding=UTF8&btkr=1)

In order to realize these new ways of working, as illustrated in the two above examples with Intuit and Netflix organizationals must adjust. To enable the changes that must take place both the skillsets (through [continuous learning](https://sara-sabr.github.io/ITStrategy/2019/10/15/case-continuous-improvement.html)) and organization must evolve with the constantly changing possibilites that emerge as new technologies are created.

All right then, we all want to be able to make thousands of changes per day to our production environments, and run Chaos Monkey on our production networks to ensure maximal stability. But hey, I hear you say, I work in a large highly regulated institution that isn't anywhere near capable of doing the aforementioned approaches (yet). Where do I start? How does my organization go from what is intuitive to what is possible?

## Where to Start: Engineering Organizations

Modern software has the fortunate attribute that it can be easily modified, rebuilt, and deployed, at will. Unfortunately, this is not so with many organizations (although this can be mitigated by adopting a culture of continuous learning). Change is difficult. Adopting new procedures and processes is a several year long task. So how can we be confident our approach is the right one before dedicating ourselves to the arduous task of pushing for change? I find it curious that when it comes to building complex systems like satellites, or networks, we incorporate all the mathamatical and engineering mastery we can muster -- to great results. When it comes to organizations we often seem to settle for hand wavey justifications based on beliefs or experience. This is not sufficient. If we have the tools to design robust networks and complex systems, why can we not apply the same rigour to our organizations?

Given the difficulty in changing existing organizations, in order to guide decisions, I find it best to identify a basic axiom and apply it a given situation. If you have picked a good, simple, and reliable, axiom then when the axiom does not align with a given situation, change the situation. Here's an example. My axiom for the below case is that a series network is less reliable than a parallel (assuming an equal reliability for each node), and we will use this simple (and proveable claim) to redesign our approach to process within our organizations.

![A Series Network]({{site.baseurl}}/assets/images/seriesnetwork.PNG)
reliability = _1-(1-r^n)_

![A Parallel Network]({{site.baseurl}}/assets/images/parallelnetwork.PNG)
reliability = _1-(1-r)^n_

_For a quick hand wavey demonstration, assuming each node has an identical reliability of r and assuming r = 0.9, then_

_Series Network_ = 1-(1-0.9^2) = 0.81

_Parallel Network_ = 1-(1-r)^2 = 0.99

_We see here that the parallel network becomes more reliabile with each added node, while a series network becomes less reliable_

In the [above section](#CurrentSituation) we identified a common situation where an intuitive set of steps was taken in order to address a problem. Looking at that same situation again, which kind of network have we just created? Unfortunately, a series network. To make matters worse, we ensured that "all teams must go through team X in order to ensure said process". If the process is indeed solving a problem, or addressing a need, many teams within the department are going to want to go through this process. As demand increases, by design, there is nowhere else for the organization to turn. You must wait, or go rogue (which, if you have processes like these, many more people are already doing than most organizations would be comfortable admitting). As demand increases, the load on the team grows, queues begin to form, and then processes within processes emerge, each with their own overhead, in order to triage requests by priority, resulting in many in the organization waiting years to get even a small request through. From the perspective of a user this process is peculiar, as even small requests seem to get caught up in this bottle neck, as the small requests get consistently bumped in priority for big ticket items that the overworked team responsible for this process is desparately trying to cope with. Okay okay, so it's a mess. What to do? Create a parallel network.

When everything, including small repetitive tasks, needed to be done manually by humans the appeal for one process which everyone can follow without variation have an undenyable appeal. However, one of the strengths of automation is that these "small easy requests" that get backed up in the queue described above can be easily automated. The answer then, address the low hanging fruit and create automated processes. What would our network look like now, and what would its reliability be?

Below is the intuitive process we have defined above

![An example process]({{site.baseurl}}/assets/images/simpleSeriesProcess.png)

## Working in the Open

## References

- [Brave New Work](https://www.bravenewwork.com/)
- [Design Reliability - Fundamentals and Applications](https://www.amazon.com/Design-Reliability-Fundamentals-B-S-Dhillon/dp/0849314658)
- [War & Peace & IT](https://itrevolution.com/war-and-peace-and-it/)
