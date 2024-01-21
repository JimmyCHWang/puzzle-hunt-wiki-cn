---
title: 棋盘密码 Polybius
description: 棋盘密码及其变种
status: frequent
---

别称： Polybius Square

## 转换方式

棋盘密码的加密需要用到一个 5 × 5 的字符方阵。如果没有特别提供这个加密方阵，默认按照下面的方阵作为加密或解密密钥。

```plain title="Polybius 加密方阵"
\  1 2 3 4 5
1  A B C D E
2  F G H I K
3  L M N O P
4  Q R S T U
5  V W X Y Z
```

这里默认 I 与 J 共用一个格子。

棋盘密码的目的是将每一个字母替换成两个数字，如 P 替换为 35 ， I 替换为 24 。棋盘密码通常默认表示行的数字在列的数字前面。

## 加密举例

明文： `PUZZLEHUNT`

密文： `35 45 55 55 31 15 23 45 33 44`

## 变种

### 通过密钥生成加密方阵

若提供了一份密钥（一个字符串），可以由密钥生成加密方阵。
具体做法为先移去密钥里重复的字符（总是保留第一次出现的字符），
然后将这些字符填入 5 × 5 的方阵，再将字母表中没有用到的其他字符按顺序填入。

```plain title="Polybius 加密方阵，密钥 = PUZZLEHUNT"
P U Z L E
H N T A B
C D F G I
K M O Q R
S V W X Y
```
