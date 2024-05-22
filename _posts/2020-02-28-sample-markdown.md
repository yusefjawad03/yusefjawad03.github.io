---
layout: post
title: Implementing the core facilities for containers in xv6
subtitle: providing a subset of the functionality provided by software like Docker
tags: [C, xv6, kernel]
comments: true
mathjax: true
---

{: .box-success}
The main functionality of this project is that I implemented a container infrastructure for xv6 UNIX. I have linked the [github](https://github.com/yusefjawad03/project-23-xv6) for this project.

Here's the four components:

| Modules | Description | 
| :------ |:--- |
| Container Manager | Uses the kernel API and your container-specific extensions to the kernel, which creates and manages new containers. | 
| Shared Memory | memory support for communication between the CM, and the processes that are using the CM’s container support (e.g. dockv6). | 
| Synchronization | provide synchronization on a shared buffer | 
| Scheduler | adds multiple priorities, and schedule the highest priority thread at any point in time. | 

## Sumamry {#local-urls}

I integrated many aspects of OS design and implementation, from containers, to scheduling, to synchronization, to memory management, and file systems in xv6 OS. The core servers, logic, and
coordination facilities for a container environment are all dealt with in **xv6!**
