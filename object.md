# Object

모 든 르로퍼티와 객체의 부모임

객체지향 메서드 , 상속 

오브젝트가 가진  프로토타입을 모든 개체에서 기능을함 

 확장하면 번거러움 전체에 영향을 미치기 때문 

```javascript
Object.prototype.contain = function(neddle) {
    for(var name in this){
        if(this[name] === neddle){
            return true;
        }
    }
    return false;
}
var o = {'name':'egoing', 'city':'seoul'}
console.log(o.contain('egoing'));
var a = ['egoing','leezche','grapittie'];
console.log(a.contain('leezche'));

for(var name in o){
    console.log(name);  
} //name contain
```



