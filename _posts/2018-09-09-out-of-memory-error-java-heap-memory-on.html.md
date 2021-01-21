---
layout: post
title: 'Out of memory error: Java heap memory on Android Studio'
date: '2018-09-09T02:33:00.002-07:00'
author: schoolhompy
tags: 
modified_time: '2018-09-09T04:43:49.494-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-3927802420968295075
blogger_orig_url: https://yunhos.blogspot.com/2018/09/out-of-memory-error-java-heap-memory-on.html
---

OpencvLibrary342 를 빌드하려 하니.메모리 .에러가...<br /><br />Run/Debug Configurations&nbsp; 에서<br /><br />Default-&gt;Gradle-&gt;Configuration-&gt;VM options-Xmx2048m -XX:MaxPermSize=512m<br /><br />추가하면 됨.<br /><br />나 같은 경우에는<br />안드로이드 스튜디오 터미널 에서<br />jps -lvm 해보니 용량이 512m 로 정해져있어서<br /><br />환경변수에<br />_JAVA_OPTIONS ,&nbsp;-Xms512m -Xmx512m 로 되어있어서<br /><br />-Xms1G -Xmx2G 로 변경해서됨