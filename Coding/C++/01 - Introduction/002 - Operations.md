Operations as normal for arithmetic and logical operations.
Note: division causes the return type to be a float (even if one of the variables are int)

# Bitwise Operations
```
&        # Bitwise AND
|        # Bitwise OR
^        # Bitwise XOR
~        # Bitwise NOT
<<       # Bitwise Left Shift
>>       # Bitwise Right Shift
```

Intuition: since an int is 4 bytes, there is 32 bits, hence you can shift 1 by 32 bits to the left until the value becomes 0 (ie the 1 bit is lost due to overflow).
