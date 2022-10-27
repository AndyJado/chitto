enum discrimination

only works on fieldless enum.

```rust
enum Duh {
    a,
    b(i32),
}

let error_downcast = Duh::b as isize;
```