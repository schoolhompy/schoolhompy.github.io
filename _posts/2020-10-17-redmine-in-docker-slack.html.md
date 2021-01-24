---
layout: post
title: Redmine in Docker 에서 Slack 연동하기
date: '2020-10-17T21:15:00.001-07:00'
author: schoolhompy
categories:
- DEVOPS
tags:
- Redmine
- Slack
modified_time: '2020-10-17T21:15:05.394-07:00'
thumbnail: https://1.bp.blogspot.com/-hJtamU25kyg/X4vAi-eLYLI/AAAAAAABFeY/1zyLy45D54ULHPr5BhxoLKiy9O1QsxwsACLcBGAsYHQ/s72-c/Screen%2BShot%2B2020-10-18%2Bat%2B13.11.05.png
blogger_id: tag:blogger.com,1999:blog-4954243635432022205.post-1086982596604259859
blogger_orig_url: https://yunhos.blogspot.com/2020/10/redmine-in-docker-slack.html
---

도커로된 레드마인에 슬랙을 연동해보자.<div><br /></div><div>참고 :&nbsp;https://jhb.kr/397&nbsp;</div><div><br /></div><div>쉽다.</div><div><br /></div><div>도커로 공식 레드마인 컨테이너 띄우고,</div><div>컨터이너쉘로 들어가서 plugin 으로 이동한다.</div><div><br /></div><div><br /></div><div><div>wget https://github.com/sciyoshi/redmine-slack/archive/master.zip</div><div>또는&nbsp;</div><div>git clone https://github.com/sciyoshi/redmine-slack.git redmine_slack</div></div><div><br /></div><div><br /></div><div>해서 플러그인을 가져온다.</div><div>bundle install</div><div><br /></div><div>하고 컨터이너를 재가동한다.</div><div><br /></div><div>레드마인에 admin으로 접속해서 plugin메뉴에 가보면 아까 추가한 슬랙이 있다.</div><div><br /></div><div class="separator" style="clear: both; text-align: center;"><a href="https://1.bp.blogspot.com/-hJtamU25kyg/X4vAi-eLYLI/AAAAAAABFeY/1zyLy45D54ULHPr5BhxoLKiy9O1QsxwsACLcBGAsYHQ/s2674/Screen%2BShot%2B2020-10-18%2Bat%2B13.11.05.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" data-original-height="1164" data-original-width="2674" src="https://1.bp.blogspot.com/-hJtamU25kyg/X4vAi-eLYLI/AAAAAAABFeY/1zyLy45D54ULHPr5BhxoLKiy9O1QsxwsACLcBGAsYHQ/s320/Screen%2BShot%2B2020-10-18%2Bat%2B13.11.05.png" width="320" /></a></div><div class="separator" style="clear: both; text-align: center;"><br /></div><div class="separator" style="clear: both; text-align: left;">슬랙에서 add apps -&gt;&nbsp;Incoming WebHooks 를 선택한다. 거기서 나오는 hook주소를 복사해서 위의 설정에 넣는다.</div><div class="separator" style="clear: both; text-align: left;"><br /></div><div class="separator" style="clear: both; text-align: left;">레드마인에서 이슈를 생성해본다.</div><div class="separator" style="clear: both; text-align: left;"><br /></div><div class="separator" style="clear: both; text-align: center;"><a href="https://1.bp.blogspot.com/-_dpAAsGe7qk/X4vBFslnmEI/AAAAAAABFeg/jAgZGfNbgCkKwdEgw57IcZI5xII8ps5lwCLcBGAsYHQ/s2280/Screen%2BShot%2B2020-10-18%2Bat%2B13.13.59.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" data-original-height="1130" data-original-width="2280" src="https://1.bp.blogspot.com/-_dpAAsGe7qk/X4vBFslnmEI/AAAAAAABFeg/jAgZGfNbgCkKwdEgw57IcZI5xII8ps5lwCLcBGAsYHQ/s320/Screen%2BShot%2B2020-10-18%2Bat%2B13.13.59.png" width="320" /></a></div><div class="separator" style="clear: both; text-align: left;">잘간다.</div><div class="separator" style="clear: both; text-align: left;"><br /></div><div class="separator" style="clear: both; text-align: left;">이건 정말 심플한 플러그인이지만 좀 더 좋은 플러그인도 많다.(다만 설정이 복잡)</div><br /><div class="separator" style="clear: both; text-align: left;"><br /></div><br /><div><br /></div>