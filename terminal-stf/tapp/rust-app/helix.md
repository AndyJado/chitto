# 下载

[下载链接](https://docs.helix-editor.com/install.html)

```sh
# 回到home文件夹
cd
# 创建文件夹 && 进入该文件夹
mkdir repos && cd repos
# 拉下这个仓库到本地
git clone https://github.com/helix-editor/helix
# 到这个仓库里
cd helix
# cargo 安装本地仓库的软件
cargo install --path helix-term
# 将仓库中的配置文件同步到本机的配置文件
ln -s $PWD/runtime ~/.config/helix/runtime
# 下载lsp
cd && cd repos
git clone https://github.com/rust-lang/rust-analyzer.git && cd rust-analyzer
cargo xtask install --server
# 下载语法高亮, 编译
hx -g fetch
hx -g build
# 检查
hx --health

```

