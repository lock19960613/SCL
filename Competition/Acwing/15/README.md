## 15场周赛总结

做的比较差，感觉还是要把提高课刷了。

1. 第一题很裸的找规律

2. 第二题有通用的做法，这种末尾多少个0就是在找多少个2*5

3. 第三题就是一个记忆化dp（参考滑雪），判环的思路比较多，可以在记忆化搜索中判环。


另外关于memset的坑记录一下

memset 是按照字节(byte)对a进行逐个填充,所以-1和0可以得到你想要的结果（字面意思）。

在ACM中，

如果 `a` 的类型是 有符号整数（signed）

那么可以用这段代码，来将a指向的有符号整数都初始化为-1，但注意只有-1可用（0也可以）

原理是，signed int -1 在内存中的补码和 按char计算的4个byte，-1-1-1-1的补码相


```
-1(signed int) 补码为： 0xFFFFFFFF

4个-1（char）的补码为: 0xFFFFFFFF(他们在内存上是连续的）
```

别的就不尽相同了

```
‭-2(signed int)的补码为：0xFFFFFFFE‬

4个-2（char）的补码为：0xFEFEFEFE
```