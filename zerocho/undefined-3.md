# 틱택톡

```javascript
           var body = document.body;
                
                var Numlist;
                var Numarray;

                function numSelect () {
                    for ( var i = 0; i < 4; i +=1 ){
            var select = Numlist.splice(Math.floor(Math.random() * (9 - i)), 1)[0];
            Numarray.push(select);
        }
                }

                Numlist = [1,2,3,4,5,6,7,8,9];
                Numarray = [];

                numSelect();
        console.log(Numarray);

                var  result = document.createElement('h1');
                body.append(result);

                var formPop = document.createElement('form');
                document.body.append(formPop);
                

                var inputPop = document.createElement('input');
                formPop.append(inputPop);
                inputPop.type = 'text'
                inputPop.maxLength = 4;
            
                var button = document.createElement('button');
                button.textContent = '입력!';
                formPop.append(button);

                var wrongNum = 0;

      //배열을 문자로 바꿀떄에는 join
      //문자를 배열로 바꿀떄에는 split

        formPop.addEventListener('submit', function callback (e){ //엔터를 쳤을 떄
            e.preventDefault();
            var answer = inputPop.value;
            if(answer === Numarray.join('')){ //답이 맞으면 
                result.textContent = '홈런';
                inputPop.value = '';
                inputPop.focus();
                numSelect();
         wrongNum = 0;
            }else{ // 답이 틀리면
                var answerArray = answer.split('');
                var strike = 0;
                var ball = 0; 
                wrongNum ++;
                if( wrongNum > 4){ // 4번 이상 틀렸을 경우
                    result.textContent = '4 chance gone, you fail answer is' + Numarray.join(',') +'임';
                    inputPop.value = '';
                    inputPop.focus();
                    numSelect();
                wrongNum = 0;
            }else{
                console.log('답이 틀리면', answerArray);
                for (var i = 0; i < 4; i += 1 ){
                    if (Number(answerArray[i]) === Numarray[i]){ //같은 자리인지 확인 
                        console.log('같은 자리?');
                        strike ++;
                    }else if(Numarray.indexOf(Number(answerArray[i])) > -1 ) { //같은 자리는 아니지만, 숫자가 겹치는지 확인 
                        console.log('겹치는 숫자?');
                        ball ++; 
                    }
                }
                result.textContent = strike + 'strike' + ball + 'ball';
                inputPop.value = '';
                inputPop.focus();
                
            }
         }

        });
```

