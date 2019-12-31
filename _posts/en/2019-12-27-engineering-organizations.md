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

Given that I am writing this as a member of the IT Strategy team from ESDC, I will be speaking largely to government organizational structures, though I would imagine much of the content applies to most large organizations that have existed long enough to acquire the dreaded and inevitable technnical and organizational debt (for a more indepth discussion of organizational debt I would suggest giving [Brave New Work](https://www.bravenewwork.com/) a read).

## Introduction

In [Brave New Work](https://www.bravenewwork.com/) author [Aaron Dignan](http://www.aarondignan.com/#intro) remarks in the opening chapters how the org chart hasn't changed in decades. He recalls showing groups organizational charts and asking them roughly what year the org charts are from? It so happens that in this case from the book the org chart was from the late 1800s. The point being made here is that while the world has changed around us our organizations have remained largely unchanged. Is it the case that organizations have not needed to change, or is it the case that our organizational transformations are indeed lagging behind other forms of innovation? By the end of this article a case will be made for the latter, though we're not going to address the organizational chart specifically. Rather, we will discuss that new models or problem solving are required within organizations in order to be successful in the digital age.

## Current Situation

> The older way of thinking about risk is by planning and thinking through things in great detail. This will work well in a situation where things don't change much, but that just isn't the situation we have. Every day I walk into work, something surprises me. Even in government, in immigration, things changed all the time. Technology changes all the time and new things become possible and demanded by users. Relying on a plan to mitigate risk is not going to work.

- [War & Peace & IT](https://itrevolution.com/war-and-peace-and-it/) by Mark Schwartz

Often in large organizations the following set of events is common place

1. We identify a problem
2. Create team X to rectify said problem, and said team becomes "responsible" for ensuring "compliance"
3. Team X creates a process to steamline their approach to solving said problem
4. Henceforth, all teams must go through team X in order to ensure said process is followed for consistency

Often when digging through process documentation one may find phrases something akin to "this process is intended such that all requests must go through it in order to ensure create a deterministic and consistent process". That sounds like a good thing, right?

The trick with change, and this only worsens as the change is procrastinated over time which makes the leap that much greater, is that sometimes something intuitive can be wrong, or become wrong as cicrumstances change (like new technologies, for example). The intuitive answer may have been right at some point or another, though with the advent of new tools and technologies new possibilities are uncovered. Five or ten years ago I recall hearing colleagues joke about 'doing it live' while logging on to a production server to fix an urgent issue, something that was known to be somewhat of a cowboy move as it often resulted in even larger issues being caused, given that proper quality control had not taken place to test the change. Someone who began their career in this kind of environment may have difficulty accepting the new model where situations as follows are becoming increasingly popular

> ... TurboTax performed production experiments during their peak traffic seasons. For decades, especially in retailing, the risk of revenue-impacting outages during the holiday season were so high that we would often put into place a change freeze from mid-October to mid-January. However, by making software deployments and releases fast and safe, the TurboTax team made online user experimentation and any required production changes a low-risk activity that could be performed during the highest traffic and revenue generating periods.

- [The DevOps Handbook](https://www.amazon.ca/dp/B01M9ASFQ3/ref=dp-kindle-redirect?_encoding=UTF8&btkr=1)

Another example would the famous Chaos Monkey from Netflix. Everyone who has worked in an operational environment knows how fragile a production environment can be. Historically we have created entire teams of people to separate responsibilities in order to ensure the proper _processes_ are followed, ensuring checks at every turn, and entire teams are dedicated to a given step in the process to ensure care and repeatability. In less desirable situations, I have worked on teams where once something enters production it is never touched again. Ever. If you want a new version of whatever is in production you just host _the_best_app_ever_v2.sh_ and then people have the option of using whichever version they require. In any case, in the past production has been thought of as fragile, and something that must be protected at all costs, espcially from the developers who keep breaking it with their newest and greatest feature, to reduce the chances of outages. Someone who developed their skillset in this environment may not find it intuitive then that leading IT companies such as Netflix runs software like Chaos Monkey on their production networks.

> ... in addition to implementing these architectural patterns, they also built and had been running a surprising and audacious service called Chaos Monkey, which simulated AWS failures by constantly and randomly killing production servers. They did so because they wanted all “engineering teams to be used to a constant level of failure in the cloud” so that services could “automatically recover without any manual intervention.”

- [The DevOps Handbook](https://www.amazon.ca/dp/B01M9ASFQ3/ref=dp-kindle-redirect?_encoding=UTF8&btkr=1)

In order to realize these new ways of working, as illustrated in the two above examples with Intuit and Netflix organizationals must adjust. To enable the changes that must take place both the skillsets (through [continuous learning](https://sara-sabr.github.io/ITStrategy/2019/10/15/case-continuous-improvement.html)) and organization must evolve with the constantly changing possibilites that emerge as new technologies are created.

All right then, we all want to be able to make thousands of changes per day to our production environments like the leading tech companies, and run Chaos Monkey on our production networks to ensure maximal stability. But hey, I hear you say, I work in a large highly regulated institution that isn't anywhere near capable of doing the aforementioned approaches (yet). Where does one start? How does one's organization go from what is old school and intuitive to what is now possible?

## Where to Start: Engineering Organizations

Modern software has the fortunate characteristic of being easily modifiable, rebuilt, and deployed, at will. Unfortunately, this is not so with many organizations. Change is difficult in large organizations. Adopting new procedures and processes can be a several year endeavour. So how can we be confident our approach is the right one before dedicating ourselves to the arduous task of pushing for change? I find it curious that when it comes to building complex systems like satellites, or networks, we incorporate all the mathamatical and engineering rigour we can muster to great results. When it comes to organizations we often seem to settle for hand wavey justifications based on beliefs or experience. This is not sufficient. If we have the tools to design robust global networks and complex systems like satellites, why can we not apply the same rigour to properly engineering organizations?

In order to guide difficult decisions I find it best to identify a basic axiom and apply it to the world. If you have picked a good, simple, and reliable, axiom then when the axiom does not align with a given situation or circumstance, change the situation -- not the axiom.

My axiom for how we should engineer our organizations is the below case where I submit that a series network is less reliable than a parallel network (assuming an equal reliability for each node), and we will use this simple (and proveable claim) to redesign our approach to solving problems within our organizations.

_Both images borrowed from [Design Reliability - Fundamentals and Applications](https://www.amazon.com/Design-Reliability-Fundamentals-B-S-Dhillon/dp/0849314658)_

![A Series Network]({{site.baseurl}}/assets/images/seriesnetwork.PNG)
reliability = _1-(1-r^n)_

![A Parallel Network]({{site.baseurl}}/assets/images/parallelnetwork.PNG)
reliability = _1-(1-r)^n_

_For a quick hand wavey demonstration, assuming each node has an identical reliability of r and assuming r = 0.9, then_

_Series Network_ = 1-(1-0.9^2) = 0.81

_Parallel Network_ = 1-(1-0.9)^2 = 0.99

_We see here that the parallel network becomes more reliabile with each added node, while a series network becomes less reliable_

In the [above section](#CurrentSituation) we identified a common situation where an intuitive set of steps was taken in order to address a problem. Looking at that same situation again, which kind of network have we just created? Unfortunately, a series network. To make matters worse, we ensured that "all teams must go through team X in order to ensure said process". If the process is indeed solving a problem, or addressing a need, many teams within the department are going to want to go through this process. As demand increases, by design, there is nowhere else for the organization to turn. You must wait, or go rogue (which, if you have processes like these, many more people are already doing than most organizations would be comfortable admitting). As demand increases, the load on the team grows, queues begin to form, and then processes within processes emerge, each with their own overhead. For example, in order to triage requests by priority big ticket items bump small tickets, which results in many small simple requests waiting years to get through the process. From the perspective of a user this process is peculiar, as even small requests seem to get caught up in this bottle neck as the small requests get consistently bumped in priority for big ticket items, all the while the overworked team responsible for this process is desparately trying to cope with all of the tickets alonside an avalanche of dissatisfied internal clients asking about the state of their tickets.

When everything, including small repetitive tasks, need to be done manually by humans the appeal for one process which everyone can follow without variation has an undenyable appeal. Simplicity, repeatability, and therefore deterministic. This of course does often not turn out to be the case. As the number of requests continue to climb new teams are formed responsible for some subset of tasks that the initial team used to be responsible for. We've not introduced more overhead, plus an arbitrary (at least as far as the clients are concerned) assignment process where one group has their SOPs (standard operating procedures), while the second team has their own. Now seemingly identical requests (from the clients perspective) seemingly get evaluated differently. Two very similiar requests get submited, each gets routed to a different team, and the result is that two simimlar requests get treated differently -- not particularly deterministic or simple, is it? The issue here is that to fix the problem of too much traffic, the organization opted for [toil](https://landing.google.com/sre/sre-book/chapters/eliminating-toil/).

So _do_ we do? Creating the process didn't work. Creating new teams to assist with the process didn't work. What to try next? Create parallel networks.

One of the strengths of automation is that these "small easy requests" that get backed up in the queue described above can often be easily automated, or at least some subset of them can be. The answer then, is to address the low hanging fruit and create an automated processes. What would our network look like now, and what would its reliability be?

Below is the intuitive process we have defined above looks something like this

![An example process]({{site.baseurl}}/assets/images/simpleSeriesProcess.png)

Let's assume the capacity for this process is 100 requests per year (only because 100 is an easy number to work with). Assuming a reliability of 95%. This number is likely accurate, bordering on generous. For example, please refer to some of the digits referred to [here](https://backend.orbit.dtu.dk/ws/portalfiles/portal/10626190/Report_on_HRA_for_Banedanmark_v_2_02_Final_Issue.pdf) or [here](https://www.lifetime-reliability.com/cms/tutorials/reliability-engineering/human_error_rate_table_insights/), though there are many human reliability data banks available to confirm this value. Keeping in mind that each 'request' likely involves many different steps, each of which have a likelihood of failure.

Using a 95% reliability for each node gives us a reliability of

_Series Network_ = 1-(1-0.95^7) = 0.698 ~= 0.7

Meaning if that we put 100 requests through this process, we expect that roughly 70% will be completed successfuly on the first try. In all likelihood, failed requests in this circumstance will either be rejected, or have to re-enter the process at some particular step, increasing the load on the process without increasing its efficiency as some of the 100 requests being processed will actually be the same request twice. Given that, 70 successful requests is generous, as we are assuming we are not substracting from the 100 for requests that needed to be processed twice.

![First Attempt: Parallelized]({{site.baseurl}}/assets/images/firstparallel.png)

In this model we are able to process the initial load (70 items), however we also have a parallel approval process able of addressing some subset of requests -- the low hanging fruit. For the sake of this article, let's assume that 10% of tasks fall into the category of low hanging fruit that is easily automatable. If that is the case, and assuming a modest 70% efficiency (that is to say, we are assuming our automated process is equally as reliable as our manual one), then we are able to successfully process another 7 (70% of 10 = .7 * 10 = 7) requests. Again, this is an extremely conservative estimate of the gained efficiency, given that the automated tool should be able to respond with approval or rejection within minutes, while the manual process likely takes weeks or months. Therefore, if we assume that we're measuring the number of approvals over some given time *t\*, we could safely (still conservatively) double the number of requests processed by the automated process, giving us 14 successfully approved requests. Though even ignoring these conservative increased efficiency estimates, we can see that with our parallel process we are able to process strictly greater than 77 (70 from the initial process, an 7 from the automated one) requests, rather than our previous 70 requests. Why were we able to keep the initial process processing 100 requests, then 7 requests were sent to the automated process? A few reasons.

Firstly, when our processes are slow, arduous, and frustrating to our users, our users will stop using the process and just do what they need to do to get their job done. Compliance is a bonus for someone just trying to get work done. Their first and foremost goal, which will almost always take priority, is just getting the job done. That is to say, the process becomes more efficient you will get a better idea as to the actual activities of your department, as people will start using the official processes, resulting in more requests, and therefore better metrics organically collected from your organization.

Secondly, as we defined in our moch process, this is the one funnel for all processes. Small tasks are getting bumped for high priority ones, meaning there is a long queue of requests waiting to be processed. As the process becomes more efficient one becomes to process extra requests that would have otherwise be waiting in the queue.

The last observation here is that another added bonus of this new process is that by reducing the load on the manual process, the stress on the people responsible for the initial process is reduced, which will likely increase the reliability of the process or system. The queue still exists, so stress is not entirely removed, though as the queue of small ticket items gets reduced, the stress of an ever increasing number of requests diminishes, and the reliability of the system increases.

![Human performance vs stress]({{site.baseurl}}/assets/images/stressreliability.PNG)

As a result, we can bump up our reliability of the initial system due to the decreased stress, and therefore increased reliability.

_Series Network_ = 1-(1-0.96^7) ~= 0.75

Then we can add our 7 extra requests approved through the automated process (75 + 7), giving us 82 successfully processed requests. That's better! By addressing the low hanging fruit using a non-toil approach, we were able to bump up the number of successsfuly processed requests from 70 to 82, that's ~17% increase in productivity. This is easily anecdotally verifiable. If one goes to talk with their operation teams responsible for filtering or approving software, it doesn't take long to hear something along the lines of, "we would like to do more thorough checks, but we just don't have the time". What you are hearing there, is that the reliability of the process is reduced because the system is overstressed (for those of you who are mathamatically inclined and interested in learning more about stregth vs stress it is discussed in chapter 10 of [Design Reliability - Fundamentals and Applications](https://www.amazon.com/Design-Reliability-Fundamentals-B-S-Dhillon/dp/0849314658)).

Keep in mind we are able to [continually improve](https://sara-sabr.github.io/ITStrategy/2019/10/15/case-continuous-improvement.html) our automated process until it is able to process much more than our initial iteration of 10%.

One may critisize that in our model the manual process must go through committee approval while the automated process does not. Firstly, we reduced the efficiency of the automated process to the same as the manual process, so we can assume that each step of the automated process is 95% and that there are similar steps involved as the manual process. So not unfair advantage was given. However, it was drawn this way to underline an important point. If we want to achieve the Chaos Monkey situation discussed previously, or the thousands of changes to production a day by Amazon, we must be able to _fully automate_ our processes, from start to fininsh, without requiring human approval for each change. Mark Schwartz acknowledges this challenge in [War & Peace & IT](https://itrevolution.com/war-and-peace-and-it/) by explaining

> ... there are also tensions between moving quickly and retaining control, between improvising and following a plan, and between the creation of new competitive advantages and the destruction of old ones. These opposites seem impossible to reconcile; it is war, with brief periods of peace as temporary accommodations are reached.

Fully automated processes are a long way away for many of us. Though small low risk subsets of existing processes is the best place to start. Design the automated process in such a way that it can be approved by the committee, given that it will be truly deterministic. The committee approves the automated process, the committee does not approve each approval from the process. This prevents the creation of queues (where much time is lost) and moves us towards being able to more quickly process requests in an automated fashion, allowing us to more quickly respond to change (as is promoted in the [agile manifesto](https://agilemanifesto.org/iso/en/manifesto.html)).

Alright, 70 to 82 (17% increase). That's a start, but we can still do better.

## Working in the Open

[War & Peace & IT](https://itrevolution.com/war-and-peace-and-it/) Mark Schwartz quotes Christopher Avery's book _Responsible Change_ while discussing that "we must understand that we’re dealing with a complex system, where changes in one location might have unpredictable effects in another."

> We can never direct a living system, only disturb it and wait to see the response. . . . We can’t know all the forces shaping an organization we wish to change, so all we can do is provoke the system in some way by experimenting with a force we think might have some impact, then watch to see what happens.

Armed with this knowledge, we shall leverage working in the open to increase the reliability of our processes, and allow for continuous improvement of said process.

Step 1: Make all documentation relating to the process open to everyone
Step 2: Allow users to fill in the documentation on behalf of the teams responsible for the process

- Optionally, the teams can maintain responsibility for "signing off" on the documentation filled out by the client, although ideally one should opt for a trust over control option.

Step 3: Committee approves the request

What are the advantages of this approach?

**1 - It forces those responsible for the process to document their own processes thoroughly so anyone would be able to complete the checks.**

**2- It enables your clients to understand the process**

This aligns well with the [Agile Manifesto](https://agilemanifesto.org/iso/en/manifesto.html) which reads

> Individuals and interactions over processes and tools

Furthermore, the organization has many more skills at it's disposal than any individual team. Perhaps the expertise required to improve this process exists somewhere else within the organization. By exposing the process, and when coupled with continuous learning, would allow teams to help improve the process (even if entirely out of self interest to help them get their own requests through quicker). Keep in mind that people within the organization can only improve a process they understand, which is why it is important that the group(s) presently responsible for the process document their own processes thoroughly (as per number 1 above).

For more on working in the open, I suggest the following blog, [Working in the Open: Part 1](https://sara-sabr.github.io/ITStrategy/2019/11/19/working-in-the-open-part-1.html)

So how does this approach assist us with making our processes more reliable? Let's take a look. Our process would now look something like this

## Closing Thoughts

## References

- [Brave New Work](https://www.bravenewwork.com/)
- [Design Reliability - Fundamentals and Applications](https://www.amazon.com/Design-Reliability-Fundamentals-B-S-Dhillon/dp/0849314658)
- [War & Peace & IT](https://itrevolution.com/war-and-peace-and-it/)
