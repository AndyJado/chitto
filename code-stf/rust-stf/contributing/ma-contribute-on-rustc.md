
# 做个RUST Contributer

[翻译诊断](https://blog.rust-lang.org/inside-rust/2022/08/16/diagnostic-effort.html) 是每个人都想要的功能

想想吧, 你的程序报错了

在一大堆英文, 斜杠, 和字符里有一句

**你这个生命周期没标注, 给编译器搞紧张了, 试试这个🤏**

`get involved`他们说

offical 建议[这里开始](https://github.com/rust-lang/rust/issues/100717)

但第二步`开始配置环境`就险象丛生.

`#llvm`好大个怪物,下不动, 也编译不动.

换个[起点](https://rustc-dev-guide.rust-lang.org/getting-started.html)

` git clone https://github.com/rust-lang/rust.git`

很大, GB级别.

`cd rust`

`./x.py setup` 花掉五分钟

安装交互选b : 贡献给编译器

`./x.py check` 花掉五分钟

`./x.py build` 花掉五分钟

可以开始搬砖了

但搬砖的时候也有些[窍门](https://rustc-dev-guide.rust-lang.org/building/suggested.html)

2022年 8月19日 星期五 11时52分47秒 CST

edited 2022年 11月19日

---

第三步`cd rust/compiler/` 选择无人认领的`crate`

我学别人在评论区说话,要了`rustc_borrowck`

他们@了我

这活就给我干啦

`rustc`指的是`rust compiler` 我才知道

吃下红色药丸, 再次 `./x.py check`

出现了225个报错

我不知道我在干什么,但大概我做的是对的

就像在Lumon的macrodata refinement上班💼

我向rust提交了我的第一个PR

migrate some `rustc_borrowck` diagnostic

不到几分钟

`a member reviewed my code`

我回复了他的每个评论,带着问题

但他没有, 我的, 我以为这是一个对话

我自己想办法吧


2022年 8月20日 星期六 21时33分19秒 CST

---

我在本地修改代码

push到我fork来的远程仓库中

出现了个小插曲

[我的PR未经审阅被自动接收了](https://github.com/rust-lang/rust/pull/100798)

双脸火燎燎

Member说你重开一个吧

好的但等我再次提交的时候

上游仓库已经更新了很多

`merge conflict`斗智斗勇

代码里出现了很多的`======`

`<<<<<<<<<<<<<<<<<<<<`

hunk, hunk

[学会git](https://rustc-dev-guide.rust-lang.org/git.html#standard-process)

2022年 8月22日 星期一 20时34分30秒 CST

---

没有把自己的修改提前`stash`

文件夹里发生踩踏事件, 场面失控

`x.check`报大错, member说我ice了

摘掉全部我的`commit` 

`stash`, `rebase`, `pop`

合成一个大`commit`

提交`draft PR`

`CI`报错 : `failed 112 tests`

`#fluent`的空格`u+0020`和多行缩进我拎不清


2022年 8月23日 星期二 15时12分18秒 CST

---

我摸清`rustc`的报错怎么玩的了

`err`是砖头

`span`是图纸

`diag`把墙垒起

我的工作是拆墙然后垒砌

诶, 为什么塌了?

`undo commit`

`stash stash stash`

学点儿shell帮了很多忙

尽管只写一点`alias`

新砌的墙到时候

见到中国人会说你好

见到法国人说蚌住

提交代码之后

说`r?`

等着review


Wed Aug 24 20:53:15 CST 2022

---

member 每次回复我消息

都在句末带一个`:)`

我: 🤡

不过我我想我现在真的知道我在干什么了

事情无聊起来

Thu Aug 25 10:00:38 CST 2022

---

`📌 Commit 622217d has been approved by davidtwco

It is now in the queue for this repository.`



Fri Aug 26 21:05:56 CST 2022

---

Merged #100900 into master.



Sat Aug 27 13:20:23 CST 2022

---

`trait system` & `borrowcheck`是RUST的两大新活

我承包的是`borrowcheck`

尽管知道该怎么玩了

但面前还有十几面墙要拆

是日my day job给了我一些压力

我发脾气, 撂挑子不干

不搞错, 我爱ma day job

并为因其承担的一点点🤏社会责任感到快乐

我闹脾气是其中让人变蠢的那部分事务

我花几个小时把工作做完

大部分时间花在了处理情感

撕扯, 咀嚼, 吞咽

我是想说, 这让我墙拆的有点急了

我边拆边垒, 没有听大提琴

听的MJ, 我想来点劲儿

`Do you remember the time, how we`

几个小时改了400行代码提交但

`CI`说, 多处塌方

但不告诉是哪块砖头出了问题

呜,酸楚


Sun Aug 28 13:24:16 CST 2022

---

我不会了

```
4  LL | fn transmute<'a, 'b>(x: Type<'a>, y: Type<'b>) -> (Type<'a>, Type<'b>) {
  -     |              --  -- lifetime `'b` defined here
  +     |              --  -- lifetime `'a` defined here
  6     |              |
  7     |              lifetime `'a` defined here'`'`'`
}

```

`-` 意思是这行应该有但你的代码没有

`+` 意思是这行是你那代码跑出来的

人家不要

我的直觉是某个函数调用放错行了

我找不到,跑过去改了一大通

引用,解引,生命周期标注

原文的&&我之前写成&的我严格改回&&

原文的&String我改成了&*String

没有用🤡

Mon Aug 29 10:04:35 CST 2022

---

我终于定位问题了!

好像掀起一块阴暗角落的大石块

鼻涕虫四处跑开

我感到解脱

Mon Aug 29 19:34:38 CST 2022

---

掀起来的石头下面还藏着一块呢

把修改的代码定位到一行

穷举可能性, be like

`impl <'a: 'b, 'b> for &'a &'b RegionName`

没用, 我认输了

到群里问了一嘴

member说这是个BUG🐛

我的问题解决了

心气儿球也破了个洞

放缓

Tue Aug 30 16:33:41 CST 2022

---

写代码?

择菜!

Fri Sep  2 16:21:48 CST 2022

---

不可知的上游bug让我修改起来如履薄冰

三周过去了吧?

一个大[PR](https://github.com/rust-lang/rust/pull/101276)

一千多行了

我感觉风雨欲坠



Mon Sep  5 20:13:58 CST 2022

---

我不知觉的篡改了很多历史

`git reset --soft HEAD~2`

修改,提交

commit看起来漂亮了

却给同步和review带来麻烦

学乖了

使用

`git revert <commit SHA>`

Mon Sep 12 11:54:09 CST 2022

---

作为变量传入的字符串中的英文也被要求翻译

意思除了翻译一句话的意思

还要翻译这一句话能够带来的所有意思

但不能比翻译一句话慢

所以最好不要[string-based-dispatching](https://github.com/rust-lang/rust/pull/101686#discussion_r977448701)

翻译官多少有点甩锅[n-m-p](https://github.com/projectfluent/fluent/issues/353)

上游bug导致停工

ad-hoc增加了基础设施

但未能完全解决[English-in-descr](https://github.com/rust-lang/rust/pull/102623/commits/113e94369cb72a98648c12c263475821bbff7d9c#r1000288735)

