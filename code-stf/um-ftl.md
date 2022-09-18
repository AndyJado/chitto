```fluent

infer_subtype = ...so that the {$requirement ->
    [method_compat] method type is compatible with trait
    [type_compat] associated type is compatible with trait
    [const_compat] const is compatible with trait
    [expr_assignable] expression is assignable
    [if_else_different] `if` and `else` have incompatible types
    [no_else] `if` missing an `else` returns `()`
    [fn_main_correct_type] `main` function has the correct type
    [fn_start_correct_type] #[start]` function has the correct type
    [intristic_correct_type] intrinsic has the correct type
    [method_correct_type] method receiver has the correct type
    *[other] types are compatible
}

```