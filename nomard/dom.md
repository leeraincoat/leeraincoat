# Dom

DOM = **D**ocument **O**bject **M**odul

html 문서의 요소들을 객체로 만들어 여러 이벤트를 만들 수 있음 

```javascript
const title = document.querySelector("#title");
const CLICKED_CLASS = "clicked";

function handleClick(){
    title.classList.toggle(CLICKED_CLASS);
}

function init() {
    title.addEventListener("click",handleClick);
}
init();
```

