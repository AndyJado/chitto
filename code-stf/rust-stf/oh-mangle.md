rust defaultly mangle the `identifier` ala hash it so compiler recgonize it
```rust
#[no_mangle]
// `start` here is the identifier
pub extern "C" fn _start() -> ! {
  loop{}
}
```