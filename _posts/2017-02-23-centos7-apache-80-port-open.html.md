---
layout: post
title: Centos7 apache 80 port open
date: '2017-02-23T19:30:00.000-08:00'
author: schoolhompy
tags:
- 서버 및 보안
modified_time: '2017-06-25T02:22:54.939-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-7438651149130242850
blogger_orig_url: https://yunhos.blogspot.com/2017/02/centos7-apache-80-port-open.html
---

포트를 방화벽에 추가합니다.<br/>sudo firewall-cmd --zone=public --add-port=80/tcp --permanent<br/><br/>방화벽을 리로드<br/>sudo firewall-cmd --reload