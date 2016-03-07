---
published: true
title: Zen of Architecture in 4 lines
layout: post
---
O'Reilly Webcast on [Strategic Approaches to Real-world Architectural Challenges](http://www.oreilly.com/pub/e/3672).

First talk was by Juval Löwy on the Zen of Architecture.

Crux was that 
1. Functional Decomposition is bad, since it makes re-use and re-factoring difficult.
2. Domain de-composition is better
3. Volatility based Decomposition is best. Since this splits architectural elements which are most likely to change.

Whilst functional decomposition is the simplest route, and can seem like the best way to deliver incremental software, you are making a rod for your own back. (i.e. not technical debt management friendly).

Functional Decomposition is also susceptible to solutions masquerading as requirements. i.e. requirement to send SMS, is really a solution on how to notify the end user. This could also be solved by sending an email for example.

Functional Decomposition can result in business logic being implemented in the client. This makes implementing new interfaces more expensive (i.e. adding a native app alongside an existing web interface) .


 