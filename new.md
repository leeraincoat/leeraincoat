# 생성자 , new

## 객체  

연관된 변수와 함수를 그룹핑\(Grouping\)  , 변수는 프로퍼티 , 함수는 메소드  

```javascript
//(1)
var person = {}
person.name = 'egoing';
person.introduce = function(){
    return 'My name is '+this.name;
}
document.write(person.introduce());
//위 코드는 객체를 만드는 과정에 있어서 분산되어 있음, 중간에 다른 내용이 끼기 쉬움.

//(2)
var person = {
    'name' : 'egoing',
    'introduce' : function(){
        return 'My name is '+this.name;
    } // {}를 사용해서 grouping하여 가독성도 좋고, 내용이 분산되지 않음.
}
document.write(person.introduce());
```

## 생성자 

객체를 만드는 역할을 하는 함수 

첫글자를 대문자로 표시!.. 

```javascript
function Func_name(){}
var name = new Func_name(){}; 
```

## new 

함수를 호출할 때 new를 붙이면 새로운 객체를 만들어서 리턴함 

```javascript
function Person(){}
var p = new Person();
p.name = 'egoing';
p.introduce = function(){
    return 'My name is '+this.name; 
}
document.write(p.introduce());
```



