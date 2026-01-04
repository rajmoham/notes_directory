Namespace -> named scope or container that organize and enclose a collection of code elements.
Divides and manage codebase, giving more control.
```cpp
namespace animals {
	 std::string dog = "Bob";
}

int main() {
	std::cout << animals::dog << std::endl;
	
	return 0;
}
```

- You can nest namespaces in one another. To access them: `a::b::c ...`
- The `using` keyword imports namespace elements so the scope does not have to be declared. However, it can be unstable if there are name conflicts
```cpp
using animals::dog;         // Single elements

using namespace animals;    // Entire Namespace
```