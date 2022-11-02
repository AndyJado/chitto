>Generally all macros (procedural as well as macro_rules) designed to be used
by other people should refer to every single thing in their expanded code
through an absolute path, such as std::result::Result.

>the compiler always treats the expansion of a macro as a complete AST node
