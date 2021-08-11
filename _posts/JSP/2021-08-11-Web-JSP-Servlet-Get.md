---
layout: post
title: "[Web-JSP-Servlet] Get 방식의 요청"
author: "Bananag"
tags: JSP, Servlet
---

<br>

- Serlvet 파일

  GET 방식의 요청이 전송되는 경우에는 Servlet파일 내의 doGet 메소드가 호출되어 처리함

  <blockquote>
      doGet(HttpServletRequest request, HttpServletResponse response)
  </blockquote>

<br>

### 1. Form 태그를 사용한 GET 방식의 요청 처리

- HTML 파일

  ```html
  <!DOCTYPE html>
  <html>
      <head>
          ...
      </head>
      <body>
          ...
          <form action="" method="get"> // form 태그
              ...
          </form>
      </body>
  </html>
  ```

  

<br><br>

### 2. a 태그를 사용한 GET 방식의 요청 처리

- HTML 파일

  ```html
  <body>
      <a href="요청URL?파라미터이름=파라미터값">____</a>
      <!-- 여러 파라미터를 나열하고 싶을 경우 '&'를 붙여 이어가면 됨-->
  </body>
  ```

<br><br><br>

### 3. 주소 표시줄에 URL을 직접 입력하여 요청하는 GET 방식의 요청 방식

- Servlet 파일(예시)

  ```java
  ...
  ...
  protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
      // name과 age 파라미터를 받아 각 변수에 저장
      String name = request.getParameter("name");
      String age = request.getParameter("age");
      
      // 응답하는 데이터 타입을 html 타입으로 지정
      // charset=euc-kr로 지정하여 응답데이터들의 한글처리 수행
      request.setContentType("text/html;charset=euc-kr");
      
      // 문자열 단위로 response 객체에 내용을 출력할 수 있는 출력 스트림을 생성
      PrintWriter out = response.getWriter();
      
      // 응답에 name과 age 변수 값을 출력
      out.println("이름 : " + name + " <br>");
  	out.println("나이 : " + age + " <br>");
  }
  ```

  위의 Servlet 파일을 실행한 후

  URL뒤에 전송할 파라미터 값을 추가하면

  파라미터 값이 GET방식으로 Servlet에 전송됨

  <img width="640" alt="web_jsp_servlet_get" src="https://user-images.githubusercontent.com/61573968/129047113-cc87e46c-1449-4a98-baa0-abf324cfa08a.PNG">

  URL뒤에 ''?name=myname&age=50'을 기입함으로써 출력됨



<br><br><br><br>[참고자료]

오정원, JSP 2.3 & Servlet 3.1, 혜지원(2017)