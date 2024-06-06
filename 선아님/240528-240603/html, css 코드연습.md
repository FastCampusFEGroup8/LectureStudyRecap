# html, css 코드

## html
h1 {
  margin-left: 140px;
}

/*  min-width 아무리 줄여도 적어도 이크기 */
/* 전체적으로 가운데로 margin:0 auto; */
body {
  font-size: 20px;
  align-items: center;
  width: 600px;
  height: 2000px;
  min-width: 600px;
  font-family: -apple-system, BlinkMacSystemFont, "Malgul Gothic"
    "맑은고딕", helvetica, "Apple SD Gothic Neo", sans-serif;
  margin-left: 20px; 
}

/*disable를 쓰는경우 css에서는 [disable] {}로 해야한다*/
/* 클릭했을때 포커스됨, 포커스되는요소가 있음*/
input:focus {}
input {
  margin-left: 10px;
}
.container {
  display: flex;
  align-items: center;
  margin-left: 10px;
}
table {
  margin-left: 20px;
  margin-top: 10px;
}
td {
  border: 1px solid white;
  padding: 10px;
}
ul {
  margin-left: 20px;
}
/* 하위선택자 띄어쓰기필수 */
table .a {
  color: royalblue;
}

/* 일반형제 선택자, 흐림 밑으로 모두 블루, 막내가 우선순위*/
.cloudy~li {
  color: royalblue;
}

/* 인접형제 선택자 */
.clean+li {
  color: darkslateblue;
}

/*짝수순 막내요소는 최근 우선순위라 안변함 */
.weather li:nth-child(2n) {
  color: black;
}

/* frist-child 첫째 */
.weather li:first-child {
  color: green;
}

/* last-child 막내 */
.weather li:last-child {
  color: dimgray;
}

/* 부모요소 스타일 상속, 부정선택자가 우선 */
.weather2 {
  color: whitesmoke;
}

/* 부정선택자 span이 아닌것, color:inherit;입력시 상속됨.*/
.weather2 *:not(span) {
  color: #fc5603;
}
/* 우선순위 정리 *<태그(1)<class(20)<id(100)<style(1000)<!important 
  -> .container * {color:black !important;} */


/* border-radius 둥글게, opacity 투명도*/
img {
  width: 300px;
  height: 300px;
  margin: 20px 0 0 100px;
  border-radius: 50%;
  opacity: 1;
}


/* display:block은 인라인요소를 블록으로 text-align 수평정렬 */
/* justify-content:center; align-items:center;  */  
.site{
  display:flex;
  margin:25px 0 0 0;
  }  
a {
    width: 100px;
    height: 30px;
    background-color: #bb1fbb;
    color: white;
    text-decoration: none;
    text-align: center;
    font-weight: bold;
    margin-right: 20px;
    margin-left: 10px;
}
.site2 {
  background-color: white;
    color: green;
}
.site3 {
  background-color:rgb(231, 60, 60);
    color: white;
}
.site4 {
  background-color:white;
    color: rgb(231, 60, 60);
}


/* overflow:hidden 튀어나오는글 숨김. scroll->auto도 있다. */
/* line-height 글씨수직정렬, 보통 2;,text-indent 들여쓰기  */
.box {
  font-size: 16px;
  line-height: 30px;
  margin-top: 20px;
  width: 55px;
  height: 30px;
  background: LavenderBlush;
  overflow: hidden;
  text-indent: 15px;
  transition: 1s;
}

/* 가상클래스 선택자 hover  마우스 커서가 올라가 있는동안만 */
.box:hover {
  width: 120px;
}
.box:focus {
  width: 350px;
}

/*가상클래스 선택자 active 클릭중일때 */
.box:active {
  width: 10px;
}

/*.box::afer {content:""}와 before로 content 앞뒤에 가상의 요소를 넣을수 있음.*/
.box::after {
  content: "헤이즈 - 비도오고 그래서"
}


p {
  font-size: 15px;
}
.green {
  color: green;
  text-decoration: underline;
}
#pink {
  color: pink;
}

/* .green 10점 < span.green 11점 */
span.green {
  color: red;
  font-size: 18px;
}
span#pink {
  text-indent:20px;
  color: brown;
}

/* 점수같은경우 가장 최근 작성 코드 적용*/
p>.green {
  color: royalblue;
}
.select{color:darkgreen;
  text-decoration: underline;
  font-size: 18px;
}
