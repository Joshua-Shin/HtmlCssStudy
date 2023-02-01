### HTML

#### 개발환경
- VScode
- 새로 설치한 확장 : auto rename Tag, css peek, html to css autocompletion, html css support, live server
- bracket pair colorizer, indent-rainbow, prettier는 내 스타일 아니라서 설치 안함

#### 기본 태그
- \<h1> \<hr> \<br> \<p> \<a href = ""> \<ul> \<li> \<title>

#### emmet
- 자동완성 기능이네
- ! > + * 정도는 일단 사용해보고, 더 많은건 나중에 개념 다 익히고 다시 보자.

#### 폰트
- \<i> \<em> \<b> \<strong>

#### 목록
- \<ol> \<ul> \<li> \<dl> \<dt> \<dd>

#### 표
- \<table> \<caption> \<tr> \<th> \<td> \<thead> \<tbody> \<tfoot>
- \<colgroup> \<col class = "col1"/> 사용해서 칼럼별로 스타일 적용할 수 있음
- 셀 병합 할때 : rowspan, colspan

#### semantic 태그
- header, nav, main, footer
- main 안에 section, article
- main 옆에 aside

#### div vs span 태그
- 둘다 영역 태그
- div는 block 레벨, span은 inline 레벨
- block 레벨 요소는 전체공간, 세로배치, width와 height와 text-align 적용됨
- inline 레벨 요소는 컨텐츠만큼만, 가로배치, width 와 height와 text-align 적용 안됨

#### 이미지 오디오 비디오 하이퍼링크
- \<img src="../tree.jpg" height="300" alt="나무" >
- \<audio src = "../assets/audios/water.mp3" controls>\</audio>
- \<video src = "../assets/videos/clouds.mp4" loop width="400" muted autoplay>\</video>
- controls는 재생바 표시해주는 옵션. audio에는 없으면 안돼
- 크롬에서는 autoplay는 muted 옵션이 들어가야만 기능함

#### form
- 사용자가 정보를 입력하는 양식
- \<form action= "양식 데이터를 처리할 서버프로그램의 URI" method ="post">
- fieldset, legend, label, input.
- label for 값이랑 input id 값을 맞춰줘야돼.
- input type을 적절히 지정해주면 유효값인지 자동체크해주네
- email, password, tel, number, date, submit.. 등등
- checkbox는 여러개 선택가능 radio는 하나만 선택. 단 name으로 같이 묶어줘야 그 묶인것중에 하나를 선택할 수 있게 설정됨.
- textarea, select, datalist, button
- \<textarea id ="" name ="" rows="10" cols="10">It was a dark area\</textarea>
- \<select name="" id=""> \<option value="10kg" selected >10kg\</option> \</select>
- \<button type="submit">제출하기\</button>

#### head
- base, link, style, title, meta,,

-----------------------------


### CSS

#### css 외부 연결
- \<link href="style.css" rel="stylesheet">

#### 선택자
- 전체 선택자 : *
- 타입 선택자 : h2
- 클래스선택자 : .클래스명
- ID선택자 : #ID값
- 속성선택자 : h2[class], h2[class='email'], *=(포함), ^=(시작), $=(끝), ~=(포함),, 
- 그룹 선택자: section, span
- 자손 선택자: section div : section 안에 있는 모든 div
- 자식 선택자: section > div : section 바로 아래 있는 div
- 형재 결합자: section ~ div : 같은 위치에 있는 div
- 인접형재결합자 : section + div : 하위 개념이 아니라 그냥 바로 아래줄에 있는 div

#### 폰트
- 구글 웹 폰트에서 확인하고 import하고, html에 해당 글꼴 font-family: 로 설정
- vw, vh 는 전체 보이는 화면의 비율로 값을 조정. 
- text- indent: 문단 앞 들여쓰기

#### 테이블
- border-collapse : 경계선 중첩 없애줌
- #movies tr:nth-child(even) 짝수번째 행 선택자

#### Box Model
- content, padding, border, margin
- margin 10px 5px 3px 2px top right bottom left
- margin 10px 상하좌우 다 적용
- margin 10px 5px 상하 10px, 좌우 5px
- border-radius : 모서리 둥글게 조절
- box-sizing: border-box, content-box
    - border-box 일때는 딱 border까지의 크기가 height, width로 잡히기에 배치하기 좋아
    - content-box 일때는 content 사이즈만 height width로 잡혀서 그 후 padding 더해지고 border 더해지고 하다보면 배치하기가 어려울 수 있어.

#### 나머지
- inline-block : div 들을 가로로 배치할 수 있게 해주네. 근데 이것보다 display : flex 로 두는게 좋아
- 전체 배치 : main > section > article > div div div
- position에서 sticky 옵션 주고 top:0px; 해주면 스크롤 내려도 해드가 고정됨.
- 맥에서는 이미지 클릭하고 도구에서 사이즈 조절할 수 있어
- lorem*4: 아무 의미없는 문장 넣을 수 있네
- background-image: url(''); : 배경이미지 넣을 수 있음. 반복되고,
- a:visited 방문한곳 가상클래스
- a:hover 마우스 커서 가리키는곳 가상 클래스
- 전체에 margin, padding 0px 주고 시작하네
- @media(max-width: 599px): 핸드폰 테블릿 노트북 데스크톱에 따라 화면을 다르게 줄때 
- 보통 0\~599 // 600\~1239 // 1240\~ 으로 나눔
- flexbox
    - div들의 화면 배치를 해줌
    - display : flex
    - flew-wrap : wrap 자동 개행
    - justify-content : 가로 배치 옵션
    - align-content : 세로 배치 옵션

#### 네비게이션 바 만들때
- ul.nav-container>(li.nav-item>a)*4

---------------------

#### 유용한 사이트
- 무료 이미지 : https://pixabay.com/
- 무료 오디오, 비디오 : https://www.videvo.net/
- html 스팩 : https://developer.mozilla.org/ko/
- 강의 : https://youtube.com/playlist?list=PLlaP-jSd-nK-ponbKDjrSn3BQG9MgHSKv
- 강의교안 : https://www.gymcoding.co/htmlcss

----------------------
