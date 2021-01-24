---
layout: post
title: google play service for signed package - proguard settting
date: '2014-03-29T04:28:00.001-07:00'
author: schoolhompy
categories:
- MOBILE DEV
tags:
- android

modified_time: '2017-06-25T02:22:52.135-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-6183155651827541449
blogger_orig_url: https://yunhos.blogspot.com/2014/03/google-play-service-for-signed-package_29.html
---

<pre class="default prettyprint prettyprinted"><code><span class="pun">-</span><span class="pln">dontwarn com</span><span class="pun">.</span><span class="pln">google</span><span class="pun">.</span><span class="pln">android</span><span class="pun">.</span><span class="pln">gms</span><span class="pun">.*</span><span class="pun">-</span><span class="pln">ignorewarnings  <br /><br />proguard.cfg add</span></code></pre>