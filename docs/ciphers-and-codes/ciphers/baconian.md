---
title: 培根密码 Baconian
description: 培根密码
---

## 转换方式

培根密码先将所有的明文字符先分为两种：`a` 类和 `b` 类，然后按五个字符一组进行分组。
分组的依据不定，最经典的一种方法是按粗体字区分，亦有用字体区分。

每五个字符将会按照类似[二进制](./base.md)的方法进行转换，转成一个字符，可以参考下方表格。

标准的培根代码转换表中，I 与 J 共用一个代码，类似的，U 与 V 共用一个代码。

（因为培根密码有时用二进制表示会更加直观，本表在培根代码旁边增添了其二进制表示）

<table>
    <thead>
        <tr class="table-vertical">
            <td>字母</td>
            <td>代码</td>
            <td>二进制对应</td>
            <td>字母</td>
            <td>代码</td>
            <td>二进制对应</td>
        </tr>
    </thead>
    <tbody>
        <tr class="table-vertical">
            <td>A</td>
            <td>aaaaa</td>
            <td>00000</td>
            <td>N</td>
            <td>abbaa</td>
            <td>01100</td>
        </tr>
        <tr class="table-vertical">
            <td>B</td>
            <td>aaaab</td>
            <td>00001</td>
            <td>O</td>
            <td>abbab</td>
            <td>01101</td>
        </tr>
        <tr class="table-vertical">
            <td>C</td>
            <td>aaaba</td>
            <td>00010</td>
            <td>P</td>
            <td>abbba</td>
            <td>01110</td>
        </tr>
        <tr class="table-vertical">
            <td>D</td>
            <td>aaabb</td>
            <td>00011</td>
            <td>Q</td>
            <td>abbbb</td>
            <td>01111</td>
        </tr>
        <tr class="table-vertical">
            <td>E</td>
            <td>aabaa</td>
            <td>00100</td>
            <td>R</td>
            <td>baaaa</td>
            <td>10000</td>
        </tr>
        <tr class="table-vertical">
            <td>F</td>
            <td>aabab</td>
            <td>00101</td>
            <td>S</td>
            <td>baaab</td>
            <td>10001</td>
        </tr>
        <tr class="table-vertical">
            <td>G</td>
            <td>aabba</td>
            <td>00110</td>
            <td>T</td>
            <td>baaba</td>
            <td>10010</td>
        </tr>
        <tr class="table-vertical">
            <td>H</td>
            <td>aabbb</td>
            <td>00111</td>
            <td>U/V</td>
            <td>baabb</td>
            <td>10011</td>
        </tr>
        <tr class="table-vertical">
            <td>I/J</td>
            <td>abaaa</td>
            <td>01000</td>
            <td>W</td>
            <td>babaa</td>
            <td>10100</td>
        </tr>
        <tr class="table-vertical">
            <td>K</td>
            <td>abaab</td>
            <td>01001</td>
            <td>X</td>
            <td>babab</td>
            <td>10101</td>
        </tr>
        <tr class="table-vertical">
            <td>L</td>
            <td>ababa</td>
            <td>01010</td>
            <td>Y</td>
            <td>babba</td>
            <td>10110</td>
        </tr>
        <tr class="table-vertical">
            <td>M</td>
            <td>ababb</td>
            <td>01011</td>
            <td>Z</td>
            <td>babbb</td>
            <td>10111</td>
        </tr>
    </tbody>
</table>

除了上面较为常见的转换表外，还有一种 I, J, U, V 各自独立的转换表。

<table>
    <thead>
        <tr class="table-vertical">
            <td>字母</td>
            <td>代码</td>
            <td>二进制对应</td>
            <td>字母</td>
            <td>代码</td>
            <td>二进制对应</td>
        </tr>
    </thead>
    <tbody>
        <tr class="table-vertical">
            <td>A</td>
            <td>aaaaa</td>
            <td>00000</td>
            <td>N</td>
            <td>abbab</td>
            <td>01101</td>
        </tr>
        <tr class="table-vertical">
            <td>B</td>
            <td>aaaab</td>
            <td>00001</td>
            <td>O</td>
            <td>abbba</td>
            <td>01110</td>
        </tr>
        <tr class="table-vertical">
            <td>C</td>
            <td>aaaba</td>
            <td>00010</td>
            <td>P</td>
            <td>abbbb</td>
            <td>01111</td>
        </tr>
        <tr class="table-vertical">
            <td>D</td>
            <td>aaabb</td>
            <td>00011</td>
            <td>Q</td>
            <td>baaaa</td>
            <td>10000</td>
        </tr>
        <tr class="table-vertical">
            <td>E</td>
            <td>aabaa</td>
            <td>00100</td>
            <td>R</td>
            <td>baaab</td>
            <td>10001</td>
        </tr>
        <tr class="table-vertical">
            <td>F</td>
            <td>aabab</td>
            <td>00101</td>
            <td>S</td>
            <td>baaba</td>
            <td>10010</td>
        </tr>
        <tr class="table-vertical">
            <td>G</td>
            <td>aabba</td>
            <td>00110</td>
            <td>T</td>
            <td>baabb</td>
            <td>10011</td>
        </tr>
        <tr class="table-vertical">
            <td>H</td>
            <td>aabbb</td>
            <td>00111</td>
            <td>U</td>
            <td>babaa</td>
            <td>10100</td>
        </tr>
        <tr class="table-vertical">
            <td>I</td>
            <td>abaaa</td>
            <td>01000</td>
            <td>V</td>
            <td>babab</td>
            <td>10101</td>
        </tr>
        <tr class="table-vertical">
            <td>J</td>
            <td>abaab</td>
            <td>01001</td>
            <td>W</td>
            <td>babba</td>
            <td>10110</td>
        </tr>
        <tr class="table-vertical">
            <td>K</td>
            <td>ababa</td>
            <td>01010</td>
            <td>X</td>
            <td>babbb</td>
            <td>10111</td>
        </tr>
        <tr class="table-vertical">
            <td>L</td>
            <td>ababb</td>
            <td>01011</td>
            <td>Y</td>
            <td>bbaaa</td>
            <td>11000</td>
        </tr>
        <tr class="table-vertical">
            <td>M</td>
            <td>abbaa</td>
            <td>01100</td>
            <td>Z</td>
            <td>bbaab</td>
            <td>11001</td>
        </tr>
    </tbody>
</table>

## 加密举例

明文： `PUZZLE`

对应培根代码： `abbba baabb babbb babbb ababa aabaa`

类别区分方式：粗体（ a 为正常， b 为粗体）

找一个30个字母的句子： This message is using baconian code

加密： T**his**m **e**ss**ag** **e**i**sus** **i**n**gba** c**o**n**i**a nc**o**de

恢复正常空白：T**his** m**e**ss**age** i**s** **usi**n**g** **ba**c**o**n**i**an c**o**de

## 识别方式

主要的线索主要是二进制，特别是两种不同的文字。有时“培根”这种肉食也会被刻意凸显来说明培根密码的存在。

## 历史

培根密码通常认为出自英国哲学家弗朗西斯·培根之手。培根密码很多时候并不是直接使用，而是作为一种隐写术 (Steganography) 的方法存在。

培根密码本质上是将二进制信息通过样式的区别，加在了正常书写之上。培根密码所包含的信息可以和用于承载其的文章完全无关。

## 解码工具

- [dCode](https://www.dcode.fr/bacon-cipher)
- [Rumkin](https://rumkin.com/tools/cipher/baconian/)
