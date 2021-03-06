#제목1
##제목2

-리스트1
- 리스트2
- 
1. 첫 번째
2. 두 번째 리스트
헬로우 **월드**
[토이코드](http://toycode.net)
Github

# Github 업로드 하는 방법(필요한 단축어)
1. 변경사항을 적는다
2. 컨트롤 + S (내 컴퓨터에 변경사항이 저장된다)
3. git add .(변경사항을 git hub에 인식시킨다. -. 이란 명령어를 쓸 경우 모든 변경사항들이 인식된다)
4. git commit -m "000" (변경사항을 저장한다)
5. git push (git hub에 업로드한다)
6. 그외 ) git diff (변경사항을 요약해서 알려주는 명령어) / git log (변경사항에 대한 이력)

# PART1. HTML CSS의 기본
## CHAPTER 01. HTML 기본
1. HTML의 기본 구조
1) HTML은 웹 페이지 구조 제작에 필요한 언어

2) 태그 : HTML 문서를 구성하는 요소로서 일반적으로 ‘여는 태그(<태그>)’와 닫는 태그(</태그>)가 한 쌍으로 구성되어 있다. (닫는 태그가 없는 태그도 있다)
- 여는 태그와 닫는 태그 사이에는 텍스트나 다른 태그들을 넣을 수 있다.

3) HTML의 기본 구조
- <!DOCTYPE html> : HTML5 최신 웹 표준을 사용하겠다는 선언(항상 맨 위에 작성)
- <html> ... </html> : HTML의 시작과 끝
- <head> ... </head> 엡 페이지의 제목과 정보를 구성하는 태그들이 위치하는 문서의 서문 영역
- <body> ... </body> 실제로 화면이 보여지는 문서의 본문영역
* 본 태그들은 HTML 문서의 뼈대를 잡는 태그일 뿐 결과물도 볼 수 없음

2. 홈페이지 제목 작성
1) Title 태그
- <title>은 웹 페이지의 제목을 정의하는 태그
- <head> ... </head> 서문 영역 안에 작성해야 한다.

“<title>HTML CSS 기초</title>” 

3, meta 태그
1) meta 태그 
- HTML 문서의 메타 데이터를 정의하는 태그
- 메타 데이터 : 문서의 근간 정보 / 가령 디지털 카메라로 촬영할 때 촬영된 사진의 기본적인 정보(날짜. 해상도. 시간 등...) 
- <meta>는 닫기 태그가 없으며, title 태그처럼 <head> ... </head> 사이에 작성해야 한다

2) 문자 인코딩
- 문자 인코딩 : 문자의 형태나 형식을 변환하는 처리 
- <meta>의 charset 속성을 이용해야 한다.

“<meta charset=”글씨체“>

4. h1 ~ h6 태그
- 표제를 만들 때 사용하는 태그 (본 페이지에 나오는 내용이므로 <body> ... </body> 사이에 쓴다)
- h1 ~ h6 순서대로 크기가 작아진다

“<h1>HTML 기본 태그들</h1>”

5. p 태그
- <p>는 문단을 나눌 때 사용하는 태그

- HTML 문서에서 두 칸 이상의 공백이나 줄바꿈은 하나의 공백으로 출력된다.

“<p>내용</p>” 

6. br 태그
- <br> 태그는 줄바꿈 하는 태그
- 닫는 태그가 없다
- HTML 문서에서 두 칸 이상의 공백이나 줄바꿈은 하나의 공백으로 출력된다.
= 엔터로 줄바꿈을 할 수 없다 (그냥 한 줄에 쭈루룩 적힌다)
- <p> 와의 차이 : “한 문장 내에서 줄바꿈을 할 경우 문장 중간에 <br>. 아에 단락을 나눌 경우 여는 태그. 닫는 태그로 앞 뒤에 <p> 

7. hr 태그
- <hr> 태그는 수평선을 긋는 태그
- 문장 중간에 들어가므로, “닫는 태그가 없다”

8. pre 태그
- <pre>태그를 사용하면 공백과 줄바꿈을 그대로 표현한다

9. div 태그
- 레이아웃을 만드는 데 사용되는 태그
- 여러 태그들을 감싸 하나의 그룹 영역을 만든다 
<div> 여 러 가 지 태 그 들 </div> <<-- 하나의 영역으로
- 흡사 여러 가지 태그들을 묶어 하나의 도화지에 뭉쳐놓는 것과 같은 형태로, 추후 CSS라는 물감같은 존재와 함께 사용할 경우 여러 가지로 활용 가능

## Chapter2. CSS 시작하기
1. Style 속성
- CSS란 HTML 태그로 이뤄진 요소와 구조에 디자인을 적용하는 역할
- 사용하는 방식은 3가지가 있다 : 인라인 방식 / 내부 스타일 시트 / 외부 스타일 시트
- 인라인 방식 : 태그에 style 속성을 추가하여 그 안에 직접 CSS 코드를 작성하는 방식
- CSS코드 : 속성: 속성값;  으로 구성되어 있다. 
예시) color: green;  (폰트 색상을 초록색으로 한다)
     background-color: blue; (배경 색깔을 파란색으로 한다)

“<div> ==(CSS코드 적용)==> <div style=”color: #333; background-color 000;>

2. class 적용
1) 인라인 방식이 비효율적인 이유
- style 속성이 적용된 요소가 여러번 쓰이게 되었을 때, 이를 수정하기 위해서 여러 번 작업을 수행하여야 함

2) class
- class를 통해 태그에 이름을 부여할 수 있다. / 보다 적확하게는 “카테고리화 할 수 있다”
<태그 class=“클래스이름”)</태그>
- 공백을 통해 한 태그에 여러 클래스를 지정하는 것도 가능하다
<태그 class=“클래스A 클래스B”></태그>
- Class 속성은 style 속성과 달리 아무런 CSS 코드를 가지지 않는다 
=> 내부/외부 스타일 시트에서 모든 CSS코드를 다른 곳(스타일 시트)에서 관리한다
=> 즉, html 내부에서 태그를 통해 디자인을 수정하는 것이 아니다. 
- 스타일 시트에서 여러 가지 클래스에, 여러 가지 CSS 속성을 지정할 수 있으며, 태그는 자신이 가지고 있는 클래스에게 지정된 CSS 속성을 부여받게 된다.
예시) A 태그가 1클래스 2클래스 3클래스에 속해있다. 1클래스가 CSS에서 안경을 끼게 정해지고 2클래스가 붉은 옷을 입게 되고 3클래스가 검은색 바지를 입게 된다면
=> A태그는 안경을 끼고 붉은 옷을 입고 검은색 바지를 입게 된다.

- Class와 ID의 차이 : CLASS는 “분류. 종류”이며, ID는 “이름”이다. 그러므로 특정한 태그는 여러 가지 Class를 가질 순 있지만, 한 가지 ID만을 가진다.
=> 비유하자면, 남정훈이라는 개인은 누군가의 아들이며, 대학생이고, 과외선생님이지만 남정훈이라는 개인은 유일한 것.

“<div class=”section“> : section이라는 Class로 div 로 묶이는 영역이 지정된다.

3. style 태그
1) 내부 스타일 시트 : HTML 문서 안에 CSS 코드를 따로 관리할 수 있는 공간을 만들어 사용한다.

2) style 태그
- <head> ... </head> 안에 <style> ... </style>을 작성한다.
- 그 안에 모든 CSS 코드를 작성한다.

4. style 태그 : 내부 스타일 시트에 스타일 적용하기
1) CSS 작성 규칙
- 모든 CSS 속성은 { } 안에 포함되어야 한다
- class를 선택할 때는 이름 앞에 .을 붙인다
- id를 선택할 때는 이름 앞에 #을 붙인다.
- CSS 속성들은 ; 으로 구분된다

5. 외부 스타일 시트
1) 외부 스타일 시트 방식 : HTML 문서 외에 CSS파일을 따로 분리하여 사용한다
==> 내부 스타일 시트는 HTML 문서 내에 CSS 코드를 삽입하는 것 / 외부 스타일 시트는 이를 외부 스타일 시트에 떼서 따로 적는 것 
- HTML 코드와 CSS코드를 따로 관리할 수 있고 파일 각각이 더욱 가벼워진다.

6. link 태그 : 외부 스타일 시트를 HTML 파일과 연동시키기
- <link>는 HTML 파일에서 외부 파일을 불러올 때 사용
• rel="stylesheet" CSS 파일을 불러올 때 추가하는 속성
• media="all" 모든 디바이스에서 불러올 때 추가하는 속성
• href="css/style.css" 불러올 파일(css 폴더 속의 style.css)의 경로

2) 파일 경로
- <link>에 작성하는 href 파일 경로는 해당 태그를 작성하고 있는 HTML 파일을 기준으로 작성

“  <link rel="stylesheet" media="all" href="css/style.css">” 
(<head> ... </head> 사이에다가 작성)

# Part 2 시맨틱 태그로 레이아웃 잡기
## Chapter1. header와 footer
1. 시맨틱 태그 – header 태그
1) header 태그
- <header>는 주로 사이트 상단에 위치하여 로고, 메뉴, 머리말 등으로 사용

2) 시맨틱 태그
- 문서의 구조를 만드는 요소
- <div>와 기능적 차이는 없지만 의미상으로 태그의 이름이 나누어져 있다는 점이 포인트
- <header> <footer> <nav> <article> <aside> <section> 등이 있음

* <body> ... </body> 사이에 삽입 <-- 본문에 표시되는 내용이므로

2. header 태그 – css 속성 입히기
- css 창에서 시맨틱 태그를 불러올 때는 그냥 바로 header 이렇게 치면 된다.

==> 비유컨대 시맨틱 태그는 “이름 붙여진 Div / section”과 유사하다.

3. 가운데 정렬하기
1) text-align 
- 텍스트를 정렬하는 CSS 속성
- 대표적인 속성 값은 left. center. right
“ text-align: center; ”

4. padding으로 여백 주기
1) padding 속성
- padding은 내부 여백을 지정하는 속성
- 기존 크기에서 지정한 padding값만큼 크기가 늘어난다
- 반대로 margin은 외부 여백을 지정하는 속성

5. 시맨틱 태그 – footer 태그
1) footer 태그
- 주로 사이트 하단에 위치하여 저작권 정보. 꼬리말 등의 용도로 사용

## Chapter2. nav와 section
1. 시맨틱 태그 – nav 태그
- <nav>는 네이버게이션. 사이트 메뉴 역할

2. 시맨틱 태그 – section 태그
- <section>은 영역을 나누는 태그
- 특정한 영역이 정해져있기보다는 여러 요소들을 그룹핑한다는 점에서 <div>와 닮음
=> <div> 대신에 <section>을 동일하게 사용하여도 기능적으로 별반 차이는 없다
- <div>와의 차이점 : <div>에 기본적인 css가 적용된 것처럼, <section>또한 이에 해당하는 기본 css가 적용되어 있음 

3. 태그에 CSS 작성하기
- 클래스가 아닌 태그 자체에 CSS코드를 작성하려면 선택자에 .(온점)없이 태그 이름만 작성해주면 됩니다.

4. nav 태그와 content를 왼쪽/오른쪽으로 나누기
1) 부모-자식 관계 / 형제 관계


2) float 속성
- 정렬과 관련된 CSS 속성으로 대표적인 속성값으로 left. right가 있다
- text-align(텍스트 정렬)과는 다르게 해당 요소 자체를 정렬합니다

3) overflow 속성
- 영역을 벗어나는 요소들을 어떻게 보여줄 것인지 지정하는 것
- overflow: hidden (영역 바깥으로 넘쳐날 경우 넘치는 부분을 보이지 않도록)
- overflow: scroll(넘치는 부분은 스크롤 바를 만들어 롤링으로 볼 수 있도록)


- 비유컨대, 두 장의 종이를 앞뒤로 겹치면 앞에서 볼 때 각각의 영역이 한 면이 두 개로 나뉜것처럼 보이는 것과 유사

5. body 태그 기본 여백 없애기
- <body>는 기본적으로 소량의 margin 여백이 존재 (전체 큰 창이 살짝 떼어져 있는 느낌)
- CSS 창에서 margin 여백을 조정하는 것 가능

“ body {margin: 0;} ” (margin 여백을 0으로)


# Part 3 HTML 태그 연습해보기
## chapter 1. 강조 태그와 링크 태그
1. 새로운 section 태그 – 텍스트 강조 태그
1) 블록요소 vs 인라인 요소
- 블록 요소로 문장 사이의 단어를 감싸면 그 요소의 영역은 부모의 영역만큼 채워지며, 그 여파로 문장에서 독립됩니다.


- 인라인 요소는 문장에 소속된 채로 영역을 잡을 수 있습니다.


2. b태그와 strong 태그
1) b태그와 strong 태그
- <b> 와 <strong>은 텍스트를 굵게 만들어주는 “인라인 요소 태그”
- 다음의 css 속성과 동일한 효과 (font-weight: bold;)

3. I 태그와 em 태그
- <i>와 <em>은 텍스트 기울임 효과를 주는 “인라인 요소 태그”
- 다음의 css 속성과 동일한 효과 (font-style: italic;)

4. section과 section 사이에 선 넣어보기
1) border 속성
- border는 요소의 전방(앞)에 테두리를 만들어주는 속성 (css코드)
- 다음 CSS 코드는 요소의 전방(앞)에 1px의 검정색 직선 테두리를 만듭니다.

“ border: 1px solid black; ”

2) border-bottom
- 요소의 하단에 테두리를 만들기 위한 속성

5. span 태그
1) span 태그의 활용
- <span> 자체는 아무 효과도 없지만, CSS를 통해 그 영역만을 꾸밀 수 있게 된다.
- 비유컨대, 한글의 “블록”과 같은 효과


“ <span style="color: green;">style 속성</span>이나,
  <span class="red">class</span> 등을 이용하여 효과를 줄 수 있다 “
(위는 style을 활용한 것. 아래는 red 라는 클래스를 먼저 생성하여 그것을 외부 스타일 시트 형태로 활용한 것)

6. a 태그 : 텍스트에 링크 걸기
1) <a>는 링크를 거는 태그 
2) a 태그의 href 속성
- href 속성에 이동할 주소를 지정할 수 있다
(다른 사이트 / 특정 사이트의 하나의 웹 페이지 다 연결 가능하다는 것)
3) a 태그의 target 속성
- target 속성 없음 : 현재 페이지가 이동할 페이지로 전환
- target 속성에 _blank라는 값 삽입 : 새 탭에서 페이지 뜸
“ <a href="http://www.toycode.net" target="_blank">토이코드</a>”

7. img 태그 – url를 이용하여 이미지 불러오기
1) src 속성
- <a>의 href 속성과 비슷 : 해당 속성에 주소를 적으면 해당 주소의 이미지가 화면에 나타난다
“  <img src="http://goo.gl/q6lh7b"> ”

## chapter 2. 리스트와 테이블
1. 리스트 태그
1) 리스트의 구성
- 첫 번째는 리스트 전체를 감싸는 <ul>과 <ol>
- 두 번째는 리스트의 아이템 하나 하나를 나타내는 <li>
- 리스트를 감싸는 태그는 <ul>, <ol> 중 필요한 걸 쓰면 되고, 리스트 항목을 작성할 때는 반드시 <li>를 써야 함

2) ol 태그
- ol = Ordered List (순서가 있는 리스트)
- type 속성을 지정하지 않은 경우 목록에 숫자로 순서 매겨짐

- 앞에 붙는 숫자는 type 속성을 주어 바꿀 수 있다
“<ol> ===> <ol type=”바꿀숫자“>

3) ul 태그
<ul>은 Unordered List의 줄임말로, 순서가 없는 리스트 (점으로 리스팅)


2. a 태그(링크걸기) 밑줄 지우기
1) a태그는 기본적으로 text-decoration: underline; 이라는 속성이 적용되어 있음
- 지우기 위해선 css에 “ text-decoration: none; ” 이라는 속성을 주면 됨

2) css에서 원하는 요소 잡기

- 위의 사례의 경우, 모든 a 태그(링크)의 밑줄이 사라집니다. 
- 만약 왼쪽(nav) 메뉴에 있는 a 태그 밑줄만 없애고 싶다면...

- 다음과 같이 코드를 작성하면, nav 태그(부모) 안쪽의 a 태그(자식)에게만 속성이 적용됨

3. 텍스트 사이의 간격 벌리기
1) line-height 속성
- CSS속성 중 하나인 line-height를 이용하여 줄 사이 간격 조절 가능
“ line-height: 30px; ” 

4. 테이블 태그


th (제목 셀)
tr (행) ==> 세로로 (줄)넘어가는 단위
td (내용 셀(열)) ==> 가로로 넘어가는 단위
table border 속성 (테이블의 선 두께)

## chapter 3. 폼 태그
1. 폼 태그 – 기본 틀
- <form> ... </form>

2. 폼 태그 – 텍스트 입력
1) input 태그
- <input> : form 태그 안에 여러 가지 컨트롤 요소를 만드는 태그
- <input type=“text”>  : 텍스트 필드로 한 줄 정도의 텍스트를 입력할 수 있는 란을 만드는 속성
id : <input type="text" name="id">  (닫는 태그 없음)

3) 폼 태그 – 비밀번호 입력
- <input type=“password”> : 사용자가 입력할 때 내용이 *로 표시되는 비밀번호 텍스트 삽입란
password : <input type="password" name="password"> (닫는 태그 없음)

4) 폼 태그 – 여러 줄의 텍스트 입력
- rows 10 : 세로로 10줄 / cols 50 : 가로로 열 줄
- <textarea rows="10" cols="50" name="about_me"></textarea> (닫는 태그 있음)

5) 폼 태그 – 고르기
- input type=“radio” : 여러 가지 항목 중 한 가지만 선택하는 버튼을 만드는 속성
- name 속성의 값을 맞춰주게 되면 한 그���처럼 사용되고, 이 중에서 한 가지만 선택할 수 있게 됩니다.
성별 :
        <input type="radio" name="gender" value="man">남
        <input type="radio" name="gender" value="woman">여
        <br>


6) 폼 태그 – 선택하기
- <select> : 
국적 :
        <select name="country">
          <option value="korea">한국</option>
          <option value="usa">미국</option>
          <option value="china">중국</option>
          <option value="japan">일본</option>
        </select>



7. 폼 태그 – 제출 버튼
- <input type=“submit”>
- value 속성으로 버튼의 텍스트를 바꿀 수 있음

 <input type="submit" value="제출">
 
# part4. CSS의 여러 속성들
## chapter 1. 앨범 이미지 만들어보기
1. album-css 입히기
1) background 속성
- 이미지는 html의 img 태그를 이용하거나 css의 background 속성을 이용
- background: url(“0000”)
2) background 속성 –no-repeat
- 배경 이미지 크기가 그 이미지를 적용하는 요소의 크기보다 작을 경우 기본적으로 바둑판 배열으로 채워지는 데 이를 방지하기 위해 뒤에 no-repeat 코드 추가
- background: url(“000”) no-repeat
3) background 속성 –cover
- 배경 이미지 요소의 크기만큼 꽉 채워주면서 이미지의 비율을 잃지 않고 자연스럽게 보여주기 위한 속성
- background-size: cover;

2. padding 속성 
- padding 값이 두 개일 경우, 첫 번째 값은 상하 여백, 두 번째 값은 좌우여백
- padding: 110px 50px;

3. box-sizing 속성 –border-box
일반적으로 크기가 지정된 요소에 padding으로 내부 여백을 지정하면 기존 크기에 내부 여백 값이 더해져서 원하지 않는 결과물이 나올 수 있습니다.
예를 들어, 너비 650px의 요소에 좌우 내부 여백 50px을 주면 너비가 750px까지 늘어나게 됩니다.50px(왼쪽 내부 여백) + 650px(기존 너비) + 50px(오른쪽 내부 여백) = 750px
box-sizing을 border-box로 지정해주면padding, border 등 요소의 크기를 해칠 수 있는 속성을 지정할 때도 요소의 기존 크기를 유지할 수 있습니다.
4. 여백 활용하기
- margin / padding 
여백: 10px; // 모든 방향에 10px의 여백
여백: 10px 20px; // 위쪽 아래쪽에 10px, 오른쪽 왼쪽에 20px의 여백
여백: 10px 20px 30px 40px; // 위쪽 10px, 오른쪽 20px, 아래쪽 30px, 왼쪽 40px의 여백(시계 방향)
“ margin: 15px 0px; ”

5. 요소 반투명하게 만들기
- opacity : 불투명도를 지정하는 css 속성
- 0(투명) ~ 1(불투명)
- “ opacity: 0.5; ”

## Chapter2. Hover 연습해보기
1. hover class 추가
- hover는 마우스를 올렸을 때 발생하는 이벤트(효과)

2. border-radius 속성
- 모서리를 둥글게 만드는 css 속성
- 속성 값으로는 픽셀단위, 퍼센트 단위 등을 사용 가능

3. :hover 

## Chapter3. 모바일 고려해보기
한글파일 참조zz

입니다.