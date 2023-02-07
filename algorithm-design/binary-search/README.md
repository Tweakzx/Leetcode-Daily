# Search

### 二分查找的通用模板

模板 1：

```java
boolean check(int x) {}

int search(int left, int right) {
    while (left < right) {
        int mid = (left + right) >> 1;
        if (check(mid)) {
            right = mid;
        } else {
            left = mid + 1;
        }
    }
    return left;
}Copy to clipboardErrorCopied
```

模板 2：

```java
boolean check(int x) {}

int search(int left, int right) {
    while (left < right) {
        int mid = (left + right + 1) >> 1;
        if (check(mid)) {
            left = mid;
        } else {
            right = mid - 1;
        }
    }
    return left;
}
```

### DFS



### BFS





<table><thead><tr><th data-type="checkbox"> </th><th>Problem</th><th data-type="select">Diff</th><th>Data</th><th data-type="rating" data-max="5"></th><th>Flag</th></tr></thead><tbody><tr><td>true</td><td><a data-mention href="34.-zai-pai-xu-shu-zu-zhong-cha-zhao-yuan-su-de-di-yi-ge-he-zui-hou-yi-ge-wei-zhi.md">34.-zai-pai-xu-shu-zu-zhong-cha-zhao-yuan-su-de-di-yi-ge-he-zui-hou-yi-ge-wei-zhi.md</a></td><td></td><td>2023/01/30</td><td>4</td><td>二分</td></tr><tr><td>true</td><td><a data-mention href="1870.-zhun-shi-dao-da-de-lie-che-zui-xiao-shi-su.md">1870.-zhun-shi-dao-da-de-lie-che-zui-xiao-shi-su.md</a></td><td></td><td>2023/01/31</td><td>4</td><td>二分</td></tr><tr><td>true</td><td><a data-mention href="1894.-zhao-dao-xu-yao-bu-chong-fen-bi-de-xue-sheng-bian-hao.md">1894.-zhao-dao-xu-yao-bu-chong-fen-bi-de-xue-sheng-bian-hao.md</a></td><td></td><td>2023/02/01</td><td>4</td><td>二分</td></tr><tr><td>true</td><td><a data-mention href="1898.-ke-yi-chu-zi-fu-de-zui-da-shu-mu.md">1898.-ke-yi-chu-zi-fu-de-zui-da-shu-mu.md</a></td><td></td><td>2023/02/02</td><td>4</td><td>二分</td></tr><tr><td>true</td><td><a data-mention href="1306.-tiao-yue-you-xi-iii.md">1306.-tiao-yue-you-xi-iii.md</a></td><td></td><td>2023/02/07</td><td>4</td><td>BFS</td></tr></tbody></table>
