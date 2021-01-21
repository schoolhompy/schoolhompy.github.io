---
layout: post
title: android cli 서명
date: '2016-05-24T06:16:00.000-07:00'
author: schoolhompy
tags:
- 안드로이드
modified_time: '2017-06-25T02:22:54.503-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-6588213097777292781
blogger_orig_url: https://yunhos.blogspot.com/2016/05/android-cli.html
---

jarsigner -verbose -keystore jewonagency.keystore release-unsigned.apk jewonagency<br/>zipalign -f -v 4 release-unsigned.apk release-signed.apk<br/><br/>zipalign 은 C:\android\sdk\build-tools\ 밑에 버젼별<br/><br/>http://jewonagency.com/%EC%B4%88-%EA%B0%84%EB%8B%A8%ED%95%98%EA%B2%8C-%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-apk-%EC%82%AC%EC%9D%B8%ED%95%98%EA%B8%B0-signing-cli-%EC%BB%A4%EB%A7%A8%EB%93%9C%EB%9D%BC%EC%9D%B8/