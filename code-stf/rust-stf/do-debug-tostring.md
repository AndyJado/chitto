# I cannot find where it impl trait `Display`

---

[where-it-impl-Display?](https://github.com/rust-lang/rust/blob/11bb80a92b4f46fa7dfa9148d0bdfc185a7621bd/compiler/rustc_borrowck/src/region_infer/opaque_types.rs#L406)

```rust
&format!(
    "used non-generic {} `{}` for generic parameter",
    opaque_param.kind.descr(),
    arg,
),
```
---

## what i did

1. I went to defination of `opaque_param.kind.descr(),`, it's `Region`

2. I check all `impl` for `Region`

3. I don't find `Display`

4. but I can use `.to_string()` on it

## FIXED

还是得去看文档.

实现全列出来的

源码中macro的impl无法被helix追到.

光看源码好傻逼
