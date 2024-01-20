---
title: 埃特巴什 Atbash
description: Atbash 密码
---

别称： Mirror Cipher 、 Reverse Alphabet

## 转换方式

Atbash 密码属于经典的替换密码。替换的表格为将字母表倒过来排， A 替换成 Z ， B 替换成 Y ，以此类推。

<table>
    <tr class="table-horizontal">
        <th>字母</th>
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
        <th>Atbash</th>
        <td>Z</td>
        <td>Y</td>
        <td>X</td>
        <td>W</td>
        <td>V</td>
        <td>U</td>
        <td>T</td>
        <td>S</td>
        <td>R</td>
        <td>Q</td>
        <td>P</td>
        <td>O</td>
        <td>N</td>
    </tr>
    <tr class="table-horizontal">
        <th>字母</th>
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
        <th>Atbash</th>
        <td>M</td>
        <td>L</td>
        <td>K</td>
        <td>J</td>
        <td>I</td>
        <td>H</td>
        <td>G</td>
        <td>F</td>
        <td>E</td>
        <td>D</td>
        <td>C</td>
        <td>B</td>
        <td>A</td>
    </tr>
</table>

## 加密举例

明文： `PUZZLEHUNT`

密文： `KFAAOVSFMG`

## 历史

Atbash 密码最初用于希伯来文的加密与解密。希伯来语的前两个字符分别为 Aleph (א) 和 Bet (ב) ，他们分别被替换为
Taw (ת) 和 Shin (ש) 。其首字母 A, T, B, SH 构成了这个密码的名字。

## 识别方式

主要的线索包括镜像、反着写的单词。除此以外，希伯来文、以色列、从右往左写也是相关提示。

如果没有具体提示词，可以根据字母出现频率进行分析，英语里最常出现的字母 E, T, A, I, O, N 等在 Atbash 里被加密为
V, G, Z, R, L, M 。

## 解码工具

- [dCode](https://www.dcode.fr/atbash-cipher)
