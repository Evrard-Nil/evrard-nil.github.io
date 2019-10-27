---
layout: page
menus: header
title: Styleguide
permalink: experience/sopra-steria
---
Software Engineer Apprentice
======
***

As part of my training in software engineering, I work half of the year at Sopra Steria a large european information technology company. My project works for a french public company called the CNAM(Caisse National d'Assurance Maladie) responsible for social security. The project, in which I am, built an infrastructure management solution based on *[Saltstack](https://docs.saltstack.com/en/latest/)* open source software. *Saltstack* allows to use *Infrastructure as Code* type of management for a very large amount of distant server. Its core function is parallel remote execution, built with *[ZeroMQ](https://zeromq.org/)*.


## Deployment
The project in which I work was initially created to reduce the duration of the development life-cycle, especially deploying new applications. The process was old and costly. Sopra Steria proposed a tool based on *Saltstack* to deploy in seconds multiple applications across the whole infrastructure with one command line. Concretly, it is a collection of [formulas](https://docs.saltstack.com/en/latest/topics/development/conventions/formulas.html), which are pre-written sets of instructions describing the state in which we would like to have our server. Coupled with a description of the infrastructure as a whole it becomes incredibly powerful.

## Automatic testing tool

Code quality is important. We are well aware of this and we are constantly trying our best to test everything. For exemple we have a code coverage by unit tests of **89.9%**. The problem is that testing deployment is hard. Most of it is done manually by developpers or testers, it is a boring and timely task. We already had an automatic testing tool based on *Kitchen* but it was not really well maintained and its fiability was decreasing with time. Furthermore, description and configuration of test cases were not in the same repositoty, which means that we had to first code our new feature, write the test in another repo and make sure the version were the same for the test repository and the main one. As soon as two features get developped at the same time it gets complicated. Additionnally, when things are crowding testing take second place and are sometimes not updated. 

Goal with this new tool was to make testing unavoidable by using Gitlab CI we would block merging of a new feature if it did not pass tests and we would now place testing configuration (tests cases and scenarios) within the main repo. 

In addition we built the new testing tool from scratch using *Python* and *Docker*. I was the main developper on this tool, I worked on it for about a month before having a MVP, and I was sometimes helped by another coleague. 
This new tool decreased testing time by more than **50%**.