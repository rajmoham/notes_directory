## Function Prototype
Declaring the signature of a function for use before its implementation.
This is commonly done in the header of the file.
```
int addNumbers(int x, int y);

int main() {
	int total = addNumbers(5, 10);
}

int addNumbers(int x, int y) {
	return x + y;
}
```

## Key notes
- Duration compilation, lines are processed one at a time. So an error happens if a function call to something not declared before happens.
- Function prototyping in header files means the linker knows where to link each function call between different .cpp files. Otherwise, the alternative is a single code page with the main function at the bottom. This is because each file compilation happens separately and independently to other files.

# Operator Overloading
Redefining how operators work for user-defined types like classes and structs
SYNTAX: `type` '`operator`' `operator-symbol` `(parameter-list)`
List of redefinable operators: [Learn.Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/operator-overloading?view=msvc-170)

# Lambda Functions
Anonymous (unnamed) function defined within code.
```
[capture-list](parameters) -> return_type {
	// function body
}
```
Capture-list - list of variables from scope that lambda function can access,
	By default the variables in the capture list are passed by value (a copy is made), this means changes to the variable are not affected in the surrounding scope (like a normal function), passing by reference changes this.
Parameters - list of input parameters
return_type - type of the value returned by function

```
auto printHello = []() {
	std::cout << "Hello World\n";
}
```