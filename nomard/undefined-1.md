# 함수

## Function 

내장함수 기본적으로 자바스크립트 안에 장착되어있는 \(console.log\(\) 같은 것들 



### Parameters

\(\)안에 들어가는 값 &gt;  arguments, 인자 

arguments는 변수와 비슷한 개념으로 이해   
 우리가 지정한 \(\)이 안 값을 넣어서 

함수는 그걸 사용해서 실행시킬 것이다.  
 외부에 있는 데이터를 읽는 함수를 만드는 방법이라고 할 수 있다.



## Return 

함수의 실행된 결과 값을 출력하는 값 

#### Back Ticks \( \` \)  

템플릿 리터럴 

```javascript
function sayHello(name, age){
  console.log(`Hello ${name} you are ${age} years old`);
}
sayHello("Kelly" , 26);
```



