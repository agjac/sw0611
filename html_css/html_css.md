# HTML

- Contents
  - Text
  - Media
    - Image, Video, Audio

- Structure
  - Semantic : 의미있는 구조
  - Layout

## HTML basic

- HTML : Hyper Text Markup Language
  - Hyper Text : 하이퍼링크로 연결된 문서 => 웹페이지(콘텐츠, 구조)
  - Mark up : 표시
  - Language : 언어

- HTML 문법
  - 명칭 : Tag / Element
  - 구성 : 시작 ~ 종료태그
  - 종료태그가 없는 태크 : 반태그(Empty Element)
```
<tag> content </tag> : Element

<tag ...> : Empty Element
```
-HTML 속성(Attribute)
  - HTML Element를 표시할 때 필요한 추가정보 입력
  - name="value"
```
<a href="https://www.naver.com">네이버</a>

<img src="photo.jpg">

```



## HTML Basic Structure
```
<!DOCTYPE html>

<html>
  <head>
    <title></title>
  </head>
  <body></body>  
</html>

```

### DOCTYPE

- HTML 문서타입
  - HTML 버전
  - HTML5 표준

### Head - 웹사이트 기본정보

- meta : 웹사이트 관련정보(검색엔진)
- title : 웹사이트 제목

### Body : 웹 사이트 컨텐츠

- 웹사이트에 contents, structure... 표시하는 모든 태그

## HTML Contents

### Text

#### heading(제목)

- h(heading) : 제목태그
- 1 ~ 6 단계로 표시됨

#### paragraph(단락)

- p(paragraph) : 단락태그
- 강제줄바꿈, 강제공백은 인식되지 않고 공백 한 칸으로만 인식
  - line break : br(강제 줄바꿈 태그)
  - space : &nbsp;(강제 공백 엔터티(Entity))
- hr(horizontal rule) : 수평선 긋기
  - 단락을 선의 형태로 구분

#### List(목록)

- 순서없는 목록/순서있는 목록
- ul(unordered List) : 순서없는 목록
- ol(Ordered List) : 순서있는 목록
- Li(List Item) : 목록 항목

** 포함관계 (Nested Structure)

- 태그안에 다른 태그들이 포함되는 것
- 포함하는 요소
  - 조상요소(Ancestor)
  - 부모요소(Parent)
- 포함되는 요소
  - 자식요소(Child)
  - 자손요소(Descendant)
- 옆에 나란히 있는 요소
  - 형제요소(Sibling)
```
(1) <html>
(2)   <body>
(3)     <h1>내용 제목</h1>
(4)     <p>
(5)       단락내용<br>
        </p>    
      </body>
    </html>
```
(1) 조상 요소 | 기준 요소 | 조상 요소
(2) 조상 요소 | 자식 요소 | 부모 요소
(3)          | 자손 요소 | 형제 요소 
(4) 부모 요소 | 자손 요소 | 기준 요소
(5) 기준 요소 | 자손 요소 | 자식 요소

#### table(표)

#### hyper link(하이퍼링크)

### Media

#### image(이미지)

#### video(영상)

## HTML Structure

### Semantic

- header
  - logo, login ...
- nav(igation)
  - menu
- section
  - 본문 영역
- article
  - 본문 영역
- aside
  - 본문 영역,  부수적인 콘텐츠
- footer
  - 연락처, 주소, 회사 이름

### Layout

- Block & Inline
  - Block 요소
    - 태그가 브라우저에 표시될때 각 태그 영역이 새줄에서 표시
    - 태그 영역이 부모요소에 전체 채워짐
  - Inline 요소
    - 태그가 브라우저에 표시될때 각 태그 영역이 같은 줄에서 표시
    - 태그 영역이 콘텐츠에 맞춰짐

### container element

- div(sion)
  - block
- span
  - inline


## 경로지정 방식
- 파일의 위치, 인터넷 주소(url)

- 상대경로 
  - 리소스 파일을 사용하는 HTML 파일 기준
  - html 파일 위치에 따라 주소(url) 변경
  - root(/) 폴더를 기준으로 주소 적용 => root 상대 경로
```
[root(/)] - [html1] - home.html
        - [html2] - [about] - about.html
        - [images] - photo.jpg

1) home.html -> photo.jpg
- ../images/photo.jpg
- /images/photo.jpg

2) about.html -> photo.jpg
- ../../images/photo.jpg
- /images/phot.jpg
```
- 절대경로
  - 이미지를 표시하는 HTML 페이지가 기준이 아니고,  해당 서버가 기준
  - 서버부터 주소(url)를 사용하기 때문에 변동이 없음.
```

image.com

[root(/)] - [html1] - home.html
        - [html2] - [about] - about.html
        - [images] - photo.jpg
1) home.html
- www.image.com/images/photo.jpg

2) about.html
- www.image.com/images/photo.jpg

```

## 강조태그, 기타태그

- 텍스트 특정 부분 강조
  - strong : 강한 강조
  - em(phasize) : 일반 강조
  - mark : html5 버전, block 강조

- 텍스트를 표현할 때 부족한 태그를 보완하는 태그
  - i(talic)
  - b(old)

# CSS

- content styling
  - text styling
  - media styling

- layout(structure styling)
  - 가로배치(Flexbox)

## CSS Basic

- CSS : Cascading Style Sheet

```
h1 {color:blue;font-size:20px;}

h1 {
  color: blue;
  font-size:20px;
}
```

## Selector(선택자)

- 선택자로 HTML 요소를 선택
- HTML 요소선택 방법
  - Simple Selector(단순 선택자)
    - Tag/Element 이름 사용
    - Class 이름 사용
    - Id 이름 사용

```

<a href="https://www.naver.com" class="naver">네이버</a>
<a href="https://www.daum.net" id="daum">다음</a>

/* a 태그 2개모두 red 적용  */
a {
  color:red;
}

/* a 태그 각각 다른 color 적용 */

.naver {
 color:blue;     
}
#daum {
  color:green;
}

```

### id, class 이름의 특징

- Id 
  - 같은 HTML 페이지에서 고유(유일)해야함. 
  - 프로그래임 언어의 변수와 연결 가능성이 있음
  - HTML요소에 여러 개의 ID 이름 적용 불가능

- Class (활용 필!!)
  - 같은 HTML페이지에서 여러번 사용 가능.
  - HTML 요소에 여러개의 class 이름 사용 가능

```
<p class="paragraph">단락1</p>
<p class="paragraph">단락2</p> (o)
<p id="content">단락3</p>
<p id="content">단락4</p> (x)

<p class="gnb-list-item">회사소개</p>

```

### CSS 선택자 우선순위

- Cascading 규칙
  - 동일한 대상에 여러 스타일이 적용될 때 제일 마지막에 적용된 스타일이 반영

-선택자 우선순위
  - 선택자 종류에 따라 CSS 적용 우선순위가 다르게 정의
  - cascading 규칙에 따르지 않고 CSS 를 적용할 때 사용
  - inline: 1000
  - id: 100
  - class: 10
  - tag: 1
  
  ### text styling


  #### Color

```
h1{
  color:blue;
}
```


### text alignment
```
p{
  text-align:center;
}

```

- 정렬 값 : left, center, right, justify(양쪽정렬)

- 단어 중간에 줄바꿈

```
p{
  word-break:break-all;
}

```

#### Text Decoration
```
h1{
  text-decoration:underline;
}

h1{
  text-decoration:line-through;
}

h1{
  text-decoration:overline;
}

a{
  text-decoration:none;
}

```

#### Text Spacing
```
p{
  text-indent: 16px;
}

h2{
  letter-spacing:5px;
}

P{
  word-spacing:3px;
}

p{
  white-space:nowrap;
}

```

- line-height
  - 텍스트 줄을 포함한 줄 높이
  - 값 
    - PX
    - 배수 : 소수점을 포함한 숫자 가능, 폰트 크기를 기준

** 조상요소나 부모요소에 CSS 속성을 적용했을 때, 자식요소에도 적용되는 것을 상속
  - HTML Element중에 상속되지 않는 태그가 있음
  - CSS 속성중에 상속되지 않는 속성이 있음

#### Font Family

- CSS 파일이 브라우저에서 렌더링되기 때문에 폰트 파일을 클라이언트 PC에서 찾음
  - 다수의 클라이언트 PC에 설치될 만한 폰트를 선택(Web safe)
- Font-family 속성에 값으로 정해준 폰트 종류를 차례대로 찾음(Fallback)

- 서버에서 폰트를 사용할 수 있게 하는 기능
  - Web font

- 구글 폰트

- 폰트 종류(저작권)
  - 폰트 파일 포함 여부


#### Font size

- font-size
- 폰트 크기
- px

#### Font Style

- font-style
- 기울임꼴 설정
- italic 값

#### Font Weight

- font-weight
- 굵기
- normal/bold
- 단위없는 100단위 숫자 값 사용

























