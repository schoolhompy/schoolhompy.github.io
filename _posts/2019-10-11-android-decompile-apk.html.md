---
layout: post
title: Android Decompile 해서 다시 apk 로 만들어보기
date: '2019-10-11T00:46:00.001-07:00'
author: schoolhompy
categories:
- MOBILE DEV
tags:
- android

modified_time: '2019-10-11T00:46:37.896-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-2539360412591276027
blogger_orig_url: https://yunhos.blogspot.com/2019/10/android-decompile-apk.html
---

-1 apktool 명령어로 해보기<br /><br />1.java -jar apktool_2.4.0.jar d 앱이름.apk<br />2.압출풀린 폴더가 생긴다.<br />3.Manifest.xml 에 application 태그에&nbsp; android:debuggable="true"&nbsp; 을 추가함.<br />4.java -jar apktool_2.4.0.jar b 앱이름폴더<br />5.임시키를 만듬<br />"C:\Program Files\Java\jre1.8.0_191\bin\keytool.exe" -genkey -v -keystore my-release-key.keystore -alias alias_name -keyalg RSA -keysize 2048 -validity 10000<br />6.그 키로 jar 싸인<br />"C:\Program Files\Java\jdk1.8.0_191\bin\jarsigner.exe" -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore my-release-key.keystore com.nttdocomo.android.dpoint_2019-09-24.apk alias_name<br />7.에뮬레이터에 던져넣기.<br /><br /><br />-2 java 원본보기<br />dex2jar<br />- apk파일이나 apk파일에 포함된 classes.dex파일을 .jar파일로 변환<br /><br /><br /><br />사용법<br /><br />1.dex2jar 폴더 안에 apk 파일 넣기<br />2.해당 폴더에서 명령창 띄어 jar 파일 생성<br />dex2jar.bat [디컴파일할 apk]:bat 파일에 던져넣어도됨.<br />3.JD-GUI 에서 보기<br /><br />https://programist.tistory.com/entry/Apktool%EC%9D%84-%EC%9D%B4%EC%9A%A9%ED%95%9C-%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-apk-%ED%8C%8C%EC%9D%BC-%EB%94%94%EC%BB%B4%ED%8C%8C%EC%9D%BC-%EB%B0%8F-%EB%A6%AC%ED%8C%A8%ED%82%A4%EC%A7%95<br /><br /><br />-3 bytecode-viewer<br />https://brunch.co.kr/@c4u/23