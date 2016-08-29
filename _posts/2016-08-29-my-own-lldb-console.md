---
layout: post
title: I'm going to build my own LLDB console! 
date: 2016-08-29 11:18
comments: yes
---

I wrote [LLDB console sux](/2016/08/28/lldb-console-suxx/), and that's true! Look at `mem read`. I can use expression for an address, but can't use if for a count of bytes to read:

	(lldb) mem read <can use expression> --count <can't use expressions>

Thouns of such weird things are in LLDB console. "I'm going to build my own theme park! With blackjack! And hookers!" (c)
