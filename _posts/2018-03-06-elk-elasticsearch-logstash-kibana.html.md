---
layout: post
title: ELK = Elasticsearch + Logstash + Kibana
date: '2018-03-06T01:41:00.000-08:00'
author: schoolhompy
tags:
- ELK
modified_time: '2018-03-31T19:05:11.902-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-3563418851787074658
blogger_orig_url: https://yunhos.blogspot.com/2018/03/elk-elasticsearch-logstash-kibana.html
---

0.먼저 이해<br />Logstash 로 서버 로그 수집프로그램. 여기서 수집한 정보는 Elasticsearch 에게 json 으로 쏜다.그걸 kibana 에서 쿼리로 그래픽분석하는 흐름<br /><br />0-1. Logstash<br />-https://evilimp79.wordpress.com/2014/10/23/logstash-이해하기/<br />-http://asuraiv.blogspot.jp/2015/07/elasticsearch-logstash.html *설치와기본개념<br />test.conf 에 아래처럼입력하고 logstash -f test.conf 하면<br />input {<br />&nbsp; &nbsp; &nbsp; &nbsp; stdin{ }<br />}<br />filter {<br />}<br />output {<br />&nbsp; &nbsp; &nbsp; &nbsp; stdout {<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; codec =&gt; rubydebug { }<br />&nbsp; &nbsp; &nbsp; &nbsp; }<br />}<br />아래가 출력<br />desuk<br />{<br />&nbsp; &nbsp; "@timestamp" =&gt; 2018-03-06T07:48:31.450Z,<br />&nbsp; &nbsp; &nbsp; "@version" =&gt; "1",<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; "host" =&gt; "pc1.local",<br />&nbsp; &nbsp; &nbsp; &nbsp;"message" =&gt; "desuk"<br />}<br /><div><br /></div><br />