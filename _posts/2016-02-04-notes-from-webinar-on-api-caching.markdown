---
published: true
title: Notes from Webinar on API Caching
layout: post
---
Webinar link is [here](http://www.oreilly.com/pub/e/3628).

Interesting talk by Sean Leach, CTO at Fastly.

Fastly are a CDN who specialise in Dynamic Site Acceleration.
They are keen users of Varnish which is better suited for Dynamic Site Acceleration (as well as API caching) than NGINX.

As well as reducing workload on Origin Servers belonging to customers they also provide origin shielding.

Optimisation for performance is provided, not only by caching, but optimising connections to Origin servers via the CDN to a local POP. This includes techniques such as hot connections.

He also described a number of useful tools such as [Redbot](https://redbot.org/about/) and Curl.

He also described some DDOS techniques and how they can help, as a CDN.