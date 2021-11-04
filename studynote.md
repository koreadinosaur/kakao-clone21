#2.1

1. 확장프로그램들
   1. waka time: vsc 사용시간, 언어별 사용시간 알려주는 프로그램
   2. Community Material Theme : vsc의 테마를 변경해주는 프로그램. 디폴트로 해놓고 써도 됨
   3. Material Icon Theme : 아이콘 추가해주는 프로그램

#2.2

1. 태그를 모두 외울 필요 없다.
<h1>text</h1> 텍스트를 태그 다음 넣은 뒤 태그를 닫아줘야만 적용이 되는 원리는 알아야 한다.

2. html에는 오류가 없다.
   브라우저는 내가 적은 코드가 아무 의미 없어도, 태그가 틀렸다 하더라도 출력을 할 것이다. 다만 존재하지 않은 태그를 입력하면 브라우저에서 해당 태그는 작동하지 않는다. 오류를 알려주지 않는다는 의미인듯??

#2.3

1. ul과 ol태그
   unodered list / ordered list를 의미한다. li라는 자식태그가 필요하다. 자식 태그를 입력하지 않으면 텍스트들이 옆으로 나열되기만 한다

2. prettier :
   html 작성 중 태그를 닫아주지 않고 저장하면 태그를 자동으로 닫아줌. 정렬도 해준다.
   다운로드 후 왼쪽 아래 setting 아이콘 클릭 -> 설정 -> editor 검색 -> Editor: Format On Save 찾아서 체크박스에 체크

#2.4-2.6

1. <a>태그 :
   다른 웹사이트를 link하기 위함 a태그는 href라는 attributes를 추가적으로 입력해줘야 한다.
   1-1) attributes(속성) : tag에 추가하는 부가적인 정보
   1-2) href : HTTP Reference 또는 hyperlink reference를 의미. 이동할 사이트를 알려주는 속성
   <a href="http://google.com">Go to google.com</a>
   이런식으로 사용하면 된다.
   href는 다른 태그에 추가해도 작동되지 않는다.
   1-3) target="\_blank"를 추가적으로 입력해주면 새 창이 새로운 탭에서 열린다. target태그의 기본 속성값은 \_self다

2. <img>태그:
   닫아주는 태그가 없는 self-closing tag다. 이미지 태그에는 텍스트가 없기 때문에 닫아줄 필요도 없는 것. <img>text 블라블라</img> 이렇게 쓰지 않는다는 의미. 말그대로 이미지만 사용한다.
   <img src="https://url" />
   <img src="파일명.jpg" />
   이렇게 사용하면 됨.
   다른 폴더일 경우 폴더명/파일명.jpg 이런 형태로 작성

3. html파일의 규칙 1)모든 html파일의 시작은 다음과 같다.
   <!DOCTYPE html>
   이 코드를 입력하지 않아도 브라우저가 텍스트를 출력하겠지만, 해당 코드는 브라우저에게 이 파일이 단순 텍스트 파일이 아니라 html파일이라는 것을 알려주는 것 2) html태그 사이에 작성해야 html코드가 됨
   <html>

</html>

    3)head와 body
        (3-1) head : 웹사이트의 환경을 설정하는 부분, 외부적으로 보이지 않는 설정
        (3-2) body: 사용자들이 보여줄 수 있는 content

#2.7

1.  head 태그 1) meta 태그
    (1-1) charset, name attributes
    <meta charset="UTF-8"> //사용 언어가 무엇인지 알려줌
    <meta name="description" content="This is web site"> //웹사이트 설명

            (1-2) og:image

    카카오톡 채팅방에서 url공유할 때 나오는 이미지를 출력해주는 속성.

        2)link 태그

    <link rel="shortcut icon" sizes="16x16 32x32 64x64" href="/m.png">
    shortcut icon은 탭의 타이틀 옆에 아이콘이 나타나도록 해주는 속성.

2.  html tag - mdn 사이트에 가면 찾을 수 있음. 1) <audio> tag
    controls라는 속성을 부여해야 작동됨 controls=enabled, 여기서 enabled는 true와 동일함. 생략해도 작동된다. 2) Obsolete and deprecated elements
    지금은 사용하지 않는 태그들.

#2.8

1. tag와 attribute 사용법
   <tagname attrname="attrvalue">text</tagname>의 형태임을 기억할 것.

2. label
   1)input과 같이 사용해야함.
   <label for="profile">aa</label> // label의 for와 input의 id는 값이 같아야 한다.
   <input id="profile">

---

#3.0

1. css를 html에 추가하기

   1. inline css : <style></style>

   - html의 head 영역에 추가하기.

   2. external css : <link>

<link rel="stylesheet" href="css/style.css">
style.css 파일을 따로 만들어 href로 참조하게끔 한다. rel은 relationship의 약자로 html과 style.css의 관계를 설명해주는 속성이다. style.css가 html의 stylesheet라는 의미.

#3.1

1.  css의 원리

        1) selector

        css는 html의 '태그'를 가리켜 해당 태그의 속성(property)을 정해준다. 색, 모양 등등. 태그를 가리키는 것을 selector라고 한다.(어떤 태그인지 선택한다는 의미) 역시 모든 property를 외울 필요는 없다.

        2) property

            (2-1) css property는 띄어쓰기를 하지 않는다.

            (2-2) property 끝에는 세미클론(;)을 꼭 입력해야 한다.

        .welcome-header {
            text-align: center;
        }

    이렇게 text-align과 :은 붙여쓰고, 끝에는 세미콜론 써줘야한다.

popertyname: propertyvalue; 의 형식을 지켜서 쓰면 됨.

#3.2

1. css의 특성

   1. Cascading Style Sheets

      - cascade는 폭포라는 뜻. cascading은 위에서 아래로 흐르는 것을 의미한다. 브라우저는 css의 코드를 위에서부터 차례대로 읽는다.

그래서 같은 태그에 대해 css의 코드가 충돌되면 마지막에 작성된 코드를 따른다.

#3.3-3.4

1.Box 종류

1.  block

    -block 옆에는 다른 block 오지 않는다. div옆에는 다른 div가 출력되지 않고 줄을 바꿔서 출력이 된다. <p>도 마찬가지. 대부분의 박스는 block이다.

    -높이와 너비가 있음.

2.  inline

    - 다른 요소들이 옆에 올 수 있음. span, link, img

    - 높이와 너비가 없음

3.  block과 inline의 전환

            display: inline;
            display: block;

    이라는 코드를 이용해 block을 inline으로 inline을 block의 속성을 가지게 해줄 수 있다.

2)  Box 속성

        1) margin : border 밖의 공간. body는 default 값으로 8px 크기의 margin을 갖는다.

        margin-left: 5px;
        margin-right: 6px;
        margin-top: 7px;
        margin-bottom: 8px;

    이렇게 좌우상하 각각 값을 줄 수 있는데

margin: 7px 6px 8px 5px;
이렇게 한 줄로 줄일 수 있다. 차례대로 위 오른쪽 아래 왼쪽의 값을 각각 주는거다. 시계방향으로 차례대로 값이 부여된다고 생각하면 됨.

margin: 5px 10px;
이렇게 값이 두 개면 첫 번째는 상하값, 두 번째는 좌우값을 의미한다.

    2) border :

    3) padding :

3. Collapsing margins
