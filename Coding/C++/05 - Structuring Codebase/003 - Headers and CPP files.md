Code Splitting -> breaking down large code base into smaller, manageable files
Another benefit to code splitting is separate compilation: instead of source files being compiled in one go, they can be compiled into respective object files and then linked into executables or libraries. This means if a source file has not been updated, then the object file also does not need to be updated. Therefore, this can increase compilation time. 

### Header Files
Responsible for declaring classes, functions and variables needed by multiple source files.
You can think of them as defining the interface for other source files. 
### Source Files
Responsible for implementing the actual functionality defined in the corresponding header file.