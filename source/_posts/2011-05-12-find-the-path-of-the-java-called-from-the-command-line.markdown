--- 
layout: post
title: find the path of the java called from the command line
date: 2011-5-12
comments: true
link: false
---
From <a href="http://www.commandlinefu.com/commands/view/8452/find-the-path-of-the-java-called-from-the-command-line">commandlinefu.com</a>:

$ ls -l $(type -path -all java)

This will give you the path of the java command that is used from the command line. I discovered that Mac OS X's java is <em>not</em> in /usr/bin/java, which is in fact nothing more than a symbolic link that goes to the true java buried deep in the system library:

/System/Library/Frameworks/JavaVM.framework/Versions/Current/Commands/java

&nbsp;
