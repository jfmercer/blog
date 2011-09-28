--- 
layout: post
title: Find Broken Symlinks
date: 2011-4-7
comments: true
categories: cli
link: false
---
$ find . -type l | xargs file  | grep broken

via <a href="http://www.commandlinefu.com/commands/view/8257/find-broken-symlinks?utm_source=feedburner&amp;utm_medium=feed&amp;utm_campaign=Feed%3A+Command-line-fu+%28Command-Line-Fu%29">commandlinefu.com</a>
