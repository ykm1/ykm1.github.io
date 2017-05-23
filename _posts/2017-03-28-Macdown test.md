---
layout: post
title: "Markdown Test"
categories: test
tags: [test]
---

### 제목 Headers<br>
`#`으로 시작하는 텍스트.<br>
`#`은 하나부터 여섯개까지 쓸 수 있고, `#`이 늘어날때마다 제목의 수준은 내려간다.<br>(보통 글씨 크기가 작아진다.)
# Markdown
## Markdown ??
### Markdown
#### Markdown
##### Markdown
###### Markdown
또는 `-`, `=`을 이용하여 h1, h2를 쓸 수 있다

---

### 인용 Blockquotes
`>`으로 시작하는 텍스트.
>인용문
>> 들여쓰기 인용문 따옴표
>>

---

### 코드 블럭 Code Blocks
첫 줄과 마지막 줄에 Back quote ( ` ) 또는 물결( ~ ) 3개 삽입
~~~
코드 블럭의
예시
입니다
~~~

---

### 인라인 코드 블럭 Inline Code Blocks

Back quote ( ` ) 로 감싸진 텍스트 <br>

`div` `인라인 코드 블럭` `인라인` `코드` `블럭`

---

### 강조 Emphasis

기울여 쓰기(italic) : `*` 또는 `_`로 감싼 텍스트<br>
굵게쓰기(bold) : `**` 또는 `__`로 감싼 텍스트

*기울여쓰기*
**굵게쓰기**
***기울이고 굵어지기***

---

### 외부링크 External Links
인라인링크 : [구글](http://www.google.com “구글”)

참조링크 : 
[Google][1] [Naver][2]
[1]:http://google.com/"구글"
[2]:http://naver.com/"네이버"

URL링크 : <http://www.google.com>

---

### 내부링크 Internal Links
`[링크](#name)`내부 링크

---

### 리스트 Lists
`No.` 숫자 다음 `.`을 찍는다. (적힌 숫자랑 상관없이 순서대로 번호가 매겨진다.)
0. list 1
3. list 3
5. list 5
6. list 6
7. list 7

---

### 순서 없는 리스트 Unlists
`*`, `+`, `-` 으로 시작하는 텍스트.
* list 1
 * list (1)
 * list (2)
 * list (3) 
* list item 1
    * list item 1-1
    * list item 1-2

---

### 테이블 Tables
표 작성에 유용한 사이트 [Markdown Tables Generator](http://www.tablesgenerator.com/markdown_tables)