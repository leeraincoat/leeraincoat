# 상속, prototype

## 상속\(inheritance\) 객체에는 변수, 메서드 가 있음

이 객체로 새 객체\(상속\)를 만들 수 있다.

 이 객체는 원본객체와 동일한 기능이다. 

상속받은 객체가 로직을 재활용 가능하다.

 자기에게 맞도록 개선 하는 것이 상속의 기본적인 원리이다.



### 생성자가 아닌  prototype으로 오리지널 객체 생성  

1.생성자 바깥쪽에 함수\(객체\).prototype&gt;&gt;

key값\(변수,함수...\) 로 설정 가능함. 

```javascript
function Person(name){
    this.name = name;
    this.introduce = function(){
        return 'My name is '+this.name; 
    }   
}
var p1 = new Person('minji');
document.write(p1.introduce()+"<br />"); //my name is minji

//prototype 활
function Person(name){
  this.name = name
}
Person.prototype.name =null;
Person.prototype.introduce = function(){
    return 'My name is '+this.name; 
}
let a = new Person('minji');
console.log(a.introduce()); //my name is minji
```

2, 버전 

함수 객체에 prototype 사용시 동일한 기능을 수행하는 new 생성자를 만들수 있고,

새로운 객체를 추가 할 수 있다. 

```javascript
function Person(name){
  this.name = name;
}
Person.prototype.name = null;
Person.prototype.introduce = function(){
  return 'my name is' + this.name;
}

function Programmer(name){
  this.name = name;
}
Programmer.prototype = new Person();
Programmer.prototype.coding = function(){
  return 'hello,world'
};
let a1 = new Programmer('minji');
console.log(a1.introduce())
console.log(a1.coding())
```

## prototype

생성자 &gt;&gt;&gt; 함수, 

 함수를 호출할때 new로 표기하면  생성자 함수

 어떤 객체를 만들때 객체의 메서드,프로퍼티를 가져올려고

여러방식을 거쳐 귀찮다 못해 생겨난 방식으로 

개발자의 영역은  불편충들 덕분에 나날이 발전하는게 아닌가 싶다. 

```javascript
function Ultra(){}
Ultra.prototype.ultraProp = true;
 
function Super(){}
Super.prototype = new Ultra();
 
function Sub(){}
Sub.prototype = new Super(); //Super.prototype(사용x)사용하면 상속자에도 영향미
 
var o = new Sub();
console.log(o.ultraProp); //결과는  true
```



