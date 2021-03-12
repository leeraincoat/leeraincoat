# 콜백 함수

## 자바스크립트에서는 함수도 값이다. 

### 함수는 객체의값으로 포함될 수 있다. 

이렇게 객체의 속성 값으로 담겨진 함수를 메소드\(method\)라고 부른다.

함수는 값이기 때문에 다른 함수의 인자로 전달 될수도 있다. 아래 예제를 보자.

```text
a = {
    b:function(){
    }
};
```

함수는 함수의 리턴 값으로도 사용할 수 있다.

```text
function cal(mode){
    var funcs = {
        'plus' : function(left, right){return left + right},
        'minus' : function(left, right){return left - right}
    }
    return funcs[mode];
}
alert(cal('plus')(2,1));
alert(cal('minus')(2,1));  
```

당연히 배열의 값으로도 사용할 수 있다.

```text
var process = [
    function(input){ return input + 10;},
    function(input){ return input * input;},
    function(input){ return input / 2;}
];
var input = 1;
for(var i = 0; i < process.length; i++){
    input = process[i](input);
}
alert(input);
```

## 처리위임 

값으로 사용될 수 있는 특성을 이용하면 함수의 인자로 함수로 전달할 수 있다. 값으로 전달된 함수는 호출될 수 있기 때문에 이를 이용하면 함수의 동작을 완전히 바꿀 수 있다. 인자로 전달된 함수 sortNumber의 구현에 따라서 sort의 동작방법이 완전히 바뀌게 된다.

```text
function sortNumber(a,b){
    // 위의 예제와 비교해서 a와 b의 순서를 바꾸면 정렬순서가 반대가 된다.
    return b-a;
}
var numbers = [20, 10, 9,8,7,6,5,4,3,2,1];
alert(numbers.sort(sortNumber)); // array, [20,10,9,8,7,6,5,4,3,2,1]
```



