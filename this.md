# This

전역객체 

모든 전역변수와 함수는 window의 객체로 프로퍼티임 

```javascript
function func(){
    alert('Hello?');    
}
func(); //Hello?
window.func(); //Hello?
```

## This 

### this는 함수 내에서 호출 맥락을 의미하며 호출방식에 따라 달라진다. 

####  함수의 소속에 따라 this는 그 객체를 가리킨다. 

```javascript
function func(){
    if(window === this){
        document.write("window === this");
    }
}
func();
// window === this (기본적으로 this의 default값은 window라는 것을 알 수 있음)
```

함수호출 

```javascript
function func(){
    if(window === this){
        document.write("window === this");
    }
}
func();
// window === this (기본적으로 this의 default값은 window라는 것을 알 수 있음)
```

메 소드 호출

```javascript
var o = {
    func : function(){
        if(o === this){
            document.write("o === this");
        }
    }
}
o.func();  
//o === this (o === window.o)
```

생성자 호출 

* 생성자를 만들기 전에 호출하면 객체가 아니라 판단 \*

```javascript
var funcThis = null; 
function Func(){
    funcThis = this;
}
var o1 = Func();
if(funcThis === window){
    document.write('window <br />'); 
} //window
 
var o2 = new Func(); // 이 코드에서 this는 만들어진 o2객체.
if(funcThis === o2){
    document.write('o2 <br />');
} //o2
```

apply,call을 이용하여 thist값 제어 

```javascript
var o = {}
var p = {}
function func(){
    switch(this){
        case o:
            document.write('o<br />');
            break;
        case p:
            document.write('p<br />');
            break;
        case window:
            document.write('window<br />');
            break;          
    }
}
func(); //window
func.apply(o); //o
func.apply(p); //p
```

