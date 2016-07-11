# Bitwise Shift Operators
The shift operators is related to having two operands where the first operand is the number to be modified and the second operand is the number of bit positions to shift the first operand, or number, with.  With the shift operations we will explore 3 operators:  

  - Left Shift Operator:  <<
  - Right Shift Operator:  >>
  - Zero-Fill Right Shift Operator:  >>>

Let's take a look at each of these shift operators and how to calculate the results.
_____________________
### Left Shift Operator:  <<
This operation on a number will shift the base 2 value a specified number of bits to the left.  If we have X << Y ; then the Y will represent the number of bits we will shift on the X represented in   base 2 value.  The rule is that any excess bits shifted off to the left most side will be discarded, while we will have zero bits shifted in from the right hand side.

Let’s explore an example where we have a value where we wish to shift 3 bit positions.  What that looks like in code is:

```js
var temp
temp = 13 << 3
```
And what is happening underneath the code when we execute the above is:
```
13 —> Decimal Format in base 10
```
The 13 is turned into:
```
00000000 00000000 00000000 00001101  —> Binary Format in base 2 of 13
```
Operating now on the binary format of 13, we can now do bit shifting of:
>13 << 3 —> in base 10
```
00000000 00000000 00000000 00001101 << 3 -> 13 in binary to shift 3 bit positions left
```
```
00000000 00000000 00000000 01101000 —> After shifting 3 bit positions left
```

Converting the above value of the Binary Format (base 2) in what we got after bit-shifting 3 positions left, the table below shows the converted value in base 10:

| Format | Value | 
|---------------------------|-----|
| Base 2:                  | 00000000 00000000 00000000 01101000 |
| Base 10:                  | 104  |

The equation to follow or double check is where bit-shifting any number X to the left by Y bits will produce an end value in base 10 of:

> x*2^y

For the example in our case, this would be for x=13, y=3 giving us the exact binary value that is converted from the table above, **104**.  Using the equation we would get 13*(2^3) = **104** which is the same as the converted binary.

Try implementing now a solution in code with the questions below:
>Q:  Write a function that takes in a value in base 10 and a value that represents the number of bit positions to shift left with.  Return or print out the final base 10 value after the shift.

>Q:  How would you verify if the above function is producing the correct value?

When you have completed, push the questions/solutions into a folder named 'Left Shift Operator' in your GitHub repo.
_____________________

[2] >> [Right Shift Operator]
Similar to the Left Shift operator, this operation on a number will shift the base 2 value a specified number of bits to the right now.  If we have X >>Y ; then the Y will represent the number of bits we will shift on the X base 2 value.  The rule is that any excess bits shifted off to the right most side will trail off and be discarded.  Then zero bits are shifted in from the left hand side but the difference from the Left Shift operator is that the ‘sign bit’ value, leftmost bit, is kept after the right shifts.  This way, the sign propagates and is kept after bit shift right.

Let’s explore an example where we have a value where we wish to shift 3 bit positions but now we will shift right.  What that looks like in code is:
     13 >> 3
And what is happening underneath the code when we execute is:

13 —> Decimal Format in base 10

00000000 00000000 00000000 00001101  —> Binary Format in base 2 of 13

13 >> 3 —> in base 10

00000000 00000000 00000000 00001101 >> 3 bit positions
00000000 00000000 00000000 01101000 —> After shifting 3 positions right on the decimal value of 13

Converting the above value of the Binary Format (base 2) of what we got after bit-shifting 3 positions right:

00000000 00000000 00000000 01101000 (base 2) = X (base 10)

You can see now that is why the right shift operator is often also called the sign-propagating right shift operator as the sign of the number is preserved.

[3] >>> [Zero-Fill Right Shift Operator]
Similar to the Right Shift Operator now, the zero-fill right shift operator differs by discarding the sign bit value at the end.  This is where zero bits are shifted in from the left while excess bits are discarded when shifting to the right.  By this nature, the leftmost bit will always be zero after the zero-fill right shift operation is complete and therefore the result is always non-negative.

Now if we have X >>>Y ; then the Y will represent the number of bits we will shift on the X base 2 value.  The rule is that any excess bits shifted off to the right most side will trail off and be discarded while zero bits are shifted in from the left hand side.

Let’s explore an example where we have a negative value where we wish to shift 5 bit positions to the right.  What that looks like in code is:
     -17 >>> 5
And what is happening underneath the code when we execute is:

-17 —> Decimal Format in base 10

[1]We first take the positive value of the number
00000000 00000000 00000000 00010001  —> Binary Format in base 2 of 17

[2] First invert all the current bits of a number
11111111 11111111 11111111 11101110  —> One’s Complement of 17 in Binary Format
[3] Add 1-bit to the very end of the invert bits
11111111 11111111 11111111 11101111—> Two’s Complement of 17 in Binary Format

Remember why we do the two’s complement by adding one as the final step?  By adding one, positive numbers will have the left most bit set to 0 and negative numbers will have the left most bit set to 1.

-17 >> 5 —> in base 10

11111111 11111111 11111111 11101111 >> 5 bit positions
00000111  11111111 11111111 11111111  —> After shifting 5 positions right on the decimal value of -17

Converting the above value of the Binary Format (base 2) of what we got after bit-shifting 5 positions right:

00000111  11111111 11111111 11111111 (base 2) = X (base 10)  (wrong)

Try implementing now this solution in code.
Q:  Modify the above function that takes in a value in base 10 and a value that represents the number of bit positions to shift with.  Add in additional logic that would print out the final base 10 value after executing the 3 different shift operators.

Q:  For non-negative numbers, does the Zero-Fill Right Shift Operator differ from the Right Shift Operator in terms of producing the end result?  Why or Why not?   Eg.  11 >>> 4 vs 11>>4