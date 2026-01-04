Static Polymorphism = compile time polymorphism, resolves types and method calls during compile time.

# Function Overloading
Creating multiple functions with the same name but different parameter list. Compiler can determine the correct function based on types and number of arguments used when the function is called.
```
void print(int i);
void print(double d);
void print(const char* s);
```

# Templates
Creating generic functions of classes. The actual code for specific types generated at compile time avoiding overhead of runtime polymorphism.
"The use of templates is the main technique to achieve static polymorphism in C++"
```
template<typename T>
void print(const T& value) {
	std::cout << value << '\n';
}

print(42);       // int
print(3.14159);  // double
print("Hello");  // const char*

// At compile time the functions with the above types are created 
```
