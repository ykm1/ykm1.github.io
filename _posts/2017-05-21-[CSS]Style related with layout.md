---
layout: post
title: "[CSS]Style related with layout"
categories: study
tags: [CSS,layout]
---
#### 1. CSS와 박스 모델
* **블록 레벨 요소와 인라인 레벨 요소** 
	* 블록 레벨 요소
		* 해당 요소의 너비가 100%
		* 왼쪽이나 오른쪽에 다른 요소가 올 수 없음
		* 너비, 마진, 패딩 등을 이용해 크기나 위치를 지정하려면 블록 레벨 요소
		* `<p>`,`<h1~h6>`,`<ul>`,`<ol>`,`<div>`, `<form>`, `<table>`
	* 인라인 레벨 요소
		* 줄을 차지하지 않는 요소. 화면에 표시되는 콘텐츠만큼만 영역을 차지
		* 나머지 공간에는 다른 요소가 올 수 있음
		* `<img>`, `<object>`, `<br>`, `<span>`, `<input>`, `<button>`<br>
* **width, height** - 콘텐츠 영역의 크기<br>
	* 박스 모델에서 콘텐츠 영역의 크기를 지정할 때는 너비를 지정하는 width 속성과 높이를 지정하는 height 속성을 사용
	* 박스의 크기를 백분율로 지정할 경우, 웹 문서 창의 크기에 따라 달라짐<br>
~~~
.box1 {width:<크기>|<백분율>|auto
		  height:<크기>|<백분율>|auto}
~~~

* **display** - 화면 배치 방법 결정<br>
블록 레벨 요소<->인라인 레벨 요소 바꿀 수 있음<br>
`display: none|contents|block|inline|inline-block 등`
	* block : 해당 요소를 블록 레벨로 지정
	* inline : 블록 레벨 요소를 인라인 레벨 요소로 변경
	* inline-block : 요소를 인라인 레벨로 배치하면서 내용에는 블록 레벨 속성을 지정
	* none : 해당 요소를 화면에 아예 표시하지 않음(공간조차 차지하지 않음)

#### 2. 테투리 관련 속성들
**border** - 테두리 스타일 묶어 지정 (속성 순서 상관없음)<br>
`.box1 {border: <스타일> | <두께> | <색상>`

* **border-style** - 테두리 스타일 지정<br>
`border-style : none|hidden|dashed|dotted|double|groove|inset|outset|ridge|solid`
* **border-width** - 테두리 두께 지정<br>
`border-(top/right/bottom/left)-width: <크기>|thin|medium|thick`
~~~
.box1 {border-width: 2px;}  /* 네 방향 테두리 굵기 모두 2px */
.box2 {border-width: thick thin;}  /* 위아래 굵게, 좌우 가늘게 */
.box3 {border-width: 5px 10px 15px 20px;}  /* 상,우,하,좌 */
~~~
* **border-color** - 테두리 색상 지정<br>
`.box1 {border-color: gray;}`

* **border-radius** - 박스 모서리 둥글게<br>
`border-(top-left/top-right)-radius: <크기>|<백분율>`<br>
`border-(bottom-left/botton-right)-radius: <크기>|<백분율>`

#### 3. 여백을 조절하는 속성들
* **margin** - 요소 주변 여백 설정, 요소 사이의 간격을 조절<br>
`margin-(top/right/bottom/left): <크기>|<백분율>|auto`<br>
`margin: <크기>|<백분율>|auto`
* **padding** - 콘텐츠 영역과 테두리 사이 여백 설정, 테두리 안쪽의 여백<br>
`padding-(top/right/bottom/left): <크기>|<백분율>|auto`<br>
`padding: <크기>|<백분율>|auto`
<br>
![margin](https://ykm1.github.io/images/margin.png)
![padding](https://ykm1.github.io/images/padding.png)
<br>
*top > right > bottom > left (시계방향)으로 속성 적용*













