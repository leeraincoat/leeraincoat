# Json

HTTP

AJAX 

XML

json 유용사이트

{% embed url="http://www.jsondiff.com/" %}

{% embed url="https://jsonbeautifier.org/" %}

{% embed url="https://jsonparser.org/" %}



{% embed url="https://tools.learningcontainer.com/json-validator/" %}





## JSON는 오브젝트 처럼 키와 벨류로 이루어짐

* simplest data interchange format
* lightweight text-based structure
* easy to read
* key-value pairs
* used for serialization and transmission of data between the network 
* the network connection
* independent programming language and platform 

### object &lt;&lt;&lt; string \(json\) \|\|\|\|\|\|\|\|\|\|\|  object &gt;&gt;&gt;  string \(json\) 

```javascript
//1. Object to JSON
//stringify(obg)

const rabbit = {
    name: 'rabbit',
    color: 'white',
    size: null,
    birthDate: new Date(),
    jump: () => {
        console.log(`${name} can jump!`);
    },
};


json = JSON.stringify(rabbit);
console.log(json);

//내가 원하는 프로퍼티만 json으로 
json = JSON.stringify(rabbit, ["name"]);
console.log(json);

//함수로 

json =  JSON.stringify(rabbit, (key, value) => {
    console.log(`key: ${key}, value:${value}`);
    return key === 'name' ? 'ellie' : value;
});
console.log(json);


//2. JOSM to Object
//parse(json)
// 객체안에 있는 함수는 제이슨으로 변환이 안됨 개빡치게 
// 그래서 다 제이슨을 객체로 바꾸면 함수가 없어요
console.clear();
json = JSON.stringify(rabbit);
const obj = JSON.parse(json);
console.log(obj);
```



