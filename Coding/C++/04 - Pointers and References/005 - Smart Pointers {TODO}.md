# weak_ptr

# shared_ptr

# unique_ptr
- Claims exclusive ownership over a value.
- Ownership cannot be shared with another pointer at any given time

```
std::unique_ptr<int> p1 = std::make_unique<int>(10);

std::unique_ptr<int> p2 = p1;             // This throws an error, cannot share
std::unique_ptr<int> p3 = std::move(p1);  // Ownership is transferred

std::cout << *p1 << std::endl;             // Segmentation fault, p1 is nullptr
std::cout << *p2 << std::endl;             // prints 10
```