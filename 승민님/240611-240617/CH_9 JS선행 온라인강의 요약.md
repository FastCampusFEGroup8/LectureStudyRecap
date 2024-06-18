# CH 9. JS 선행

## 표기법

### dash-case(kebab-case)

HTML, CSS 에서 주로 사용되는 표기법<br>
단어와 단어 사이에 - 을 작성하여 표기하는 방법<br>
the-quick-brown-fox-jumps-over-the-lazy-dog<br>

### snake_case

HTML, CSS 에서 주로 사용되는 표기법<br>
단어와 단어 사이에 \_ 를 작성하여 표기하는 방법<br>
the_quick_brown_fox_jumps_over_the_lazy_dog<br>

### camelCase

JS에서 사용되는 표기법<br>
첫 번째롤 시작하는 단어는 소문자, 그 다음부터 오는 글자가 대문자로 표기하는 방법<br>
theQuickBrownFoxJumpsOverTheLazyDog<br>

### ParcelCase

JS에서 사용되는 표기법<br>
첫 글자가 대문자로 표기하는 방법<br>
TheQuickBrownFoxJumpsOverTheLazyDog<br>

## Zero-based Numbering

0 기반 번호 매기기!<br>
특수한 경우를 제외하고 0부터 숫자를 시작한다.<br>

## 주석

// 한 줄 주석 <br>
/_ 한 줄 메모 _/<br>

/\*\*<br>

- 여러 줄<br>
- 메모 1<br>
- 메모 2<br>
  \*/<br>

## 데이터 종류(자료형)

### String(문자 데이터)

따옴표를 사용한다.

```javascript
let myName = "Mini";
let email = "mini@gmail.com";
let hello = "Hello ${myName}?!";

console.log(myName); // Mini
console.log(email); // mini@gmail.com
console.log(hello); // Hello Mini?!
```

### Number

정수 및 부동 소주점 숫자를 나타낸다.

```javascript
let number = 123;
let opacity = 1.57;

console.log(number); // 123
console.log(opacity); // 1.57
```

### Boolean

true, false 두 가지 값밖에 없는 논리 데이터.

```javascript
let checked = true;
let isShow = false;

console.log(checked); // true
console.log(isShow); // false
```

### Undefined

값이 할당되지 않은 상태를 나타냅니다.

```javascript
let undef;
let obj = { abc: 123 };

console.log(undef); // undefined
console.log(obj.abc); // 123
console.log(obj.xyz); // undefined
```

### Null

어떤 값이 의도적으로 비어있음을 의미합니다.

```javascript
let empty = null;

console.log(empty); // null
```

### Object

여러 데이터를 Key:Value 형태로 저장합니다. { }

```javascript
let user = {
  // Key: value,
  name: "mini",
  age: 28,
  isValid: true,
};

console.log(user.name); //mini
console.log(user.age); //28
console.log(user.isValid); // true
```

### Array

여러 데이터를 순차적으로 저장합니다. [ ]

```javascript
let fruits = ["apple", "banana", "cherry"];

console.log(fruits[0]); // 'apple'
console.log(fruits[1]); // 'banana'
console.log(fruits[2]); // 'cherry'
```

## 변수

데이터를 저장하고 참조(사용)하는 데이터의 이름<br>
var(권장되지 않음), let , const<br>

### let

```javascript
// 재사용이 가능
let a = 2;
let b = 5;

console.log(a + b); // 7
console.log(a - b); // -3
console.log(a * b); // 10
console.log(a / b); // 0.4
```

```javascript
// 값(데이터)의 재할당 가능!
let a = 12;
console.log(a); //12

a = 999;
console.log(a); // 999
```

### const

```javascript
// 값(데이터)의 재할당 불가!
const a = 12;
console.log(a); //12

a = 999;
console.log(a); // TypeError: Assignment to constant variable
```

## 에약어

특별한 의미를 가지고 있어, 변수나 함수 이름 등으로 사용할 수 없는 단어

```javascript
let this = 'hello'  // SyntaxError
let if = 123; // SyntaxError
let break = treu; // SyntaxError
```

## 함수

특정 동작(기능)을 수행하는 일부 코드의 집합(부분)<br>
function

```javascript
//함수 선언
function helloFunc() {
  //실행 코드
  console.log(1234);
}

// 함수 호출
helloFunc(); //1234
```

```javascript
//함수 선언!
function sum(a, b) {
  // a와 b는 매개변수(Parameters)
  return a + b;
}
let a = sum(1, 2); // 1과 2는 인수(Arguments)
let b = sum(7, 12);
let c = sum(2, 4);

console.log(a, b, c); //3, 19, 6
```

```javascript
// 기명(이름이 있는)함수
// 함수 선언 !
function hello() {
  console.log("Hello");
}

//익명(이름이 없는) 함수
//함수 표현 !
// 호이스팅(Hoisting)에 사용
let world = function () {
  console.log("World~");
};

//함수 호출!
hello(); //Hello~
world(); //World~
```

```javascript
const heropy = {
  name: "HEROPY",
  age: 85,
  // 메소드(Method)
  getName: function () {
    return this.name;
  },
};
const hisName = heropy.getName();
console.log(hisName); // HEROPY
//or
console.log(heropy.getName()); // HEROPY
```

## 조건문

조건의 결과(truthy,falsy)에 따라 다른 코드를 실행하는 구문

```javascript
let isShow = true;
let checked = false;

if (isShow) {
  console.log("Show!"); //Show!
}
if (checked) {
  console.log("Checked"); //거짓이므로 실행이 안된다.
}
```

```javascript
let isShow = true;
//if()의 내용이 참이면 if 안의 내용실행 거짓이면 else()의 내용 실행
if (isShow) {
  console.log("Show!");
} else {
  console.log("Hide?");
}
```

## DOM API

Document Object Model, Application Programming Interface<br>
자바스크립트로 HTML을 제어할 때 사용하는 여러가지 명령들

```javascript
let boxEl = document.querySelector(".box");

console.log(boxEl); //null 이라고 뜸
```

main.js가 실행될 때 그 해당하는 요소가 무엇인지 모르는데 찾아달라고 했기 때문에 결국엔 찾지 못하고 콘솔 창에는 null이라는 의미 없는 데이터가 출력.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <script src="./main.js"><script>
</head>
<body>
  <div class="box">Box!!<div/>
</body>
</html>
```

첫번째 방법. 스크립트가 있던 부분을 잘라서 이 body 태그가 있는 부분의 가장 밑 쪽에서 코드 실행

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <div class="box">Box!!<div/>
  <script src="./main.js"><script>
  // 브라우저는 코드를 위에서 부터 아래로 읽어나가기 때문에 결과적으로 이 box라는 클래스를 가지고 있는 이 div요소를 읽은 상태로 main.js를 실행하는 것이기 때문에 main.js안에 있는 box라는 클래스를 찾으라는 내용이 정상적으로 실행이 될 수 있는 구조가 된다
</body>
</html>
```

두번째 방법. 스크립트 태그 부분에 deeper라는 속성을 추가하여 HTML코드를 다 읽은 상태로 다시 main.js 내용을 실행하겠다는 의미를 부여

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <script defer src="./main.js"><script>
</head>
<body>
  <div class="box">Box!!<div/>
</body>
</html>
```

```javascript
// HTML 요소(Elemet) 1개 겁색/찾기
const boxEl = document.querySelector(".box");
// HTML 요소에 적용할 수 있는 메소드!
boxEl.addEventListener();
// 인수(Arguments)를 추가 가능!
boxEl.addEventListener(1, 2);
// 1 - 이벤트(Event, 상황)
boxEl.addEventListener("click", 2);
// 2 - 핸들러(Handler, 실행할 함수
boxEl.addEventListener("click", function () {
  console.log("Click~!");
});

// 요소의 클래스 정보 객체 활용!
boxEl.classList.add("active");
let isContains = boxEl.classList.contains("active");
console.log(isContains); // true

boxEl.classList.remove("active");
isContains = boxEl.classList.contains("actvie");
console.log(isContains); // false
```

```javascript
// HTML 요소(Element) 모두 검색/찾기
const boxEls = document.querySelectorAll(".box");
console.log(boxEls);

// 찾은 요소들 반복해서 함수 실행!
// 익명 함수를 인수로 추가!
boxEls.forEach(function () {});

// 첫 번째 매개변수(boxEl) : 반복 중인 요소.
// 두 번째 매개변수(index) : 반복 중인 번호
boxEls.forEach(function (boxEl, index) {});

// 출력!
boxEls.forEach(function (boxEl, index) {
  boxEl.classList.add(`order-${index + 1}`);
  console.log(index, boxEl);
});
```

```javascript
const boxEl = document.querySelector(".box");

//Getter, 값을 얻는 용도
console.log(boxEl.textContent); // Box!!
//Setter, 값을 지정하는 용도
boxEl.textContent = "HEROPY?!";
console.log(boxEl.textContent); // HEROPY?!
```

## 메소드 체이닝

```javascript
const a = "Hello~";
// split: 문자를 인수 기준으로 쪼개서 배열로 반환.
// reverse: 배열을 뒤집기.
// join: 배열을 인수 기준으로 문자로 병합해 반환.
const b = a.split("").reverse().join(""); // 메소드 체이닝...

console.log(a); // Hello~
console.log(b); // ~olleH
```
