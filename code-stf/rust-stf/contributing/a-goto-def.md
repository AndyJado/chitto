I need to be sure if there are english words in [a function](https://github.com/rust-lang/rust/blob/36e530cb08950f1d03ab733e43ecec2802d099cf/compiler/rustc_borrowck/src/diagnostics/mod.rs#L185)

The return type is `Option String`

the String is stored in `buf`

```rust
// pushed a symbol
let mut ok = self.append_local_to_string(local, &mut buf);

// pushed a symbol
buf.push_str(self.infcx.tcx.item_name(*def_id).as_str());

// my rust-analyzer don't recognize `place` here but it's from
// /rust/compiler/rustc_middle/src/ty/closure.rs:335
// which returns a symbol if not `bug!`
buf = self.upvars[var_index].place.to_string(self.infcx.tcx);

// pushed a symbol
buf.push_str(&field_name_str);

```

and I found no english words.