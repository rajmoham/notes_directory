- Declare the symbol before defining the implementation. This includes class, functions, or variables.
- This helps the compiler understand the type, size, and existence of symbols.
- Useful when there is cyclic dependencies, or to reduce compilation time by avoiding unnecessary header inclusions.
```cpp
int add(int a, int b); // forward declaration

int main() {
    int result = add(2, 3);
    return 0;
}

int add(int a, int b) {
    return a + b;
}
```

Note: You cannot forward declare `enum` and `typedef`. This is because there is not a separate declaration and definition for these.