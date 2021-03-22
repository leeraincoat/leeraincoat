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
 
```

