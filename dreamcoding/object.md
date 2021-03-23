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

//5. in operator: property existence check (key in ob)
console.log('name' in ellie);

//6. for..in vs for.. of 
//for (key in obj)
for ( key in ellie ) {
    console.log(key);
}

//for (value of iterable)
const array = [1,2,3,4,];
for ( let i = 0; i < array.length; i++){
console.log(array[i]);
}

for(value of array) {
     console.log(value);
}

//7. fun cloning
//object.assign(dest, [obj1, obj2, obj3...])

const user = {name: 'ellie', age : '20'};
const user2 = user;
console.log(user);

//oldway
const user3 = {};
for (key in user)  {
    user3[key] = user[key];
}

const user4 =
Object.assign({},user);
console.log(user4);

const user4 = Object.assign({},user);
console.log(user4);


```

