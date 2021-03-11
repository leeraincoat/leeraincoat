# 배열

## 반복문의 제어 break continue <a id="break-continue"></a>

1.break

```text
for(var i = 0; i < 10; i++){    if(i === 5) {        break;    }    document.write('coding everybody'+i+'
');
```

2.continue \(5에서 컨티뉴로 중지되지만 반복문은 계속 실행 \)

```text
for(var i = 0; i < 10; i++){    if(i === 5) {        continue;    }    document.write('coding everybody'+i+'
');}
```

```text
coding everybody 0coding everybody 1coding everybody 2coding everybody 3coding everybody 4coding everybody 6coding everybody 7coding everybody 8coding everybody 9
```

## 반복문의 중첩 <a id="undefined"></a>

```text
// 0부터 9까지 변수 i에 순차적으로 값을 할당        for(var i = 0; i < 10; i++){    // 0부터 9까지의 변수를 j의 값에 순차적으로 할당    for(var j = 0; j < 10; j++){            // i와 j의 값을 더한 후에 출력        // String은 숫자인 i와 j의 데이터 타입을 문자로 형태를 변환하는 명령이다.         // String()을 제거하고 실행해보면 의미가 좀 더 분명하게 드러날 것이다.        document.write(String(i)+String(j)+'
');    }}
```

## 함수 <a id="undefined-1"></a>

함수\(function\)란 하나의 로직을 재실행 할 수 있도록 하는 것으로 코드의 재사용성을 높여준다

```text
function numbering(){    i = 0;    while(i < 10){        document.write(i);        i += 1;    }   }numbering();
```

##  함수의 입력\(\)과 출력\(return\) <a id="return"></a>

함수의 함이 상자를 말한다. 상자안에 숫자를 넣으면 다른값이 출력

익명함수 \(\)\(\); 이름이 없고 바로 실행

## 배열\(array\) <a id="array"></a>

#### 배열\(array\)이란 _**연관된 데이터를 모아서 통으로 관리하기 위해서**_ <a id="array-1"></a>

 사용하는 데이터 타입이다. 변수가 하나의 데이터를 저장하기 위한 것이라면 배열은 여러 개의 데이터를 하나의 변수에 저장하기 위한 것이라고 할 수 있다.

* 대괄호로 시작해서 대괄호로 끝나야 한다.
* 함수는 여러개의 입력값을 받을 수있지만 출력 하나인점을 보안하기 위해 사용
* 배열의 진가는 반복문에서 나타난다.

## 배열과 반복문의 만남  <a id="undefined-2"></a>

```text
function get_members(){    return ['egoing', 'k8805', 'sorialgi'];}members = get_members();​// members.length는 배열에 담긴 값의 숫자를 알려준다.for(i = 0; i < members.length; i++){    // members[i].toUpperCase()는 members[i]에 담긴 문자를 대문자로 변환해준다.    document.write(members[i].toUpperCase());       document.write('
');}
```

* .length는 배열에 담긴 값의 숫자를 알려준다.
* .push 는 배열에 원소 값을 새로 추가한다.
* .unshift는 새로운 원소값을 배열의 첫번째에 추가한다. index값 1번으로
* .splice는 첫번째 인자에 해당하는 원소부터 두번째 인자에 해당하는 원소의 숫자만큼의 값을 배열로부터 제거한 후에 리턴한다. 그리고 세번째 인자부터 전달된 인자들을 첫번째 인자의 원소 뒤에 추가한다. 0이면 삭제없이 추가 1이면 삭제하고 추가

## 배열의 제거와 정렬  <a id="undefined-3"></a>

### 1.제거  <a id="1"></a>

* .shift는 제일 앞에 원소를 제거함
* .pop은 제일 뒤에 있는 원소를 제거함

### 2.정렬  <a id="2"></a>

* .sort 정순
* .reverse 역순

​

