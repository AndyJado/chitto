```Rust
#[must_use = "iterators are lazy and do nothing unless consumed"]
#[stable(feature = "rust1", since = "1.0.0")]
#[derive(Debug)]
pub struct Incoming<'a> {
    listener: &'a TcpListener,
}
```