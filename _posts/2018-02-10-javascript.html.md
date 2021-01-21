---
layout: post
title: JAVASCRIPT 유용한 함수들 -- 잘까먹거나 안썼던 것들
date: '2018-02-10T21:08:00.000-08:00'
author: schoolhompy
tags:
- front-end
- javascript
- reactjs
modified_time: '2018-02-11T03:35:35.894-08:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-2977768816070265343
blogger_orig_url: https://yunhos.blogspot.com/2018/02/javascript.html
---

<b>-Array.every(function(value){</b><br /><b>&nbsp; return conditional;</b><br /><b>});&nbsp;</b><br />&nbsp;: 모든 항목이 true 여야만 결과가 true 가된다.조건의 하나라도 실패하면 실패가된다.<br />--&gt;ex<br />var array = [1, 3, 5, 7, 9];<br />array.every(function(i) {<br />&nbsp; return i % 2 === 1;<br />}); // true<br />array.every(function(i) {<br />&nbsp; return i &lt; 9;<br />}); // false<br /><br /><b>-Array.some(function(value){</b><br /><b>&nbsp; return conditional;</b><br /><b>});&nbsp;</b><br />&nbsp;: 한개의 항목이라도 조건에서 true 면 성공이다. 마치 sql 의 in_array 비슷한기능<br /><div><div>--&gt;ex</div><div>array.some(function(i) {</div><div>&nbsp; return i === 9;</div><div>}); // true<br /><br /><b>-Array.isArray(값)</b><br />&nbsp;: 값이 배열인지 확인, 값이 없으면 에러..<br /><div><div>--&gt;ex</div><div>Array.isArray(array1)// true</div><div><br /><br /><b>-함수안에 객체함수를 만드는 것보다 prototype 을 만드는게 메모리에 효과적이다. 함수안의 객체는 new 로 새로 만들떄마다 각 함수마다 객체함수를 들고다니지만, prototype 은 함수자체에 포함되어 메모리를 아낄수 있다.</b><br /><br />function MyMethod(arg1, arg2){<br />&nbsp; &nbsp;this.arg1 = arg1<br />&nbsp; &nbsp;this.arg2 = arg2<br />&nbsp; &nbsp;this.innerMethod = function() {<br />&nbsp; &nbsp; &nbsp; return this.arg1&nbsp;+ this.arg2;<br />&nbsp; &nbsp;}<br />}<br />보다는<br /><br />function MyMethod(arg1, arg2){<br />&nbsp; &nbsp;this.arg1 = arg1<br />&nbsp; &nbsp;this.arg2 = arg2<br />}<br />MyMethod.prototype.innerMethod= function() {<br /><br />&nbsp; &nbsp; &nbsp; return this.arg1&nbsp;+ this.arg2;<br />&nbsp; }<br /><b><br /></b><b><br /></b><b>-JAVASCRIPT 의 상속방법은 Object.create.</b><br /><div><div>단일상속</div><div>Rectangle.prototype = Object.create(Shape.prototype);</div><div>Rectangle.prototype.constructor = Rectangle;</div><div><br /></div><div>멀티상속</div><div>mixin(MyClass.prototype, OtherSuperClass.prototype); // mixin</div></div><div><br /></div>https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Object/create<br /><br /></div></div></div></div>