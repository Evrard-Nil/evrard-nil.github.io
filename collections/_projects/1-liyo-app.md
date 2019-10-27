---
layout: page
menus: header
title: liyo
thumbnail: liyo.jpeg
---
Profile Picture Adviser - liyo
======
***

**liyo** is a mobile application allowing user to share and get feedback about its profile picture.

![post-picture](/assets/img/posts/liyo.jpeg)

We built it as a side project, with my roommates. We first wanted to learn about new technologies especially *micro-services* with *Kubernetes*. Because the goal was to learn, we choose to break down the back-end as much as possible. For the front-end we choose to work with *Flutter* because it offer the huge advantage of being cross-platform and still great performance. We already tried *Flutter* but we wanted to learn more about it.

## Back-end

Most of our services are built using *Golang*. To ensure communication between services we choose to work with *gRPC*, an open source framework using *HTTP/2* and *Protocol Buffer*. For the database we used *PostgreSQL*. One of the most interesting thing in building this kind of project from scratch is to think about how to design it to ensure scalability and make sure the choices made will still be relevant with the growth of the project. As it was the first time for us to work with *Kubernetes*, *Golang* and *gRPC* we surely didn't made the best choices but we will continue to improve our back-end as the project lives.

To host our back-end we went with *Google Cloud Platform*, we knew little about it but, let's be honest, the $300 credit was a pretty convincing argument for broke students. And to be fair, our deployment and back-end management has been simpler since then. 

We asked ourselves if we should have the database inside our cluster but we preferred to use Google Cloud Platform SQl instance.
## Front-end

For the front-end we decided to have 3 principal screens, the main one for the duel, one for the profile and last one for the leaderboard. We tried to apply best practices as much as possible. We used the *BLoC pattern* to keep our code base clean and organised. Furthermore, we tried to push the state to the leaves by using *reactive programming* principles.