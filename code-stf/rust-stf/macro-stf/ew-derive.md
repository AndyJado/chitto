oh it's a [lot of dependency](https://github.com/imbolc/rust-derive-macro-guide)

```bash
cargo install cargo-edit
cargo install cargo-expand

cargo new --lib mytrait-derive
cargo add mytrait-derive --path mytrait-derive

cat >> mytrait-derive/Cargo.toml << EOF
[lib]
proc-macro = true
EOF

cd mytrait-derive
cargo add proc-macro2@1.0 quote@1.0
cargo add syn@1.0 --features full
```
