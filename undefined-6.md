# 표준내장객체의 확장

자 바스크립트 자체에서 지원하는 내장 객체 

object,function,array,string,boolean,number,math,date,RegExp\(정규표현식\) 등 

 내장객체에 추가 하는 형식으로 prototype 

```javascript
// let arr = new Array('a','b','c','d','e')
// function getRandom(randomthing){
//   let index = Math.floor(randomthing.length*Math.random());
//   return randomthing[index];
// }
// console.log(getRandom(arr))

//prototype을 활용한 내장객체의 확
let arr = new Array('a','b','c','d','e')
Array.prototype.random = function(){
  let index = Math.floor(this.length*Math.random());
  return this[index];
}
console.log(arr.random());
```

