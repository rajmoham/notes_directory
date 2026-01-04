RTTI allows a way to obtain the type information of an object during execution. This is useful when using dynamic typing.

## `typeid`
This is an operator which returns a reference to an object. This return is of type `std::type_info`
The header file `<typeinfo>` is required to use this.

## `dynamic_cast`
A type-casting operator which performs runtime type check and safely downcasts to base pointer or reference to derived pointer or reference.
A null or bad_cast exception (for casting references) can be thrown when casting fails.

"Safely converts pointers and references to classes up, down, and sideways along the inheritance hierarchy." [cppreference.com](https://en.cppreference.com/w/cpp/language/dynamic_cast.html)


>RTTI can have performance overhead due to the additional compiler generated information needed to be stored and recalled during runtime

