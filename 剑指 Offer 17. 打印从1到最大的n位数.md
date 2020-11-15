# 剑指 Offer 17. 打印从1到最大的n位数

<https://leetcode-cn.com/problems/da-yin-cong-1dao-zui-da-de-nwei-shu-lcof/>

1. 暴力解 ：先计算出最大位数的限制，创建一个Array，循环push

时间复杂度 O(n)

空间复杂度 O(n)

```js
var printNumbers = function(n) {
    let limit = Math.pow(10, n)
    console.log
    let arr = []
    let i = 1
    while (i < limit) {
        arr.push(i)
        i++
    }
    return arr 
};
```

