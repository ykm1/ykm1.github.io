---
layout: post
title: "[CSS]Style related with text"
categories: study
tags: [CSS,font,text]
---
**font** - 글꼴 속성을 한꺼번에 묶어 표현 가능
~~~
font: <font-style> <font-variant> <font-weigt> <font-size/line-height>
<font-family> | caption | icon | menu | message-box | small-caption 
| status-bar | initial | inherit; 
~~~
<br>
#### 1. 글꼴 관련 스타일
* **font-family** - 글꼴을 지정하는 속성<br>
`body {font-family: "맑은고딕", 돋움, 굴림;}`
     * serif(장식이 있는 폰트)
     * sans-serif(장식이 없는 폰트)
     * cursive(흘림체)
     * fantasy
     * monospace(고정폭)
* **font-weight** - 글자 굵기를 지정하는 속성<br>
`p {font-weight: bold | 100~900;}`
     * normal : 기본 값
     * bold : 굵게
     * 100~900 : 400은 normal,700은 bold에 해당
* **font-size** - 글자 크기를 지정하는 속성<br>
`p {font-size: 3rem;}`
     * rem : html 태그의 폰트 크기에 따라 상대적으로 크기가 결정(권장)
     * em : 해당 글꼴의 대문자 M의 너비를 기준으로 크기가 결정
     * px : 픽셀. 모니터에 따라 상대적으로 크기가 결정

#### 2. 텍스트 스타일     
* **color** - 글자 색을 지정하는 속성
색상 값은 색상이름, rgb, 16진수로 표기<br>
`p {color: blue | rgb(0,200,0) | #ff0000;}`
* **text-decoration** - 텍스트에 줄 표시하기/없애기<br>
`a {text-decoration: none;}`
     * none : 밑줄 표시 안함
     * underline : 밑줄 표시
     * overline : 영역 위로 선 표시
     * line-through : 영역을 가로지는 선(취소 선) 표시
* **text-transform** - 텍스트 대.소문자 변환하기<br>
`p {text-transform: capitalize | uppercase | lowercase;}`
     * none : 기본 값
     * capitalize : 시작하는 첫 번째 글자를 대문자로 변환
     * uppercase : 모든 글자를 대문자로 변환
     * lowercase : 모든 글자를 소문자로 변환

#### 3. 문단 스타일
* **text-align** - 텍스트 정렬 방법을 지정하는 속성<br>
`.align {text-align: left | right | center | justify;}`
     * left : 왼쪽 정렬
     * right : 오른쪽 정렬
     * center : 가운데 정렬
     * justify : 양쪽 정렬
* **line-height** - 줄 간격을 조절하는 속성<br>
`p {font-size: 15px; line-heigh: 2.0;}`<br>
기본 값은 normal로 수치로는 1.2에 해당. 값이 1.2라면 현재 엘리먼트 폰트 크기의 1.2배만큼 간격을 준다는 의미.

#### 4. 목록과 링크 스타일
* **list-style-type** - 목록의 불릿과 번호 스타일을 지정하는 속성<br>
`li {list-style-type: none | <순서 없는 목록의 불릿> | <순서 목록의 번호>;}`
     * 순서 없는 목록
          * disc : 채운 원
          * circle : 빈 원
          * square : 채운 사각형
          * none : 불릿 없애기
     * 순서 있는 목록
          * decimal : 1로 시작하는 십진수
          * decimal-leading-zero : 앞에 0이 붙는 십진수
          * lower/upper-roman : 소문자/대문자 로마 숫자
          * lower/upper-alpha : 소문자/대문자 알파벳
* **list-style-image** - 불릿 대신 이미지를 넣는 속성<br>
`li {list-style-image: none | url(이미지 파일 경로);}`
