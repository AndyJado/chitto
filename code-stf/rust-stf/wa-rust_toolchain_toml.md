

链接编译器

rustup toolchain link stage1 build/x86_64-apple-darwin/stage1

其中，x86_64-apple-darwin应当换成主机的编译目标。

当我们用stage1编译应用程序前，在目标仓库新建一个rust-toolchain.toml文件，填入以下内容。

```toml
[toolchain]
channel = "stage1"
```

这样使用cargo build等指令就不需要带其它参数了。另外，开发工具比如rust-analyzer也可以识别此文件的内容，以避免额外的配置。
