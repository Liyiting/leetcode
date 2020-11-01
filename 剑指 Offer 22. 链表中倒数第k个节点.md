# 剑指 Offer 22. 链表中倒数第k个节点

<https://leetcode-cn.com/problems/lian-biao-zhong-dao-shu-di-kge-jie-dian-lcof/>

1. 双指针法，第二个指针在两个指针相差为k的时候再开始走，第一个指针到达最后一个节点的时候返回第一个指针

时间复杂度 O(N)

空间复杂度 O(1)

```js
var getKthFromEnd = function(head, k) {
    let count = 0
    let res = head
    while(head) {
        head = head.next
        if(count - k >= 0) {
            res = res.next
        }
        count++
        console.log(head, res)
    }
    return res
};
```



2. 压栈：把原链表全部压栈，取出后k个节点重新组成链表

时间复杂度 O(N)

空间复杂度 O(N)

```js
var getKthFromEnd = function(head, k) {
    let stack = []
    let res = []
    while(head) {
        stack.push(head)
        head = head.next
    }
    while(k > 0) {
        res = stack.pop()
        k--
    }
    return res
};
```

