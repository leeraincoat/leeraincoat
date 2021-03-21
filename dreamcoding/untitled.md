# async ,defer, use strict

## async

parsing HTML\(fetching && ecxuting js \)&gt; BLOCK &gt;&gt;parsing HTML

자바스크립트에 의존적인 코드라면 비추함.

```javascript
<script async src="a.js"></script>
```

## defer

\(fetching js  \)parsing HTML &gt;&gt; executingjs &gt;&gt;&gt;

```javascript
<script defer src="b.js"></script>
```

## use strict

유연한 언어 이기때문에 비상식적인 코딩이가능하기떄문에 방지하고자 쓰임

'use strict' 스트릿 모드에선 효율적이고  상식적인 코딩이가능하다고 함.

