# 下载

[下载链接](https://docs.helix-editor.com/install.html)

```sh
# 回到home文件夹
cd
# 创建文件夹 && 进入该文件夹
mkdir tapps && cd tapps
# 拉下这个仓库到本地
git clone https://github.com/helix-editor/helix
# 到这个仓库里
cd helix
# cargo 安装本地仓库的软件
cargo install --path helix-term
# 将仓库中的配置文件同步到本机的配置文件
ln -s $PWD/runtime ~/.config/helix/runtime

```

# helix vs vim

`vi` 的行为在选中前

`hx` 反过来

删除光标下单词

`vim`是`dw`

`hx`是`wd`

`m`让我感到新奇

从源码编译的话

要把`runtime/`拷贝到`.config/helix/`

语法高亮什么的600多个MB

