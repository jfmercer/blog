--- 
layout: post
title: How To Calculate SHA1 on Mac OS X
date: 2011-7-6
comments: true
link: false
---
1. Open Terminal (located in /Applications/Utilities).

2. Type the following at the Terminal prompt: <tt>

openssl sha1 [<em>full path to file</em>]</tt>

<strong>Example</strong>: <tt>

openssl sha1 /Users/myaccount/Documents/1024SecUpd2003-03-03.dmg

</tt>The SHA-1 digest is displayed as: SHA1 (<em>full path to the file</em>)= [checksum amount]
<tt>
SHA1(/Users/</tt><tt>myaccount</tt><tt>/Documents/1024SecUpd2003-03-03.dmg) =2eb722f340d4e57aa79bb5422b94d556888cbf38</tt>

From <a title="SHA1" href="http://support.apple.com/kb/HT1652" target="_blank">Apple Support</a>
