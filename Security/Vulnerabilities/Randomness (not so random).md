# Linear Congruential Generator
Formula: `s = (s * 9301 + 49297) % 233280`

The above formula above aims to reduce any patterns in the generated numbers. Hence causing randomness.

The numbers in the formula have a specific requirements: Hull-Dobell Theorem:
1. m and c are coprime
2. a - 1 is divisible by all prime factors of m
3. a - 1 is divisible by 4 is m if divisible by 4
### Reversing LCG
When there is a coprime modulus, you can multiply it by a certain value to reverse its application.
For example:
y = (x * 2) % 5 -> x = (y * 3) % 5
So the value used to reverse the modulus is 3 (ie the Modular Multiplicative Inverse).
# XOR-Shifts
You can convert a number into binary, perform some XOR and shift operations to affect the value, giving randomness to the resulting number.
For example:
```
s ^ (s << 13)    # shifts 13 to left then XOR
s ^ (s >> 17)    # shifts 17 to the right then XOR
s ^ (s << 5)     # shifts 5 to the left then XOR
```
### Reversing XOR-Shift
To reverse an XOR operation, you just have to perform another XOR operation on top. (A ^ B ^ A = B)
We can make use of the shifted positions to know that this section is the original.
```
To reverse:
s = s ^ (s << 13)
s = s ^ (s >> 17)
s = s ^ (s << 5)

we do the following:
s = s ^ (s << 5)
s = s ^ (s << 10)
s = s ^ (s << 15)

s = s ^ (s << 17)

s = s ^ (s << 13)
s = s ^ (s << 26)
```