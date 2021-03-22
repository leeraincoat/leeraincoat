# operator, if ,for ,loop

## Variable types

#### primitive, **single item**: number, string , boolean , null , undefined ,symbol 

#### object, box container 



## 1.string concatenation 

```javascript
console.log('my'+'cat');
console.log('1'+2);
console.log(`string literals:
....
1+2 = $("ellie's /n book  )
>>>>>ellie's
>>>>>book  
 
 // \n 띄워쓰기
 // \t 탭 
```

## 2.numeric operators 

```javascript
console.log(1+1); //add
console.log(1-1); // substract
console.log(1/1); // divide
console.log(1*1); // multiply
console.log(1%1); // remainder
console.log(1**1); // exponentiation

```

## 3.increment and decrement operators

```javascript
let counter = 2;
const preIncrement = ++counter;
//counter = counter+1;    값을 올리고  
//preIncrement = counter;  할

const postIncrement = counter++;
//postIncrement = counter; 할당을 하고 
//counter = counter +1 ;  값을 올림  

  순서의 차이 
  
  x+=y // x = x + y 

```

## 4. \|\| \(or\) ,  && \(and\)  , !\(not\)



## 5. Equality

```javascript
const stringFive = '5';
const numberFive = 5;

// == loose equaltiy, with type conversion 내용물이 같냐  
console.log(stringFive == numberFive);
console.log(stringFive != numberFive);

//=== strict equality, no type conversion  타입 까지 같냐 
console.log(stringFive === numberFive);
console.log(stringFive !== numberFive);
```

## 6. Conditional operators : IF 

### if , else if , else 

```javascript
const name = 'df';
if(name = 'df'){
console.log('Welcome,Ellie');
}else if (name === 'coder'){
console.log('you are amazing coder');
}else {
  console.log('unknown')
}
```

## 7. Ternary operator : ?

```javascript
console.log(name === 'ellie' ? 'yes' : 'no') ;
```

## 8.switch statement 

```javascript
const browser = 'IE';
switch (browser) {
 case 'IE':
 console.log('go away');
 break;
 
 case 'Chrome':
 case 'Firefox':
 console.log('love you!');
   break;
   default:
 
 console.log('same all');
 break;



}

```

## 9. LOOPS 

```javascript
//while loop, while the condition is truthy
//body code is executed.

let i = 3;
while (i > 0) {
 console.log(`while: ${i}`);
 i--;
}

//do while  loop, body code is executed first,
//then check the condition.
do {
  console.log(`do while:${i}`);
  i--;
}while (i > 0);


//for loop , for ( begin;  condition; step)
for ( i = 3; i > 0; i--) {
 console.log(`for:${i}`);
}

for (let i = 3; i > 0; i = i-2 ){
 //inline variable declaration
 console.log(`inline  variable for: ${i}`);
}
```

