# basic-aspnet-2024
IoT 개발자과정 ASP.NET 리포지토리

## 1일차
- 웹기술 개요
    - World Wide Web 은 인터넷의 한 파트
    - Full-Stack
        - Front-end : 웹사이트 화면으로 사람들에게 보이는 부분 기술
        - Back-end : 웹사이트 뒤에서 동작하는 서버기술
        - Server-Operation : 하드웨어, OS, SW등 운영(클라우드)

- 업무용 웹 사이트 참조
    - https://www.ecount.com/kr/ECK/ECK004M_CN.aspx

- Front-end(클라이언트)
    - HTML5
    - CSS3
    - Javascript

- Back-end(서버)
    1. Java - Spring, Spring Boot, JSP, EJB ...
    2. Javascript - Node.js, Express ...
    3. Python - Django, Flask, fastAPI ...
    4. C# - ASP.NET 
    5. Ruby - Ruby on rails
    6. C - cgi, fasCGI ...
    7. PHP 

- 개발
    - 프론트엔드 전부 + 백엔드 여러개 중 하나 + DB
    - 웹 브라우저에서 F12(개발자도구)
    - VS Code 플러그인 
        - HTML Code Snippet(설치 후 , Ctrl+Space 누른 후 html 적고 Tab)
        - Live Server

- HTML5
    - XML(eXtensible Markup Lang)이 웹페이지 구성하기 위한 선행기술, 너무 복잡해서 간략화 시킨 것
    - Hyper Text Markup Language
    - 기본적으로 확장자 .html
    - TIP! lorem 탭, 긴 샘플텍스트 생성
    - 기본태그(body)
        - h1 ~ h6 : 제목(마크다운 #, ##와 동일)
        - p : 일반문장
        - div, span : 그룹화 구분자, 아주 중요!(CSS 연계 디자인)
        - img : 이미지 표현
        - br : 한줄 내리기(엔터)
        - hr : 가로선
        - 특수문자 : & ; 사이에 영문자로 표시(너무 많음..)
        - strong 또는 b : 볼드체
        - em 또는 i : 이탤릭체
        - mark : 형광펜 효과
        - small, sub, sup : 글자 작게, 아래첨자, 윗첨자
        - u, strike : 밑줄, 취소선
        - a : 웹페이지 링크(중요!)
        - ul, ol > li : 순서없는 목록, 순번있는 목록
        - table, tr, th, td : 테이블 만드는 태그
        - audio, video : 오디오, 비디오
        - object, embed : 객체 추가

    - HTML + CSS + Javascript
        - 내부 스타일, 외부 스타일, 인라인 스타일
        - 내부 스크립트, 외부 스크립트, 인라인 스크립트

    - 오류, 디버그
        - F12 개발자도구로 활용

    - 양식태그(body > form안에 사용 필수)
        - front-end 입력한 내용이 back-end로 보내기 위한 관문
        - form 을 반드시 사용
        - input
            - type = "text" : 텍스트박스
            - type = "password" : 비밀번호 박스
            - type = "button" : 일반버튼
            - type = "submit" : 제출(!)
            - checkbox : 체크박스
            - radio : 라디오버튼
            - file : 파일 업로드
            - image : 이미지(img 와 유사)
            - reset : form내의 입력양식 태그값들이 초기화
        - textarea : 여러행 텍스트 입력
        - select, option : 콤보박스
        - fieldset : 그룹박스
        - submit 클릭 loopback(값 전달) 발생
        - 값 전달 방법
            - GET : URL뒤 ? 다음에 key=value&key=value ... 데이터 전달 
            - POST : 화면 뒤로 숨겨서 데이터 전달 방식
        
    - 공간구분 태그
        - span : 인라인 형식으로 공간 분할(한줄로 공간구성)
        - div : 블록 형식으로 공간 분할

## 2일차
- HTML5
    - 시맨틱 웹 - 시멘틱 태그로 화면 구조를 잡는 웹구성 방식
        - header,main, content, nav, footer, aside, section, article ... 구조태그(화면에 안나타남) 사용
        - 시맨틱 태그를 div로 바꿔도 똑같이 동작하기 때문에 요새는 많이 사용안함. 걷어내고 있는 추세

- CSS3
    - 웹 디자인 핵심, Cascading Style Sheets 
    - 상단에서부터 <body> 부터 하위에 태그들 계속해서 적용되는 스타일이라는 뜻
    - 선택자에게 주어지는 디자인 속성
    - 선택자(selector)
    - 속성(property)
    - 배경, 폰트 ...
    - 레이아웃
        - HTML 만으로는 화면 레이아웃이 만들어지지 않음
        - 중앙정렬, 원트루, 고정바..
    - 반응형 웹(Responsive Web)
        - 메타태그 viewport를 사용하면 그때부터 반응형 웹이 됨!
        ```html
        <meta name='viewport' content='width=device-width, initial-scale=1'>
        ```
        - @media 태그 : 디바이스 종류별로 CSS 따로 디자인 가능
        
## 3일차
- Javascript
    - 스크립트 언어, ECMAScript
    - 웹 브라우저 주로 사용
    - 바닐라스크립트 : 완벽하게 기본에 충실한 자바스크립트
    - 기본적으로 클라이언트(웹 브라우저에서 프론트엔드에 표시) 베이스
    - Node.js : 자바스크립트로 백엔드를 구현(파이썬과 유사)
    - 특징
        - 자료형 선언이 없음. var 변수 선언
        - 인터프리터 언어(not Compile Lang) -> 실행파일이 만들어 지는 것 
        - 확장자 .js
        - 속도가 컴파일 언어에 비해서 느림
        - VS Code도 자바스크립트로 만든 앱
        - 문장끝 ; 은 생략 가능, but 최대한 쓸 것 
        - 정수와 실수를 구분하지 않음
        - 0으로 나눠도 예외가 발생하지 않음
        - 파이썬과 동일하게 ', " 모두 사용  
        - 완전히 동일함을 비교하는 === 연산자
        - 변수선언시 let(일반), var(지역변수), const(상수) 
        - HTML 태그와 연계(DOM) 중요!!

    - DOM(Document Object Model)!!
        - 실행 순서!
        - HTML에 있는 모든 요소를 제어할 수 있음
        - html 애니메이션, 게임, 통신 모두 가능
        - 이벤트 on- 으로 시작
            - onload : 화면이 다 렌더링되면 그 다음 발생
            - onfocus : 객체에 마우스를 클릭해서 포커스가 가면 발생
            - onclick : 객체를 마우스로 클릭하면 발생
            - ondbclick : 더블클릭
            - onmousemove : 마우스를 이동하면 발생
            - onmouseover : 객체 위에 마우스가 올라가면 발생
            - onkeydown, onkeypress : 객체에서 키보드를 타이핑하면 발생
            - ...

    - jQuery
        - 자바스크립트 라이브러리
        - js를 매우 편리하게 사용할 수 있도록 도와주는 서포트 라이브러리
        - 순식간에 웹개발 업게를 장악했던 라이브러리
        - 사용빈도가 줄고는 있지만 아직도 80% 웹사이트가 사용 중
        - js 파일 다운로드 후 사용하거나
        - CDN 링크를 사용하는 방법 (추천)

## 4일차
- HTML + CSS + js(jQuery) 응용
    - jQuery 응용
        - javascript와 jQuery를 혼용해도 상관없음
        - jQuery로 코딩이 편할때와, javascript가 편할 때가 있음
    - Bootstrap
        - 오픈소스 CSS 프레임워크
        - 트위터 블루프린트 -> 부트스트랩
        - 현재 전세계에서 가장 각광받는 프레임워크 중 하나
        - CSS를 동작시키기 위해서는 Javascrpit도 포함
        - 소스 다운로드 받아서 사용(1), CDN으로 링크만 사용(2)
            - 제한된 네트워크에서는 1번
            - 인터넷에 항상 연결된 환경에서는 2번이 편리
        - 핵심!
            - Bootstrap은 화면사이즈를 12등분!
                - 12를 넘어서면 디자인이 깨짐!!!
            - container 밑에 마치 table처럼 div를 구분해서 사용
            - container > row > col div 태그에 클래스 정의
        - 부트스트랩 학습에 시간을 들이는 게 아님. Copyleft가 정석!
            - https://getbootstrap.com/docs/5.3/getting-started/introduction/ 참조
            - https://getbootstrap.com/docs/5.3/examples/ 스니펫을 활용 추천
        - 무료 테마(템플릿)가 아주 잘되어 있음
            - https://startbootstrap.com/

    - 웹페이지 클로닝
        - 핀터레스트 타입 + 부트스트랩 웹페이지 만들기(진행중)

## 5일차
- HTML + CSS + js(jQuery) 응용
    - 웹페이지 클로닝
        - 핀터레스트 + 부트스트랩 웹페이지 만들기(완료)

    - https://github.com/qkrskdusdlqslek/basic-aspnet-2024/assets/158007421/89180b03-5888-4d9f-93d0-3c7c390e79f4

        - Codehal 유튜버 로그인 웹페이지 튜토리얼 따라하기
            
            ![login](https://raw.githubusercontent.com/qkrskdusdlqslek/basic-aspnet-2024/main/day05/images/login.png)
        
        - Codehal 슬라이더 애니메이션 웹페이지 튜토리얼 따라하기
        
## 6일차
- HTML + CSS + js(jQuery) 응용
    - 웹페이지 클로닝
        - Codehal 슬라이더 애니메이션 웹페이지 튜토리얼 따라하기(완료)
    
    https://github.com/qkrskdusdlqslek/basic-aspnet-2024/assets/158007421/0d34e9fb-bbab-43b9-97f2-1f36a22c7095


    - 개인 웹페이지 클로닝
        - Weather_App(진행중)

## 7일차
- 개인 웹페이지 클로닝
    - Weather_App(완료)

    https://github.com/qkrskdusdlqslek/basic-aspnet-2024/assets/158007421/1de2ee20-c9f8-4aa0-a3c2-be47559d4caa
    
    - Personal Portfolio Website(진행중)


https://github.com/qkrskdusdlqslek/basic-aspnet-2024/assets/158007421/72cd7078-6174-4751-a6a4-a5fda667a83b



## 8일차
- ASP.NET
    - ASP.NET 역사
        - 1990년대 MS가 웹 서버기술로 ASP(Active Server Page)를 배포. like JSP(Java Server page)
        - ASP는 .NET으로 된 언어가 아닌, VBScript를 사용, 확장자(.asp)
        - 스파게티 코드! - HTML + CSS + javascript + VBScript 짬뽕으로 만든 웹 페이지
        - 많이 사용되었지만, 유지보수 어렵고, 성능이 나쁨.. 

        - 2000년대 MS가 .NET Framework를 발표.
        - C#, VB.NET, C++.NET 등의 새로운 언어를 배포, 여기에 맞춰서 웹 서버기술을 다시 만듬 -> ASP.NET
        - 가장 큰 장점은 윈폼 개발하는 것처럼 웹개발 가능
        - 초창기에는 스파게티 코드를 거의 그대로 사용, 성능도 안좋고, 속도 느림..
        - 2009년 ASP.NET MVC(Model View Controller 디자인패턴) 공표. 성능은 좋아짐.
        - 하지만, 윈도우에서만 동작
        - 2016년 모든 OS플랫폼에서 동작할 수 있는 .NET Core를 재출시
        - 거기에 웹 서버기술을 또 다시 만듦 -> ASP.NET Core  
    
    - .NET Core(현재는 .NET 9.0, Core라는 이름은 사용안함)의 장점
        - 빠르고, 오픈소스
        - 크로스 플랫폼, os에 종속받지 않음
        - 성능!

    - ASP.NET 종류
        - ASP.NET Webforms - 2000년도 초반에 나오다가 사장된 웹사이트 개발기술(X)
        - **ASP.NET Core 웹앱(MVC) - 가장 기본적인 프론트엔드(HTML, CSS, JS .cshtml) + 백엔드(C# .aspx.cs) 웹사이트개발**
        - **ASP.NET Core 웹 API - 데이터포털, 네이버, 카카오, 영화API 사이트를 만드는 백엔드(프론트엔드가 없어서 화면이 없음)**
        - Js(Vue, Angular, React) 프론트엔드 + ASP.NET Core 백엔드 
        - Edge용 웹 드라이버 테스트 - 엣지 브라우저에 종속된 테스트용(X)
        - ASP.NET Core gRPC 서비스 - 고성능 원격프로시저호출(스트리밍 호출) 서비스
        - Blazor - Js 프론트엔드를 따라서 C# 컴포넌트 기반으로 개발하는 웹개발 방식 웹사이트 개발
        - Razor - 프론트엔드 개발에 C# 코드가 특화되서 사용되는 웹사이트 개발방식 
        - .NET Aspire - Blazor 프론트엔드 + Redis + 웹 API 백엔드 

    - 참조사이트
        - https://learn.microsoft.com/ko-kr/aspnet/core/?view=aspnetcore-3.1
        - https://github.com/dotnet 
        - https://mixedcode.com/
        - https://github.com/gilbutITbook/006824

    - ASP.NET Core 웹앱(Model-View-Controller)
        - 현재 기본적인 웹개발의 가장 표준
        - Java 계열도 Spring (Boot) MVC로 개발
        - MVC 개념도
        
        <img src="https://raw.githubusercontent.com/qkrskdusdlqslek/basic-aspnet-2024/main/day09/images/an0002.png" width="730">

        - 프론트엔드가 예전엔 스파게티코드가 무지 심했다면, 현재는 스파게티코드가 최소화 되어있음.(SpringBoot, Python flask든 모두 동일)
        - IIS Express Server - VS에서 ASP.NET 웹사이트를 운영하는 개발용 웹서버
        - index.* - 웹사이트 가장 대문되는 페이지 이름 
        - 파일 저장시 핫다시로드(HotReload) 체크
        - @로 시작하는 C# 구문. Tag helper, Html helper 로 HTML 구문 내에 C# 코드를 적어서 활용하는 방법 = Razor 구문
        - Action == HTML에서 form태그내 submit버튼 클릭! / 링크를 클릭하는 것, 윈앱에서 이벤트와 동일
        - 액션(이벤트)이 발생한 이후 처리하는 메서드의 결과를 ActionResult
        - 콘솔 서버로그 잘 확인할 것, 프로세스가 종료되면 웹사이트 실행 안됨.

    - 데이터베이스 연동방법
        - DB first - 가장 전통적인 DB 연동방식. DB설계, DB구축, C#과 연동
        - Code first - 최근 트렌드가 되는 DB 연동방식. C# 엔티티 클래스 작성, DB연결 설정 후 실행하면 DB에  테이블이 생성 
        - EntityFramework를 사용하면 아주 손쉽게 구축가능

    - EntityFramework(Core) 설치
        - Microsoft.EntityFrameworkCore
        - Microsoft.EntityFrameworkCore.Tools
        - Microsoft.EntityFrameworkCore.SqlServer
        
    - Code first 구현순서
        - ASP.NET 프로젝트 생성
        - EF 패키지 설치
        - 엔티티 클래스 작성
        - appsettings.json에 DB연결문자열 추가
        - Data/ApplicationDbContext.CS 중간연결 클래스 생성
        - Program.CS Services 내에 DbContext 종속성을 주입
        - NuGet 패키지 관리자 > 패키지 관린자 콘솔 실행
            ```shell
            PM> Add-Migration 마이그레이션명
            Build started...
            Build succeeded.
            ...
            PM> Update-Database
            ...
            Done.
            ```

## 9일차(07.16)
- ASP.NET Core MVC
    - 필요 이론
    - 연습
    - 개인 포트폴리오 웹사이트 
    - Bootstrap 테마 적용

    - Model은 개발자가 따로 만듦
    - View, Controller 폴더는 미리 만들어짐
    - 웹브라우저에서 접근할 페이지를 만들려면(작업순서)
        1. 해당 컨트롤러를 생성
        2. 뷰를 같이 생성할지 나중에 따로 만들지 선택
        3. 컨트롤러 이름과 동일한 뷰 폴더, 메서드 이름과 동일한 cshtml 페이지가 생성
        4. 컨트롤러에 모델에 DB와 연결될 내용을 작성
        5. 모델내용을 뷰로 리턴

- ASP.NET Core 포트폴리오 웹사이트, MyPortfolio
    1. Visual Studio 에서 ASP.NET Core 웹앱(MVC) 프로젝트 생성
    2. 부트스트랩 템플릿 사이트, 알맞은 템플릿 다운로드
    3. wwwroot 폴더 밑에 템플릿 html,css,js,이미지 등 위치
    4. 템플릿 페이지에 공통적인 부분(Header, Bottom)은 _layout.cshtml 에 위치
    5. 중간에 페이지마다 변경되는 부분은 각 Views 밑에 포함
    6. _layout.cshtml 에 공통부분 옮기기
    7. index.cshtml에 index.html에서 공통부분 외 영역 옮기기
    8. index.cshtml 내용 수정

    9. ResumeController.cs 생성, DB관련된 설정이 없으면 모델, 뷰를 만들기 어려움
    10. Resume 란 폴더가 Views 아래에 만듦. index.cshtml
    11. resume.html에 네비게이션 아래 변경부분만 복사해서 index.cshtml에 붙여넣기
    12. Project, Contact도 동일하게 적용

    13. Code First방식으로 Board테이블 생성
    14. NuGet 패키지에서 Microsoft.Entity.FrameworkCore 패키지 검색, 설치
    15. Microsoft.EntityFramework.Core.Tools 검색, 설치
    16. Microsoft.EntityFramework.Core.sqlserver 검색, 설치
    17. model/Board.cs 로 엔티티 클래스 생성
    18. appsettings.json 에 DB 연결문자열 추가
    19. Data/ApplicationDbContext.cs 생성
    20. Program.cs에 DbContext 종속성 주입
    21. NuGet패키지 관리자 콘솔 > Add-Migration, Update-Database 진행
    22. _layout.cshtml Board 링크 수정
    23. /Controller/BoardController.cs를 생성(모델, 뷰 연결)
        - Entity Framework를 사용하며 뷰가 포함된 MVC컨트롤러

        <img src="https://raw.githubusercontent.com/qkrskdusdlqslek/basic-aspnet-2024/main/images/an0004.png">

## 10일차
- ASP.NET Core 포트폴리오 웹사이트, MyPortfolio
    1. Board.cs 멤버속성 ModeDate -> ModDate
        - BoardController.cs 에서 ModeDate->ModDate 변경
        - Views/Board/*.cshtml ModeDate-> ModDate 변경
    2. ASP.NET Core 템플릿으로 만들어주는 CRUD(Insert, Select, Update, Delete)
    3. 테이블 삭제, 재생성
    4. 게시판 관련된 화면 수정작업
        - Views/Board/Index.cshtml 게시판 리스트 화면 수정
        - Index.cshtml 테이블 틀 변경, 삭제, 수정, 상세버튼 삭제
        - Models/Board.cs에 테이블 한글이름 추가 ->[DisplayName("")]

        - Views/Board/Details.cshtml 부트스트랩 적용
        - 수정, 삭제 등 버튼 디자인적용
        - Views/Board/Create.cshtml 부트스트랩 적용
    
    5. SSMS에서 Board 테이블 Hit, RegDate, ModDate Null허용으로 변경

    6. 웹사이트 동작 순서
        1. https://localhost:7154/Board/Create 링크오픈
        2. BoardController -> Create 액션메서드
        3. Submit -> BoardController -> Create 액션메서드 발동
        4. Create 액션 메서드 내 로직처리 DB에 데이터 입력
        5. Models/Board.cs ModDate를 DateTime -> DateTime? 변경(물음표 넣으면 null 허용으로 변경됨)
        6. Edit 동일, Create.cshtml 내용을 그대로 복사/붙여넣기 단, asp-action="Edit"로 변경!!!

## 11일차(07.23)
- ASP.NET Core 포트폴리오 웹사이트, MyPortfolio
    1. EntityFramework로 SQL 사용없이 DB 핸들링
        - DbContext.Add(삽입), Update(수정), Remove(삭제) 기능 존재
        - 위의 명령을 실행 후 DbContext.SaveChangesAsync() 실행해서 실제 DB에 반영
        - ToListAsync(), FirstOrDefaultAsync()는 SELECT로 트랜잭션 발생X, 그래서 SaveChangeAsync()를 실행하지 않음
    2. 글 조회수 올리기
    3. 게시글 삭제
        - _layout.cshtml의 @await RenderSectionAsync("Scripts", required: false) 이 각 페이지에 필요시 스크립트영역을 만들어써라는 의미
        - AJAX 삭제는 나중에 다시!!!
    4. 페이징!!
        - 웹사이트에서 가장 중요한 기능 중 하나
        - 한페이지에 표시할 수 있는 글의 수를 제한
        - 스크롤 페이징, 번호 페이징
        - 번호 페이징
            1. BoardController.cs Index() 액션메서드 내 FromSql()로 변경(비동기 적용 안됨/ 비동기 부분 제거(async, await, Task<>)) 
            2. 페이징 쿼리 작성

                ```sql
                SELECT *
                    FROM (
                        SELECT ROW_NUMBER() OVER (ORDER BY Id DESC) AS rowNum
                                , Id
                                , Name
                                , UserId
                                , Title
                                , Contents
                                , Hit
                                , RegDate
                                , ModDate
                            FROM Board
                        ) AS base
                    WHERE base.rowNum BETWEEN 1 AND 10 -- 1과 10에 10씩 더하면 다음 페이지를 조회 쿼리
                ```


               https://github.com/user-attachments/assets/2e8e2ee4-e99f-435b-abfa-08dbae2cb357


                
            3. IndexI() 내 로직 수정
            4. Views/Board/Index.cshtml 화면코드 수정

    5. 검색
        - FromSqlRaw() 메서드 변경
        - html 링크에 ?page=1&search=검색어 추가

    6. HTML 에디터
        - Markdown 에디터
        - simpleemde(https://simplemde.com)
        - _layout.cshtml에 js, css 링크만 추가
        - 실제 사용페이지에서 특정 js만 실행
        - Create.cshtml, Edit.cshtml은 동일하게 작업
        - NuGet패키지 Westwind.AspNetCore.Markdown 설치

        <img src="https://raw.githubusercontent.com/qkrskdusdlqslek/basic-aspnet-2024/main/images/an0006.png">

## 12일차
- ASP.NET Core 포트폴리오 웹사이트, MyPortfolio
    1. 삭제로직 수정
        1. BoardController.cs 사용X -> BoardResController.cs 다시 생성
        2. /Views/Details.cshtml jQuery를 작업 팝업
        3. /Board/Index로 화면 전환

    2. 회원가입, 로그인, 권한
        1. /Model/User.cs 클래스 새성
        2. User클래스와 Board클래스간 관계형성 (virtual)
        3. AppDbContext.cs에 User DBset 추가
        4. Add-Migration, Update-Database 실행
        5. Program.cs에 로그인 세션 설정
        6. _layout.cshtml 로그인/로그아웃 메뉴 추가
        7. HomeController.cs Login/Logout 액션메서드 작성
        8. Login() 액션메서드 마우스 오른쪽 버튼 뷰생성 Login.cshtml 
        9. bootstrap 사이트에서 예제 파일 다운로드
        10. sign-in 폴더 내 index.html. sign-in.css Static 경로(wwwroot) 복사
        11. Login.cshtml을 위의 파일 참조해서 수정
        12. HomeController.cs 에 Register() 액션메서드 작성
        13. Register.cshtml 회원가입 페이지

## 13일차
- ASP.NET Core 포트폴리오 웹사이트, MyPortfolio
    1. 회원가입 계속..
        1. Register.cshtml에 asp-for로 변경
        2. HomeController.cs Register Post 메서드 작성
        3. Login.cshtml에 C# Razor tag로 변경
        4. HomeController.cs Login Post 메서드 작성
        5. Logout Get메서드 추가


        https://github.com/user-attachments/assets/2cbcd6c9-1815-4a66-bb40-a77d02bbcccf

    2. 게시판 글 오류 수정
        1. Board.cs에 있는 Name, UserID를 삭제, User?로 변경, UserName을 virtual 추가
        2. BoardController.cs 있는 Board 클래스와 관련된 변수도 삭제
        3. Views/Board/*.cshtml Name, UserID를 삭제, 변경
        4. BoardController.cs 게시글 리스트 쿼리 변경
        5. View/Board/*.cshtml 수정
        6. BoardController.cs에 Create Post 메서드에 사용자 데이터 추가 수정

    3. 프로젝트 파일업로드 
        1. Project.cs 모델 생성
        2. AppDbContext.cs에 DbSet<Project> 추가
        3. Add-Migration, Update-Database
        4. ProjectController, View 생성
        5. Views/Project/Create.cshtml 수정
        6. ProjectController, Create Post 메서드 수정

## 14일차
- ASP.NET Core 포트폴리오 웹사이트, MyPortfolio
    1. AWS 라이트세일로 윈도우서버 인스턴스 만들기
        1. 구글 AWS 라이트세일 검색
        2. AWS 프리티어로 회원가입
        3. AWS 라이트세일로 로그인
        4. 루트 사용자로 로그인
        5. 인스턴스 생성
            - Linux/Unix는 라즈비안과 거의 동일
            - MS Windows OS 전용 > Windows Server 2016 선택
            - 무료 중 가장 성능이 좋은 거 선택
            - 인스턴스 확인 이름 변경
            - 인스턴스 생성 클릭
        6. 인스턴스 관리
            - 관리로 진입
            - 네트워킹 탭 > 고정 IP 연결 클릭
            - 자신의 고정아이피
            - Administrator
            - 비번 확인
        7. 원격 데스크톱 연결
            - 컴퓨터 : 고정아이피 주소
            - Network2 Yes 클릭
            - 서버 매니저 오픈
            - IE Enhanced Security Config. ON->OFF
            - 인터넷 익스플로러 오픈 구글
            - 크롬 브라우저 설치
            - FileZilla Server 검색 /설치
         8. 파일질라 서버 설정
            - 메뉴 > Configure 클릭
            - Server listners > 0.0.0.0 -> 내부 아이피로 변경
            - FTP and FTP over TLS 
            - Generate New > Disting,../HostName 입력, 새로 생성
            - Passive Mode 사용
                - From : 55000
                - To : 55999
            - User 생성
                - MountPoint
                    - Virtual path : /
                    - Native path : 본인 지정
                - Authentication : Required Password
                - 패스워드 입력 후 Apply
        9. 윈도우 방화벽 설정
            - Control Panel(제어판)
            - Windows Firewall > Advanced Setting
            - Inbound : 21, 55000-55999 열기

        10. AWS 방화벽 설정
            - 네트워킹 IPv4 방화벽
            - 21 포트 규칙추가
            - 55000-55999 포트 규칙추가

        11. 사용PC에서 파일질라 클라이언트 설치
            - 기본 설치
            - 사이트 관리자 
                - 새 사이트만들고
                - 호스트 : AWS pubilc ip
                - 사용자, 비번 : Filezilla server 설정한 사용자 계정
                - 전송설정 수동형 선택

        12. Visual Studio ASP.NET Core 게시
            - 프로젝트 > MRB > 게시 클릭
            - FTP/FTPS 서버 선택 > 다음
            - 서버 : aws public ip
            - 사이트 경로 : /
            - 수동모드
            - 사용자이름 패스워드 입력, 암호저장
            - 연결 유효성 검사 > 녹색체크
            - 게시 하면 됨            

        13. SQL Server 다운로드
            - 윈도우 서버 패스워드 정책 변경
                - 8문자이상 특수문자1자이상 영어대소문자
            - secpol.msc 보안정책
            - 패스워드 정책 변경 enabled -> disabled
            - 설치 후 SQL Config Manager
            - Network configuration
                - TCP/IP enable
            - 서버 재시작
            - 윈도우 방화벽, AWS 방화벽 1433포트 오픈
            - SSMS 접속 확인

        14. IIS(Interner Information Service)
            - ASP, ASP.NET 종류 웹서버 
            - Server Manager 오픈
            - Add Roles and Features 클릭
            - 기본 선택 Next
            - Select Server Roles
                - IIS Server 선택 다음
                - 기본 설치 

        15. SQL Server를 복제
            - SSMS 로컬 DB를 접속
            - 서버 종료
            - EMS.mdf, EMS_log.ldf 복사
            - FTP로 전송

        16. IIS 서버에서 ASP.NET 실행
            - 제어판 열기
            - Administraiton Tools
            - IIS 오픈
            - Default Web > Basic Setting 사이트 경로 변경
                - C:\Websites\MyPorfolio 
            - 폴더 설정 > Secuiry 탭
                - IIS_IUSERS 그룹 설정 추가

            - 구글에서 ASP.NET 코어 런타임 8 검색 다운로드
                - aspnetcore-runtime-8.0.7-win-x64.exe
                - dotnet-hosting-8.0.7-win.exe

            - IIS - Application Pool
                - ASPNETCore 애플리케이션 풀 생성
                - .NET CLR Version > No Managed... 선택
                - IIS 재시작

        17. 다음부터는 
            - Visual Studio 개발
            - Visual Studio 게시
            - DB가 변경되었으면, mdf, ldf를 FTP로 업로드
            - SQL 서버 중지 파일 이동

## 15일차(7.30)
- ASP.NET Core 포트폴리오 웹사이트, MyPortfolio
    1. 프로젝트 화면 DB 연동하기
        - 지난 목요일 만들던 것 확인
        - ProjectController.cs Create() Post 메서드 수정
        - 업로드 확인
        - Edit.cshtml은 Create.cshtml과 동이랗게 수정
        - Edit() Post 메서드 역시 동일 -> DB에 프로젝트 내용 추가

        - HomeController.cs Project() Get 메서드에 DB연동 내용 추가
        - Views/Home/Project.cshtml DB 연동 내용 추가 -> 프로젝트 DB 내용 표시

    2. 프로젝트 이미지 올리기
        - 이미지 올리기 중간 모델(클래스) 하나 필요 - TeamProject
        - Project.cshtml 부트스트랩 클래스 수정

    3. Contact 메일보내기(네이버 연동)
        - (구글), 네이버 동일 - 메일계정 2단계보안 설정
        -  네이버 메일 환경설정 > POP3/SMTP 설정 사용함으로 변경
        - 아래 코드를 



    4. 부트스트랩 템플릿 커스터마이징, 본인 포트폴리오 사이트 만들기
        - 구글에서 부트스트랩 템플릿 검색
            - https://bootstraptaste.com/
            - https://startbootstrap.com/
            - https://themewagon.com/themes/
            - https://getbootstrap.com/docs/5.0/examples/
        
 



