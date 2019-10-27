---
layout: page
menus: header
title: Green IT Study
thumbnail: green-it.jpg
---
Green IT Study
======
***
*Icon photo by Andreas Gücklhorn*

As a final project for our first year at *IMT Atlantique* we studied energy consumption with a micro-services designed back-end. We used *Hipster Shop* a cloud native micro-services demo made by *Google*.
We wanted to show that dynamic change in services could impact energy consumption and availability of service.
**This study was then used by a full-time researcher working on infrascture management at Sigma.**

![post-picture](/assets/img/posts/architecture-diagram.png)
*Diagram from github.com/GoogleCloudPlatform/microservices-demo*

To do so we decided to emphasize the study on the recommendation service because it suits well the role of the service that can consumes a lot of energy but can be degraded. For example, an online shop invests a lot on this kind of service because it can really increase the amount of thing buyed by a single user. So the idea was, let's say we have two implementation:
- One energy intensive, for example a machine learning based algorithm for recommendation. In our case, simulated by a calculus of the beginning of Fibonacci suite.
- One more efficient, for exemple tag based association. In our case, simulated with a random generator of product ID.

When you have green energy available or little traffic you want to use the best of your implementations, the energy intensive one, but when the traffic increases and the time to respond goes up, you may want to switch implementations.

This project allowed us the better understand micro-services design and *Kubernetes*.
