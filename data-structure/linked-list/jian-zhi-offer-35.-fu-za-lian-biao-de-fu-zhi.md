# 剑指 Offer 35. 复杂链表的复制

### Link

{% embed url="https://leetcode.cn/problems/fu-za-lian-biao-de-fu-zhi-lcof/" %}

### Problem

请实现 copyRandomList 函数，复制一个复杂链表。在复杂链表中，每个节点除了有一个 next 指针指向下一个节点，还有一个 random 指针指向链表中的任意节点或者 null。

示例 1：

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

{% code overflow="wrap" %}
```
输入：head = [[7,null],[13,0],[11,4],[10,2],[1,0]]
输出：[[7,null],[13,0],[11,4],[10,2],[1,0]]
```
{% endcode %}

示例2：

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

{% code overflow="wrap" %}
```
输入：head = [[1,1],[2,1]]
输出：[[1,1],[2,1]]
```
{% endcode %}

示例3:

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

{% code overflow="wrap" %}
```
输入：head = [[3,null],[3,0],[3,null]]
输出：[[3,null],[3,0],[3,null]]
```
{% endcode %}

示例4:

```
输入：head = []
输出：[]
解释：给定的链表为空（空指针），因此返回 null。
```

提示：

* `-10000 <= Node.val <= 10000`
* `Node.random` 为空（null）或指向链表中的节点。
* 节点数目不超过 1000 。

&#x20;

### Solution

{% tabs %}
{% tab title="C++" %}
```cpp
class Solution {
public:
    Node* copyRandomList(Node* head) {
        unordered_map<Node*, Node*> mp;
        for (Node* cur = head; cur != NULL; cur = cur->next) {
            mp[cur] = new Node(cur->val);
        }
        for (Node* cur = head; cur != NULL; cur = cur->next) {
            mp[cur]->next = mp[cur->next];
            mp[cur]->random = mp[cur->random];
        }
        return mp[head];
    }
};
```
{% endtab %}

{% tab title="Go" %}
```go
```
{% endtab %}
{% endtabs %}
