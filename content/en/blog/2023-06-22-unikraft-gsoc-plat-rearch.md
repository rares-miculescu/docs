+++
title = "re:Arch Unikraft"
date = "2023-06-22T18:00:00+03:00"
author = "Rares Miculescu"
tags = ["GSoC'23", "plat re-arch"]
+++

<img width="100px" src="https://summerofcode.withgoogle.com/assets/media/gsoc-2023-badge.svg" align="right" />

## About Me

I'm [Rareș Miculescu](https://github.com/rares-miculescu), a second year bachelor student at [University POLITEHNICA of Bucharest](https://upb.ro/en/).
This is my first open source project that I am part of, and I love it.
Outside Unikraft and university, I am obsessed with cars and Formula 1.

## GSoC'23: re:Arch Unikraft

### Motivation

Unikraft provides specialization and strong modularity by strictly following the "everything is a library" concept.
Despite this concept, Unikraft requires architectural changes that can optimize and clearly define drivers and platform support, and in doing so, reduce maintenance effort.

### Summary of Objectives

The goal of this GSoC'23 project is to optimize and clearly define drivers and platform support.
This can be achieved by solving the tasks from [the `Platform Re-architecting` GitHub project](https://github.com/orgs/unikraft/projects/36).

The main tasks are:

* [Move register definitions into `arch/`](https://github.com/orgs/unikraft/projects/36/views/1?pane=issue&itemId=15412393)

* [Replace libc data types with Unikraft-specific data types](https://github.com/orgs/unikraft/projects/36/views/1?pane=issue&itemId=19037961)

* [Migrate `plat/drivers/` into `drivers/`](https://github.com/orgs/unikraft/projects/36/views/1?pane=issue&itemId=23820110)

* [Introduce `drivers/boot-entry`](https://github.com/orgs/unikraft/projects/36/views/1?pane=issue&itemId=23821458)

After completing these, I will focus on other tasks.

### Progress

So far, I managed to move the register definitions from `plat/x86` into `arch/x86`.
We are making the final touches on replacing the libc data types.

### Next Steps

The next steps will be to finish the [PR for the replacement of libc data types](https://github.com/unikraft/unikraft/pull/954) and start working on migrating the drivers.
