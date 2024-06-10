# JavaScript 라이브러리


### Reset
```html
  <link href="https://cdn.jsdelivr.net/npm/reset-css@5.0.2/reset.min.css" rel="stylesheet" />
```
[reset.css](https://www.jsdelivr.com/package/npm/reset-css)
***

### Swiper
```html
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css" />
```
[swiperjs](https://swiperjs.com/demos)

```js
// new swiper(선택자, 옵션)
new Swiper(".notice-line .mySwiper", {
  direction: "vertical",
  autoplay: true,
  loop: true,
  spaceBetween: 30,
});

new Swiper(".notice .promotion .mySwiper", {
  slidesPerView: 3, // 한 번에 3개 보이기
  spaceBetween: 10, // 사이 여백 (px)
  centeredSlides: true, // 내용 정 가운데에 넣기
  loop: true,
  autoplay: {
    delay:5000
  },
  navigation: {
    nextEl: ".notice .promotion .swiper-next",
    prevEl: ".notice .promotion .swiper-prev",
  },
  pagination: {
    el: ".notice .promotion .swiper-pagination",
    clickable: true,
  },
});
```
***

### Lodash
```html
  <script src="https://cdnjs.cloudflare.com/ajax/libs/lodash.js/4.17.21/lodash.min.js" integrity="sha512-WFN04846sdKMIP5LKNphMaWzU7YpMyCU245etK3g/2ARYbPK9Ub18eG+ljU96qKRCWh+quCY7yefSmlkQw1ANQ==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
```
[lodash](https://lodash.com/)

```js
window.addEventListener('scroll', _.throttle(function () {
  // _.throttle(함수, 시간(ms)) -> 스크롤 이벤트가 스크롤 할때 마다 우르르 실행되지 않게 하기 위한 외부 라이브러리
}, 300));
```
***

### Gsap
```html
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js" integrity="sha512-7eHRwcbYkK4d9g/6tD/mhkf++eoTHwpNM9woBxtPUBWm67zeAfFC+HrdoE2GanKeocly/VxeLvIqwvCdk7qScg==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>  
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollToPlugin.min.js" integrity="sha512-1PKqXBz2ju2JcAerHKL0ldg0PT/1vr3LghYAtc59+9xy8e19QEtaNUyt1gprouyWnpOPqNJjL4gXMRMEpHYyLQ==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
```
[gsap](https://gsap.com/)  
[gsap -scroll to plugin](https://gsap.com/docs/v3/Plugins/ScrollToPlugin/)
```js
// gsap.to(요소, 지속시간(s), 옵션);
    gsap.to(badgeEl, .6, {
      opacity:0,
      display: 'none'
    });
    // to-top 버튼 보이기
    gsap.to('#to-top', .2, {
      x:0
    });
```
```js
//이벤트 실행 시 윈도우 스크롤탑 수치 0
toTopEl.addEventListener('click',function(){
  gsap.to(window, .7, {
    scrollTo:0
  });
});
```
***

### Scroll Magic
```html
  <script src="https://cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.8/ScrollMagic.min.js" integrity="sha512-8E3KZoPoZCD+1dgfqhPbejQBnQfBXe8FuwL4z/c8sTrgeDMFEnoyTlH3obB4/fV+6Sg0a0XF+L/6xS4Xx1fUEg==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
```
[scroll magic](https://scrollmagic.io/)
```js
const spyEls = document.querySelectorAll('section.scroll-spy');
spyEls.forEach(function(spyEl){
  //감시
  //code chaining 줄바꿈처리 한거임
  new ScrollMagic.
    Scene({
      triggerElement:spyEl, //보여짐 여부를 감시할 요소를 지정
      triggerHook : 0.8 //뷰포트에 어떤 지점에서 보여질지
    }).
    setClassToggle(spyEl, 'show'). // 요소, 클래스
    addTo(new ScrollMagic.Controller());
});
```
***
