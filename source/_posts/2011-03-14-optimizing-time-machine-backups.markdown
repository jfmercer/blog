--- 
layout: post
title: Optimizing Time Machine Backups
date: 2011-3-14
comments: true
categories: featured
link: false
---
<div class="posterous_autopost">
<div>
<p style="text-align: left;"><a href="http://www.apple.com/macosx/what-is-macosx/time-machine.html" target="_blank">Time Machine</a> backups are a necessary part of using Mac OS X wisely. However, your backup disk does not have an infinite amount of storage space, and, if you're not careful, your Time Machine backups will eventually fill up even a large backup disk. Fortunately, Time Machine allows you to exclude directories (folders) of your choice. This allows you optimize Time Machine backups to exclude redundant or non-essential material. But which directories would be best left without backup? Rather than debate this question at length, I will simply recommend to you certain directories that I myself do not backup. I have divided them into two groups: No-Brainers (directories where you should <em>never</em> lose essential data) and Be-Wary (directories that, in some cases, should be backed up, but not necessarily in all cases).</p>
<p style="text-align: left;"><span style="text-decoration: underline;"><strong>Getting Started</strong></span></p>
<p style="text-align: left;">Go to System Preferences &gt; Time Machine &gt; Options. Click on the + symbol to add a directory for back exclusion. Note that if you want to see invisible items, you need to check off the "Show invisible items" box.</p>
<p style="text-align: left;"><span style="text-decoration: underline;"><strong>No-Brainers</strong></span></p>
<p style="text-align: left;">I see no reason to ever back these up. Trash is always on the way out. The downloads folder is not a place to store important items. As for the caches . . . I can't believe Apple doesn't automatically exclude them. As for the Developer folder, you can always reinstall that from your OS X install disk or grab a copy f<a href="http://itunes.apple.com/us/app/xcode/id422352214?mt=12" target="_blank">rom the Mac App Store</a>.</p>
<p style="text-align: left;">~/.Trash</p>
<p style="text-align: left;">~/Downloads</p>
<p style="text-align: left;">~/Library/Caches</p>
<p style="text-align: left;">/System/Library/Caches</p>
<p style="text-align: left;">/Developer</p>
<p style="text-align: left;"><span style="text-decoration: underline;"><strong>Be-Wary</strong></span></p>
<p style="text-align: left;">~/Library/Application Support</p>
<p style="text-align: left;">/System/Library/Application Support</p>
<p style="text-align: left;">Some would argue that excluding these might break a Time Machine re-install of certain essential programs (e.g., iLife). This is true. However, it's also true that these folders are jam-packed with replaceable junk. Those "essential" iLife directories can be restored by simply reinstalling iLife. That's also true of any other app that makes heavy use of this directory. However, for the most part, you will find your /Application Support libraries both littered with the detritus of uninstalled programs and full of non-essential disk-devouring files. By dropping these two directories, I saved 4.81 GB without losing anything essential. However, if you don't feel comfortable with this, I'd recommend against it. Go with your gut.</p>
<p style="text-align: left;">~/Movies</p>
<p style="text-align: left;">I'd only do this is you don't have anything personal in your Movies folder.</p>
<p style="text-align: left;"> </p>
</div>
<p style="text-align: left;"> </p>
</div>
