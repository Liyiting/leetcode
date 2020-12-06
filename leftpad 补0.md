leftpad 补0

1. 暴力解

```js
function leftpad(str, len, ch = ' ') {
  let length = len-str.length
  return ch + Array(length).join(ch) + str
}
leftpad('hello', 10, 0)
```

2. 二分法

```js
function leftpad2 (str, len, ch = ' ') {
  let length = len-str.length
  let total = ''
  while(length) {
  	console.log(length)
  	if(length%2===1) {
  		total += ch
  	}
  	if (length === 1) {
  		return total + str
  	}
  	ch += ch
  	length = parseInt(length / 2)
  }
}
leftpad2('hello', 10, 0)
```

