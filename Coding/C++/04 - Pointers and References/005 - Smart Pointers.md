# unique_ptr
- Claims exclusive ownership over a value.
- Ownership cannot be shared with another pointer at any given time

```cpp
std::unique_ptr<int> p1 = std::make_unique<int>(10);

std::unique_ptr<int> p2 = p1;             // This throws an error, cannot share
std::unique_ptr<int> p3 = std::move(p1);  // Ownership is transferred

std::cout << *p1 << std::endl;             // Segmentation fault, p1 is nullptr
std::cout << *p2 << std::endl;             // prints 10
```
# shared_ptr
Unlike unique_ptr, shared_ptr allows multiple ownership over an object. As variables come and go, the object in memory persists as long as there is at least one shared pointer referencing the object.
### How is this done?
Under the hood, a counter is set for that object. Every time a new shared_ptr is created, the counter increases. And when the counter gets to 0, the object is deleted from the heap.

```cpp
std::shared_ptr<int> p1 = std::make_shared<int>(10);  // Counter at 1
std::shared_ptr<int> p2 = p1;                         // Counter at 2
```
# weak_ptr
weak_ptr is similar to shared_ptr but addresses the issue of circular link:
	ObjectA has a shared_ptr to ObjectB and ObjectB has a shared_ptr to Object A
	This means neither object is deleted since they still have a reference
weak_ptr solves this by allowing a non-owning reference to an object. Since it is non-owning, the internal counter which handles whether to delete the object does not increment.

There is no special `make_weak` initialiser for this smart pointer. You get the reference from a shared_pointer object

```cpp
std::shared_ptr<int> p1 = std::make_shared<int>(10);  // Counter at 1
std::weak_ptr<int> p2 = p1;                           // Counter still at 1

p2.use_count();       // number of shared_ptr objects managing object
p2.expired();         // check if referenced object has been deleted
p2.lock();            // creates a share_ptr to manage the referenced object
```

```cpp
#include <iostream>
#include <memory>

int main() {
    // Write C++ code here
    std::shared_ptr<int> b;
    std::weak_ptr<int> c;
    {
        std::shared_ptr<int> a = std::make_shared<int>(10);
        b = a;  // if you comment this line, you get a segmentation fault
        c = a;
    }
    
    std::cout << c.expired << std::endl;
    std::cout << *c.lock() << std::endl;

    return 0;
}
```
