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

