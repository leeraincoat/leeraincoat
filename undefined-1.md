---
description: 25~50
---

# 객체

## 객체 \(object\)  <a id="object"></a>

* 객체는 중괄호로 시작해서 중괄호로 끝난다.
* 객체는 키와 벨류로 구분된다. {'egoing': 10 } 앞이 키 뒤과 벨

```text
var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};
```

```text
var grades = {};grades['egoing'] = 10;grades['k8805'] = 6;grades['sorialgi'] = 80;
```

```text
var grades = new Object();grades['egoing'] = 10;grades['k8805'] = 6;grades['sorialgi'] = 80;
```

```text
var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};alert(grades['sorialgi']);
```

## 객체와 반복문의 만남 \(for in 문 \) <a id="for-in"></a>

```text
var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};for(key in grades) {    document.write("key : "+key+" value : "+grades[key]+"
");}
```

```text
key :   egoing value : 10key :   k8805 value : 6key :   sorialgi value : 80
```

## 객체 지향 프로그래밍  <a id="undefined"></a>

객체에는 객체를 담을 수 도 있고 함수도 담을 수 있다.

```text
var grades = {    'list': {'egoing': 10, 'k8805': 6, 'sorialgi': 80},    'show' : function(){        for(var name in this.list){            document.write(name+':'+this.list[name]+"
");        }    }};grades.show();
```

this는 소유하고 있는 객체를 가리키는 변수를 말한다.

​

## 모듈  <a id="undefined-1"></a>

프로그램은 작고 단순한 것에서 크고 복잡한 것으로 진화한다. 그 과정에서 코드의 재활용성을 높이고, 유지보수를 쉽게 할 수 있는 다양한 기법들이 사용된다. 그 중의 하나가 코드를 여러개의 파일로 분리하는 것이다. 이를 통해서 얻을 수 있는 효과는 아래와 같다.

​

* 자주 사용되는 코드를 별도의 파일로 만들어서 필요할 때마다 재활용할 수 있다.
* 코드를 개선하면 이를 사용하고 있는 모든 애플리케이션의 동작이 개선된다.
* 코드 수정 시에 필요한 로직을 빠르게 찾을 수 있다.
* 한번 다운로드된 모듈은 브라우저에 저장, 동일한 로직을 실행할 때 트래픽 절약가능

## 정규표현식  <a id="undefined-2"></a>

정규표현식 리터럴

### 정규표현식 객체 생성자 <a id="undefined-3"></a>

```text
var pattern = new RegExp('a');
```

​

