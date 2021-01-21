---
layout: post
title: Jenkins in Docker,  로컬 안드로이드 sdk 를 이용하여 github 프로젝트 빌드하기
date: '2021-01-10T21:47:00.001-08:00'
author: schoolhompy
tags:
- docker
- android
- jankins
- github
modified_time: '2021-01-20T03:59:45.076-08:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-2096382097759565442
blogger_orig_url: https://yunhos.blogspot.com/2021/01/jenkins-in-docker-sdk-github.html
---

<p>&nbsp;Jenkins in Docker에서 커스텀도커로 로컬의 android_sdk 를 젠킨스에서 접근할수 있도록 했다.</p><p>https://yunhos.blogspot.com/2021/01/jenkins-in-docker.html</p><p><br /></p><p>젠킨스에서 github의 안드로이드 프로젝트를 빌드해보자.</p><p>간단하다.</p><p>0.manage jenkins -&gt; configure system 에서</p><p>Global Section -&gt; Environment&nbsp; &nbsp;variables 에</p><p>ANDROID_HOME 과 값으로 마운트했던 /var/android_sdk 를 지정하자</p><p><br /></p><p>1.New Item 선택해서 [Free Style Project]를 생성하자.</p><p>2.Source Code Management 부분에서&nbsp;</p><p>Repository URL : github의 프로젝트 주소 (.git)</p><p>credential: add 해서 username에는 github사용자id 를 입력한다. 비밀번호는 github-&gt;user settings-&gt;developer settings-&gt;personal access token 을 새로 생성해서 토큰값을 암호로 쓰자.(단 토큰값메모를...)</p><p>빌드할 브랜치도 선택하다.</p><p><br /></p><p>3.build-&gt;execute shell 에&nbsp;</p><p>./gradlew clean assembleDebug</p><p>Post-build Actions-&gt;archive the artifacts에</p><p>*/build/**/*.apk</p><p>입력한다.</p><p>참고:</p><p>https://softwaree.tistory.com/62</p><p>https://medium.com/temy/android-ci-with-jenkins-docker-and-kitematic-step-by-step-b40ddbcaf5ff</p><p><br /></p><p>4.Build Now 하면 빌드가 되고 apk 를 다운받을수 있도록 해준다.</p>