---
title: 关于 Puzzle Hunt
description: 介绍了关于 Puzzle Hunt 的定义以及常见的玩法
---

## 解谜寻宝 (Puzzle Hunt) 是什么？

解谜寻宝 **( Puzzle Hunt，简称 PH )** 是一类综合解谜活动。在该语境下也可以直接用 **Hunt** 指代。

与日常生活中的解谜不同的是，解谜寻宝通常需要参与者通过团队合作解开一系列的谜题。

解谜寻宝一般具有竞技性质，主办方往往会根据完成时间给参加的队伍排名。因此，解谜寻宝也属于一种比赛。
值得注意的是，相对于其他的解谜活动（例如密室逃脱），解谜寻宝的谜题结构和剧情往往更加立体和严谨，期望的完成时间也相对更长。
因此，目前大部分解谜寻宝都采用线上举办的方式。

## Hunt 的一般流程

参与 Hunt 的玩家一般最开始并不会看到所有的谜题。玩家通过先解决一部分的谜题，可以看到新的谜题，即**解锁 ( Unlock )** 。
在积累了一定数量的谜题答案后，会解锁一个被称为**元谜题 ( Meta Puzzle，简称 Meta )** 的题目。
这个题目通常会使用到你已经解开的谜题答案。将 Meta 解开后，你便完成了这次 Hunt ，又称为**完赛**。

``` mermaid
graph LR
  A[开始] --> B[发现题目];
  B -->|解谜| C[解开题目];
  C -->|解锁新题| B;
  C -->|达到一定条件时| D[解锁 Meta];
  D ---->|解开 Meta| E[结束];
```

!!! note "关于解锁机制"
    对于一些比较小型的 Hunt，可能不存在解锁机制，即玩家一开始就能看到所有的题目。但是，玩家仍然需要通过解开最终的 Meta 才能结束这次 Hunt 。

## 多区域 Hunt

对于一些比较大型的 Hunt ，可能会出现不止一道 Meta 的情况。这种 Hunt 通常会存在多个**区域 ( area )** ，玩家需要将每个区域逐个击破。
通常来说，对于这种多个区域的 Hunt ，会出现使用到多个跨区域的小题答案或 Meta 答案的情况，
这种谜题被称为 **Meta Meta ( 简称 MM )** 。

最后的一道 Meta Meta 通常被称为**最终元谜题 ( Final Meta，简称 FM )** 。
在这种情况下，解开最终元谜题标志着玩家顺利完成了本次活动。

目前，国内知名度较高的大型 Puzzle Hunt ，如 CCBC 、 PnKU 、 MiaoHunt ，均采用这种多区域模式。

## Puzzle Hunt 怎么参加？

若要查询接下来要举办的国内外 Puzzle Hunt ，您可以前往以下解谜寻宝日历查询：

- 由 喵喵喵解谜 团队维护的日历： [https://calendar.puzzlehunt.cn/](https://calendar.puzzlehunt.cn/)
- 由 北京大学推理协会 团队维护的日历： [https://info.pkupuzzle.art/calendar.html](https://info.pkupuzzle.art/calendar.html)

目前国内比较知名的大型 Puzzle Hunt 均采取组队参加的方式，人数上限为 4 至 6 人左右。
玩家可以在主办方管理的玩家群内找到兴趣相投的其他玩家，也可以找到现实中身边的朋友一起参赛。
访问日历中的 Hunt 网址即可查询相关报名信息。

国内举办的大型 Puzzle Hunt 的时长通常为两周左右，一般从周五晚上或假期前一天晚上开始，直到下一个周末结束。

除了大型 Puzzle Hunt 以外，也会有一些较小型的解谜活动，例如公众号解谜、网页解谜等，具体可以在上述日历上查询。

??? note "对国外 Hunt 有兴趣的玩家"
    可以访问由 Puzzle Hunt Calendar 维护的日历： [https://puzzlehuntcalendar.com/](https://puzzlehuntcalendar.com/)
    该日历上的内容多为国外举办的 Hunt ，语言多为英文，部分 Hunt 可能需要在线下才能参与。
