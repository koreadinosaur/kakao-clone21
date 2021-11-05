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

#3.3-3.6

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

box와 body의 border가 같다면, 마진의 위아래의 값이 달라도 더 큰 값으로 출력되는 현상.

    1) div

    div{
        height: 150px;
        width: 150px;
        background-color: tomato;
    }

div값을 이렇게 주게되면 정사각형의 토마토색깔의 박스가 나온다.

    2) body

    body{
        background-color: violet;
    }

이러면 150\*150px의 정사각형범위를 제외한 div의 영역이 violet 색이됨.

그런데 여기서 body의 top마진값을 20px, div의 top 마진값을 80px을 부여하면 div와 body top margin값이 동일하게 80px이 됨.

    3) 결론

        (1) body와 box의 border가 같을 때,

        (2) top과 bottom에서만

        (3) body와 box의 margin값이 다르더라도 둘 중 더 큰 값으로 함께 적용됨.

#3.7-3.8

1. padding

border 안쪽의 공간

body든에 padding을 부여하면 collapsing margins이 해결된다. div에는 해도 안됨.

2. border

말그대로 경계를 의미함 border style mdn으로 검색하면 여러 스타일 나옴.

점선, 혹은 실선의 스타일 등이 있는데 디자인이 예쁘지 않아서 거의 하나만 사용한다.

        *{
            border: 2px solid black;
        }

\*는 전체를 의미함. 해당 코드는 경계선을 2px만큼의 두께의 검은색 실선으로 출력하라는 의미. border: 다음에는 line-width || line-style || color 순서로 입력한다.

#3.9 - 3.11

1. inline block

   1. inline에서 block 속성 부여하기

inline box는 높이와 너비를 가질 수 없는데

        div{
            display: inline-block;
            width: 150px;
            height: 150px;
            color: red;
        }

해당 display속성을 주면 inline임에도 불구하고 높이와 너비를 가지게되고 빨간색이 출력됨.

게다가 한 줄에 나란히 출력된다.

단점 : 디폴트값으로 box사이에 빈공간이 있음. 빈공간에 규칙이 없음

반응형 디자인을 지원하지 않는다.

2. flexbox

   1. 자식 태그에는 아무것도 적으면 안된다.

<body>
    <div></div>
    <div></div>
    <div></div>
</body>

이렇게 body안에 div를 세 개 작성 후

        body {
            display: flex;
            margin: 20px;
            padding: 20px;
        }

flex속성을 주면 세 개체가 나란히 빈 공간 없이 정렬됨

여기서 justify-content: center;이나 flex-end 등으로 중앙 정렬, 우측정렬 등 가능. space-evenly / between 속성을 주면 각 개체의 빈 공간을 동일한 비율로 만들어서 떨어뜨려준다. 창이 작아지면 거기에 맞춰서 빈공간이 조절됨

    2) flex의 축

         (2-1)main axis(주축, 수평축) - justify-content

         (2-2)cross axis(교차축, 수직축) - align-items

        body {
            height: 100vh; /* 100vh는 viewport height, 즉 screen 높이의 100%를 의미한다 */
            display: flex;
            justify-content: space-between; /*가로축 정렬*/
            align-items: center;
            margin: 20px;
            padding: 20px;
        }

이러면 세로축을 기준으로 화면의 정중앙에 정렬됨. height를 정해준 상태에서는 align-items의 속성으로 strech를 부여할 수 없다. 높이가 정해져있기 때문.

3.  수평축, 수직축 바꾸기

    1. flex-direction

column, row의 옵션이 있음. display: flex;의 기본 옵션은 row(수평)이다. (수평정렬) 이것을

flex-direction: column;으로하면 수직으로 정렬된다. 이때 주축은 수직축이되고, 교차축은 수평축이 된다.

이 때 align-items: flex-end;로 정렬하면 box가 우측 끝으로 정렬된다. 수평축이 되었기 때문.

4. flex box의 property

   1. flex container

body가 div들의 flex container인데 div 또한 flex container가 될 수 있다.

            display: flex;
            justify-content: center;
            align-items: center;

div의 css에 이렇게 추가하면 텍스트가 박스 정중앙으로 정렬됨.

    2) flex-wrap: nowrap;

flex는 width를 무시한다. 같은 줄에 여러 elements를 두기 위해 초기 width값이 300px이더라도 자동으로 조정한다.

    3) flex-wrap: wrap;

wrap은 부여된 width값에 따라 width값을 초과하는 elments들은 줄을 바꿔 정렬시킨다.

    4) flex-direction: reverse;

    거꾸로 정렬시키기.

---

#3.12

1. position

   요소들을 미세하게 움직일 때 유용하다.

   1. position: fixed;

      커서를 내려도 고정된 자리에서 출력됨 ex) netflex의 메뉴바

   2. position: static;

      박스를 처음 위치한 곳에 두는 것

   3. position: relative;

      처음 위치한 곳을 기준으로 수정할 수 있음

left: -10px; /_처음 위치에서 왼쪽으로 10px만큼 이동_/
상하좌우 다 마찬가지.

    4) absolute

        부모태그 중 relative 속성을 가진 부모를 기준으로 정렬되는데, 아무도 그 속성이 없으면 body를 기준으로 움직인다. 그래서 bottom: 0px; 입력하면 body 맨 아래에 정렬됨.

# 3.13

1.  psedo selector

    n번째 태그를 select하는 방법

            div:first-child{ /*첫 번째 div*/
                background-color: green;
            }
            div:nth-child(2){  /*div중 2번째 div에 red출력, even입력하면 짝수번째 div 선택함.*/
                background-color: red; /*2n+2, 5n 이런식으로도 가능 */
            }
            div:last-child{ /* 마지막 div*/
                background-color: silver;
            }

    여러개의 div가 있을 때.

2.  combinator

        <div>
            <span>hello</span>
            <p>
                태정태세문단세 예성연중인명선 광인효현숙경영정 순헌철고순
                <span>이순신장군 만세</span>
            </p>
        </div>
        1) 이 상태에서 span과 p안에있는 span의 색상을 다르게 정해주기

            span{
                color: springgreen;
            }
            p span{  /*부모태그 먼저 입력 후 자식태그 입력 */
                color: tomato;
            }

        2. 첫 번째 span에만 밑줄효과 주기

           (2-1)

           span{
           color: springgreen;
           text-decoration: underline; /_ 모든 span태그에 밑줄 _/
           }
           p span{
           color: tomato;
           text-decoration: none; /_ 여기에는 밑줄 x _/
           }
           (2-2)

           div > span { /_ div > span 은 span이 div 바로 아래의 자식태그라는 것을 의미 _/
           text-decoration: underline;
           }

        3. p 다음에 오는 span에 밑줄효과주기

           p + span { /_ p의 자식인 span이 아니라 p 다음에 오는 span을 의미 _/
           text-decoration: underline;
           }

    이때, span은 p의 '바로' 다음에 와야한다. 중간에 다른 태그 있으면 안됨

        4) 중간에 다른 태그 있을 때 사용하는 combinator

p ~ span {
text-decoration: underline;
}
이때 p와 span은 형제관계여야한다. 부모 자식의 관계가 아니어야 한다는 뜻.

    5) 특정 속성(attribute)가진 input select하기

        -attribute selectors mdn이라고 검색하면 됨

        input:required {
            border-color: tomato;
        }

required 속성 가진 input만 선택할 수 있음. optional은 required을 가지지 않은 input 선택.

        input[type="password"] {
            background-color: tomato;
        }

type, placeholder는 중괄호를 이용한다

        input[placeholder~="name"] {
            background-color: tomato;
        }

~=의 의미는 placeholder 중 name을 포함하는 input을 선택하는 것.

#3.17

1. states

   1. active - 클릭했을 때 색깔이 변하고 클릭 버튼을 떼면 원상복귀

      button:active{
      background-color: tomato;
      }

   2. hover - 마우스 커서가 버튼에 올라갔을 때 작동

      button:hover{
      background-color: tomato;
      }

   3. focus - focus되고 있을 때(마우스로 클릭해서 커서가 반짝이고 있는 상태)

   4. visited - 링크에만 적용됨

      body에 a태그 추가하고

<a href="http://www.naver.com">go to naver</a>
css 추가하기

        a:visited{
            color:gray;
        }

이러면 링크를 클릭하고나면 방문했던 사이트라는 의미에서 색깔이 회색으로 바뀜

    5) focus-within - form 안에 자식 태그인 input이 있고, 그 input이 focus 됐을 때의 form의 상태 설정.

        form:focus-within{
            border-color: greenyellow;
        }
        form{
            border: 2px solid blue;
            display: flex;
            padding: 20px;
            flex-direction: column;
        }
    6) 부모의 state에 따라 자식태그의 style 변경하기

        form:hover input{
            background-color: greenyellow;
        }
    이러면 form에 hover되었을 때(마우스 커서 가져다 댔을 때) input의 색깔이 바뀜

        form:hover input:focus{
            background-color: greenyellow;
        }

이러면 조건이 두 개 달림. form에 hover가 되어있고 input에 focus 되었을 때 색이 바뀜

#3.18

    1. pseudo elements

    1) ::placeholder


        input::placeholder{
            color: blue;
        }

placeholder 꾸밀 수 있음.

    2)::selection - 텍스트를 블록지정 했을 때 색깔 바뀜


        span::selection{
            background-color: blue;
        }
    3)::first-letter - 첫번째 글자에만 style 부여


        p::first-letter{
            color: red;
            font-size: 40px;
        }
    그런데 이거는 span에는 적용 안되더라. 왜지? 암튼 first-line도 있음.

#3.19 colors

    1. hexadecimal color(16진수 컬러)

color:#FAE100; 2. rgb방식

color:rgb(250, 225, 0, 0.8);
red, green, blue 값을 부여하는 것, 0.8은 알파값임. 투명도를 의미하는데 0에 가까울수록 연해짐.

color picker 이용하면 색상 추출 가능

    3. custom property(variable)

        1) root에 변수 선언해주기 - --main-color를 document의 root에 저장하는 것.


        :root{
            --main-color: #FAE100;
        }
        2) 변수사용법


        p{
            color: var(--main-color);
            font-size: 40px;
        }

css에서 변수를 주는 것이라 javascript하고 문법이 달라서 조금 어색하긴 함.

---
