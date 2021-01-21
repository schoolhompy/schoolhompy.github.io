---
layout: post
title: 3.Template Method 패턴
date: '2015-10-10T22:03:00.001-07:00'
author: schoolhompy
tags:
- design pattern
modified_time: '2017-06-25T02:22:53.360-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-5412263184041246802
blogger_orig_url: https://yunhos.blogspot.com/2015/10/3template-method_10.html
---

상위클래스는 처리의 흐름이 정의 되어 있는 추상클래스이고 ,하위 클래스는 사우이클래스를 상속받아 구체적인 처리를 구현한 클래스가 된다.<br/><br/>따라서 상위 클래스는 하위 클래스가 실제적으로 어떤 구체적인 작업을 하는지 모르며, 서로 다른 하위 클래스들은 나름대로의 방식대로 구현하되 처리의 흐름은 상위 클래스에 정의된대로 따르게 된다.<br/><br/>즉, 탬플릿의 주체가 되는 콘트롤러 의 성격을 띄는 상위클래스에서 흐름을 관장하고, 상속받은 실제 하위 클래스에서는 상위클래스에서 정의된 순서와 규정에 맞게 오버라이딩 하고, 추가 기능등을 구현하게 된다.<br/><br/>따라서 일련의 상속받은 하위 클래스들은 모두 상위 클래스의 템플릿구성대로 구현과 실행하게 되는 패턴이다.<br/><br/>구조가 일관적인 형식의 제품이나 기능들을만들때 주로 사용하는 패턴이다.<br/><br/>Abstract  UpperClass {<br/><br/>abstract public function init();<br/>abstract public function run();<br/>abstract public function end();<br/>final function showMain(){<br/>this-&gt;init();<br/>this-&gt;run();<br/>this-&gt;end();<br/><br/>}<br/>protected int sharedVal = 0; //하위 클래스에서 공통으로 공유하는 변수등.<br/><br/>}<br/><br/>추상클래스인 UpperClass 에는 오버라이디이 불가능한 final 인 showMain 에 정의된 초기와-&gt;실행-&gt;종료 라는 템플릿으로 하위 클래스에서 실행되도록 구현된것이다.<br/><br/>하위 클래스는 추상메쏘드 들을 각 상황에 맞에 오버라이딩 한다음 showMain() 을 실행하여 동일한 실행 프로세스를 가질수 있도록 했다.<br/><br/>&nbsp;<br/><br/>http://copynull.tistory.com/124<br/><br/>http://egloos.zum.com/iilii/v/3806897<br/><br/>http://secretroute.tistory.com/entry/Head-First-Design-Patterns-%EC%A0%9C8%EC%9E%A5-Template-Method-%ED%8C%A8%ED%84%B4<br/><br/>http://blog.jdm.kr/116<br/><br/>http://skmagic.tistory.com/entry/Template-Method-Pattern-Class-%EC%A0%95%EB%A6%AC%EB%B3%B8<br/><br/>http://darkneo.tistory.com/7