---
layout: post
title: JAVASCRIPT 성능 최적화
date: '2015-11-03T19:57:00.001-08:00'
author: schoolhompy
categories:
- BACKEND
tags:
- JAVAscript
modified_time: '2017-06-25T02:22:53.680-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-7423004771116940284
blogger_orig_url: https://yunhos.blogspot.com/2015/11/javascript_3.html
---

<ul><br/>	<li>스크립트는 body 최하단</li><br/>	<li>자주쓰는 스코프 외부변수는 지연변수에 복사해서 쓰면 속도가 개선된다.</li><br/>	<li>for .. in 은 느리다.</li><br/>	<li>대량 루프일때 반복횟수 줄이기 Duff's device , 제프 그린버그의 방법참고.</li><br/>	<li>..대략 아는내용</li><br/></ul>