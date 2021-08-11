---
layout: post
title: "[Tomcat Server Error] Could not publish server configuration for Tomcat v9.0 Server at localhost."
author: "Bananag"
tags: TomcatErrors
---
<br>
#### Error
<blockquote>
    Could not publish server configuration for Tomcat v9.0 Server at localhost.
</blockquote>
<br>
<img width="246" alt="tomcatError_could_not_publish_server" src="https://user-images.githubusercontent.com/61573968/128979264-4766464a-8daf-447d-9307-f28590ea57ae.PNG">
<br>
<br>


#### 해결법

1. Servers --> Tomcat Server at localhost 더블 클릭 --> Modules -> Edit으로 path 재수정
<img width="510" alt="tomcatError_modules" src="https://user-images.githubusercontent.com/61573968/128979268-661ccc75-ff3f-4dab-a1ac-56da297c5d30.PNG">

2. Servers --> Tomcat Server at localhost 클릭 --> Web Module 하나만 남기고 삭제

