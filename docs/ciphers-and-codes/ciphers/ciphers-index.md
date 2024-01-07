---
title: 密码 Ciphers
description: 密码页面索引
---

## 密码的分类

古典密码通常分为两种：替换式密码和移位式密码。PH 中两种密码均会有所涉及。

### 替换式密码

**替换式密码 ( Substitution Cipher )** 基于对明文的替换。

我们考虑最简单的一种单字母替换，每个字母被替换成它后面的一个字母， A 变成 B ， B 变成 C 这样。

这样单词 `HELLO` 就会被替换成 `IFMMP` ，失去了实际意义。想要把这个密文变回明文，只要将每个字母替换成它前面的一个字母即可。

这便是 key=1 的凯撒密码。

### 移位式密码

**移位式密码 ( Transposition Cipher )** 基于对明文字母的移位。

我们考虑一种经典的移位：将字母两两交换。AB 换成 BA ，TD 换成 DT 这样。

我们将 `THE QUICK FOX JUMPS OVER A LAZY DOG` 这句话，在去掉空格后每两个字母进行交换，
可以得到 `HTQEIUKCOFJXMUSPVORELAZADYGO` 。

可以看到虽然没有改字符，只是换了位置，交换后的字符串就已经比较难以理解。
