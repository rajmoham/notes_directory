Dynamic typing = data types are defined at run-time.

### `void*` Pointers
A generic pointer that points to objects of any data type.
Used to store a reference to any object type without knowing its specific type.
```
int x = 42;
void* void_ptr;

void_ptr = &x;
std::cout << *(static_cast<int*>(void_ptr))
```

### `std::any` (C++ 17)
Represents a generalised type-safe container for single values of any type.
```
std::any some_value;
some_value = 42;

int num = std::any_cast<int>(some_value);
```

Both the above has performance impacts due to additional type checking and casting needed during runtime.
Either of these should be used very sparingly.