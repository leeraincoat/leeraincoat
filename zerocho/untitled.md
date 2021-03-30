# 끝말잇기

제로초 강의는 정이 안간다.. 거실에서 번쩍이는 형광등도 그렇고 암튼 그렇다. 

말속도도 넘느려서 2배속하고 듣는다.   새삼 웹스썜의 강의질이 높다는 것을 느낀다. 

```javascript
var question = "돈까스"

while(true){
    var answer = (prompt(question));
    if(answer[0] === question[question.length -1]){
        question = answer;
        console.log('딩동댕!!');
    }else{
        console.log('땡^^!');
      
        break;
    }
}
```

