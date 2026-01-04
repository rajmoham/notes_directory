Scope -> visibility and accessibility of variables, functions, classes and identifiers

Global scope -> declared outside of functions or classes, can be accessed from any part of the program. Lifetime is the duration of the program.

Local scope -> declared within function or block, can only be accessed within function it was declared in, lifetime limited to duration of function or block.

Namespace scope -> named scope which groups related identifiers and declared within namespace scope, can be accessed with namespace name and scope resolution operator (`::`)

Class scope -> declared within class and have class scope, can be accessed using class name and scope resolution operator (`::`), non-static members can be accessed with dot (`.`) or arrow (`->`)