Pointer -> variable that stores memory address of another variable/function
```
dataType *pointerName;

// Initialising pointer
int num = 10;
int *ptr = &num;

// Accessing value using pointer
int value = *ptr;
```

References -> alias for existing variable ie different name for same memory location.
	References cannot be null like pointers
	They must be initialised when they are declared.
	They also cannot be changed to refer to another variable

```
dataType &referenceName = existingVariable;

int num = 10;
int &ref = num;
```

References are commonly used for pass a variable by reference into a variable.

## Constants
```
int* const ptr = &x;
const int* ptr = &x;

// The above two are different!!!
```

`int* const ptr = &x;` -> the pointer cannot change to another address, the pointer itself is constant, but the value it is pointing to can change
`const int* ptr = &x;` -> the int cannot change, the pointer however can point to another address