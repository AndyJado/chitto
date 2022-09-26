say you got a `struct` & a `enum`

they have the same name

but they are different

why? `namespace`

```rust
pub enum Namespace {
    TypeNS,
    ValueNS,
    MacroNS,
}
```