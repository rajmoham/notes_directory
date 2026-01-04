## Stack Memory
- Stack memory stores local variables and function call data.
- This memory is managed by the compiler, allocation and deallocation is done automatically.
- It is in the form of a stack data structure (last in first out)
- Memory increases and decreases on command with how much the program needs
## Heap Memory
- Dynamic storage duration (longer than scope of code blocks).
- Objects stored on the heap are defined using the `new` key word
- Programmer controls the allocation and deallocation using `new` and `delete`
- Heap is much slower than stack, but has a larger pool or memory.

## Data Segments
Data segments includes two parts: initialised data segment and uninitialized data segment.
As name suggests, uninitialized data segments are globally defined variables that have no been given a value.

Initialized data segment -> stores global, static and constant variables with initial values
Uninitialized data segment -> stores uninitialized global and static variables.
## Code Segment
Code segment/text segment -> stores executable code for program
Contained within the read-only area of memory