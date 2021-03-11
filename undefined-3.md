# 유효범위

## 유효범위\(scope\)는 변수의 수명을 의미한다. 

### 지역변수\(local\),   전역변수\(global\) 

함수안에서 만들어진 변수와 밖에서 만들어진 변수의 차이인지. 

호출 시점, 사용시점이  아닌 정의될떄   정적 유효범위의 이해 



#### 아래 두개의 예제는 변수 i를 지역변수로 사용했을 때와 전역변수로 사용했을 때의 차이점을 보여준다. 전역변수는 각기 다른 로직에서 사용하는 같은 이름의 변수값을 변경시켜서 의도하지 않은 문제를 발생시킨다.

```javascript
function a (){
    var i = 0;
}
for(var i = 0; i < 5; i++){
    a();
    document.write(i);
}

>>>>>>01234
```

전역변수 사용 

```javascript
function a (){
    i = 0;
}
for(i = 0; i < 5; i++){
    a();
    document.write(i);
}  무한반복.. 끝이 안남.

```

불가피하게 전역변수를 사용해야 하는 경우는 하나의 객체를 전역변수로 만들고 객체의 속성으로 변수를 관리하는 방법을 사용한다.

```javascript
MYAPP = {}
MYAPP.calculator = {
    'left' : null,
    'right' : null
}
MYAPP.coordinate = {
    'left' : null,
    'right' : null
}
 
MYAPP.calculator.left = 10;
MYAPP.calculator.right = 20;
function sum(){
    return MYAPP.calculator.left + MYAPP.calculator.right;
}
document.write(sum());

```

전역변수를 사용하고 싶지 않다면 아래와 같이 익명함수를 호출함으로서 이러한 목적을 달성할 수 있다.

```javascript
(function(){
    var MYAPP = {}
    MYAPP.calculator = {
        'left' : null,
        'right' : null
    }
    MYAPP.coordinate = {
        'left' : null,
        'right' : null
    }
    MYAPP.calculator.left = 10;
    MYAPP.calculator.right = 20;
    function sum(){
        return MYAPP.calculator.left + MYAPP.calculator.right;
    }
    document.write(sum());
}())  
```

로직을 모듈화 하는 일반적인 방법; 



