type = posibilities of the representation

struct: product type

enum<Rust>: sum type

```rust
/// 2*2^8 possibilities for Bbool
struct Bbool {
  a: bool,
  b: u8,
}
/// 2+2^8 possibilities for Ebool
struct Ebool {
  A(bool),
  B(u8),
}
```