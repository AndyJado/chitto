# 下载源码本地构建

e.g. `helix`

```
git clone https://github.com/helix-editor/helix
cd helix
cargo install --path helix-term
ln -s $PWD/runtime ~/.config/helix/runtime

```

`ln -s` : create symbolic link

 就是windows的快捷方式嘛?

## wa-xtask

```
git clone https://github.com/rust-lang/rust-analyzer.git && cd rust-analyzer
cargo xtask install --server
```
