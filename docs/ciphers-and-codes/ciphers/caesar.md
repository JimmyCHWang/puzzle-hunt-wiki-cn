---
title: 凯撒密码 Caesar
description: 凯撒密码
status: frequent
---

别称： 移位密码 ( Shift Cipher ) 、 Rotation Cipher

## 转换方式

凯撒密码属于经典的替换密码。替换方法为将明文的每一个字母按照字母表向后推一定的数值（移位）进行偏移。
比如向后推 3 个的话，A 替换成 D，B 替换成 E，以此类推。
过头的字母将会从头开始，比如 X 替换成 A，Y 替换成 B。

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
        <th>凯撒 (+3)</th>
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
        <td>N</td>
        <td>O</td>
        <td>P</td>
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
        <th>凯撒 (+3)</th>
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
        <td>A</td>
        <td>B</td>
        <td>C</td>
    </tr>
</table>

凯撒密码可以用在除了正常的英文字母表以外的其他字母表上，比如数字或者 ASCII 码，甚至其他语言的字母表的情况。

## 加密举例

明文： `PUZZLEHUNT`

密钥（移动数量）： +3

密文： `SXCCOHKXQW`

## 历史

凯撒密码的发明者不可考，其命名是由于凯撒大帝 (Gaius Iulius Caesar) 曾经在传递军事情报时使用过而得名。

尽管凯撒密码的加密方式有 25 种（移动数量为 25 个，不动的不算），有个狭义的说法认为凯撒密码特指密钥为 +3 的情况。

## 识别方式

主要的线索包括凯撒、罗马等。

如果没有具体提示词，可以根据字母出现频率进行分析。

## 变种

凯撒密码的变种中比较有名的包括：

- ROT13 ：特指密钥为 13 的情况。
- ROT5 : 特指密钥为 5 的情况，多数用于字符集为数字的情况。
- ROT47 : 特指密钥为 47 且字符集为 [ASCII](../codes/ascii.md) 可见字符的情况。

## 解码工具

- [dCode](https://www.dcode.fr/caesar-cipher)
