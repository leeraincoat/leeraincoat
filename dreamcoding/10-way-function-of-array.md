# function of array

## split

```javascript
//make an array out of a string
{
     const fruits = 'apple,banan,cherry';
     const result = fruits.split(,);
     console.log(result);
    
}
```

## find

```javascript
const students = [
new Student ('A',29, true, 45),
new Student ('B',28, false, 80),
new Student ('C',30, true, 90),
new Student ('D',40, false, 66),
new Student ('E',18, true, 88),
];

//find a student with the score 90
{
const result = students.find(function (student,index){
  return student.score === 90;
  });
  console.log(result);  
}
{
const result = students.find((student) =>
 student.score === 90;
 ); 
  console.log(result);  
}


```

map

```javascript
//make an array containing only the students' scores
//result should be: [45,80,90,66,88]
{
    const result = students.map((student) => student);
    console.log(result);
}
{
    const result = students.map((student) => student.score);
    console.log(result);
}
{
    const result = students.map((student) => student.score * 2);
    console.log(result);
}
```

