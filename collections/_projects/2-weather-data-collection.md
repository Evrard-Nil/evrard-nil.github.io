---
layout: page
menus: header
title: Weather data collection
thumbnail: liyo.jpeg
---
Weather data collection
======
***

As a learning project, we built an application simulating the generation of data from IoT sensors in airports sending information about wind speed, atmospheric pressure and temperature. Goal was to use a *MQTT broker* and *Redis* database and learn more about *Golang*.

![post-picture](/assets/img/posts/weather-data-col-arch.png)

We were a team of 4 persons to develop this application, we choose to organise ourselves according the following:
- One of us developped the sensors
- One of us developped the redis subscriber
- One of us developped the csv subscriber
- One of us developped the REST server

Then the first of us to finish its initial task, would take on the UI. Afterward we did a big phase of refactoring because of course of lot of code could be shared, especially regarding the connection to the broker and *Redis*.

To launch the application we worked on a docker compose approach, which would set a container for each component of the application. It might seems overkill, and it is, but I really wanted to see docker compose's possibilities.