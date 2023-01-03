# how to notate lifetime in a closure defination

```rust
let path_dies = |p: &Path| p.segments.iter().rev().next().expect("Path has segement");
```