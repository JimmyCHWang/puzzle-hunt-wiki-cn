---
title: 列位移 Columnar
description: 列位移置换密码
---

全称： Columnar Transposition Cipher

简称： Transposition Cipher

## 转换方式

列位移密码是一种移位密码。列位移密码需要首先选取一个**每个字母都不一样**的词作为密钥。(1)
{.annotate}

1. 选取的不一定要是真实存在的词，只要每个字母都不一样就行。当然就算有重复，也可以踢掉重复的字母。

按照密钥的长度画出对应的列数，比如选取 `CIPHER` 为密钥就有 6 列。将明文**从左到右，从上到下**填写进这 6 列。
如果填写到最后一列没有填完，剩下的空白可以使用不常用的 X 补上。

之后，将选取的密钥进行字典序排序，排序时将带着那一列一起移动，得到新的 6 列。

最后，从字典序的第一列开始，**从上到下，从左到右**写出最终变换的结果。

!!! warning ""
    注意两条加粗文字的区别。将明文填写进列表里是沿着行的方向写，即**行优先**。
    将字母写成密文是沿着列的方向写，即**列优先**。

??? tips "说点闲话"
    有时候说到**移位加密** (Transposition Cipher) 这个名词，它既可以指能和置换加密同等地位的加密类型，
    也可以特指列位移这种具体的加密方式，足以彰显其在移位加密中的地位。

    需要指出，国内提到移位加密，第一反应多为**栅栏密码**。然而，其翻译 Railfence Cipher 在英文中
    实际上指的是另外一种加密。国内的栅栏密码实际指的是**不进行任何移动的列位移密码**。

    关于 Railfence Cipher ，请参考[栅栏密码](./railfence.md)页面。

## 加密举例

明文： `WELCOME TO PUZZLE HUNT WIKI CN`

密钥： `CIPHER`

进行排列：

<table>
    <thead>
        <tr class="table-vertical">
            <td>C</td>
            <td>I</td>
            <td>P</td>
            <td>H</td>
            <td>E</td>
            <td>R</td>
        </tr>
    </thead>
    <tbody>
        <tr class="table-vertical">
            <td>W</td>
            <td>E</td>
            <td>L</td>
            <td>C</td>
            <td>O</td>
            <td>M</td>
        </tr>
        <tr class="table-vertical">
            <td>E</td>
            <td>T</td>
            <td>O</td>
            <td>P</td>
            <td>U</td>
            <td>Z</td>
        </tr>
        <tr class="table-vertical">
            <td>Z</td>
            <td>L</td>
            <td>E</td>
            <td>H</td>
            <td>U</td>
            <td>N</td>
        </tr>
        <tr class="table-vertical">
            <td>T</td>
            <td>W</td>
            <td>I</td>
            <td>K</td>
            <td>I</td>
            <td>C</td>
        </tr>
        <tr class="table-vertical">
            <td>N</td>
            <td>[X]</td>
            <td>[X]</td>
            <td>[X]</td>
            <td>[X]</td>
            <td>[X]</td>
        </tr>
    </tbody>
</table>

注意这里使用了 `[X]` 来表示空白的地方。接下来我们对 `CIPHER` 这个词进行字典序排序，排序时要带着它下面的列一起动。

<table>
    <thead>
        <tr class="table-vertical">
            <td>C</td>
            <td>E</td>
            <td>H</td>
            <td>I</td>
            <td>P</td>
            <td>R</td>
        </tr>
    </thead>
    <tbody>
        <tr class="table-vertical">
            <td>W</td>
            <td>O</td>
            <td>C</td>
            <td>E</td>
            <td>L</td>
            <td>M</td>
        </tr>
        <tr class="table-vertical">
            <td>E</td>
            <td>U</td>
            <td>P</td>
            <td>T</td>
            <td>O</td>
            <td>Z</td>
        </tr>
        <tr class="table-vertical">
            <td>Z</td>
            <td>U</td>
            <td>H</td>
            <td>L</td>
            <td>E</td>
            <td>N</td>
        </tr>
        <tr class="table-vertical">
            <td>T</td>
            <td>I</td>
            <td>K</td>
            <td>W</td>
            <td>I</td>
            <td>C</td>
        </tr>
        <tr class="table-vertical">
            <td>N</td>
            <td>[X]</td>
            <td>[X]</td>
            <td>[X]</td>
            <td>[X]</td>
            <td>[X]</td>
        </tr>
    </tbody>
</table>

然后按照 C 列， E 列， H 列这样的顺序竖着写出，得到

密文： `WEZTN OUUIX CPHKX ETLWX LOEIX MZNCX`

## 识别方式

由于列位移密码仅仅只是更改了字母顺序，并没有变换原文，对于杂序的内容都可以尝试猜测密钥长度的方式将密文列出来。

有些列位移密文中会把 X 填补在空位，有些则不会，如果能够看到列出的每列最后有大量的相同字母，那么你很有可能猜中了列位移的长度。

之后可以通过解码工具进行辅助，将所有可能的排序列出，找到能够读通顺的内容。

## 解码工具

- [dCode](https://www.dcode.fr/columnar-transposition-cipher)
