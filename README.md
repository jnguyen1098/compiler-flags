# Compiler Flags

idk...

* `-Wall` enables all questionable warnings (aka the errors people should care about). Enables:

    * `Waddress`: taking the address of something will never be `NULL`
    * `Warray-bounds` (only with -O2): compile-time subscript may be out of bounds
    * `Wc++0x-compat`: something to do with C++11 compatibility
    * `Wchar-subscripts`: subscripting an array using a `char` (problem being `char`s are usually signed)
    * `Wimplicit-int`: occurs when a function doesn't have a `return` type and it defaults to `int`
    * `Wimplicit-function-declaration`: function called without prior declaration
    * `Wcomment`: nested comment (e.g. `/* foo /* bar */ baz */`)
    * `Wformat`: argument checking for formatted string functions like `printf`, `scanf`, etc.
    * `Wmain` (only for C/ObjC and unless -ffreestanding): suspicious `main` function
    * `Wmissing-braces`: initializer may be missing braces
    * `Wnonnull`: `NULL` in compiled code where non-`NULL` is required
    * `Wparentheses`: vital parentheses may have been omitted (or there's confusion between `=` and `==`)
    * `Wpointer-sign`: occurs when two pointers differ in signedness (?)
    * `Wreorder`: occurs when initializing a `struct` using an abnormal ordering of members
    * `Wreturn-type`: occurs when a function relies on the default `int` `return` type (see `-Wimplicit-int`) or when a function returning `void` attempts to `return` something else
    * `Wsequence-point`: compiled code does more than one thing between sequence points
    * `Wsign-compare` (only in C++): potential discrepancy in implicit conversion between a signed value to unsigned
    * `Wstrict-aliasing`: potential violation of strict aliasing rules
    * `Wstrict-overflow=1`: warns about compiler optimizations based on the assumption that signed overflow does not occur (for example `x + 1 > 1` being optimized to `1`)
    * `Wswitch`: warns if a `switch` statement indexes an `enum`erable type and lacks a `case` for one or more of the named codes of said `enum`eration
    * `Wtrigraphs`: warns of trigraphs that may affect the meaning of the program 
    * `Wuninitialized (only with -O1 and above)`: warns if an `auto`matic or allocated object is being used without having been initialized
    * `Wunknown-pragmas`: `#pragma` directive not understood by `gcc`
    * `Wunused-function`: self-explanatory...
    * `Wunused-label`: self-explanatory...
    * `Wunused-value`: self-explanatory...
    * `Wunused-variable`: self-explanatory...

- `-Wextra` enables some more extra warnings:

    * `Wclobbered`: warns about variables that may be changed by `longjmp` or `vfork`
    * `Wempty-body`: empty body for `if`, `else`, or `do while` statement(s)
    * `Wignored-qualifiers`: warns when qualifiers are ignored by default (for example returning a `const` variable)
    * `Wmissing-field-initializers`: initializer for a `struct` lacks some field(s)
    * `Wmissing-parameter-type` (C only): function declared without a type specifier
    * `Wold-style-declaration` (C only): obsolescent declaration
    * `Woverride-init`: initialized field without side effects is overridden when using designated initializers
    * `Wsign-compare`: comparison between signed and unsigned value(s) could produce an incorrect result when the signed value is converted to unsigned
    * `Wtype-limits`: limited range of data type makes comparison obsolete (for example checking if a `char` variable is `< 128` will always `return` `1`)
    * `Wuninitialized` (only with -O1 and above): see definition in `-Wall`
    * `Wunused-parameter` (only with -Wunused or -Wall): self-explanatory...
