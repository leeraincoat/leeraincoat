# Class Vs Object

### Class

* template
* declare once
* no data in

### object

* instance of a class
* created many times
* data in

## 1.class declarations

```javascript
class Person {
//constructor
 constructor(name, age) {
  // fields
  this.name = name;
  this.age = age;
  }
  
 //methods
 speack(){
 console.log(`${this.name}:hello!`);
  }
 }
 
 
 const ellie = new Person('ellie',20);
 console.log(ellie.name);
 console.log(ellie.age);
 ellie.speak();
 
 
 
```

## 2. Getter and Setters

```javascript
class User  {
     constructor(firstName, lastName, age) {
       this.firstName = firstName;
       this.lastName = lastName;
       this.age = age;
   }
   get age() {
     return this._age;
   }
   
   set age(value) {
    //  if (value<0) {
    //  throw Error('age can not be negative');
    // }
     this._age = value < 0 ? 0 : value;
   }
 }

const user1 = new User('steve','job',-1);


//겟으로 리턴하고 셋으로 설정한다.
//이게 뭔개소리야! 
 
```

## 3. Fields  \(public, private\) 

```javascript
class Experiment {
    publicField = 2;
    #privateField = 0;
}
const experiment = new Experiment();
console.log(experiment.publicField);
console.log(experiment.privateField);

//넘나리 최신 문법이라 지원이 안된데 
// 그럼 왜 알려주는거냐. 
```

## 4.static \(듣긴 했는데 최신문법이라 주저리 어쩌리 . 궁금하면 

## 영상 다시보자꾸나 \)



## 5.inheritance 

```javascript
class 뉴블라블라 extends 올드블라블라 {}  
// 상속해줌  
```



## 6.instanceof

```javascript
console.log(rectangle instabceof Rectangle); 
//checking true or false
```

[https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference)

