# promise

```javascript
//Promise is a javascript object for asynchronous operation
//state: pending ->> fulfilled or refected
//Producer vs Consumer

 //1.Producer 
 
  const  promise = new promoise((resolve, reject) => {
  //doing some heavy work (network , read files )
   console.log('doing something');
   setTimeout(()=> { 
      //resolve('ellie');
      reject(new Error('no network'));
   }, 2000 );
  });
  
  //2. Consumer: then , catch , finally
  promise// 
    .then(value => {
      console.log(value);
    })
    .catch(error => {
        console.log(error);
    });
    .finally( () => {
        console.log('finally');
    });
    
    //3. Promise chaining
    const fetchNumber = new Promise((resolve, reject)=>{
        setTimeout(() => resolve(1),1000);
    });
    
    fetchNumber
        .then(num => num *2)
        .then(num => num *3)
        .then(num => {
            return new Promise((resolve, reject)=> {
                setTimeout(() => resolve(num-1), 1000);
            });
        })
        .then(num => console.log(num));
```

