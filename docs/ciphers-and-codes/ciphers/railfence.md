---
title: 栅栏密码 Railfence
description: 栅栏密码
---

!!! warning ""
    本页面提到的栅栏密码指的是英文环境中的 Railfence Cipher ， 并非国内的栅栏密码。
    关于国内“栅栏密码”的解释，请查看[列位移密码](./columnar.md)

别称： Zig-zag Cipher

## 加密方式

栅栏密码是一种移位密码，将明文字母按照之字形的方法书写。使用栅栏密码加密需要一个密钥，通常是一个 2 到 7 左右的数字。
举例，密钥为 3 ，然后想象有 3 条非常长的横栅栏。

明文从左上角开始向斜下方写入假想的栅栏和连续的“轨道”上，触底时向斜上方继续书写，如此反复，就像在写之字 (zig-zag) 一样。

以下是密钥为 3 ，明文为 `WELCOME TO PUZZLE HUNT WIKI CN` 的加密情况。

```plaintext
W...O...O...Z...U...I...N
.E.C.M.T.P.Z.L.H.N.W.K.C.
..L...E...U...E...T...I..
```

最后从第一行开始，按行写出密文。密钥为 3 的栅栏加密结果为 `WOOZUINECMTPZLHNWKCLEUETI` 。

## 加密样例

明文： `WELCOME TO PUZZLE HUNT WIKI CN`

密钥： 4

密文： `WEZTNEMTZLNWCLOOUEUIICPHK`

## 识别方式

题目中出现**之字**、**栅栏**、**上下**、**锯齿**、**驼峰**等信息均可指代此栅栏密码。

但需要注意的是国内环境中的栅栏密码不一定指这个栅栏密码，也有可能指[列位移](./columnar.md)。

破解栅栏密码往往需要猜测密钥，也就是栅栏数量，通过解码工具进行暴力查找。

## 解码工具

- [dCode](https://www.dcode.fr/rail-fence-cipher)
