# arguments

생활코딩 

함수안에서 사용할 수 있도록 그 이름이나 특성이 약속된 배열 

노마드 코더 

인자. 

```javascript
function sum(){ //매개변수가 없음.
    var i, _sum = 0;    
    for(i = 0; i < arguments.length; i++){
        document.write(i+' : '+arguments[i]+'<br />');
        _sum += arguments[i];
    }   
    return _sum;
}
document.write('result : ' + sum(1,2,3,4)); //인자가 전달됨.(arguments 덕분!)
//0 : 1
//1 : 2
//2 : 3
//3 : 4
//result : 10
```

매개변수의 수 

함수.lengh  

{% embed url="https://arguments.length" %}



