use union as a type eraser

inside a union, you know its type

given a union, you know its a union

```rust
#[repr(C)]
union A {
  f1: u32,
  f2:f32,
}
```

