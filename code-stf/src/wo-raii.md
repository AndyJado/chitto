```rust
// app/src/main.rs
fn main() {
  let mem_limit = 64 * 1024;
  let memory = vec![0u8; mem_limit];
  app::run(&mut memory)
}

// app/src/lib.rs
#![no_std] // <- the point of the exercise

pub fn run(memory: &mut [u8]) {
  ...
}
```

[`and it's architechtually salient thing`](https://matklad.github.io/2022/10/06/hard-mode-rust.html)
