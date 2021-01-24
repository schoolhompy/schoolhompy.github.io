---
layout: post
title: Jenkins 에 slack연동
date: '2020-09-26T20:24:00.002-07:00'
author: schoolhompy
categories:
- DEVOPS
tags:
- jenkins
- Slack
modified_time: '2020-09-26T20:24:32.378-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-4182364502729704530
blogger_orig_url: https://yunhos.blogspot.com/2020/09/jenkins-slack.html
---

<p>슬랙에서 app추가에서&nbsp; Jenkins CI를 추가함. 그러면&nbsp; 인터그레이션 설정토큰과 채널명,설정방법이나옴.</p><p><br /></p><p>젠킨스에 슬랙 플러그인을 설치한다.</p><p>젠킨스설정(configure)에 가서&nbsp;</p><p>워크스페이스를 슬랙의 워크스페이스이름으로</p><p>인증을 kind: SectetText , Secret: 슬랙에서 준 토큰, ID: 워크스페이스이름 이름으로 저장</p><p>채널명은 알림할 채널명으로 지정</p><p>테스트해보면 메시지가 감.</p><p>젠킨스 프로젝트 설정에 가보면</p><p>빌드후조치-&gt;Slack notification 이 적당한 것들을 체크하면 빌드시에 슬랙에 문자옴</p><p><span style="background-color: #f8f8f8; color: #1d1c1d; font-family: NotoSansJP, Slack-Lato, appleLogo, sans-serif; font-size: 14px; font-variant-ligatures: common-ligatures;">fuck-curtaincall - #13 Started by user kim (Open)&nbsp;</span></p><p><br /></p>