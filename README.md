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
    * Wsequence-point
    * Wsign-compare (only in C++)
    * Wstrict-aliasing
    * Wstrict-overflow=1
    * Wswitch
    * Wtrigraphs
    * Wuninitialized (only with -O1 and above)
    * Wunknown-pragmas
    * Wunused-function
    * Wunused-label
    * Wunused-value
    * Wunused-variable

- `-Wextra` enables some more extra warnings:

    * Wclobbered  
    * Wempty-body  
    * Wignored-qualifiers 
    * Wmissing-field-initializers  
    * Wmissing-parameter-type (C only)  
    * Wold-style-declaration (C only)  
    * Woverride-init  
    * Wsign-compare  
    * Wtype-limits  
    * Wuninitialized (only with -O1 and above)  
    * Wunused-parameter (only with -Wunused or -Wall)  
