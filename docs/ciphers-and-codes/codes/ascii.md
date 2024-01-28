---
title: ASCII
description: ASCII 美国标准信息交换码
status: frequent
---

误称： ASC2 、 ASCLL

## 介绍

美国标准信息交换码 (American Standard Code for Information Interchange, 首字母简称 ASCII ) 是一种电脑编码系统。

在计算机中，所有的数据在存储和运算时都要使用二进制数 (Binary) 表示，这其中包括各种文字，比如大小写英文字母 A, B, c, d ，
数字 0, 1, 2 ，还有常用的符号 *, + 等。 ASCII 标准将每一个常用的文字对应到一个二进制数上，计算机都按照这种标准运行并交流，
就像一种语言一样，说同一种话的人才能互相理解。

ASCII 编码使用 **7 位的二进制数**来代表一个字符。能表达的 128 个字符之中，有 95 个是可见字符，编号从 32 (0x20) 至 126 (0x7E)。

ASCII 表的全表比较大，请参考下方附录。

## 在 PH 中的应用

在 PuzzleHunt 中， ASCII 常用于将一种数字与英语字母对应的方式。
一般而言， ASCII 表需要关注的内容包括以下三个部分：

- 编号 48 - 57 (0x30 - 0x39) ： 数字区，分别对应数字 0 至 9
- 编号 65 - 90 (0x41 - 0x5A) ： 大写字母区，对应字母 A 至 Z
- 编号 97 - 122 (0x61 - 0x7A) ： 小写字母区，对应字母 a 至 z

也就是所有的字母与数字的区域。括号中的内容是它们的十六进制编号。
线索中如果经常出现这些范围内的数，将它们转换成 ASCII 码或许是一个不错的选择。

## ASCII 的扩展

第一份 ASCII 标准公布于 1963 年，限制于当时的计算机处理器宽度，只允许一次性处理 8 位的二进制字符，
因此 ASCII 只涵盖 128 个字符。在这之后，更多的文字和符号需要在电脑上显示出来，
人们设计出了新的字符集 [Unicode](./unicode.md) 与编码标准 UTF-8 。

## 附录：ASCII 表

<figure markdown>
  ![ASCII表](../../_static/images/ascii-table.svg){ width="500" }
  <figcaption markdown>ASCII 表</figcaption>
</figure>
