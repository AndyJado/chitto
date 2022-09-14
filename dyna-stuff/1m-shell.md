模拟三米厚的土

用了三个shell

每层一米厚

还不是thick shell

就default shell

一层给他三百个积分点

又不是不能算

但dyna懵了

dyna的报错是相当人性化的

如果有什么地方不对劲了

它总是会在你需要知道的时候告诉你

这回它懵了

卡那说不出话来

CPU占用13%

内存占用一度跑到20g

第二天早上回来看

还是算动了

应该是单个单元写入整体刚度矩

顺序写入

无法并行

log里面记录了dyna哑巴时候的心路历程

```
 Memory required to complete solution   :      12M
 Additional dynamically allocated memory:    1388M
                                   Total:    1399M
```

也有可能是初始穿透哦



Wed Sep 14 17:38:50 CST 2022

---

