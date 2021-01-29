#### [剑指 Offer 24. 反转链表](https://leetcode-cn.com/problems/fan-zhuan-lian-biao-lcof/)

1. 

时间复杂度 O(n)

空间复杂度 O(n)

```js
var reverseList = function(head) {
    var cur = null
    while(head) {
        let tmp = new ListNode(null)
        tmp.val = head.val
        tmp.next = cur
        cur = tmp
        head = head.next
    }
    return cur
};
```



2. 用set

```js
var getIntersectionNode = function(headA, headB) {
    let set = new Set()
    while(headA) {
        set.add(headA)
        headA = headA.next
    }
    while(headB) {
        if(set.has(headB)) {
            return headB
        }
        headB = headB.next
    }
};
```

