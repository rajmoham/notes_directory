
The binary representation for floating point is calculated using 32 bits with following amount dedicated for the following:
- Sign bit - 1
- Exponent width - 8
- Signifcand precision / mantissa - 24 (23 explicitly stored)

### Sign bit
 0 = positive number
 1 = negative number
### Exponent
Contains the biased exponent of the number.
There is a biased involved because this number is two's complementary representation, to allow for negative exponents
Denary -> binary : add 127 (0111 1111)
Binary -> denary : minus 127
### Mantissa
Contains the fraction part of a normalised version of significant figure. Therefore, since the first (and whole) digit is always 1 this is disregarded.
```
1.001110011 x 2^4
Mantissa = (1) 001110011   # the leading 1 is not needed, so storing 23 bits here
```

## Example

Image from Wikipedia
<img style="background-color: white" src="https://upload.wikimedia.org/wikipedia/commons/d/d2/Float_example.svg">

Sign bit = 0
	Therefore the end result is a positive number
Exponent = 01111100
	The value of the exponent as an unsigned binary representation is 124.
	Minus 127 means the intended value is -3
	That gives the exponent value to be 1111 1011 which is -5 in two's complement binary
Mantissa = 01000...
	Actual implied value is 1.01 (in binary)
	To get the actual number this needs to be shifted correctly based on the exponent.
	Since this is -3 the value in binary can be represented as `1.01 * 2^(-3)`
	So the number which is being represented is 0.00101 which is 0.125 + 0.03125 = 0.15625
	