---
layout: page
title: PC - what you need to run SnabbDDoS
permalink: /pc/
---

What do you need to run SnabbDDoS?

## NIC

SnabbDDoS is built on the Snabb framework so by and large it plays by the rules
of Snabb. Unlike many other VNF style applications that use DPDK, The Snabb
project has instead opted to write their own drivers. Let's not go into the
details of that more than to say that the selection of NIC drivers is a tad
limited with Snabb. Anyway, if you are serious about forwarding (or dropping)
packets with a PC you should have no problem investing in a good NIC or two.

You want the Intel 82599 based 10G card. They are available in multiple
different models, from single port to 4 port and with various media options.
Pick what suites your environment - as long as it's 82599.


## CPU

Snabb is currently single threaded and you are only able to bind one process
per NIC, effectively limiting one Snabb process per 10G, which also affects
SnabbDDoS. It's potentially possible to run multiple SnabbDDoS processes per
NIC by using virtual function (VFs) in the NIC. For example, one could setup 10
different MAC addresses for the NIC to listen to and each MAC address is mapped
to one SnabbDDoS process. The router would see these as 10 different
destinations and do ECMP hashing over them. For the time being, SnabbDDoS is
not intended to be deployed in such a way, instead we have optimised
performance such that it is possible to achieve close to line rate 10G
performance per CPU core.
