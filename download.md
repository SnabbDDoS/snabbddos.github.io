---
layout: page
title: Download SnabbDDoS
permalink: /download/
---
You can download SnabbDDoS to play around with. It's not mature enough for production.

Read about what kind of computer [is optimal for SnabbDDoS](/pc).

SnabbDDoS is only available as source code from GitHub and you compile it just
like you would compile anything written with Snabb;

```bash
git clone git@github.com:SnabbDDoS/snabb.git
cd snabb
git checkout snabbddos
make
```

The SnabbDDoS code is on a branch, aptly named `snabbddos`, so make sure you
are on the correct branch before complaining that things are not working.
Provided that the compilation went well, you should be able to run;

```bash
cd src
./snabb snabbddos --help
```

this will yield a pretty long help text on how to use `snabbddos`.

The actual logic code is mostly in src/apps/ddos/ddos.lua.
