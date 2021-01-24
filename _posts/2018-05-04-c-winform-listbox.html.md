---
layout: post
title: C# Winform listBox 선택된 아이템 간단히 얻기
date: '2018-05-04T03:20:00.002-07:00'
author: schoolhompy
tags:
- "C#"
modified_time: '2018-05-04T03:20:40.433-07:00'
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-2549327841230095194
blogger_orig_url: https://yunhos.blogspot.com/2018/05/c-winform-listbox.html
---

&nbsp;this.textBox1.Text = (string)listBox1.SelectedItem ?? "not Selected";<br />string 은 오브젝트로 바꿔도됨.