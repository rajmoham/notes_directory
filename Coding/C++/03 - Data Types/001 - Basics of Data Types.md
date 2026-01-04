# Fundamental Data Types
## Integers
`int` - 4 bytes (but can be dependent on system architecture)

`short int` - smaller range than int
`long int` - larger range than int
`long long int` - even larger range than long int
## Floating Point (Float, Double)
`float` - 4 bytes, single precision floating point [[001 - Floating Point]]
`double` - 8 bytes, double precision floating point
### Characters
`char` - 1 byte, stores the ASCII value of the letter, digit, or symbol
### Boolean
`bool` - 1 byte

# Derived Data Types
### Arrays
Stores multiple values of the same data type in consecutive memory locations
### Pointers
Store memory address of variable
### References
Alternative way to share memory locations between variables. Create alias for another variable.

# User Defined Data Types
### Structures (Struct)
Used to store multiple data types under a single variable (like objects in javascript)
```
struct Person {
	std::string name;
	int age;
} 
```
### Classes
More heavyweight version of structures where accessibility of member variables and functions is controlled. By default access is private.
```
class Person {
public:
	std::string name;
	int age;
	
	void printInfo() {
		std::cout << "Name: " << name << ", Age: " << age << std::endl;
	}
}
```
### Unions
Stores different data types in same memory location.
The purpose is only to save memory and when you safely know that after having overwritten the data with what you need, you will not need the other types that are part of the union.
**This is not meant to be some clever way to type conversion.**
```
union Data {
	int num;
	char letter;
	float decimal;
};
```