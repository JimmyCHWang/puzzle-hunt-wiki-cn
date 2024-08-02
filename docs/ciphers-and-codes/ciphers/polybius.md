---
title: 棋盘密码 Polybius
description: 棋盘密码及其变种
status: frequent
---

别称： Polybius Square

## 转换方式

棋盘密码的加密需要用到一个 5×5 的字符方阵。如果没有特别提供这个加密方阵，默认按照下面的方阵作为加密或解密密钥。

```plain title="Polybius 加密方阵"
\  1 2 3 4 5
1  A B C D E
2  F G H I K
3  L M N O P
4  Q R S T U
5  V W X Y Z
```

这里默认 I 与 J 共用一个格子。

棋盘密码的目的是将每一个字母替换成两个数字，如 P 替换为 35， I 替换为 24。棋盘密码通常默认表示行的数字在列的数字前面。

## 加密举例

明文： `PUZZLEHUNT`

密文： `35 45 55 55 31 15 23 45 33 44`

## 解码工具

- [焖肉面（古典密码）](https://philippica.github.io/cipher_machine/)
- [dCode](https://www.dcode.fr/polybius-cipher)

## 变种

### 通过密钥生成加密方阵

若提供了一份密钥（一个字符串），可以由密钥生成加密方阵。
具体做法为先移去密钥里重复的字符（总是保留第一次出现的字符），
然后将这些字符填入 5×5 的方阵，再将字母表中没有用到的其他字符按顺序填入。

```plain title="Polybius 加密方阵，密钥 = PUZZLEHUNT"
P U Z L E
H N T A B
C D F G I
K M O Q R
S V W X Y
```

### TapCode

TapCode 在棋盘密码的基础上，使用 `.` 的数量来代替数字。比如 `... ...` 就是棋盘 (3,3) 的 N。

以下是 `PUZZLEHUNT` 的 TapCode 密文：

```plaintext
... ..... .... ..... ..... ..... ..... ..... ... . . ..... 
.. ... .... ..... ... ... .... ....
```

解码工具： [dCode](https://www.dcode.fr/tap-cipher)

### Nihilist

Nihilist 加密在棋盘密码的基础上又加了一层密钥，即 Nihilist 包括一个加密方阵和一个密钥。

Nihilist 将每个明文字母和密钥的字母都转化成一个两位数。然后将明文和密钥进行循环匹配，
即明文第一位匹配密钥第一位，明文第二位匹配密钥第二位，以此类推。如果密钥用完了就从第一位重新用。

之后将每一位明文转换的数字与密钥转换的数字**相加**，这个取值范围在 22 到 110 之间，取末两位作为结果。

我们用以下方阵作为加密方阵：

```plain title="Polybius 加密方阵"
P U Z L E
H N T A B
C D F G I
K M O Q R
S V W X Y
```

并选取 `POLYBIUS` 为密钥。

则明文 `CIPHER CODE BREAKING` 可以加密为

`427825764080439443583900405953863377`

加密过程：

<table>
    <tr class="table-horizontal">
        <th>明文</th>
        <td>C</td>
        <td>I</td>
        <td>P</td>
        <td>H</td>
        <td>E</td>
        <td>R</td>
        <td>C</td>
        <td>O</td>
        <td>D</td>
        <td>E</td>
        <td>B</td>
        <td>R</td>
        <td>E</td>
        <td>A</td>
        <td>K</td>
        <td>I</td>
        <td>N</td>
        <td>G</td>
    </tr>
    <tr class="table-horizontal">
        <th>数字</th>
        <td>31</td>
        <td>35</td>
        <td>11</td>
        <td>21</td>
        <td>15</td>
        <td>45</td>
        <td>31</td>
        <td>43</td>
        <td>32</td>
        <td>15</td>
        <td>25</td>
        <td>45</td>
        <td>15</td>
        <td>24</td>
        <td>41</td>
        <td>35</td>
        <td>22</td>
        <td>34</td>
    </tr>
    <tr class="table-horizontal">
        <th>密钥</th>
        <td>P</td>
        <td>O</td>
        <td>L</td>
        <td>Y</td>
        <td>B</td>
        <td>I</td>
        <td>U</td>
        <td>S</td>
        <td>P</td>
        <td>O</td>
        <td>L</td>
        <td>Y</td>
        <td>B</td>
        <td>I</td>
        <td>U</td>
        <td>S</td>
        <td>P</td>
        <td>O</td>
    </tr>
    <tr class="table-horizontal">
        <th>数字</th>
        <td>11</td>
        <td>43</td>
        <td>14</td>
        <td>55</td>
        <td>25</td>
        <td>35</td>
        <td>12</td>
        <td>51</td>
        <td>11</td>
        <td>43</td>
        <td>14</td>
        <td>55</td>
        <td>25</td>
        <td>35</td>
        <td>12</td>
        <td>51</td>
        <td>11</td>
        <td>43</td>
    </tr>
    <tr class="table-horizontal">
        <th>求和</th>
        <td>42</td>
        <td>78</td>
        <td>25</td>
        <td>76</td>
        <td>40</td>
        <td>80</td>
        <td>43</td>
        <td>94</td>
        <td>43</td>
        <td>58</td>
        <td>39</td>
        <td>100</td>
        <td>40</td>
        <td>59</td>
        <td>53</td>
        <td>86</td>
        <td>33</td>
        <td>77</td>
    </tr>
</table>

解码工具： [dCode](https://www.dcode.fr/nihilist-cipher)

### ADFGVX

ADFGVX 是一战时期德军使用的加密系统。他将 A-Z 的 26 个字母和 0-9 的 10 个数字组合成 36 个字符，
并排列成 6×6 的方阵。与棋盘密码的不同之处首先在行和列的标志，他们使用的不是 1-6 的数字，而是 ADFGVX 这六个字母。

```plain title="ADFGVX 加密方阵"
\  A D F G V X
A  A B C D E F
D  G H I J K L
F  M N O P Q R
G  S T U V W X
V  Y Z 0 1 2 3
X  4 5 6 7 8 9
```

先按照常规的棋盘密码方式将密码翻译成若干对 A, D, F, G, V, X 字母组成的字符串后，选取一个密钥，
使用[列移位密码](./columnar.md)的方式将其进行置换。列移位不足的字母由 X 补上。

比如我们加密 `PUZZLEHUNT` 时，得到的第一层密文为 `FG GF VD VD DX AV DD GF FD GD`。

我们选取的列移位密码的密钥为 `CIPHERS`，其顺序为 `1453267`。

将得到的密文按密钥长度 7 排好：

<table>
    <tr class="table-vertical">
        <th>密钥</th>
        <td>C</td>
        <td>I</td>
        <td>P</td>
        <td>H</td>
        <td>E</td>
        <td>R</td>
        <td>S</td>
    </tr>
    <tr class="table-horizontal">
        <th></th>
        <td>F</td>
        <td>G</td>
        <td>G</td>
        <td>F</td>
        <td>V</td>
        <td>D</td>
        <td>V</td>
    </tr>
    <tr class="table-horizontal">
        <th></th>
        <td>D</td>
        <td>D</td>
        <td>X</td>
        <td>A</td>
        <td>V</td>
        <td>D</td>
        <td>D</td>
    </tr>
    <tr class="table-horizontal">
        <th></th>
        <td>G</td>
        <td>F</td>
        <td>F</td>
        <td>D</td>
        <td>G</td>
        <td>D</td>
        <td>[X]</td>
    </tr>
</table>

这里的最后一个 `[X]` 是因为空位补上去的。

然后将七列 CIPHERS 按照字典序排列：

<table>
    <tr class="table-vertical">
        <th>密钥</th>
        <td>C</td>
        <td>E</td>
        <td>H</td>
        <td>I</td>
        <td>P</td>
        <td>R</td>
        <td>S</td>
    </tr>
    <tr class="table-horizontal">
        <th></th>
        <td>F</td>
        <td>V</td>
        <td>F</td>
        <td>G</td>
        <td>G</td>
        <td>D</td>
        <td>V</td>
    </tr>
    <tr class="table-horizontal">
        <th></th>
        <td>D</td>
        <td>V</td>
        <td>A</td>
        <td>D</td>
        <td>X</td>
        <td>D</td>
        <td>D</td>
    </tr>
    <tr class="table-horizontal">
        <th></th>
        <td>G</td>
        <td>G</td>
        <td>D</td>
        <td>F</td>
        <td>F</td>
        <td>D</td>
        <td>[X]</td>
    </tr>
</table>

最后的密文将从第一列开始，按照列优先方式，从上到下，从左到右写出。
即，先从上到下写第一列的字符，然后第二列，以此类推。

这里我们的密文最终结果为 `FDG VVG FAD GDF GXF DDD VDX`。

解码工具： [dCode](https://www.dcode.fr/adfgvx-cipher)

#### ADFGX

该密码另有一套 ADFGX 密码，即去掉了 V 列，也拿掉了 0-9 的数字，变回经典的 5×5 的方阵。

ADFGX 密码的加密方式与 ADFGVX 一致。

解码工具： [dCode](https://www.dcode.fr/adfgx-cipher)
