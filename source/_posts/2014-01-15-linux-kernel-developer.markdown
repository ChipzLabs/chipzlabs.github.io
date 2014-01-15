---
layout: post
title: "Linux Kernel Developer"
date: 2014-01-15 05:20:49 +0700
comments: true
categories: 
---

This page is originally titled KernelDevViewPoint
from url: http://kernelnewbies.org/KernelDevViewpoint

##What is a kernel developer?
There are several ways to contribute to the Linux kernel, and become a Linux kernel developer. Some kernel developers contribute to one particular driver or subsystem (e.g. real-time scheduler, USB, or PCI). Other developers contribute to many subsystems.

A kernel developer usually contributes both code and documentation to the Linux kernel. As kernel developers become experts in their particular subsystem, they contribute to patch review on the subsystem mailing list. Eventually, they may become the maintainer of a particular driver. At that point, they test and sign off on patches to the driver, and send them off to the subsystem maintainer in a pull request. Linus Torvalds merges pull requests from those subsystem maintainers.

##Do Linux kernel developers get paid?
Many contributions to the Linux kernel are done by hobbists and students. Some kernel contributors are contractors hired to work on the Linux kernel. However, most of the top kernel maintainers are employed by companies that produce Linux distributions or sell hardware that will run Linux or Android. See the Linux Foundation's annual kernel report for which companies are top Linux kernel contributors.

In 2012, the demand for experienced Linux kernel contributors was far greater than the number of applicants to job opportunities. Being a Linux kernel developer is a great way to get paid to work on open source.

##Where do kernel developers work?
The Linux kernel community is spread across the whole world, so most of our communication is done through mailing lists and IRC. That opens up opportunites to work remotely, which is great for work/life flexibility. However, many kernel developers also prefer to go into their employer's office and work from there, especially if they need access to hardware prototypes or if they need to bounce ideas off their co-workers face-to-face.

##What do kernel developers do every day?
We joke that a kernel developer's day is filled with email, email, and more email. It's true that much of the day is spend communicating with other kernel developers via email. We'll go back and forth throughout the day on patch review, responding to bug reports on the mailing lists, and responding to our internal company email. We also develop new code for features and bug fixes, test them on our development machines, and brain storm solutions with our co-workers. Many kernel developers work with their company's hardware and specification architects to ensure the next generation of hardware works well under Linux.

Linux kernel developers who work for hardware vendors often have to deal with broken software and broken hardware at the same time. The firmware (BIOS/ACPI) is often broken as well. Having knowledge of what's happening on both the hardware and software level is key to debugging issues on these systems. Patience and creativity is also useful when debugging these systems.

##Do kernel developers work 24/7?
Some kernel developers (especially hobbists) may only work on Linux on the weekends. Many top kernel developers are employed at companies, so they work pretty standard 9 to 5 hours. However, since Linux is a passion for those developers, many of them respond to kernel email at odd hours (late in the evening, on the weekends, etc.). When a regression report comes in (especially during the merge window), we may drop everything else to focus on fixing that.

##Do you ever see remote kernel developers?
Linux kernel developers get together several times a year, during the many Linux and open source conferences. Conferences are a great way to hash out architectural details, talk about new features that will need to be worked on, and generally network with fellow kernel contributors.

##What skills do kernel developers need?
Since we spend most of the day communicating via email, Linux kernel contributors should have good english language communication skills. You not only need to know the language, you need to know how to be persuasive and communicate your intentions clearly. Being a good coder does not necessarily make you a good kernel developer. You need to know how to explain why you changed the code, what was broken in the code before, and persuade other developers that your feature is useful enough to justify the code change.

Contrary to popular belief, kernel developers rarely need to know math at the calculus level. You need to be good at basic arithmetic and you must know boolean algebra to work on device drivers.

One skill that many kernel developers learn on the job is the ability to build state machines in your head of what the code is doing. It helps to be able to mentally (or on paper) work out race conditions between two or more threads of code. This is something that only comes with practice, reading lots of code, discussing race conditions with other developers, and dealing with bug reports where your internal model of the code is challenged.

Many kernel developers are particularly meticulous about their code development. We don't want to waste time discussing trivial mistakes during patch review, since getting someone to review a patch can take days or even weeks. To avoid wasting time, we will carefully make sure the code compiles and doesn't introduce new warnings, conforms to our coding style standards, and finally, we'll test the code on multiple systems. You don't have to be a perfectionist to be a kernel developer, but it will help.

Technical skills for kernel developers include experience with the C programming language, and knowledge of git.

##Do I need a "tough skin" to be a kernel developer?
The Linux kernel community is very technically brutal when it comes to code review. We have a particular format that need your patches to be in, and newbies often get it wrong. You should look at the patch format of several different commits in the git history to get a feel for what format we're looking for. We also have a very high standard for coding style and the patch submission process. Luckily, automated tools like checkpatch will catch most of those simple mistakes, and let you avoid those critiques.

Subsystem maintainers can also be particularly picky when patches come in from a contributor that is new to their subsystem. Since they've never seen code from you before, they don't know what your coding skill level is, and they are much more likely to scrutize your code. Often, new contributors are held to higher standards than contributors who have been around for a while.

However, if you look at it from a maintainer's point of view, it makes sense. The maintainer knows you're a new person, and has no idea if you will stick around and fix bugs in the code you contribute. The maintainer is basically stuck with your code long-term, and so they need to both understand what your code is doing, and ensure it is correct. When code comes in from a long-term contributor, there is much more discussion about whether the idea is correct, and much less nitpicky code style review, because the maintainer knows the contributor will be around to fix any issues with their code.

One way to earn the maintainer's trust before submitting a big feature patchset is to submit smaller bug fixes first. That why the maintainers will know you are an experienced coder, you can work out any kinks in your patch submission process, and you can learn any subsystem specific coding rules before submitting your big patch. Asking questions and reviewing other contributors' code is also a good way to learning about the subsystem before you submit any code.
