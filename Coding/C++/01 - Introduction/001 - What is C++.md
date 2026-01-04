# Introduction
- General Purpose programming language made by Njarne Stroupstrup.
- Extension of C with object-oriented features
- Statically typed -> variables determined during compilation


| C                                                     | C++                                                           |
| ----------------------------------------------------- | ------------------------------------------------------------- |
| Error handling done through return codes              | Exception handling used to handle program execution           |
| Reusability through functions and modular programming | Better reusability with classes, inheritance and polymorphism |
| Memory management is manual (malloc, free)            | More help with handling memory (smart pointers)               |
# Getting started

### Compilers needed for development based on platform
Linux/MacOS -> GCC (GNU Compiler Collection)
Windows -> MSVC (Microsoft Visual C++), MinGW-w64 Compiler System (allows  GCC in windows)


According to GCC's online documentation [link options](https://gcc.gnu.org/onlinedocs/gcc/Link-Options.html) and [how g++ is invoked](https://gcc.gnu.org/onlinedocs/gcc/Invoking-G_002b_002b.html), `g++` is _roughly_ equivalent to `gcc -xc++ -lstdc++ -shared-libgcc` (the 1st is a compiler option, the 2nd two are linker options)
[Reference](https://stackoverflow.com/questions/172587/what-is-the-difference-between-g-and-gcc)

### Development

In the main function, `return 0` tells the program that it executed successfully. Any other integer means an error occurred. 
