# ASync , await

promise 체인을 깔끔하게 만들어주는 것 

```javascript
//1.async
function fetchUser() {
return new Promise((resolve, reject)=>{
    //do network reqeust in 10 secs...
    resolve('ellie');
    });
}

const user = fechUser();
user.then(console.log);
console.log(user);


//1.async
async function fetchUser() {
    //do network reqeust in 10 secs...
   return 'ellie';
}

const user = fechUser();
user.then(console.log);
console.log(user);

//2.await
function dleay(ms) {
    return new Promise(resolve => setTimeout,ms));
}

async function getApple(){
    await delay(3000);
    return 'apple';
}

async function getBanana(){
 await delay(3000);
 return 'banana';
}

fucntion pickFruits() {
    return getApple()
    .then(apple => {
        return getBanana().than(banana => `${apple}`+`${banana}`);
    })
}

pickFruits().then(console.log)


//2.await
function dleay(ms) {
    return new Promise(resolve => setTimeout,ms));
}

async function getApple(){
    await delay(1000);
    return 'apple';
}

async function getBanana(){
 await delay(1000);
 return 'banana';
}

async fucntion pickFruits() {
    const applePromise = getApple();
    const bananaPromise = getBanan();
    const apple = await applePromise();
    const banana = await bananaPromise();
    
    return `${apple}` + `${banana}`;
 
 }

pickFruits().then(console.log)

// 3. useful APIs
function pickAllFruits() {
    return Promise.all(
    [getApple(), getBanana()]).then(fruits => fruits.join('+') 
    );
}

pickAllFruits().then(console.log);

function pickOnlyOne() {
Promise.race([getApple(), getBanana()]);
}

pickOnlyOne().then(console.log);


```

