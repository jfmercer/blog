--- 
layout: post
title: "CloudFlare: Better Performance & Security for Your Website"
date: 2011-3-23
comments: true
categories: [featured, web development, web design]
link: false
---
If you own &amp; run websites, you are always looking into better security as well as performance enhancements for you site. I received a tip recently about a new startup called <a href="http://www.cloudflare.com/">CloudFlare</a> that fulfills both of those demands. Here I shall give a brief overview of CloudFlare so that you can see if it is something your websites could benefit from.

<span style="text-decoration: underline;"><span style="font-size: large;">Security</span></span>

In a nutshell, CloudFlare is nothing more than a <a href="http://en.wikipedia.org/wiki/Reverse_proxy" target="_blank">reverse proxy</a>. Under normal circumstances, visitors to your website connect directly from the web to your server. When a reverse proxy is added, visitors <em>do not</em> connect directly to your site; rather, visitors first go through a massive server called a <em>proxy</em> which then in turn sends them to your website. Think of your website as if it were a medieval town. The reverse proxy is your city walls: no one can get into the town without first passing through the walls. (The metaphor is not work in reverse; your site does not pass through the proxy to reach the "outside world" of the web.) A reverse proxy acts as a kind of firewall to protect your site.

CloudFlare offers a simple picture to illustrate this concept:

<a href="https://www.cloudflare.com/overview.html"><img class="alignnone" title="reverse_proxy_explained" src="http://www.cloudflare.com/media/images/overview/illustration.jpg" alt="" width="950" height="380" /></a>

Before you set up a reverse proxy such as CloudFlare, literally anything &amp; anybody on the web can visit your site. Given the vast number of spambots, hackers, malicious attackers, DoS junkies, and other jerks sowing chaos on the web these days, it makes sense that you would want a good measure of security to protect your site. (Hence, it's no accident that smart webmasters back up all of their data <em>at least</em> once per day.) The second panel illustrates the nature of CloudFlare's reverse proxy: good visitors &amp; crawler-bots (Google, Bing, Yahoo, etc.) are directed toward your site, whereas the internet thugs are bounced before their <a href="http://en.wikipedia.org/wiki/Cross-site_scripting" target="_blank">cross-site scripting</a> (XSS) jiu-jitsu can steal your data invisibly.

Of course, no security is perfect. A well-trained attacker fully devoted to destroying your site will get in eventually, even if you've paid security experts for custom, multi-thousand dollar security protection. But, be honest: is your website so important that the Ukrainian cyber-mafia will devote its best resources to you? Doubtful. It's much more likely you'll be hit by an attack bot that's sweeping hundreds or even thousands of websites at once. It's always best to put up the best protection you can &amp; hope for good results. A powerful reverse proxy, such as CloudFlare, is a dynamite tool for your defensive arsenal.

<span style="text-decoration: underline;"><span style="font-size: large;">Performance</span></span>

In addition to security, CloudFlare offers performance boosts. Although your mileage may vary, CloudFlare claims that, on average, their service will boost your website to
<ul>
	<li>Load 30% faster</li>
	<li>Use 60% less bandwidth</li>
	<li>Have 65% fewer requests</li>
</ul>
My own site's page-load time dropped from 2.25 seconds to 1.06 seconds: a 52.89% increase! And that's just the free package! This is important not only to retain visitors, but also to boost your SEO rankings. Last April, Google announced that page-load would affect search rankings, and this set off a scramble as webmasters sought to increase speed without losing quality or content. Google added that 1.5 seconds or lower was ideal. The free package includes a number of speed optimizations, including static image caching, auto-minify for JavaScript &amp; CSS, &amp; a beta feature called "Rocket Script" which asynchronously loads JavaScript resources to boost page-rendering. (It smells like free AJAX to me . . .) Pro accounts also have the option of more advanced security features, such as a Web App Firewall, as well as a website preloader which automatically preloads static resources from your site to produce much faster load times.

<span style="text-decoration: underline;"><span style="font-size: large;">Other Cool Features</span></span>

CloudFlare also offers easy Google Analytics integration, an analytics dashboard to monitor outbound links, regular traffic, crawlers &amp; bots, &amp; visits (or attempted visits) from known threats, email address obfuscation, server-side exclude (that's geek-speak for hiding sensitive info from questionable visitors), IP geolocation, browser integrity checks, hotlink protection, and more.

<span style="text-decoration: underline; font-size: medium;">Setup</span>

Given the complexity &amp; power of this technology, setup was remarkably simple. CloudFlare will import your DNS record. After double-checking it to make sure all those A, CNAME, MX, &amp; TXT records are correct, you just have to change your name servers from your existing webhost to CloudFlare. Even this is easy, because some late-nite coffee-holic at CloudFlare set up custom directions for the most popular service providers such as DreamHost, MediaTemple, etc.

<span style="text-decoration: underline;"><span style="font-size: medium;">IP Address Magic</span></span>

The more tech-savvy among you may wonder, "But what about my IP Address? Won't my site visitors see the IP address of the CloudFlare reverse proxy rather than my own IP address?" Never fear. Though some magically code-foo, your visitors won't see the CloudFlare servers at all: your IP address is what they get. For WordPress blogs, this involves installing a CloudFlare plugin. I'm not familiar with CloudFlare's solutions for other blogs &amp; websites, but I know they're out there.

<span style="text-decoration: underline; font-size: medium;">Will Good Visitors Get Bounced?</span>

So, your grandma just got an iMac, and she's so proud of you, her web-geek grandchild, that she wants to see your website herself. Could she be blocked? That's very unlikely. But if it does happen, she'll get a challenge page where she'll have to complete a CAPTCHA to pass. So good visitors do get the option of giving the not-so-secret password swirling around in the CAPTCHA picture. So, even in the very rare circumstance that granny gets bounced, she can still ask the CAPTCHA bouncer to let her in. If worst comes to worst, you could add her IP to the IP address whitelist. However, if granny was trying to look up your website in iPhoto, then maybe it's time for a <a href="http://www.teachparentstech.org/" target="_blank">free tech support package</a>.

<span style="text-decoration: underline; font-size: medium;">Costs</span>

Unless you're running serious full-scale enterprise servers, CloudFlare's free service should cover your needs. The Pro version runs at $20/month for your first site and $5/month for each additional. If I ever have money again, I'll upgrade to Pro for the added security &amp; the faster page loads. CloudFlare Enterprise is still in the works; you'll have to <a href="https://www.cloudflare.com/enterprise-advisory-board.html" target="_blank">contact CloudFlare Enterprise</a> to get an estimated price &amp; delivery date.

<span style="text-decoration: underline;"><span style="font-size: medium;">Cool Intro Video</span></span>

CloudFlare in 90 seconds:

<iframe src="http://player.vimeo.com/video/14700285?title=0&amp;byline=0&amp;portrait=0" width="400" height="225" frameborder="0" webkitAllowFullScreen allowFullScreen></iframe><p><a href="http://vimeo.com/14700285">Us in 90 Seconds</a> from <a href="http://vimeo.com/user3546461">CF Vimeo</a> on <a href="http://vimeo.com">Vimeo</a>.</p>

<span style="text-decoration: underline; font-size: large;">Conclusion</span>

In my experience, nothing but good has come out of my switch to CloudFlare. I've recommended it to my geek-friends, and I recommend it to you too. Try it out, and drop a comment to let me know what you think.

<a href="http://www.cloudflare.com/">cloudflare.com</a>
