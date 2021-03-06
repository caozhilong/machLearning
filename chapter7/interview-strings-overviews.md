# 8.3 字符串

## 字符串简介

## 面试题总体分析

**关联分析**

- 和数组相关，内容广泛
- 概念理解: 字典序
- 简单操作: 插入、删除字符、旋转
- 规则判断: 罗马数字转换、是否是合法的整数、浮点数
- 数字运算: 大数加法、二进制加法
- 排序、交换(partition过程)
- 字符计数(hash): 变位词
- 匹配: 正则表达式、全串匹配、KMP、周期判断
- 动态规划: LCS、编辑距离、最长回文串
- 搜索: 单词变换、排列组合



## 一些例题

### 【例一】0-1串交换排序

**问题描述:** 

把一个0-1串(只包含0和1的串)进行排序，你可以交换任意位置，问最少交换的次数?

**问题分析**

快速排序partition最左边的那些0和最右边的那些1都可以不管

**例子**

00...0001......0111....1

**解决方案**

**方法1**

```java
 int answer = 0;
int len = 100;
char[] a = new char[len];

for (int i = 0 , j = len-1; i < j; ++i,--j){
    for (;(i<j) && ( a[i] == '0'); ++i);
    for (;(i>j) && ( a[j] == '1'); --j);
    if(i < j) {
        ++answer;
    }
}
```



### 【例二】字符串替换和复制

### 【例三】交换星号

### 【例四】子串变位词

### 【例五】单词(字符串)翻转

