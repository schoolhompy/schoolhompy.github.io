---
layout: post
title: Cloud9 에서 Laravel 을 실행해보장
date: '2017-10-01T23:05:00.002-07:00'
author: schoolhompy
tags:
- Laravel
modified_time: '2017-10-01T23:05:52.371-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-3698060304281833661
blogger_orig_url: https://yunhos.blogspot.com/2017/10/cloud9-laravel.html
---

아래 자세한 설명 고마워요. 설치하고 세팅하는거 징그럽게 싫어 하는데 설명이 잘되어 있네요.<br /><br />https://community.c9.io/t/laravel-5-3-installation-on-cloud9/9038<br />단<br /><span style="background-color: #eeeeee; color: #333333; font-family: Consolas, Menlo, Monaco, &quot;Lucida Console&quot;, &quot;Liberation Mono&quot;, &quot;DejaVu Sans Mono&quot;, &quot;Bitstream Vera Sans Mono&quot;, &quot;Courier New&quot;, monospace; font-size: 14px;">DocumentRoot /home/ubuntu/workspace/public 요거 설정하라고 되어 있는데.</span><br /><span style="background-color: #eeeeee; color: #333333; font-family: Consolas, Menlo, Monaco, &quot;Lucida Console&quot;, &quot;Liberation Mono&quot;, &quot;DejaVu Sans Mono&quot;, &quot;Bitstream Vera Sans Mono&quot;, &quot;Courier New&quot;, monospace; font-size: 14px;"><br /></span><span style="color: #333333; font-family: Consolas, Menlo, Monaco, Lucida Console, Liberation Mono, DejaVu Sans Mono, Bitstream Vera Sans Mono, Courier New, monospace;"><span style="background-color: #eeeeee; font-size: 14px;">내경우에는&nbsp;</span></span><br /><br /><span style="background-color: #eeeeee; color: #333333; font-family: Consolas, Menlo, Monaco, &quot;Lucida Console&quot;, &quot;Liberation Mono&quot;, &quot;DejaVu Sans Mono&quot;, &quot;Bitstream Vera Sans Mono&quot;, &quot;Courier New&quot;, monospace; font-size: 14px;">DocumentRoot /home/ubuntu/workspace/laravel/public 로 해야 이쁜 라라벨 첫페이지가 뜸.</span>