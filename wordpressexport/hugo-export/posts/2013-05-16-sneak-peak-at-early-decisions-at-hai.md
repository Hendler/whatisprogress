---
title: Sneak peek at early decisions at HAI
author: hendler
type: post
date: 2013-05-16T19:37:47+00:00
url: /?p=77
publicize_reach:
  - 'a:2:{s:7:"twitter";a:1:{i:2996358;i:640;}s:2:"wp";a:1:{i:0;i:1;}}'
publicize_twitter_user:
  - hendler
tagazine-media:
  - 'a:7:{s:7:"primary";s:0:"";s:6:"images";a:0:{}s:6:"videos";a:0:{}s:11:"image_count";i:0;s:6:"author";s:7:"7513308";s:7:"blog_id";s:8:"47339107";s:9:"mod_stamp";s:19:"2013-05-16 20:16:00";}'
categories:
  - HAI
tags:
  - AI
  - aws
  - java
  - Machine Learning
  - nlp
  - php
  - python
  - scala
  - zeromq

---
Recently launched a site with some basic vision behind HAI.

<a title="HAI - Human Assisted Intelligence" href="http://hai.io" target="_blank">http://hai.io</a>

But the tech stack is where the rubber meets the road. <span style="line-height:1.6;">I&#8217;ve been coding about two months now. At the very beginning I went through a fair amount of thinking and ended up selecting a language for the backend based on a number of factors. From languages I knew, C++, Go, PHP, Python, Java/Scala, and Node.js were on the table. Python and Java were the two top contenders, but I ended up going with Python. </span>

[googleapps domain=&#8221;docs&#8221; dir=&#8221;spreadsheet/pub&#8221; query=&#8221;key=0AtSfzP3z6m_6dElyYi1xaUpQQUwxNTJwYWVCR3JBYUE&output=html&widget=true&#8221; width=&#8221;500&#8243; height=&#8221;300&#8243; /]

So far I&#8217;ve been really happy with Python for both flexibility of the language, the available libraries for both web and machine learning, and the developer community. Ruby / Rails has an amazing community and great web stack, but given my own lack of familiarity and less work being done in machine learning, it didn&#8217;t make my list.

Then I started evaluating open source projects that would be the platform. There are 132 on the list below (looked at least 4x that many). It&#8217;s been amazing getting up to speed on the projects that are open source. Although Google, IBM, Amazon and others are clearly going to lead in the machine learning space for the foreseeable future, the open source community is catching up.

[googleapps domain=&#8221;docs&#8221; dir=&#8221;spreadsheet/pub&#8221; query=&#8221;key=0AtSfzP3z6m_6dHdiNWV5S2dPNjNZemE2M052ZHhjREE&output=html&widget=true&#8221; width=&#8221;500&#8243; height=&#8221;300&#8243; /]

Open source is a moving target, and there&#8217;s no one size fits all when you are piecing together something new. So, I&#8217;ve been using the awesome <a href="http://www.zeromq.org/" target="_blank">ZeroMQ</a> library to connect services between libraries, languages.

Finally, thanks to everyone who has provided feedback so far. Can&#8217;t wait to get what I&#8217;m working on out into the world.