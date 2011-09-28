--- 
layout: post
title: My Battle to Install APC
date: 2011-4-3
comments: true
categories: featured
link: false
---
Today I decided to install APC to accelerate my WordPress install. APC is a PHP caching extension that accelerates the speed at which PHP processes code. In a nutshell, you get faster PHP &amp; a faster WordPress blog.

What I did not anticipate was that it would turn into an epic battle with my MediaTemple (dv) Dedicated-Virtual 4.0 server. I'll spare you the ugly details of how I meandered from one false solution to another. Here's the problem, and here's how I solved it.

The install should have been straightforward. Under better circumstances, this command should have installed it immediately:
{% codeblock %}[user@server ~] # pecl install apc{% endcodeblock %}
However, I got this error:
{% codeblock %}/usr/bin/phpize: /var/tmp/APC/build/shtool: /bin/sh: bad interpreter:
Permission deniedCannot find autoconf. Please check your autoconf
installation and the$PHP_AUTOCONF environment variable. Then, rerun
this script. ERROR: `phpize' failed{% endcodeblock %}
The MediaTemple forums were helpful. There I discovered the following commands which, so <a href="http://wiki.mediatemple.net/w/(dv):Installing_PECL_extensions">this article</a> claimed, would fix the install.
{% codeblock %}[user@server ~] # mount - remount,exec /tmp{% endcodeblock %}
This resulted in a permissions error which was fixed with the following:
{% codeblock %}[user@server ~] #mkdir ~/tmp[user@server ~] #mount --bind ~/tmp /tmp[user@server ~] #mount -o remount,exec /tmp{% endcodeblock %}
This fixed the <em>mount</em> permissions error, but not the <em>pecl</em> one. After running <em>pecl install apc</em> again, I still got that weird permissions error message that began it all. What the heck? I noticed that <em>/var/tmp</em> was in the error message, rather than <em>/tmp</em>. So I tried with <em>/var/tmp</em> what I did with <em>/tmp</em>:
{% codeblock %}[user@server ~] #mkdir ~/var[user@server ~] #mkdir ~/var/tmp[user@server ~] #mount --bind ~/var/tmp /var/tmp[user@server ~] #mount -o remount,exec /var/tmp{% endcodeblock %}
After that, the install went fine.
{% codeblock %}[user@server ~] # pecl install apc{% endcodeblock %}
For security, I returned <em>/var/tmp</em> &amp; <em>/tmp</em> to their original, non-executable state:
{% codeblock %}[user@server ~] #mount -o remount,noexec /tmp[user@server ~] #mount -o remount,noexec /var/tmp{% endcodeblock %}
Now for the final step. "<em>extension=apc.so</em>" must be added to the end of your <em>php.ini</em>. Mine was located at <em>/etc/php.ini</em>.

APC is up &amp; running like a charm!
