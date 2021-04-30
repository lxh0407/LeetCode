# 剑指 offer 17题

打印从1到最大的n位数

## 题目

输入数字 `n`，按顺序打印出从 1 到最大的 n 位十进制数。比如输入 3，则打印出 1、2、3 一直到最大的 3 位数 999。

### 示例

```
输入: n = 1
输出: [1,2,3,4,5,6,7,8,9]
```

### 说明

说明：

- 用返回一个整数列表来代替打印
- n 为正整数

## 自编代码

*class Solution {*

*public:*

  *int pow(int a,int b){*

​    *int s=1;*

​    *for(int i=0;i<a;i++){*

​      *s=s*b;*

​    *}*

​    *return s;*

  *}*

  *vector<int> printNumbers(int n) {*

​    *int s=pow(n,10);*

​    *vector<int> nums;*

​    *for(int i=1;i<s;i++){*

​      *nums.push_back(i);*

​    *}*

​    *return nums;*

  *}*

*};*

### 运行结果

![1.1.JPG](https://i.loli.net/2021/05/07/IQjY1xBJRT835Dt.jpg)





