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














