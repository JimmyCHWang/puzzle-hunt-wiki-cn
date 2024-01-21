---
title: 单表替换 Mono-Alphabetic
description: 单表替换
---

## 转换方式

单表替换 (Mono-Alphabetic Substitution) 是替换式密码中的最常见的方法，本章提到的很多替换类密码都可以视为一种特殊的单表替换。

单表替换的核心是一张字母表的对应关系，即字母表里的每一个明文字母应该换为哪一个密文字母。比如 A 换成 R ，C 换成 Z 之类的。替换关系可以没有任何潜在联系。

将明文字母被逐字替换后，往往生成的是无意义的字符串，也就是密文。

## 加密举例

我们选取以下表格当作加密字母表：

<table>
    <tr class="table-horizontal">
        <th>明文</th>
        <td>A</td>
        <td>B</td>
        <td>C</td>
        <td>D</td>
        <td>E</td>
        <td>F</td>
        <td>G</td>
        <td>H</td>
        <td>I</td>
        <td>J</td>
        <td>K</td>
        <td>L</td>
        <td>M</td>
    </tr>
    <tr class="table-horizontal">
        <th>密文</th>
        <td>Q</td>
        <td>W</td>
        <td>E</td>
        <td>R</td>
        <td>T</td>
        <td>Y</td>
        <td>U</td>
        <td>I</td>
        <td>O</td>
        <td>P</td>
        <td>L</td>
        <td>K</td>
        <td>J</td>
    </tr>
    <tr class="table-horizontal">
        <th>明文</th>
        <td>N</td>
        <td>O</td>
        <td>P</td>
        <td>Q</td>
        <td>R</td>
        <td>S</td>
        <td>T</td>
        <td>U</td>
        <td>V</td>
        <td>W</td>
        <td>X</td>
        <td>Y</td>
        <td>Z</td>
    </tr>
    <tr class="table-horizontal">
        <th>密文</th>
        <td>H</td>
        <td>G</td>
        <td>F</td>
        <td>D</td>
        <td>S</td>
        <td>A</td>
        <td>Z</td>
        <td>X</td>
        <td>C</td>
        <td>V</td>
        <td>B</td>
        <td>N</td>
        <td>M</td>
    </tr>
</table>

那么以下明文可以如此替换：

明文： `PUZZLEHUNT`

密文： `FXMMKTIXHZ`

??? tip "关于这张字母表"
    不知道你有没有察觉到上面那张字母表有什么意义。它在 QWERTY 键盘的基础上又加了一点变化，将第二行的顺序反了过来。
    于是你就能看到在键盘上的一个蛇形一般的顺序。

    然而，绝大多数的单表替换可能没有像这样的特殊意义。

## 密文分析

由于单表替换的绝大多数单表并没有特殊意义，人工解开单表密码往往比较繁琐和复杂，主要运用到的手段便是**频率分析** (Frequency Analysis) 。

在识别出目标语言的情况下，根据该语言里对应字母出现的频率，能够尝试性的确定某些**最常见的字母**，再根据这些字母找出常见的单词，
并以此为依据确定一些新的字母，最终实现密码表的解读。

这种工序往往是机械性且繁琐的，因此通常使用一些在线工具来辅助解决，以下是一些推荐工具：

- [焖肉面](https://philippica.github.io/cipher_machine/)
- [QUIPQIUP](https://www.quipqiup.com/)
- [不暴力不成活](https://puzz.cipherpuzzles.com/tools/bblbch.htm)

## 备注

单表替换最重要的内容是需要找到对应关系，即每一个字符真实表示的是哪一个字母。

对于一种更加广泛的单表，玩家面前的可能是一些从没有见过的文字或者图案，但这些图案都可以转化为某些数字、字母或者单词等，这通常会涉及到一些语言学的内容。

一些较为有名的图案单表替换包括：

- 跳舞的人像 ( The Dancing Men ) ——出自柯南·道尔《福尔摩斯归来记》
- 金甲虫 ( The Gold Bug ) ——出自爱伦·坡《金甲虫》
