---
layout: post
title: chrome  inspector 숨은 기능들
date: '2018-06-15T06:51:00.000-07:00'
author: schoolhompy
tags: 
modified_time: '2018-06-15T06:51:18.663-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-7031913163377986462
blogger_orig_url: https://yunhos.blogspot.com/2018/06/chrome-inspector.html
---

https://www.vobour.com/%EB%8B%B9%EC%8B%A0%EC%9D%B4-%EB%AA%A8%EB%A5%BC-%EC%88%98%EB%8F%84-%EC%9E%88%EB%8A%94-%ED%81%AC%EB%A1%AC-%EA%B0%9C%EB%B0%9C%EC%9E%90-%EC%BD%98%EC%86%94-%EA%B8%B0%EB%8A%A5%EB%93%A4-things-you-p<br /><br /><br />1.<br />$$(‘tagName’) 또는 $$(‘.class’) 를 사용 할 수도 있는데, 이것은 셀렉터에서 매치되는 모든&nbsp; DOM 엘리먼트들을 선택한다. 달러싸인이 두개인것을 눈여겨보자. 이렇게 선택된 배열에서 특정 포지션에 있는 엘리먼트를 선택 할수도 있다.&nbsp;<br /><br /><br />2.<br />document.body.contentEditable=true 하면 브라우져 에서 그냥 수정되어<br /><br />3.<br />getEventListeners($(‘firstName’)).click[0].listener&nbsp; 걸린 이벤트 찾기<br /><br />4.<br />이벤트모니터<br />monitorEvents(window, 'click');<br />monitorEvents(window, 'message');<br /><br />5.<br />코드 블록 실행 시간 확인<br />console.time('myLabel');<br />console.timeEnd('myLabel');<br /><br />6.<br />밸류를 테이블로 이쁘게<br />console.table(variableName)<br /><br />7.<br />검사기 명령어<br />$0, $1, $2,<br /><br />8.<br />해당 아이디,또는 클래스,이름이 있는 모든목록표기<br />dir($(‘selector’))<br />inspect($(‘selector’))<br /><div><br /></div>