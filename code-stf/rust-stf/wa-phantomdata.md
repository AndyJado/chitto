>Perhaps the most common use case for PhantomData is a struct that has an unused lifetime parameter

```rust
struct Slice<'a, T> {
    start: *const T,
    end: *const T,
}
```

>The intention is that the underlying data is only valid for the lifetime 'a, so Slice should not outlive 'a

so you create a `PhantomData<&'a T>` so that compiler won't complain
