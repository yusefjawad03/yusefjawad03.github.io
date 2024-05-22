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

**Here is some bold text**

## Here is a secondary heading

[This is a link to a different site](https://deanattali.com/) and [this is a link to a section inside this page](#local-urls).

Here's the four components:

| Modules | Description | 
| :------ |:--- |
| Container Manager | Uses the kernel API and your container-specific extensions to the kernel, which creates and manages new containers. | 
| Shared Memory | memory support for communication between the CM, and the processes that are using the CM’s container support (e.g. dockv6). | 
| Synchronization | provide synchronization on a shared buffer | 
| Scheduler | adds multiple priorities, and schedule the highest priority thread at any point in time. | 

## Sumamry {#local-urls}

When hosting a *project site* on GitHub Pages (for example, `https://USERNAME.github.io/MyProject`), URLs that begin with `/` and refer to local files may not work correctly due to how the root URL (`/`) is interpreted by GitHub Pages. You can read more about it [in the FAQ](https://beautifuljekyll.com/faq/#links-in-project-page). To demonstrate the issue, the following local image will be broken **if your site is a project site:**

![Crepe](/assets/img/crepe.jpg)

If the above image is broken, then you'll need to follow the instructions [in the FAQ](https://beautifuljekyll.com/faq/#links-in-project-page). Here is proof that it can be fixed:

![Crepe]({{ '/assets/img/crepe.jpg' | relative_url }})
