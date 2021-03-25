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
```

