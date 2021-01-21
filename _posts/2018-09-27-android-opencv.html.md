---
layout: post
title: android opencv  테스트 환경
date: '2018-09-27T20:46:00.002-07:00'
author: schoolhompy
tags: 
modified_time: '2018-09-27T20:46:42.821-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-1021943978215987421
blogger_orig_url: https://yunhos.blogspot.com/2018/09/android-opencv.html
---

<br /><br />http://webnautes.tistory.com/1054<br />http://wrongwrong163377.hatenablog.com/entry/2017/07/02/034003<br />http://wrongwrong163377.hatenablog.com/entry/2017/07/01/204124<br /><br /><br />&nbsp; &nbsp; defaultConfig {<br /><br />&nbsp; &nbsp; &nbsp; &nbsp; testInstrumentationRunner "android.support.test.runner.AndroidJUnitRunner"<br />&nbsp; &nbsp; &nbsp; &nbsp; externalNativeBuild {<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; cmake {<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; cppFlags "-std=c++11 -frtti -fexceptions"<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; abiFilters 'x86', 'x86_64', 'armeabi-v7a', 'arm64-v8a'<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; }<br />&nbsp; &nbsp; &nbsp; &nbsp; }<br />&nbsp; &nbsp; }<br /><br /><br /><br />&nbsp; &nbsp; sourceSets {<br />&nbsp; &nbsp; &nbsp; &nbsp; main {<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; jniLibs.srcDirs = ['src/main/jniLibs']<br />&nbsp; &nbsp; &nbsp; &nbsp; }<br />&nbsp; &nbsp; }<br />&nbsp; &nbsp; externalNativeBuild {<br />&nbsp; &nbsp; &nbsp; &nbsp; cmake {<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; path "CMakeLists.txt"<br />&nbsp; &nbsp; &nbsp; &nbsp; }<br />&nbsp; &nbsp; }