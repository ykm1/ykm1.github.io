---
layout: post
title: "[CSS]CSS Positioning"
categories: study
tags: [CSS,position,float]
---
#### 1. CSS포지셔닝과 주요 속성들
**포지셔닝(positioning)**:박스 모델을 웹 문서 안에 배치하는 것. <br>
웹 문서의 레이아웃이 만들어지는 것. (float속성과 position속성)
* **box-sizing** - 박스 너비 기준 정하기<br>
`box-sizing: contents-box|border-box`
	* 박스 모델의 width와 height속성은 박스 모델 안에 있는 콘텐츠 부분의 너비와 높이를 의미
	* content-box:width속성 값을 콘텐츠 영역 너비 값으로 사용. 기본값.
	* border-box:width속성 값을 콘텐츠 영역에 테두리까지 포함한 박스 모델 전체 너비 값으로 사용.<br>
![box-sizing](https://ykm1.github.io/images/box-sizing.png)

~~~
<style>
	.box1 {
		box-sizing: content-box;
		width: 300px;
		height: 150px;
		margin: 10px;
		padding: 30px;
		border: 2px solid red;
	}				___❶
	.box2 {
		box-sizing: border-box;
		width: 300px;
		height: 150px;
		margin: 10px;
		padding: 30px;
		border: 2px solid red;
	}				___❷
</style>

<div class="box1"> box-sizing = "content-box" </div>
<div class="box2"> box-sizing = "border-box" </div>
~~~

* **float** - 왼쪽이나 오른쪽으로 배치<br>
필요한 만큼만 차지하고 다른 요소가 들어올 만큼의 공간을 비워둠.<br>
(이미지와 텍스트를 나란히 표시하려고 할 때)<br>
`float: left | right | none`
* **clear** - float 속성 해제<br>
float속성이 더 이상 유용하지 않다고 알려주는 속성<br>
`clear: none | left | right | both`<br>
float:left(배치) -> clear:left(종료)<br>
left,right 상관없이 무효화는 clear:both
* **★position★** - 배치 방법  지정<br>
텍스트나 이미지를 나란히 배치 또는 가로,세로로 배치 가능<br>
`position: static | relative | absolute | fixed`
	* static: 문서의 흐름대로 배치
	* relative: 문서 흐름따라 위치 지정
	* absolute: 원하는 위치에 배치<br>
	가까운 부모요소 중 position이 relative인 요소를 기준으로 함
	* fixed: 브라우저 창 기준으로 배치하고 위치 고정
	* static을 제외한 나머지 속성 값은 좌표를 이용해 요소의 위치를 조절<br>  	top,bottom,left,right로 지정
* **visibility** - 요소를 보이게 하거나 보이지 않게, 겹치게<br>
`visibility: visible | hidden | collapse`
	* visible: 화면에 요소를 표시. 기본값
	* hidden: 화면에서 요소를 감춤. 크기 그대로 공간 차지
	* collapse: 서로 겹치도록 조절
* **z-index** - 요소 쌓는 순서 정하기<br>
z-index값이 작을수록 아래에, 클수록 더 큰 값이 위에 쌓임<br>
z-index값을 명시하지 않을 경우, 뒤에 삽입되는 요소의 값이 크다<br>
![z-index](https://ykm1.github.io/images/z-index.png)

~~~
<style>
	div#wrapper { 
		position: relative;
	}
	.b1 {z-index: 1;}
	.b2 {z-index: 3;}
	.b3 {z-index: 2;}
				___b1->b3->b2 순으로
</style>
<div iid="wrapper">
	<div id="box" class="b1">1</div>
	<div id="box" class="b2">2</div>
	<div id="box" class="b3">3</div>
</div>
~~~

#### 2. 다단으로 편집하기<br>
_다단 관련 속성은 브라우저별 접두사를 붙여 사용_

* **column-width** - 단의 너비 고정하고 다단 구성하기<br>
창의 너비가 커지면 단의 개수가 많아지고 좁으면 단의 개수가 줄어듦<br>
`column-width: <크기>|auto`<br>
	* <크기>: 단 너비를 직접 지정
	* auto: column-count같은 다른 속성에 따라 너비 자동계산
* **column-count** - 단의 개수 고정하고 다단 구성하기<br>
창의 너비가 커지면 단의 너비도 커짐.<br>
`column-count: <숫자>|auto`<br>
	* <숫자>: 콘텐츠가 들어갈 단의 개수
	* auto: column-width같은 다른 속성에 따라 단의 개수 자동계산
* **column-gap** - 단과 단 사이 여백 지정하기<br>
단과 단 사이에 구분선을 넣는다면 구분선도 이 여백에 포함됨<br>
`column-gap: <크기>|normal`<br>
	* <크기>: 단과 단 사이의 여백을 숫자로 지정
	* normal: 여백을 자동으로 지정
* **column-rule** - 구분선의 색상, 스타일, 너비 지정하기<br>
`column-rule: <너비> | <스타일> | <색상>`<br>
	* `column-rule-color: <색상>`
	* `column-rule-style: none|hidden|dotted|dashed|solid|double|groove|ridge|inset|outset`
	* `column-rule-width: <크기>|thin|medium|thick`
* **break-after** - 다단 위치 지정하기<br>
	* 특정요소 앞 `break-after: column | avoid-column`
	* 특정요소 뒤 `break-before: column | avoid-column`
	* 특정요소 안 `break-inside: column | avoid-column`
	* column: 단나눔, avoid-column: 단 나누지않음
* **column-span** - 여러 단을 하나로 합치기<br>
(2016년 2월 기준, 파이어폭스는 이 속성을 제대로 지원하지 않음)<br>
`column-span: 1 | all`<br>
	* 1: 단을 하나만. 합치지않는것. 기본값
	* all: 전체 단을 하나로 합쳐 표현. 단의 일부만 합칠 수 없음

#### 3. 표 스타일
* **caption-side** - 표 제목 위치 정하기<br>
`caption-side: top|bottom`<br>
* **border** - 표 테두리 스타일 결정하기<br>
	* `<table border=1>`
	* table태그의 border속성을 이용해 테두리 생성
	* CSS의 border속성을 이용해 테두리의 색상, 형태, 너비 등 지정
	* `<table border=1>`로 테두리를 표시했을 경우, 표의 바깥 테두리 뿐만 아니라 셀의 테두리까지 모두 표시
	* CSS를 이용해 표시할 때는 표의 바깥 테두리와 셀의 테두리를 따로 지정
* **border-collapse** - 테두리 통합, 분리하기<br>
`border-collapse: collapse|separate`<br>
	* collapse: 테두리를 하나로 합쳐 표시
	* separate: 테두리를 따로 표시. 기본값
* **border-spacing** - 인접한 셀 테두리 사이 거리 지정하기<br>
border-collapse:separate로 셀들을 분리했을 경우, 인접한 셀 테두리 사이의 거리를 지정<br>
`border-spacing: <크기>`
* **empty-cells** - 빈 셀의 표시 여부 지정하기<br>
border-collapse:separate로 셀들을 분리했을 경우, 내용이 없는 빈 셀들의 표시 여부를 지정<br>
`empty-cells: show|hide`
* **width, height** - 표 너비와 높이 지정하기<br>
또한 padding속성을 이용해 여백을 조금 더 꾸며줄 수 있음
* **text-align** - 셀 안에서 수평 정렬하기<br>
`text-align: left|right|center`
* **vertical-align** - 셀 안에서 수직 정렬하기<br>
`vertical-align: top|bottom|middle`



