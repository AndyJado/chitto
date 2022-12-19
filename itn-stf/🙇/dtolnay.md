## rust-quiz

1. what is a stmt && macro_rules && shl
2. bitand is some num get 2ed and left check eq? anyway you can impl it manually
4. FullRange type
8. in rust mako blackhole, tokens still be parsed with rust semantic, eg. `==>` becomes 2 nodes `==` & `>`
9. `$:ident` - `$:lifetime` - `$:tt` do not become opaque inside mako black hole
10. inherent method vs trait method, I suppose
11. 🏳️ early bound: all value has concrete type, late bound: lifetime somehow has to be calculated after it's there.
13. `&` `*` can be converted with `as`, me relate `ref` keyword in match arm
14. you can write impl in logic block however it don't follow logic, it just visible in all code. && auto ref!
18. `(S).f()` is uglier than `(S.f)()`, so when a field conflict with a method, always default to method
20. break with value just like return value
22. `-1.` is two token, `-` and `1.`
23. inherent always beat trait method
24. macro_rules hygiene, think the create spot of `!` follows a blackhole, think the call spot of `!` vomitting inside the blackhole, but const and struct won't get affect
25. a var with a uppercase naming might leads to a infalliable pattern match (some unit struct)
26. supertrait
29. (9) is identical to 9 but (9,) makes a tuple
30. `()` `&` default impl `clone`
31. if method-lookup finds nothing for `T`, then auto look for `&T` then `&&T`, in this order
35. natural drop order is bottom up, 
36. call a `(mut f)` with `(f)` won't get `err` if `f` can `Copy` because it copys to pass bck
