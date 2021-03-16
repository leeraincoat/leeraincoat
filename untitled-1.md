---
description: 17. 조건문 ~  25. 반복문
---

# 조건문,반복문

## 조건문/Boolean

조건문은 IF로 시작한다. 

불린은 true와 false 두가지 밖에 없다. 

```javascript
if(true){
    alert('result : true');
}
```

## else 

```javascript
if(true){
    alert(1);
} else {
    alert(2);
}
```

1이 출

```javascript
if(false){
    alert(1);
} else {
    alert(2);
}
```

2가 출력 

## else if 

```javascript
if(false){
    alert(1);
} else if(true){
    alert(2);
} else if(true){
    alert(3);
} else {
    alert(4);
}
```

애도 2가 출력.  if\(false\)는 건너뛰고 else if\(true\) 값은 실행되고 뒤에 3 과 4는 2가 실행되었기 때문에

안나옴. 만약 2가 실행 안되면 3이 나오겠다.   예시를 위해 만들어진 것일 뿐 . 이건 조건문이라 하기 애매하고  실용성이 없다 .

## 노마드 코더 \#2-7

```javascript
const title = document.querySelector("#title");

const CLICKED_CLASS = "clicked";

function handleClick() {
title.classList.toggle(CLICKED_CALSS);
}
//if 문으로 add / remove 도 가능 

function init(){
 title.addEventListener("click",handClick);
}
init();
```

## 비교 연산자 

말 그대로 비교해서  값을 true 혹은 false 로 구분 

```javascript
==
    동등 연산자. 좌향과 우향을 비교해
    서로 값이 같다면 true, 
    다르다면 false가 된다. 
    alert (1==2) //false
    alert(1==1) //true
    alert("one"=="two") //false
    = 는 대입연산자로 헷깔리지 않게 주의!

===
    일치 연산자. 좌향과 우향이 '정확하게' 같을 때 
    true,다르다면 false가 된다. 
    alert(1 === "1") //false 데이터의 형식도 정확히 일치해야함 
    alert(1 == "1") //true  정보의 '의미'가 동일해서 true가 됨.

null 값이 없음. 프로그래머가 의도적으로 구현 
undefined 정의되지 않음. 프로그래머가 정의하지 않음 

true와 false는 Boolean의 데이터 타입.


 > 좌향이 우향보다 크다면 참, 그렇지 않다면 거짓 
 >= 좌향이 우향보다 크거나 같다. 
```

### prompt  

```javascript
promprt('당신의 나이는 ?')

alert(prompt('당신의 나이는')); 
```

```javascript
var id = prompt('아이디를 입력해주세요.');
if(if=='egoing'){
alert('아이디가 일치 합니다.');
} else {
alert('아이디가 일치하지 않습니다.');
}
```

### 조건문의 중첩 

```javascript
<script>
        id = prompt('아이디를 입력해주세요.');
        if(id=='egoing'){
            password = prompt('비밀번호를 입력해주세요.');
            if(password==='111111'){
                alert('인증 했습니다.');
            } else {
                alert('인증에 실패 했습니다.');
            }
        } else {
            alert('인증에 실패 했습니다.');
        }
    </script>
```

## 논리연산자.

&&  ---  and 연산자  두개 이상의 불린값을 하나로 조합가능 

```javascript
var id = prompt('아이디를 입력해주세요.');
var password = prompt("비밀번호를 입력해주세요");
if(id == 'leewoobi' && password ==='00'){
    alert('로그인 하셨습니다.'+id+' 님 반갑습니다.');
}else{
    alert('아이디가 일치하지 않습니다.');
}
```

## \|\|  or 연산자. 

둘중 하나만 참이어도 가능 

```javascript
if(true || true){
    alert(1);
}
```

### !는 부정 not 불린값을 반전시킨다. 

```javascript
if(!true && !true){
    alert(1);
}
```

조건문에 사용될 수 있는 데이터 형이 꼭 불린만 되는 것은 아니다. 관습적인 이유로 0는 false 0이 아닌 값은 true로 간주된다. 아래의 예제는 2를 출력한다.

### 기타 false로 간주되는 데이터 형

```javascript
if(!''){
    alert('빈 문자열')
}
if(!undefined){
    alert('undefined');
}
var a;
if(!a){
    alert('값이 할당되지 않은 변수'); 
}
if(!null){
    alert('null');
}
if(!NaN){
    alert('NaN');
}
```

## 반복\(loop\)

### while문 \(뭐시 복잡해 보통은 for 문을 쓴다고 함 \)

```javascript
while (조건){
    반복해서 실행할 코드
}
```

언제까지 실행 시킬거냐  적당한  시점에서 false로 바꿔주기 

```javascript
var i = 0;
// 종료조건으로 i의 값이 10보다 작다면 true, 같거나 크다면 false가 된다.
while(i < 10){
    // 반복이 실행될 때마다 coding everybody <br />이 출력된다. <br /> 줄바꿈을 의미하는 HTML 태그
    document.write('coding everybody <br />');
       i++    // i의 값이 1씩 증가한다.
       
    i++ 은 전위 연산자 값을 상승시키고 작업에 들어감
    ++i 는 후위 연산자 작업을 하고 값을 상승시킴 
  
```

## for문 \(while문 보다 가독성이 좋음\)

```javascript
for(var i = 0; i < 10; i++){
    document.write('coding everybody'+i+'<br />');
}
```



