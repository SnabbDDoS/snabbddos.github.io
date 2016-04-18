---
layout: page
title: Frequently Asked Questions
permalink: /faq
---
#### Q: Can I run SnabbDDoS in production?
No. It is not mature and we are aware of limitations that will lead to crashes.
They need to be addressed before this thing can be put in production in any
network.


#### Q: How fast is SnabbDDoS?

In loopback mode, without any NICs involved, it currently does 23Mpps on a
single core on my dev machine that has an i7 CPU. It should scale close to
linearly with more cores, although CPUs with more cores usually run at a lower
clock rate per core.

With a modern dual socket Xeon at 10 cores each you should be able to do 20x10G
or even more. Make sure you get NUMA correct!


#### Q: Why use the Snabb framework?

It's kind of cool writing packet processing code in Lua. Also I suck at C so
this seemed like an easy way forward. VPP would be the other choice, although
it wasn't publically available when the first version of SnabbDDoS was written.


#### Q: Can it do 100GE?

Nope. First of, the Snabb framework uses its own drivers and there are no
drivers for any 100GE cards. Once that is solved, Snabb still suffers from the
one-core-per-NIC limitation but this is being worked on as well with support
for RSS so the NIC can hash traffic over multiple cores.


#### Q: Is hashing really good for DDoS style traffic?

Well, it's certainly possible to exploit such a weakness but given that most
DDoS mitigation equipment vendors, including the self proclaimed market leader
Arbor, does this I suppose we should be fine.
