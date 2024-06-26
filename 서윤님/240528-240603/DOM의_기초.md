# DOM의 기초

## 자바스크립트와 HTML의 만남

1. 자바스크립트 적용 전
   <br>
   첫 번째 이미지는 웹 페이지의 기본 상태를 보여줍니다. 여기서 `<h1>` 태그는 원래의 텍스트를 포함하고 있습니다.

![DOM의_기초_HTML_자스_상호작용_01](/서윤님/240528-240603/image/DOM의_기초_HTML_자스_상호작용_01.jpg)

2. 자바스크립트 적용 후
   <br>
   두 번째 이미지는 자바스크립트를 통해 `<h1>` 태그의 텍스트가 "안녕하세요"로 변경된 후의 상태를 보여줍니다. 이는 웹 페이지가 어떻게 동적으로 조작될 수 있는지를 시각적으로 설명해 줍니다.

![DOM의_기초_HTML_자스_상호작용_02](/서윤님/240528-240603/image/DOM의_기초_HTML_자스_상호작용_02.jpg)

자바스크립트를 사용하여 DOM에 접근하고 수정하는 것은 웹 개발에서 흔히 볼 수 있는 작업입니다. 이를 통해 개발자는 사용자 인터페이스의 동적인 상호작용을 구현할 수 있습니다.

## DOM이란 무엇인가?

> DOM은 Document Object Model의 약자로, HTML 또는 XML 문서의 구조화된 표현입니다.

![DOM의_기초_DOM_01](/서윤님/240528-240603/image/DOM의_기초_DOM_01.jpg)

웹 브라우저는 HTML 문서를 불러온 후, 이 문서를 파싱하여 DOM으로 변환합니다. 이 DOM은 자바스크립트를 통해 동적으로 조작될 수 있으며, 이 과정을 통해 우리는 웹 페이지에 인터랙티브한 요소를 추가할 수 있습니다.

## DOM 트리

![DOM의_기초_DOM_01](/서윤님/240528-240603/image/DOM의_기초_DOM트리_01.jpg)
<br>
_출처: https://simplesnippets.tech/what-is-document-object-modeldom-how-js-interacts-with-dom/#google_vignette_

웹 페이지가 로드될 때, 브라우저는 HTML 문서를 파싱하는 과정을 통해 각 HTML 요소를 객체로 변환하여 DOM 트리를 구성합니다. 이 트리는 웹 페이지의 뼈대를 형성하며, 각 HTML 요소가 노드로 표현됩니다. 노드는 크게 세 가지 유형으로 분류됩니다.

1. **요소 노드(Element Node)**: HTML의 각 태그는 요소 노드로 표현되며, 이는 웹 페이지의 HTML 구조를 이루는 기본 단위입니다. 예를 들어, `<div>`, `<h1>`,` <p>` 태그들이 이에 해당합니다.

2. **텍스트 노드(Text Node)**: 모든 텍스트 콘텐츠는 텍스트 노드로 관리되며, 요소 노드와 분리하여 취급됩니다. 예를 들어, `<p>` 태그 내의 텍스트가 이에 해당합니다.

3. **속성 노드(Attribute Node)**: HTML 요소의 속성들(예: class, id, style)은 각 요소 노드에 연결된 속성 노드로 표현됩니다. 이 노드들은 요소의 추가 정보를 제공하며, CSS 스타일링이나 JavaScript 조작에 사용됩니다.

## DOM API

DOM API는 DOM을 동적으로 조작할 수 있도록 해주는 메서드와 속성의 집합입니다. 다음은 웹 페이지에서 요소를 생성하고, 수정하며, 조작하는 데 사용되는 주요 DOM API 메서드 몇 가지입니다.

1. **document.getElementById()**
   <br>
   HTML 문서에서 특정 ID를 가진 요소를 찾아 그 요소를 반환합니다. 예를 들어, 아래 코드는 ID가 "myDiv"인 요소의 배경색을 파란색으로 변경합니다.

   ```javascript
   let element = document.getElementById("myDiv");
   element.style.backgroundColor = "blue";
   ```

   ![DOM의_기초_DOM_API_01](/서윤님/240528-240603/image/DOM의_기초_DOM_API_01.jpg)

2. **document.createElement()**
   <br>
   새로운 HTML 요소를 동적으로 만들고 싶을 때 사용합니다. 아래 코드는 새로운 `<div>` 요소를 만들고, "Hello, World!"라는 텍스트를 삽입한 후, 문서의 body에 추가합니다.

   ```javascript
   let newDiv = document.createElement("div");
   newDiv.innerHTML = "Hello, World!";
   document.body.appendChild(newDiv);
   ```

   ![DOM의_기초_DOM_API_02](/서윤님/240528-240603/image/DOM의_기초_DOM_API_02.jpg)

3. **parentNode.appendChild()**
   <br>
   새로 생성된 요소를 DOM에 추가하려면 appendChild() 메서드를 사용합니다. 아래 코드는 "parentDiv"라는 ID를 가진 요소 안에 새 `<p>` 요소를 추가합니다.

   ```javascript
   let parent = document.getElementById("parentDiv");
   let newChild = document.createElement("p");
   newChild.textContent = "This is a new paragraph.";
   parent.appendChild(newChild);
   ```

   ![DOM의_기초_DOM_API_03](/서윤님/240528-240603/image/DOM의_기초_DOM_API_03.jpg)

4. **document.querySelector()**
   <br>
   CSS 선택자를 사용하여 문서에서 요소를 찾고 싶을 때 사용합니다. 아래 코드는 페이지의 첫 번째 `<button>` 요소를 찾아 그 글자 색을 빨간색으로 변경합니다.

   ```javascript
   let firstButton = document.querySelector("button");
   firstButton.style.color = "red";
   ```

   ![DOM의_기초_DOM_API_04](/서윤님/240528-240603/image/DOM의_기초_DOM_API_04.jpg)

이러한 DOM API 메서드들을 활용하면 웹 페이지의 요소를 실시간으로 조작하고, 사용자의 상호작용에 반응하여 페이지를 업데이트할 수 있습니다.
