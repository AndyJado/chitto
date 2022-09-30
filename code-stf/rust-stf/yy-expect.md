```rust
fn main () {
  let path = Path::new("this is not a path");
  File::open(path).expect("reading the file")
}
```

我希望expect报错出来的错误信息里带有expect这个词，于是通顺。
