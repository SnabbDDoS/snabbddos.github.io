---
layout: page
title: SnabbDDoS - Fast DDoS mitigation for all
---
SnabbDDoS is a DDoS scrubber built for dealing with large volumetric DDoS attacks. It runs on normal x86 hardware and is capable of handling millions of packets per second.

It implements an IP address blocking mechanism for sources sending packets matching a configured BPF expression exceeding a pps or bps threshold. It is very similar to the countermeasure that Arbor calls "Zombie Detection".

Experimental integration has been written for Arbor Peakflow SP, such that SnabbDDoS can parse the same configuration that is used for the Zombie Detection countermeasure in Arbor TMS.

A proof-of-concept integration has also been written for FastNetMon.


### Snabb

Snabb is a framework for packet processing and as hinted by the name, SnabbDDoS is built using the Snabb framework. Snabb is also the Swedish word for "fast", which is rather fitting.


### Free
SnabbDDoS is free and open source under the Apache 2.0 license. Feel free to contribute!


### Authors and Contributors
SnabbDDoS was originally written by Kristian Larsson (<a href="https://github.com/plajjan" class="user-mention">@plajjan</a>).</p>
