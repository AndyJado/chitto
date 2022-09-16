# 全选
# cltr+c (需要复制到系统剪切板)
# 回到终端
# cd
# vi .cargo/config.toml
# i (可以查一查vim怎么用)
# cltr + v
[source.crates-io]
registry = "https://github.com/rust-lang/crates.io-index"
# 指定镜像
replace-with = 'tuna' # 如：tuna、sjtu、ustc，或者 rustcc

# 注：以下源配置一个即可，无需全部


# 清华大学
[source.tuna]
registry = "https://mirrors.tuna.tsinghua.edu.cn/git/crates.io-index.git"

# rustcc社区
#[source.rustcc]
#registry = "https://code.aliyun.com/rustcc/crates.io-index.git"

