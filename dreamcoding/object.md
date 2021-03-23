# object

## object

키 와 벨류로 이루어진 집합체다.

```javascript
//with javascript magic (dynamically typed language)
//can add properties later 
ellie.hasJob = true;
console.log(ellie.hasJob);

//can delete properties later
delete ellie.hasJob;
console.log(ellie.hasJob);  

//2. Computed properties
//key should be always string

console.log(ellie.name);
console.log(ellie['name']);
ellie['hasJob'] = true;
console.log(ellie.hasJob);

//3. Property value shorhand
const person1 = {name:'bob', age: 2 };
const person2 = {name:'steve', age:3};
const person3 = {name:'dave', age:4};
const person4 = {name:'ellie',age: 30};

console.log(person4);

//4. Constructor function
function Person(name, age ) {
    //this = {};
    this.name = name;
    this.age = age;
    //return  this;
}

```

