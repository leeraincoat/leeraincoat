# 정규표현식

#### 정규표현식 리터럴 

/a/  패턴이라는 변수를  사용해서  찾고자 하는 것  a 

```javascript
var pattern = /a/
```

#### 정규표현식 객체 생성자

```javascript
var pattern = new RegExp('a'); 
```

### 정규표현식 메소드 실행 

```javascript
var pattern = /a/;
pattern.exec('abcde');
>>>>>>["a"]

var pattern = /a./;
pattern.exec('abcde');
>>>>>>["ab"]
```

```javascript
var pattern = /a/'
pattern.exec('bcdef'); //찾아서 있다면 리턴해주는 함수 
>>>>>null

pattern.text('abcde'); 
>>>>>true
pattern.text('bcde');
>>>>>false
```

.exec &gt;&gt;&gt;추

.text &gt;&gt;&gt;&gt; 불린값 테스트 



### string.match\(\)

```javascript
var pattern = /a/;
var str = 'abcdef';
str.match(pattern);

>>>>>["a"]
```

### string.replace\(\)

```javascript
console.log('abcdef'.replace(pattern, 'A'));  // Abcdef
```

## i 를 붙이면 대소문 구분하지 않는다. 

```javascript
var xi = /a/;
console.log("Abcde".match(xi)); // null
var oi = /a/i;
console.log("Abcde".match(oi)); // ["A"];
```

## g 를 붙이면 검색된 모든 결과를 리턴한다. 

```javascript
var xg = /a/;
console.log("abcdea".match(xg));
var og = /a/g;
console.log("abcdea".match(og));
```

## 캡쳐  

```javascript
var pattern = /(\w+)\s(\w+)/;
var str = "coding everybody";
var result = str.replace(pattern, "$2, $1");
console.log(result);
```

## 치환 

```javascript
var urlPattern = /\b(?:https?):\/\/[a-z0-9-+&@#\/%?=~_|!:,.;]*/gim;
var content = '생활코딩 : http://opentutorials.org/course/1 입니다. 네이버 : http://naver.com 입니다. ';
var result = content.replace(urlPattern, function(url){
    return '<a href="'+url+'">'+url+'</a>';
});
console.log(result);
```

#### 결과

```javascript
생활코딩 : <a href="http://opentutorials.org/course/1">http://opentutorials.org/course/1</a> 입니다. 네이버 : <a href="http://naver.com">http://naver.com</a> 입니다.

```



