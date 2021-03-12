# 클로저

클로저\(closure\)는 **내부함수**가 **외부함수**의 맥락\(context\)에 접근할 수 있는 것을 가르킨다. 클로저는 자바스크립트를 이용한 고난이도의 테크닉을 구사하는데 필수적인 개념으로 활용된다.

#### 내부함수

#### 외부함수 

## 응용

```javascript
var arr = []
for(var i = 0; i < 5; i++){ 
//i의 값은 이 함수의 외부함수가 아님.
    arr[i] = function(){
        return i;
    }
}
for(var index in arr) {
    console.log(arr[index]());
} //55555

/* 이 함수를 내부함수로 하는 외부함수를 정의하고 
그 외부함수의 지역변수 값을 내부함수가 참조하도록 하면 01234를 얻을 수 있음. */

var arr = []
for(var i = 0; i < 5; i++){
    arr[i] = function(id) {
        return function(){
            return id;
        }
    }(i);
}
for(var index in arr) {
    console.log(arr[index]());
} //01234
```





