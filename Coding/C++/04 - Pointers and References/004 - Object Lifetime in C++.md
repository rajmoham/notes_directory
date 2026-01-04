Lifetime = time when an object exists, from creation to destruction.
### Static Storage Duration
- Exists for the entire run of the program.
- Allocated al the start of the program and deallocated when program terminates.

### Thread Storage Duration
- Exists for the lifetime of thread which they belong to.
- Created when thread is created and destroyed when thread exists.
- Specified using `thread-local` keyword
```
thread_local int my_var;
```

### Automatic Storage Duration
- Created when the object has been defined
- Destroyed when the scope is exited.
- Objects are local / stored on the stack - most understood way of variable lifetime
### Dynamic Storage Duration
