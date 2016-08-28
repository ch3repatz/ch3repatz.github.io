---
layout: post
title: LLDB console sux
date: 2016-08-28 18:00
comments: yes
---

A simple `test.py` with a custom LLDB command `test`:

	import lldb
	
	def test(debugger, command, result, internal_dict):
    	target = debugger.GetSelectedTarget()
    	target.GetProcess().Continue()

	def __lldb_init_module(debugger, internal_dict):
    	debugger.HandleCommand('command script add -f test.test test')

<!-- more -->
Not a rocket science, yes? I just want the `test` command to continue the selecter process. So what I get?

	(lldb) command script import test.py
	(lldb) test

I get a stuck LLDB :( WTF?

If I use `SBProcess::Continue()` from a Python script which use LLDB and run as a standalone script (not as a command in LLDB console), everything works ok for me.

Such idiotic bugs make development of [XLLDB project](https://github.com/ch3repatz/xlldb) more complex that I expected.
