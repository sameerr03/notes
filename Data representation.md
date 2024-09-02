
## Integer representation
- Unsigned: 0 to $2^n-1$
- Signed: (All need fixed number of bits)
	- Sign magnitude: MSB (Left most bit) is the sign. 0 for + 1 for -ve. Range becomes $-(2^{n-1}-1)$ to $2^{n-1}-1$. However there are two interpretations of 0 and there is a separate processing of -ve and +ve numbers
	- 1s complement: MSB is sign bit. For negative numbers, sign bit is 1 and the remaining bits are complemented. **For addition, carry beyond the sign bit needs to be added back.** 
	- 2s complement: MSB is sign bit. For negative numbers, sign bit is 1 and the remaining bits are complemented and 1 is added. **in addition, carry beyond the sign bit is ignored.**
For representation in base r, r's complement of x is given by $r^n-x$
r-1's complement is given by $r^n-x-1$


## Floating point representation
Decimal numbers are represented by float or double numbers. These numbers use 32 or 64 bits.

For float (single precision) -1st bit sign, 8 bits exponent, 23 fraction
For double (double precision) - 1st bit sign, 11 bits exponent, 52 bits fraction

In order to convert decimal to float,
1. Look at sign -+ve is 0 -ve is 1
2. Write number in base 2 scientific notation: (1+fraction)$\times 2^{pow}$ : this is done by dividing the number by 2 untill it is in the form 1.something. The number of divisions by 2 is the power and the number after the decimal point is the fraction. 
3. Exponent is  found by adding the pow (negative number) to the bias (127 for float 1023 for double) and then converted to binary. 
4. Writing the fraction in binary form (number after decimal place converted into binary from the binary scientific notation). Then represented as sign exponent fraction

To convert float to decmal
1. divide into the 3 groups based on number of bits sign(1) exponent(8/11) fraction(23/52)
2. Convert the exponent into decimal and subtract the bias (127/1023)
3. Convert the fraction into base 10. Multiply each position by the weight from  decimal conversion to get base 10. add 1 to it and multiply by  2^pow to get the value of the number. 
4. Check the sign bit and write the final number
