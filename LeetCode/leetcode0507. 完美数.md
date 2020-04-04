## 题目

#### [507. 完美数](https://leetcode-cn.com/problems/perfect-number/)



对于一个 **正整数**，如果它和除了它自身以外的所有正因子之和相等，我们称它为“完美数”。

给定一个 **整数** `n`， 如果他是完美数，返回 `True`，否则返回 `False`

**示例：**

```
输入: 28
输出: True
解释: 28 = 1 + 2 + 4 + 7 + 14
```





代码：



``` java

```













## 类似题目

一个数如果恰好等于它的因子之和，这个数就称为"完数"。例如6=1＋2＋3.编程找出1000以内的所有完数。



**程序分析：**

- 1) 遍历 i 从2 到 1000 的数；
- 2) 对这个数 i 从1到 a-1 进行除，然后将所有能整除 a 的数进行相加得 sum
- 3) 如果 sum==a，则说明 a 为完数，否则，不是。



代码：

``` java
public class Main {
    public static void main(String[] args) {
        System.out.println("1000以内的完美数如下：");
        int number = 1000;

        for (int i = 2; i <= number; i++) {
            int sum = 0;
            for (int j = 1; j < i; j++) {
                if (i % j == 0) {
                    sum += j;
                }
            }
            if (sum == i) {
                System.out.print(i + " ");
            }
        }
    }
}
```





