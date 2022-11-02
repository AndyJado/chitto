a typical builder

```rust
// write only
let f = File::options().write(true).open("foo.md")?;

// read only
let f = File::open("foo.md")?;
```