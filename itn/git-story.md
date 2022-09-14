Linus最初用unix下的`diff`来校验不同的发型版

因为当时市面上的版本管理系统他不爱用

迫于压力2002年他选了

选的闭源的BitKeeper配免费使用的license

因为它有好用的`fork` `merge`

直到有人逆向工程bitkeeper

人家不给用了

整个内核开发的生态链断掉

于是Linus闭关写了最初版本的git

初版git并不能high level的“版本管理”

是一堆更底层的文件操作

它记录每个文件的每个变化

这让`fork` `merge`贼快

Linus写完就丢给Junio维护了

Junio把这些操作组装,起名

才是我们现在用的git

