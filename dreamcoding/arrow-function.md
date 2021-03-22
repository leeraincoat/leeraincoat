# arrow Function

## Function 

* fundamental building block in the program
* subprogram can be used multiple times
* performs a task or calculates a value

## 1.parameters  

```javascript
// pramitive parameters: passed by value
// object parameters: passed by reference

function changeName(obj) {
obj.name = 'coder';

}

const ellie = {name:'ellie};
changeName(ellie);
console.log(ellie);
```

## 2.deFault parameters \(added in ES6\)

```javascript
function showMessage(message, form) {
    console.log(`${message} by ${from}`);
}

showMessage('Hi!');
```

## 3.call Back 

```javascript
2.callback function using function expression
function randomQuiz(answer, printYes, printNO){

    if (answer === 'love you'){
            printYes();    
    }else {
            printNo();
    }
}
```



