# New and Delete Operators
### new
`new` provides the address for the dynamically allocated memory.

Can also allocated a block of memory:
```cpp
new data_type[n];
```

If there is not enough memory in the heap, a type `std::bad_alloc` exception would be thrown. This can be suppressed with `(nothrow)`. If that is the case, the allocation returns a nullptr.
```cpp
int *p = new (nothrow) int;
if (p != nullptr)
	cout << "Allocation Failed" << endl;
```

### delete
`delete` releases the memory allocated at a pointer.
```cpp
delete ptr;
delete[] ptr;     // Deleted an assigned block of memory
```

# Issues with Dynamic Memory
## Memory Leaks
Memory allocation remains after it is no longer being used, and cannot be fetched again.
[Solution:] use smart pointers as deallocation is done automatically
## Dangling Pointers
Memory pointers that point to some address which has been deallocated. This causes undefined behaviours.
[Solution:] assign nullptr to pointers when they have been deallocated
## Double Deletion
When delete is called on the same memory location twice, this causes the program to crash or corrupt.
[Solution:] Assign nullptr to memory pointers after they have been deallocated.
## Mixing new/delete with malloc() / free()
Note: you cannot interchangeably use malloc instead of new and free instead of delete. They do not work in a similar way.