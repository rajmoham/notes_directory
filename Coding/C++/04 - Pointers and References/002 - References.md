To be declared, use the variable type followed by &.
## Usages
### Functions
To reference the original variable and change its value (ie pass by reference in functions)
```
void add(int& sum, int a, int b) {
	sum = a + b;
}

int k;
add(k, 3, 4);

// Here the summed value is stored in k. Otherwise, the calculation would have been lost if it was passed by value.
```
### Range-Based Loops
```
// Read-only, no copies
for (auto const &str : stooges)
    std::cout << str << std::endl;

// Makes a copy of each string
for (auto str : stooges)
    std::cout << str << std::endl;

// Direct reference, can modify original elements
for (auto &str : stooges)
    str += "!";

// Makes a copy of each string, but prevents modification of the copy
for (const auto str : stooges)
    std::cout << str << std::endl;
```

