---
layout: post
title: Dokcer 내의 Jenkins 에서 nodejs , npm , nuxtjs, vuejs  빌드하기
date: '2020-09-26T20:15:00.002-07:00'
author: schoolhompy
categories:
- DEVOPS
tags:
- docker
- nodejs
- Jenkins
- Nuxtjs
categories:
- FRONTEND
modified_time: '2020-09-26T22:16:08.742-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-3255849670027883946
blogger_orig_url: https://yunhos.blogspot.com/2020/09/dokcer-jenkins-nodejs-npm-nuxtjs-vuejs.html
---

<p>&nbsp;일단 Docker 에 jenkins/jenkins&nbsp; 이미지를&nbsp; 다운로드 받는다.</p><p>* 주의 kitematic 에서의 jenkins는 잘안됨</p><p>docker pull jenkins/jenkins:lts &lt;- lastest도 괘안</p><p>받아서 기동후 쉘로 들어가서 암호찾아내서 일단 스탠다드 인스톨.</p><p>인스톨이 다 되었다면 /var/jenkins_home 폴더는 로컬폴더에 연결하고 다시 기동.</p><p>왠지 jenkins에서 nodejs 플러그인을 설치하면 될것같지만, 안된다.</p><p>그래서 젠킨스 컨테이너의 쉘을 root 권한으로 들어간다.</p><p>$ docker exec -it --user root YourContainer /bin/bash</p><p>애네들을 실행한다.</p><p>apt-get update</p><p>apt-get install -y git curl vim sudo apt-utils</p><p>curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -</p><p>apt-get install -y nodejs</p><p>rm -rf /var/lib/apt/lists/*</p><p>또는</p><p>curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.32.0/install.sh | bash</p><p>를 실행해서 nvm 을 설치하고</p><p>nvm install 12.6.3</p><p>해서 node를 설치하면</p><p>/root/.nvm/versions/node/v12.16.3</p><p>이딴 폴더가 생기지만 root 폴더밑에 있어서 jenkins가 읽지 못함.</p><p>단순무식으로 v12.16.3 의 모든 내용을 /var/jenkins_home/nodes/ 밑에 복사하자.</p><p>그리고나서 젠킨스 빌드시의 execute shell 에서</p><p>cd /var/jenkins_home/workspace/Fuck-curtaincall</p><p>/var/jenkins_home/nodes/bin/npm install</p><p>/var/jenkins_home/nodes/bin/npm run build</p><p>하면 nuxtjs 가 빌드된다.</p><p>그걸 웹서버에 올리고 재가동 하면 끄읕.</p><p><br /></p><p>참. 젠킨스설정에서</p><p><span style="background-color: #f9f9f9; color: #333333; font-family: -apple-system, system-ui, &quot;Segoe UI&quot;, Roboto, &quot;Noto Sans&quot;, Oxygen, Ubuntu, Cantarell, &quot;Fira Sans&quot;, &quot;Droid Sans&quot;, &quot;Helvetica Neue&quot;, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; font-size: 14px;">이 빌드는 매개변수가 있습니다 . 에서</span></p><p><span style="background-color: #f9f9f9; color: #333333; font-family: -apple-system, system-ui, &quot;Segoe UI&quot;, Roboto, &quot;Noto Sans&quot;, Oxygen, Ubuntu, Cantarell, &quot;Fira Sans&quot;, &quot;Droid Sans&quot;, &quot;Helvetica Neue&quot;, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; font-size: 14px;">매개변수 branch 기본밸류 master</span></p><p><span style="background-color: #f9f9f9; color: #333333; font-family: -apple-system, system-ui, &quot;Segoe UI&quot;, Roboto, &quot;Noto Sans&quot;, Oxygen, Ubuntu, Cantarell, &quot;Fira Sans&quot;, &quot;Droid Sans&quot;, &quot;Helvetica Neue&quot;, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; font-size: 14px;">하고&nbsp; 소스코드관리에서 branch to build 항목에서</span></p><p><span style="background-color: #f9f9f9; color: #333333; font-family: -apple-system, system-ui, &quot;Segoe UI&quot;, Roboto, &quot;Noto Sans&quot;, Oxygen, Ubuntu, Cantarell, &quot;Fira Sans&quot;, &quot;Droid Sans&quot;, &quot;Helvetica Neue&quot;, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; font-size: 14px;">*/${branch} 하면됨</span></p>