# HTML
- HyperText Markup Language.
  - HyperText: 참조(하이퍼링크)를 통해 독자가 한 문서에서 다른 문서로 즉시 접근할 수 있는 텍스트.
  - Markup: 태그 등을 이용하여 문서나 데이터의 구조를 만드는 언어


## HTML Tag
- 꺾쇠 괄호(<>)로 감싸서 표현
- 보통 시작 태그(start tag, opening tag)와 종료 태그(end tag, closing tag)의 한 쌍으로 구성
- 종료 태그는 시작 태그와 똑같지만, 태그 이름 앞에 슬래시(/)가 붙음
- 종료 태그 없이 시작 태그만을 가지는 태그를 빈 태그(empty tag)라고 함

## HTML 구조
```html
<!DOCTYPE html>
  <html>
      <head> 
          <title>문서 제목</title>
      </head> 
      <body>
          내용
      </body>
  </html>
```
- \<!DOCTYPE html> : 현재 문서가 HTML5 문서임을 명시
- \<html> : HTML 문서의 루트(root) 요소를 정의
- \<head> : HTML 문서의 메타데이터(metadata)를 정의.
  - 메타데이터(metadata)란 HTML 문서에 대한 데이터로 웹 브라우저에는 직접적으로 표현되지 않는 정보를 의미.
  - 이러한 메타데이터는 \<title>, \<style>, \<meta>, \<link>, \<script>, \<base>태그 등을 이용하여 표현할 수 있음.
- \<title> : HTML 문서의 제목(title)을 정의하며, 다음과 같은 용도로 사용됩니다.
  - 웹 브라우저의 툴바(toolbar)에 표시
  - 웹 브라우저의 즐겨찾기에 추가할 때 즐겨찾기의 제목
  - 검색 엔진의 결과 페이지에 제목으로 표시
- \<body> : 웹 브라우저를 통해 보이는 내용 부분

## HTML 요소
- HTML 요소(element)는 여러 속성을 가질 수 있으며, 이러한 속성(attribute)은 해당 요소에 대한 추가적인 정보를 제공
- TML 요소는 시작 태그로 시작해서 종료 태그로 끝남
- 속성은 HTML 요소 중에서도 언제나 시작 태그 내에서만 정의되며, 속성 이름과 속성값(value)으로 표현

- 문법
```html
<태그이름 속성이름="속성값">
```
- 속성의 이름은 소문자로 표기
- 속성의 값은 ""로 감싸야 함

1. 스타일(Style 요소)
   ```html
   <h1 style="color: red;">빨강색</h1>
   ```
   - CSS 스타일을 HTML 요소에 직접 설정할 수 있음

## 자주 쓰이는 태그

1. 제목(Heading) 태그
   ```html
    <h1> <h2> <h3> <h4> <h5> <h6>
   ```
   - 다양한 크기의 h태그
   - 가장 큰 \<h1> 부터 가장 작은 \<h6>까지 있음
   - 여러 검색엔진은 각 웹 사이트의 내용을 \<h>태그를 이용하여 키워드를 수집하고, 그 내용을 파악

2. 단락(Paragraph) 태그
   ```html
   <p>
   ```
   - 단락이란 내용상 끊어서 구분할 수 있는 하나하나의 부분을 의미하며, 문단이라고도 부름
   - \<p>태그 내에서 작성된 여러 번의 띄어쓰기와 줄 나누기는 오직 하나의 띄어쓰기로만 표현

3. 줄바꿈 태그
   ```html
   <br/>
   ```
   - 새로운 단락을 만들지 않고도 줄바꿈을 할 수 있는 태그
   - 종료 태그가 없는 빈 태그

4. 줄바꿈과 공백이 적용되는 단락 태그
   ```html
   <pre>
       줄바꿈과
       공   백이 적용되는
       

       단
       락 태그
   </pre>
   ```
   - \
   - \<p>태그에서는 적용되지 않았던 여러 번의 띄어쓰기와 줄 나누기가 적용되는 태그

5. 영역 태그
   ```
   <div>
   ```
   - HTML 문서에서 특정 영역(division)이나 구획(section)을 정의할 때 사용
   - 여러 HTML 요소들을 하나로 묶어주어 CSS로 스타일을 변경하거나 자바스크립트로 특정 작업을 수행하기 위한 일종의 컨테이너(container)로 자주 사용

6. 주석
   ```
   <!-- 내용 -->
   ``` 

