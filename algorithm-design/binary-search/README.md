# Search

<table><thead><tr><th width="73" data-type="checkbox"> </th><th width="259">Problem</th><th width="74" data-type="select">Diff</th><th width="124">Data</th><th width="110" data-type="rating" data-max="5"></th><th width="104">Flag</th></tr></thead><tbody><tr><td>true</td><td><a data-mention href="34.-zai-pai-xu-shu-zu-zhong-cha-zhao-yuan-su-de-di-yi-ge-he-zui-hou-yi-ge-wei-zhi.md">34.-zai-pai-xu-shu-zu-zhong-cha-zhao-yuan-su-de-di-yi-ge-he-zui-hou-yi-ge-wei-zhi.md</a></td><td></td><td>2023/01/30</td><td>4</td><td>二分</td></tr><tr><td>true</td><td><a data-mention href="1870.-zhun-shi-dao-da-de-lie-che-zui-xiao-shi-su.md">1870.-zhun-shi-dao-da-de-lie-che-zui-xiao-shi-su.md</a></td><td></td><td>2023/01/31</td><td>4</td><td>二分</td></tr><tr><td>true</td><td><a data-mention href="1894.-zhao-dao-xu-yao-bu-chong-fen-bi-de-xue-sheng-bian-hao.md">1894.-zhao-dao-xu-yao-bu-chong-fen-bi-de-xue-sheng-bian-hao.md</a></td><td></td><td>2023/02/01</td><td>4</td><td>二分</td></tr><tr><td>true</td><td><a data-mention href="1898.-ke-yi-chu-zi-fu-de-zui-da-shu-mu.md">1898.-ke-yi-chu-zi-fu-de-zui-da-shu-mu.md</a></td><td></td><td>2023/02/02</td><td>4</td><td>二分</td></tr><tr><td>true</td><td><a data-mention href="1306.-tiao-yue-you-xi-iii.md">1306.-tiao-yue-you-xi-iii.md</a></td><td></td><td>2023/02/07</td><td>4</td><td>BFS</td></tr><tr><td>true</td><td><a data-mention href="33.-sou-suo-xuan-zhuan-pai-xu-shu-zu.md">33.-sou-suo-xuan-zhuan-pai-xu-shu-zu.md</a></td><td></td><td>2023/08/08</td><td>5</td><td>二分</td></tr></tbody></table>

### 二分查找的通用模板

模板 1：

```go
boolean check(x int) {}

func search(left, right int) int {
    for left < right {
        mid := (left + right) >> 1
        if check(mid) {
            right = mid
        } else {
            left = mid + 1
        }
    }
    return left
}
```

模板 2：

```go
boolean check(x int) {}

func search(left, right int) int {
    for left < right {
        mid := (left + right + 1) >> 1
        if check(mid) {
            left = mid
        } else {
            right = mid + 1
        }
    }
    return left
}
```
