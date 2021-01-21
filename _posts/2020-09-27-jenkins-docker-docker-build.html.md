---
layout: post
title: Jenkins Docker 내에서 docker build 하기
date: '2020-09-27T01:41:00.001-07:00'
author: schoolhompy
tags: 
modified_time: '2020-09-27T02:16:05.383-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-2285884928813402243
blogger_orig_url: https://yunhos.blogspot.com/2020/09/jenkins-docker-docker-build.html
---

<p>&nbsp;도커안의 젠킨스 루트로 들어가서</p><p>wget -O /tmp/docker.tgz https://download.docker.com/linux/static/stable/x86_64/docker-19.03.8.tgz</p><p>tar -xzf /tmp/docker.tgz -C /tmp</p><p>mv /tmp/docker/* /usr/bin/</p><p><br /></p><p>groupadd -o -g $DOCKER_GROUP_GID docker</p><p>usermod -g docker jenkins</p><div><br /></div><div>하여 도커설치&nbsp;</div><div>service docker start 하면 에러가 떠서&nbsp;</div><div>curl -sSL https://get.docker.com/ | sh</div><div>를 해서 서비스는 추가되는데, 도커가 안올라옴.&nbsp;</div><div><br /></div><div>--&gt; 도커안의 젠킨스에서 도커를 구동하기 위해서는 별도의 조치가 필요</div><div>https://coders-shelf.com/jenkins-docker-agent/</div>