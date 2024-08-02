---
title: Color Codes 颜色代码
description: 在PH里用于表示颜色的相关代码。包括RGB、十六进制表示、Pantone色号、HSL表示等。
status: frequent
---

Puzzle Hunt 世界里用于表示颜色的方法有很多，比较常见的包括 RGB 表示法，潘通色号等。

## RGB

RGB (Red, Green, Blue) 是使用红色、绿色、蓝色的光以不同比例混合来产生不同颜色的方法。
其主要应用在彩色显示屏、液晶显示器等电子产品上，在电脑中也经常使用 RGB 的方法来描述色彩。

通常来说，使用 RGB 表示一种颜色需要 3 个数，分别对应红色、绿色、蓝色光的比例，
每个数是一个 0 到 255 之间的整数。
其中 0 表示不用这个颜色的光， 255 表示使用这个颜色最纯的光。
使用 RGB 可以表示约 1600 万种颜色。

其中最常见的包括以下使用纯色混合的颜色（即每种光不是 0 就是 255）：

<table>
    <thead>
        <tr class="table-vertical">
            <td>名称</td>
            <td>英文</td>
            <td>颜色</td>
            <td>红</td>
            <td>绿</td>
            <td>蓝</td>
        </tr>
    </thead>
    <tbody>
        <tr class="table-vertical">
            <td>黑</td>
            <td>Black</td>
            <td style="background-color:black"></td>
            <td>0</td>
            <td>0</td>
            <td>0</td>
        </tr>
        <tr class="table-vertical">
            <td>红</td>
            <td>Red</td>
            <td style="background-color:red"></td>
            <td>255</td>
            <td>0</td>
            <td>0</td>
        </tr>
        <tr class="table-vertical">
            <td>绿</td>
            <td>Green</td>
            <td style="background-color:lime"></td>
            <td>0</td>
            <td>255</td>
            <td>0</td>
        </tr>
        <tr class="table-vertical">
            <td>蓝</td>
            <td>Blue</td>
            <td style="background-color:blue"></td>
            <td>0</td>
            <td>0</td>
            <td>255</td>
        </tr>
        <tr class="table-vertical">
            <td>黄</td>
            <td>Yellow</td>
            <td style="background-color:yellow"></td>
            <td>255</td>
            <td>255</td>
            <td>0</td>
        </tr>
        <tr class="table-vertical">
            <td>品红</td>
            <td>Magenta</td>
            <td style="background-color:magenta"></td>
            <td>255</td>
            <td>0</td>
            <td>255</td>
        </tr>
        <tr class="table-vertical">
            <td>青</td>
            <td>Cyan</td>
            <td style="background-color:cyan"></td>
            <td>0</td>
            <td>255</td>
            <td>255</td>
        </tr>
        <tr class="table-vertical">
            <td>白</td>
            <td>White</td>
            <td style="background-color:white"></td>
            <td>255</td>
            <td>255</td>
            <td>255</td>
        </tr>
    </tbody>
</table>
</tbody>
</table>

### 十六进制表示法

除了使用十进制的数来表示，RGB 颜色代码也会使用[十六进制](../ciphers/base.md)的格式来表示，分别从 00 到 FF。

表示手法一般使用形如 `#8800FF` 一样的，以井号为首，后面跟着 6 个十六进制字符的字符串。

### RGB 的标准颜色

在 RGB 表示法中通常有十六种标准颜色。

## 色彩查询工具

- [Pantone 色号查询](https://www.pantone-colours.com/)
- [ColorTell 颜色工具](https://www.colortell.com/colorspeed)
- [HSL 工具](https://hslpicker.com/)
- [HTML 具名颜色 (Named Color) 对应一览](https://developer.mozilla.org/zh-CN/docs/Web/CSS/named-color)
