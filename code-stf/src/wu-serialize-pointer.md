can a referenced structure be serialized?

```rust
let a = vec!["e-ref".to_own(),];

#[derive(Serialize)]
struct RefA<'r> {
  a: &'r Vec<String>,
}

```