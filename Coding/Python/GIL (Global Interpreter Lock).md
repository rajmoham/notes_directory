# Background
- The official Python interpreter is written in C.
- When concurrency and multithreading became popular in 1990s, python adapted to involve multiple threads.
- When Python creates a new thread, the C program creates its own thread for the kernel to observe and use.
# What is the GIL?
Although theoretically there are multiple threads created, they do not get executed at the same time despite CPUs having multiple cores. This is because in order to solve the issue of race conditions, the Python interpreter has a single global mutex lock. This means each thread can execute under the condition that no other thread is currently executing.

This implementation was not an issue when it was first introduced, this is because computers did not have the processing power to see the difference. But now, Python's poor CPU utilisation can be seen.
# Under the Hood
There is a lot of shared state that the python interpreter holds.
Some include:
- Reference counters
- Memory allocators
- Object caches
- Dictionaries
- Lists
- Internal bookkeeping and structures
Due to the complexity of all different things that need to be tracked, a simple global mutex helped solve the issue.