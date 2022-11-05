```rust
//outer: called by macro from outside
#[Derive(Debug)]
struct Blala {}

//inner: the macro works right here!
!#[deny(rustc::blablabla)]
```

> normally you need a outer.