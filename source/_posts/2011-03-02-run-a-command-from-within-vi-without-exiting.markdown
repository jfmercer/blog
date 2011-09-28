--- 
layout: post
title: Run a Command from within vi without Exiting
date: 2011-3-2
comments: true
categories: cli
link: false
---
Tip from <a href="http://www.commandlinefu.com/commands/view/7992/run-a-command-from-within-vi-without-exiting">Commandlinefu</a>:

$ :! &lt;bash_command&gt; will run a command in your current directory.

“:! ls -l ” results in listing the files in the current directory. pressing “enter” will get you back into vi.

&nbsp;
