---
layout: slides
title: "Netflix and FreeBSD: Using Open Source to Deliver Streaming Video"
date: 2019-02-02
author: Jonathan Looney
email: jtl@FreeBSD.org
video: https://video.fosdem.org/2019/Janson/netflix_freebsd.webm
---
Netflix has built a CDN to distribute streaming media through most of the world. The content caches run a lightly customized version of the FreeBSD operating system. This presentation will describe how Netflix uses FreeBSD, and the benefits to both FreeBSD and Netflix.

Netflix has built a CDN, called Open Connect, to distribute streaming media through most of the world. According to Sandvine, Netflix accounts for approximately 15% of all downstream traffic volume across the entire internet. The content caches in the Netflix CDN, also known as Open Connect Appliances (or, simply, OCAs), run a lightly customized version of FreeBSD.

In some ways, this is nothing special: many products are based on an open-source operating system. However, Netflix does something slightly unusual, in that its OCA operating system code closely tracks the FreeBSD "head" branch (their development branch). In fact, a commit to the upstream FreeBSD development branch will usually be fully deployed across Netflix's CDN within 5-15 weeks.

The Netflix development team strives for monthly releases for the content caches. We try to synchronize the latest code from FreeBSD's head branch at least once during each monthly release cycle. We then test this code thoroughly before deploying it across the Open Connect network. It is common that we find at least some bugs; however, we are able to work with upstream developers to fix these while the commits are fresh in their mind. This early (and widespread) use of the code gives the upstream FreeBSD Project the benefit of quick deployment and validation of their development-branch code across a wide fleet of servers. Netflix gets the benefit of being able to quickly use new features, and of getting quick bug fixes.

Although it might seem scary to run "development" code in production, we find that it works very well in practice. The FreeBSD development branch is usually quite stable. Additionally, we expect that we will find some bugs. However, we find that it is much better to find and fix those sooner, rather than later. Also, Netflix is committed to upstreaming most of our customizations that have general applicability. Tracking the upstream development branch keeps us in the best position to easily upstream our changes.

In this presentation, Jonathan Looney will explain how Netflix uses the FreeBSD development branch code to help Netflix produce the robust operating system which supports the Netflix CDN, and the synergies Netflix and FreeBSD see through this use.
