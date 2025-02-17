---
title: "Unikraft Reaches 1K+ GitHub Stars! (and 500 Discord Users)"
date: "2022-10-14T09:00:00+01:00"
author: "Felipe Huici"
tags: ["announcement"]
---

We're ecstatic to announce that a week ago Unikraft reached 1K stars on Github on its [main repository](https://github.com/unikraft/unikraft)!

First and foremost, a great many thanks to our fantastic open source community and anyone and everyone who has supported us, starred us and helped us throughout the years!
In addition, and as more-than-welcome coincidence, over the weekend we reached more than 500 Discord users; we are super happy to have you all on board!

{{< img
  class="max-w-2xl mx-auto"
  src="/assets/imgs/unikraft-1k-github-stars.png"
  caption="Unikraft Reaches 1K+ GitHub Stars"
  position="center"
>}}

As you can see from the stars graph, Unikraft has experienced rather healthy community growth in the past year or so, with a clear acceleration in the past months. We are really happy about achieving this milestone, and are looking forward to quickly reaching the next one thousand stars!

With that out of the way, we thought we'd take this opportunity to give a brief overview of where the project came from, its principles, and the exciting new developments and features we'll be releasing before the year's out, so please read on!

### Winding Back the Clock

About 4+ years ago we were having lots of fun building all kinds of research unikernels (specialized virtual machines) for network processing, content caches and Python worloads, to name a few. With these we were getting a fair amount of academic success and their potential was clearly large: millisecond boot times while retaining strong isolation, low memory consumption (hundreds of KBs or a few MBs), and high throughput. However, we were increasingly getting requests from companies about running a different application, or supporting a different virtualization technology; the answer, invariably, was that everything was possible given enough time (read: many months!).

It was becoming clear to us that a different approach was needed. Back then, there was no unikernel project that had high performance, efficiency and could support a wide range of applications. So we decided to build such a project from scratch, and to do so by going back to basics.

### The Unikraft Principles

From the beginning we wanted to make sure that Unikraft would allow for full specialization, that is, that the entire software stack running underneath an application, from the low level operating system code all the way up to the code that provides application compatibility, could be fully (and easily) tailored to that application's needs. To achieve this, one of the main architectural principles of Unikraft is that it be fully modular: everything in Unikraft is a library that can be included or removed from each build.

While several other unikernel projects had a small kernel (e.g., [OSv](https://osv.io/), [MirageOS](https://mirage.io/)), none of them were modular, so not very easy to customize and fully specialize. Beyond the architectural principle of being modular, there were three targets we wanted to achieve: 

 * **Performance**: those familiar with unikernels know about their high performance potential; in practice, many projects failed to deliver high performance (e.g., Rump).
 * **Application compatibility**: for Unikraft to be successful, we made it an explicit target to (1) be able to run unmodified applications and languages and (2) to run as wide a range of them as possible (more on this below). Many past unikernel projects (including some of ours) required application modifications, or could only run a single language, or sometimes only a single application.
 * **Security**: unikernels have been described as inherently safe due to features such as having a small Trusted Computing Base. Clearly this is not enough to have a secure operating system, and Unikraft is always targeting the implementation of industry standard [security features](https://unikraft.org/docs/features/security/).
 * **Arch and Platform Support**: we wanted Unikraft to be able to run on as many hypervisors, VMMs, CPU architectures and devices as possible: whether you're targeting KVM with Firecracker on an x86_64 server, Xen on ARM64 or running bare metal on an ARM-based embedded device, Unikraft  could be tweaked to cover all of these set-ups.

Since then we've been hard at work trying to achieve these targets, and we'd like to thank the OSS community for the amazing amount of progress over the past years. But enough with the past, let's look into the future!

### What's Ahead

As exciting as reaching the first 1K Github stars has been, we are even more excited about what lies ahead! These coming months we are putting particular emphasis on making the user experience as seamless as possible; this includes:

Full musl libc and binary compatibility support, to make it much easier to run a wider range of unmodified applications, languages and frameworks.
Docker/OCI integration, to allow you to take at least a few existing containers and automatically transform them into a Unikraft image.
Kubernetes integration, so you can seamlessly deploy Unikraft images.

This is of course not all: we are busy working on security features, additional VMM and hypervisor support, and many other exciting areas; check out our [roadmap](https://github.com/orgs/unikraft/projects/24/views/31) for more details.

Thank you for reading this far and please make sure to join our friendly community on Discord , or any of our upcoming [events](https://unikraft.org/community/events/) or [hackathons](https://unikraft.org/community/hackathons/). Comments, questions and any sort of feedback is greatly appreciated and can be sent directly to me at felipe@unikraft.io .
