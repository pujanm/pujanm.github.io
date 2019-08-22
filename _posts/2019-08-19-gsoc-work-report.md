---
layout: post
title: Google Summer of Code 2019 - Work Report
image: /img/gsoc_logo.png
tags: [GSoC, CERN, DIRAC, Python, Software Development]
author: Pujan Mehta
---

I have been working on **The DIRAC Project** as a part of my **Google Summer of Code 2019** project since the last 3 months and it has been an amazing journey throughout which I would like to explain through the work I completed during this period.

![GSoC 2019 Cover Image by Pujan](/img/GSoC_merged.png)

Now I would like to showcase the changes I made to the code base in accordance with the tasks:

**1) Setup DIRAC locally:** <br>
This was a challenging task for me as I was not much familiar with the DIRAC codebase and setup and I was not knowing the system's internal working, meaning how to run services, how to stop them, etc.
So while working on this I came up with a **Docker-Compose** setup for DIRAC which was liked by my mentors and it turned out to be very helpful for development purposes and till date throughout my project period I used this setup. This setup contains three different containers namely one for DIRAC code and other dependencies, one for ElasticSearch, and the other for MySQL database and all these containers can interact with each other and we can also use volume mounts for changing the code.
This was my first contribution to DIRAC and the Pull Request on this can be found **[here](https://github.com/DIRACGrid/DIRAC/pull/4085)** which was merged.

**2) Wrote Technical documentation on the gMonitor object:** <br>
In this task, I had to write technical documentation on **DIRAC's gMonitor** object which uses **Round Robin Database** tool to monitor activities of various components within DIRAC.
The work on this can be found in these **[commits](https://github.com/DIRACGrid/DIRAC/pull/4120/commits/6564f40ac953dc451066b7c01cf304952af5ea6e)** inside this [Pull Request](https://github.com/DIRACGrid/DIRAC/pull/4120) which has been merged.

**3) Added ElasticSearch support to DIRAC's Service component:** <br>
Starting with this task, I had to extend an existing ElasticSearch type named `ComponentMonitoring` which had few fields already being monitored. So based on studying DIRAC's Service component I extended this type and added new key fields and monitoring fields.
Then next in this task, I had to migrate entire Service component such that we can configure it using a flag and users must be allowed to use ElasticSearch or gMonior object based monitoring for which I used **DIRAC's Configuration System** and made everything flag enabled.
After this I started working on extending the existing plotter named `ComponentMonitoringPlotter` and added the new fields so that we can create various plots on these fields using the **WebAppDIRAC** which is DIRAC's WebApp module.
Then I created a regression test for this plotter which was used to enure the proper working of the plotter. <br>
This is a sample plot on usage of File Descriptors by various DIRAC Services:<br>
![Sample plot of MaxFD](/img/maxFD_ComponentMonitoring.jpg)
<br>
<br>
**Below is the list of commits made which are based on the above described work and inside this [Pull Request](https://github.com/DIRACGrid/DIRAC/pull/4120):** <br>
1) Commits on extending the ES type and migrating the Service component can be found here in [commit1](https://github.com/DIRACGrid/DIRAC/pull/4120/commits/0aed45b2527aa7bb940ee6b3f674cea80e0f71c9) and [commit2](https://github.com/DIRACGrid/DIRAC/pull/4120/commits/f025d506154c4416f69a62b27f28edd2780b97ec). <br>
2) Work on the plotter is inside this [commit](https://github.com/DIRACGrid/DIRAC/pull/4120/commits/4f358e5d241c31d18bd06ff576361566b341408c). <br>
3) The regression test was added in this [commit](https://github.com/DIRACGrid/DIRAC/pull/4120/commits/8274ec3b05136dd16ff6bb2052bfe59cb7ad2409). <br>

**4) Performance test:** <br>
In this task, I ran the existing performance test which is based on **multi-mechanize** and ran it  once with monitoring based on **gMonitor** object and once based on **ElasticSearch**.
The results and notes on this can be found at this [Google Docs link](https://docs.google.com/document/d/17bU507piVlNr-_vob3T4o_HiJyZ0lFNsAu67V5ec2R4/edit?usp=sharing). <br>

**5) Worked on a use case and did migration of DIRAC's Agent component to ElasticSearch:** <br>
First, I worked on solving a use case about which can be found [here](https://github.com/DIRACGrid/DIRAC/issues/2138). In this use case, basically I had to work on sending the response time of a service to the ElasticSearch backend.<br>
Work on this use case can be found inside this [commit](https://github.com/DIRACGrid/DIRAC/pull/4120/commits/0933da551c408ead6caf3480d1c2cc3059a53fae) and I also added a plot for this new field which can be found in this [commit](https://github.com/DIRACGrid/DIRAC/pull/4120/commits/e919cfe7b80dcae3e88372e26e972c349f4cfcce).<br>
Then I worked on migrating the **AgentModule** to ElasticSearch and the work on this can be found in this [commit](https://github.com/DIRACGrid/DIRAC/pull/4120/commits/b6d851741ba5cfe22cca78be8358dae51b3723cd).<br>
Apart from this I worked on this small [issue](https://github.com/DIRACGrid/DIRAC/issues/4193) where I had to make the `MonitoringReporter` thread safe which is used to send data to the ElasticSearch backend, the work on this can be found here in this [Pull Request](https://github.com/DIRACGrid/DIRAC/pull/4194).<br>

**6) Added ElasticSearch monitoring support to RequestManagementSystem and DataManagementSystem/Agent/RequestOperations/:**<br>
In this task, first I had to study the use cases of **gMonitor** object inside `RequestManagementSystem` and `DataManagementSystem/Agent/RequestOperations/` and then I had to work on designing an ElasticSearch type such that all the use cases of gMonitor object are encompassed which was a challenging task for me and I took some time in this but was later able to design it with inputs from my mentors.
After creating this ElasticSearch type I started migrating the two systems to support the new system and again made things flag configurable and also created a new plotter for this new type.<br>
A sample monitoring plot after migration to ElasticSearch:<br>
![RMS, DMS Plot](/img/RMS_Monitoring_plot.jpg)
<br>
Some work on this is in progress and all the work till now can be found in this [Pull Request](https://github.com/DIRACGrid/DIRAC/pull/4209).
<br>

Summarising things, all the major work I did during the GSoC 2019 period can be found in these two Pull Requests: [PR1](https://github.com/DIRACGrid/DIRAC/pull/4120) and [PR2](https://github.com/DIRACGrid/DIRAC/pull/4209).<br>

Lastly, I would like to thank my mentors **Christophe Haen**, **Zoltan Mathe**, and **Federico Stagni** for their constant support, inputs, and help throughout the period. I got to learn a lot of things from them and they also helped me highlight my weaknesses and mistakes I made during the period.
Overall, it was a very good experience working on **The DIRAC project** and I even look forward to contribute to DIRAC after the GSoC period ends.