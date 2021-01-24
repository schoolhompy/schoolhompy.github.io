---
layout: post
title: Vue.js 를 VSCODE 에서 디버그 하기(브레이크 포인트잡기)
date: '2020-07-02T00:27:00.003-07:00'
author: schoolhompy
tags:
- Vue.js
categories:
- FRONTEND
modified_time: '2020-07-29T21:21:24.873-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-8770478467862745004
blogger_orig_url: https://yunhos.blogspot.com/2020/07/vuejs-vscode.html
---

<div>Vue.js 를 VSCODE 에서 디버그 하기(브레이크 포인트잡기)</div><div><br /></div><div>&nbsp;js 는 브레이트포인트 잡는게 썅.&nbsp;</div><div>&nbsp;일단 Vue.js (이름참 좃같...) 의 작업을 한다.</div><div><br /></div><div><a href="https://medium.com/js-dojo/debugging-nuxt-js-with-vs-code-60a1a9e75cf6">https://medium.com/js-dojo/debugging-nuxt-js-with-vs-code-60a1a9e75cf6</a></div><div>"That basically acts as the magic goo that enables the rest of this to work." WTF NUXT!</div><div><br /></div><div>https://github.com/in28minutes/spring-boot-vuejs-fullstack-examples</div><div>예제를 기준으로!</div><div><br /></div><div>1.프론트쪽 폴더에서 npm run serve 실행</div><div>2.프론트쪽 폴더 선택후 VSCODE 에서 실행하면 launch.json 만들라고 하니까 만듬</div><div>3.런쳐는 크롬을 띄워서 디버그 해야 되니까 다음과 같이 입력</div><div><br /></div><div>{</div><div>&nbsp; &nbsp; "version": "0.2.0",</div><div>&nbsp; &nbsp; "configurations": [</div><div>&nbsp; &nbsp; &nbsp;{</div><div>&nbsp; &nbsp; &nbsp; &nbsp; "type": "chrome",</div><div>&nbsp; &nbsp; &nbsp; &nbsp; "request": "launch",</div><div>&nbsp; &nbsp; &nbsp; &nbsp; "name": "[Debug] Vue.js: chrome",</div><div>&nbsp; &nbsp; &nbsp; &nbsp; "url": "http://localhost:8080",</div><div>&nbsp; &nbsp; &nbsp; &nbsp; "webRoot": "${workspaceFolder}/src",</div><div>&nbsp; &nbsp; &nbsp; &nbsp; "breakOnLoad": true,</div><div>&nbsp; &nbsp; &nbsp; &nbsp; "sourceMapPathOverrides": {</div><div>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; "webpack:///src/*": "${webRoot}/*"</div><div>&nbsp; &nbsp; &nbsp; &nbsp; }</div><div>&nbsp; &nbsp; &nbsp; }</div><div>&nbsp; &nbsp; ]</div><div>&nbsp; }</div><div>4.브레이크 잡고 확인</div><div><br /></div><div>어이없는 이런 방식이 맞는가 싶네...</div><div><br /></div><div>참고.</div><div><br /></div><div>https://medium.com/@changjoopark/visual-studio-code%EB%A5%BC-%EC%9D%B4%EC%9A%A9%ED%95%9C-vue-js-%EC%95%B1-%EB%94%94%EB%B2%84%EA%B9%85%ED%95%98%EA%B8%B0-6a402fefafe</div>