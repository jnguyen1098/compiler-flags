# Compiler Flags

idk...

* `-Wall` enables all questionable warnings (aka the errors people should care about). Enables:

    * Waddress

    * Warray-bounds (only with -O2)

    * Wc++0x-compat

    * Wchar-subscripts

    * Wimplicit-int

    * Wimplicit-function-declaration

    * Wcomment

    * Wformat 

    * Wmain (only for C/ObjC and unless -ffreestanding)

    * Wmissing-braces

    * Wnonnull

    * Wparentheses

    * Wpointer-sign

    * Wreorder 

    * Wreturn-type

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