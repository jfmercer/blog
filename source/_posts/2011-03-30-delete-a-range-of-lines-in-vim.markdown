--- 
layout: post
title: Delete a Range of Lines in Vim
date: 2011-3-30
comments: true
link: false
---
This vim command allows you to delete a range of lines.

:a,bd where a is the first line &amp; b is the last. d is short for delete.

Example:

:335,1045d will delete lines 335-1045
