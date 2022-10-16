## WSL

[在windows中使用linux](https://docs.microsoft.com/en-us/windows/wsl/install)

[windows-terminal](https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701?hl=zh-sg&gl=SG)

打开windows-terminal, 输入

`wsl`

**你需要按下回车，下同**

此时你应该发现自己在linux系统下了

[下载Rust](https://doc.rust-lang.org/book/ch01-01-installation.html#installing-rustup-on-linux-or-macos)

`sudo apt install build-essential`

## 软件依赖换成国内的下载地址

`cd`

这是让你回到`~`

之后要使用一点点vi

`vi ./.cargo/config`

在打开的新文件中写入下方链接中代码

[更改为清华的镜像源](https://mirrors.tuna.tsinghua.edu.cn/help/crates.io-index.git/)

[或者其他镜像源](https://www.cnblogs.com/lvyongbo/p/14307293.html)

保存，返回至Linux原界面
