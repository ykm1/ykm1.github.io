---
layout: post
title: "[CSS]Style related with color and background"
categories: study
tags: [CSS,color,background]
---
**background** - 속성 하나로 배경 이미지 제어하기
~~~
backgrond: <color> <image> <repeat> <attachment>
<position> <size>;
~~~
<br>
#### 1. 웹에서 색상 표현하기
* 색상 표현 방법
     * 16진수 표기법 (ex. #000000 ~ #ffffff)
     * rgb와 rgba 표기법 (ex. rgb(255,0,0)/rgb(255,0,0,0.5)
     * 색상 이름 표기법 (ex. red, yellow, green, blue) 
<br>
example)

~~~
<style>
   body {
       background: #000000;
   }    /*   16진수로 문서 배경 색 지정   */
   .text1 {
       color: white;
   }    /*   색상 이름으로 흰색 글자 표현   */
   .text2 {
       color: rgba(255,255,255,0.8);
   }
        /*   투명도 0.8인 흰색 글자   */
   .text3 {
       color: rgba(255,255,255,0.5);
   }    /*   투명도 0.8인 흰색 글자   */
   .text4 {
       color: rgba(255,255,255,0.2);
   }    /*   투명도 0.8인 흰색 글자   */
   </style>
</head>
<body>
    <h1 class="text1">HTML + CSS</h1>
    <h1 class="text2">HTML + CSS</h1>
    <h1 class="text3">HTML + CSS</h1>
    <h1 class="text4">HTML + CSS</h1>
</body>
</html>
~~~
![color-html-capture](https://ykm1.github.io/images/color-html-capture.jpg)
#### 2. 배경 색과 배경 이미지
* **background-color** - 배경 색 지정하기 <br>
`body {background-color: gray;}` <br>
* **background-image** - 배경 이미지 넣기 <br>
`body {backrground-image: url(파일 경로);}` <br>
* **background-repeat** - 배경 이미지 반복 방법 지정하기 <br>
`body {background-repeat: repeat | repeat-x | repeat-y | no-repeat;}`
     * repeat : 브라우저 화면에 가득 찰 때까지 배경 이미지를 가로와 세로로 반복
     * repeat-x : 브라우저 창 너비와 같아질 때까지 배경 이미지를 가로로 반복
     * repeat-y : 브라우저 창 너비와 같아질 때까지 배경 이미지를 세로로 반복
     * no-repeat : 한 번만 표시하고 반복하지 않음
* **background-attachment** - 배경 이미지 고정하기 <br>
`.bg1 {background-attachment: scroll | fixed;}`
	* scroll : 화면 스크롤과 함께 배경 이미지도 스크롤, 기본 값
	* fixed : 화면이 스크롤 되더라도 배경 이미지는 고정
* **background-position** - 배경 이미지 위치 조절하기 <br>
`.bg1 {background-position: <수평 위치> <수직 위치>;}`
	* 수평 위치 : left | center | right | <백분율> | <길이 값>
	* 수직 위치 : top | center | bottom | <백분율> | <길이 값>
* **background-size** - 배경 이미지 크기 조절하기 <br>
`.bg1 {background-size: auto | contain | cover | <크기 값> | <백분율>;}`
     * auto : 운래 배경 이미지 크기만큼 표시
     * contain : 배경 이미지의 비율을 유지하면서 확대/축소하는데 이미지의 너비나 높이 중 짧은 부분을 요소에 맞춤
     * cover : 배경 이미지의 비율을 유지하면서 확대/축소하는데 이미지의 너비나 높이 중 긴 부분을 요소에 맞춤
     * <크기 값> : 너비 값과 높이 값을 지정. 너비나 높이 하나만 지정 시 원래 배경 이미지의 비율 유지
     * <백분율> : 원래 배경 이미지 크기를 기준으로 확대/축소 
#### 3. 이미지에 다양한 효과주기
* **filter** - 이미지에 다양한 효과주기<br>
최신 기술로 지원하지 않는 브라우저를 고려해 접두사를 붙여 입력하는 것을 권장<br>
아래와 같은 효과를 적용할 수 있으며 참고 페이지를 통해 공부해봅시다.<br>
참고 사이트 : [CSS Filters Playground](http://bennettfeely.com/filters)
~~~
img { -webkit-filter: grayscale();
      -o-filter: grayscale();
      filter: grayscale();
    }
~~~
	* blur()
	* brightness()
	* contrast()
	* drop-shadow()
	* grayscale()
	* hue-rotate()
	* invert()
	* opacity()
	* saturate()
	* sepia()