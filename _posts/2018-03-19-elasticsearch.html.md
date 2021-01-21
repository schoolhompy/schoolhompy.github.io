---
layout: post
title: 'ElasticSearch 를 윈도우에 설치하고 테스트 할때, '
date: '2018-03-19T07:57:00.000-07:00'
author: schoolhompy
tags:
- ELK
modified_time: '2018-03-31T06:26:57.618-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-8991003712513682129
blogger_orig_url: https://yunhos.blogspot.com/2018/03/elasticsearch.html
---

<pre style="white-space: pre-wrap; word-wrap: break-word;"></pre><pre style="white-space: pre-wrap; word-wrap: break-word;">참고 : https://stackoverflow.com/questions/48209323/content-type-header-application-x-www-form-urlencoded-is-not-supported</pre><pre style="white-space: pre-wrap; word-wrap: break-word;"></pre><pre style="white-space: pre-wrap; word-wrap: break-word;"></pre><pre style="white-space: pre-wrap; word-wrap: break-word;">-텍스트일떄는</pre><pre style="word-wrap: break-word;"><span style="white-space: pre-wrap;">curl -XGET </span>localhost:9200/ -H "Content-Type: application/json" -d "{\"query\": {\"simple_query_string\" : {\"fields\" : [\"content\"], \"query\" : \"foo bar -baz\"}}}"</pre><pre style="word-wrap: break-word;"><span style="white-space: pre-wrap;"><br /></span></pre><pre style="white-space: pre-wrap; word-wrap: break-word;">-json 파일일때는</pre><pre style="white-space: pre-wrap; word-wrap: break-word;">curl -XPOST localhost:9200/classes/class/1/ -H "Content-Type: application/json" -d @onclass.json</pre><pre style="white-space: pre-wrap; word-wrap: break-word;"></pre><pre style="white-space: pre-wrap; word-wrap: break-word;">_bulk 집어넣을떄 kibana 에서 편하게</pre><pre style="white-space: pre-wrap; word-wrap: break-word;">Dev Tools 에서</pre><pre style="white-space: pre-wrap; word-wrap: break-word;">POST _bulk</pre><pre style="word-wrap: break-word;"><span style="white-space: pre-wrap;">{ "index" : { "_index" : "basketball", "_type" : "record", "_id" : "1" } }<br />{"team" : "Golden States Warriors","name" : "Stephen Curry", "points" : 30,"rebounds" : 3,"assists" : 4, "blocks" : 5, "submit_date" : "2016-10-11"}<br />{ "index" : { "_index" : "basketball", "_type" : "record", "_id" : "2" } }</span></pre><pre style="word-wrap: break-word;"><span style="white-space: pre-wrap;">....</span></pre><pre style="word-wrap: break-word;"><span style="white-space: pre-wrap;"><br /></span></pre>