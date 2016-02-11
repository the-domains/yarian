---
inFeed: true
hasPage: true
inNav: true
inLanguage: null
starred: false
keywords: []
description: ''
datePublished: '2016-02-11T17:09:38.278Z'
dateModified: '2016-02-11T17:09:34.591Z'
title: What makes API Testing special?
author: []
sourcePath: _posts/2016-02-11-what-makes-api-testing-special.md
published: true
authors: []
publisher:
  name: null
  domain: null
  url: null
  favicon: null
url: what-makes-api-testing-special/index.html
_type: Article

---
The threshold for entry into API testing is often quite high, especially for testers new to the field. Many newcomers think of APIs as just the libraries used by programs. In reality APIs include any specification defining computer-to-computer interaction.

## Overview

Let's start with a brief overview of the technology to try and clarify some of the misconceptions out there. Most Web applications lend themselves very well to the classic three-tier architecture model.

In this model, the entire application is separated into three parts: the data tier, the logic tier, and the presentation tier. Under ideal circumstances none of the tiers know anything about the platform, technology, or structure of any of the others.

Any one tier can easily be swapped out as new development (or test) needs arise. Further, it is quite common that each of these tiers runs on a different server, or in the case very large applications on different server nodes each with its own load balancers, firewalls, et c. 

If this model is strictly adhered to, then test automation becomes simple: any of the tiers can be replaced with yourchoice of a test tool. If during development, the boundaries between the tiers start to blur, testing (as well as future enhancements to the application) becomes more difficult. This is one reason why you always want to get testing involved in the design process as early as possible.

The logic tier is the API. This is where all of the business logic belongs, and if that is the case then this tier alone makes out the entire API. In certain cases, the logic tier of your application has more complexity, and it is not uncommon that multiple technologies (web server, message queue, et c) will make up this tier.

## Challenges

An API is an interface intended to be interpreted by a computer. Since the interface boundary has to be technology agnostic, the inputs and outputs are normally text-formatted messages. Text messages may be easy for a human to read in order to interpret the inputs and outputs, but in-depth knowledge of the internals of the application is required to sufficiently test it.

This is the difference between black-box testing and white-box testing. In black-box testing, the tester is only concerned with the functionality of the overall application, exercising only the inputs and checking the outputs. 

In white-box testing, the tester is much more concerned with internal operations of the application, exercising the individual paths the data can travel through the application. 

API testing normally includes only the white-box testing approach.

Another difficulty is that testers are used to working from a set of provided business requirements. However, business requirements normally describe use cases at a fairly high level, and do not go down to the level of individual application functions. 

It is not unusual that business analysts are not even aware of low level detail and the amount of granularity that everything has to be broken down into, and are not aware that software is able to be tested at this level. 

Typically, project managers are not concerned with assigning time specifically to developing a rich and detailed API, let alone testing it. Paradoxically, if everything is done correctly, the API is the only place where business rules are coded and enforced. The end-user GUI only displays results and any error messages provided by the API.

Sadly, because of the above problems, developers are often left with testing their own code, if there is any testing at this level at all. And due to time pressures, unit tests often only glance at the positive tests -- the happy path -- and more in depth testing is left until later in the project. 

Of course, looking at only the positive paths through the application is not really testing, but only checking that the software fulfils business requirements under the most optimal conditions (see the articleWhy Test?). 

The GUI usually exposes only part of the overall functionality and by design testers are not able to go really deep into the application code, especially when it comes to testing all the negative test cases. This leaves the internals of the application possibly exposed to all sorts of breakage and attacks by end-users, accidental or malicious.

Lastly, there are situations where the API is the final product -- a public API. A simple Internet search will reveal there are thousands of public APIs for anything from GPS and mapping solutions to locating a radio station that is playing your favourite song right now. However, these APIs expose functionality that the developer hopes or thinks other developers/ users will want. In this case, the tester's role needs also to include a user advocate role, to make sure the offering is complete -- everything that any user may need is all there. This is in addition to the multitude of hats, the tester already wears: functional testing, security testing, load testing, et c.

## API Hierarchy of Needs

An excellent guide to follow in this case is theAPI Hierarchy of Needs. The guide is presented as a hierarchy:

Starting from the bottom: 

1. Usability - Is it easy to set up?
2. Functionality - Does it work as expected / documented?
3. Reliability - Is it "reliable" over time?
4. Proficiency - Does it increase the developer's skills?
5. Creativity - Can it be used in new ways?

## Advantages

Putting more effort into API testing leads to a much healthier final product. Ensuring that all data access (read and write) goes only through the API significantly simplifies security and compliance testing and thereby certification, since there is only one interface. 

Ensuring that all the required business rules are being enforced at the API tier allows time for much more complete user-experience tests once the UI is released, and not having to concentrate on testing every single business rule and path through the application near the end of the project. Ensuring that the API offers complete functionality allows for easy future expansion of the application as new business needs arise.