---
layout: post
title: C# const VS readony 차이점
date: '2018-04-22T06:39:00.001-07:00'
author: schoolhompy
tags:
- "C#"
modified_time: '2018-04-22T06:39:37.892-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-146593675696506119
blogger_orig_url: https://yunhos.blogspot.com/2018/04/c-const-vs-readony.html
---

const 는 초기에 반드시 값을 지정해야 한다. 즉 컴파일시에 값지정해야한다.<br />readonly 는 초기에 값을 지정안하고, 실행시 첫번에 한해 값을 지정할수도있다.<br /><br />즉, 실행하기 전에는 값이없다가, 어떤 조건에 의해 초기값이 정해질 필요가 있는 읽기 전용 값을 지정할때 유용하다.<br /><br />사용자 아이피나 실행시의 사용자 환경값 등은 사용자에 따라 다르지만, 실행한후에는 거의 고정되기 때문에 readonly 로 하는게 좋다.<br />때로는 서버에서 한번 읽어들인 값을 사용하자가 변하지 못하게하는 용도, 토큰이라든지,세션이라든지 UID등에 유용하다.