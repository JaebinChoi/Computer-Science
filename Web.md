## MVC 패턴
#### 코드의 재사용에 유용
#### 사용자 인터페이스와 응용 프로그램 개발에 소요되는 시간을 줄여주는 효과적인 설계 방식
#### Model, View, Controller로 구서어
    Model : 핵심적인 비즈니스 로직을 담당하며, 데이터베이스를 관리
    View : 사용자에게 보여주는 화면
    Controller : 모델과 뷰 사이에 정보를 교환할 수 있도록 연결시켜주는 역할
---
## MVC1 VS MVC2
#### MVC1
    클라이언트 요청을 JSP가 처리, JSP가 Controller와 View의 기능 모두 담당 -> 하나의 JSP 파일에 Java, HTML, Javascript를 사용
    Model은 JDBC 인터페이스로 DB 조작
    장점 : 페이지 흐름이 단순, 구조가 간단 -> 중소형 프로젝트에 적합
    단점 : 유지보수 어려움, 규모가 커질수록 복잡
#### MVC2
    라이언트 요청을 Servlet에서 처리
    JSP가 View를 담당
    Model은 1이랑 똑같음
    장점 : 유지보수 용이, Controller와 View의 분리로 명료한 구조를 가짐
    단점 : 구조 설계를 위한 시간이 많이 소요, 수준 높은 이해도 필요
---
## Servlet VS JSP (Java Server Pages)
#### Servlet
    서버에서 웹 페이지를 동적으로 생성하거나 데이터 처리를 수행하기 위해 Java로 작성된 프로그램
    Java 코드 안에 HTML 태그가 삽입
#### JSP
    서블릿의 단점을 보완하고자 만든 서블릿 기반의 스크립트 기술
    HTML 태그 안에 Java 코드가 삽입
