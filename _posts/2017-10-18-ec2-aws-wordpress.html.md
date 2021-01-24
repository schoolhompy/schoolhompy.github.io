---
layout: post
title: EC2 AWS 마켓플레이스 를 이용해서 WordPress 서비스 생성하기
date: '2017-10-18T20:50:00.002-07:00'
author: schoolhompy
categories:
- DEVOPS
tags:
- aws
modified_time: '2017-10-18T20:50:38.403-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-8955982858896943471
blogger_orig_url: https://yunhos.blogspot.com/2017/10/ec2-aws-wordpress.html
---

AWS 마켓플레이스를 이용하면 여러가지 미리 세팅된 서버 서비스를 쉽게 생성할수 있다.<br /><br /><br />마켓플레이스에서 해당 상품의 정보에 이런저런 정보가 있는데 보통 거기서 서비스의 초기 비번등을 알아낼수있다.<br />wordpress bitnami 의 경우는 instance 에서 오른쪽버튼-&gt;instance setting-&gt;get system log 에서 보면 bitnami 의 초기 app 비번(랜덤인듯) 이 보이는데 이를 복사해서<br />워드프로세스 어드민 /wp-admin/ 에 접속시 user,비번 입력하면된다.<br /><br />추가, mysql root 비번도 동일하다.