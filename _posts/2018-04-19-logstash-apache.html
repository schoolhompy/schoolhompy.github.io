---
layout: post
title: logstash 아파치 apache 설정
date: '2018-04-19T22:49:00.001-07:00'
author: schoolhompy
tags:
- ELK
modified_time: '2018-04-19T23:30:32.693-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-6214920256741516647
blogger_orig_url: https://yunhos.blogspot.com/2018/04/logstash-apache.html
---

http://hhjeong.tistory.com/109<br /><br />설정파일 : logstash-apache.config<br /><br />input {<br />&nbsp; &nbsp; &nbsp;file {<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;path =&gt; "C:\Bitnami\elk-6.2.3-0\apache2\logs\access.log"<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;start_position =&gt; beginning<br />&nbsp; &nbsp; &nbsp;}<br />&nbsp;}<br />&nbsp; &nbsp;<br />&nbsp;filter {<br />&nbsp; &nbsp;if [path] =~ "access" {<br />&nbsp; &nbsp; mutate { replace =&gt; { type =&gt; "apache_access" } }<br />&nbsp; &nbsp; grok {<br />&nbsp; &nbsp; &nbsp; match =&gt; { "message" =&gt; "%{COMMONAPACHELOG}" }<br />&nbsp; &nbsp; }<br />&nbsp; &nbsp; date {<br />&nbsp; &nbsp; &nbsp; match =&gt; [ "timestamp" , "dd/MMM/yyyy:HH:mm:ss Z" ]<br />&nbsp; &nbsp; &nbsp; locale =&gt; en<br />&nbsp; &nbsp; }<br />&nbsp; &nbsp; useragent {<br />&nbsp; &nbsp; &nbsp; source =&gt; "agent"<br />&nbsp; &nbsp; &nbsp; target =&gt; "useragent"<br />&nbsp; &nbsp; }<br />&nbsp; } else if [path] =~ "error" {<br />&nbsp; &nbsp; mutate { replace =&gt; { type =&gt; "apache_error" } }<br />&nbsp; } else {<br />&nbsp; &nbsp; mutate { replace =&gt; { type =&gt; "random_logs" } }<br />&nbsp; }<br /><br />&nbsp;}<br /><br />&nbsp;output {<br />&nbsp; &nbsp; &nbsp;elasticsearch {<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;hosts =&gt; [ "127.0.0.1:9200" ]<br />&nbsp; &nbsp; &nbsp;}&nbsp;<br />&nbsp; &nbsp; &nbsp;stdout { codec =&gt; rubydebug }<br />&nbsp;}<br /><br /><br />출처: http://hhjeong.tistory.com/109 [후니의 개발일지]