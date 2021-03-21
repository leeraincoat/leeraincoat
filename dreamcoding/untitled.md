# async  defer

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

