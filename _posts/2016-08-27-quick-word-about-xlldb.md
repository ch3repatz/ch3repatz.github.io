---
layout: post
title: A quick word about XLLDB
date: 2016-08-27 2:48
comments: yes
---

I've started [XLLDB project](https://github.com/ch3repatz/xlldb) about a week ago. It's a reverse engineering mini-framework written in pure Python. It's OOP-friendly and suitable for automating reverse engineering tasks. Actually, I could continue using "raw" LLDB Python APIs, they are more or less stable and pretty useful. However, some things made my Python code more crap that usual.

<!-- more -->

1. **Long calling chains** like

	```
	sb_debugger = sb_frame.GetThread().GetProcess().GetTarget().GetDebugger()
	```
	
	or, including all checks, even longer:
	
	```
	sb_thread = sb_frame.GetThread()
	if not sb_thread.IsValid():
		# ...do something, it's not valid!
		...
	sb_process = sb_thread.GetProcess()
	if not sb_process.IsValid():
		# ...again, it's not valid, do something
	sb_target = sb_process.GetTarget()
	if not sb_target.IsValid():
		# ...do something, it's not valid!
		...
	sb_debugger = sb_target.GetDebugger()
	if not sb_debugger.IsValid():
		# ...do something, it's not valid!
		...
	# Wow! Finally, we can do something useful:
	...
	```
	
	I don't want this shit, I want something like `my_debugger = my_frame.debugger()` or, with a check,
	
	```
	my_debugger = my_frame.debugger()
	if my_debugger.valid():
		# do smthg useful
		...
	else:
		print 'OOps!'
	```

2. **Some hard-to-use `SB*`-classes**. To turn a result of calling `GetRegisters()` to something Python-friedly, e.g. to a dictionary, and get, for example, `x0` from the dictionary, we need 10+ lines of code (if something can do it shorter, please let me know). I want to reduce that 10+ lines to just a couple:

	```
	x0 = thread.registers()['x0']
	print '%s %s = %s' % (x0.type(), x0.name(), x0.value())
	```
	
3. **Tracing code with [Threading Plans](https://llvm.org/svn/llvm-project/lldb/trunk/examples/python/scripted_step.py)** works good for me, but, IMHO, it needs to much repeated code to write. I'd like to turn the repeated code to class methods.

4. ...and many more reasons to cover `SB*` classes with my own mini-framework.

That's why, I'm working on XLLDB, it's under (more or less) active development. Will see :)
