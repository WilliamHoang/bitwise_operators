Bitwise Logical Operators

Four operators relating to combining values in their binary base 2 formats together.  These are similar to boolean operators and can be referenced in code.

[1] & [And Operator]
Explain & Examples
The & operator compares each base 2 binary digit of two integers with the rule of:

[0][0][1][1]
[0][1][0][1]
________
[0][0][0][1]

The resultant value is computed whenever both bits are ones.  Hence 1 AND 1 would produce a ‘one’  Any other combination will produce a ‘zero’  The above is called a ‘Truth Table’ and will be used throughout.

Try implementing now a solution in code.
Q:  Given that the rightmost bit is also called the ‘least significant bit’, write a function that takes in an integer value and checks to see if it is even or odd using bit-wise operations.
*rightmost bit is represented as 2^0 or 1 therefore when right most bit is 1 the number is odd.
*if(randInt & 1) == odd

Q:  Why would using bit-wise operations be potentially faster for checking even and odds as oppose to using something like randInt % 2?

[2] | [OR Operator]
Explain & Examples

Now you have knowledge about the AND operator, we will explore the | OR operator where instead of having both bits to be 1 (one), now with the OR operator as long as we have one bit set to 1 (one) then we will yield a 1 (one).  So the | operator compares each base 2 binary digit of two integers with the rule of:

[0][0][1][1]
[0][1][0][1]
________
[0][1][1][1]

The resultant value is computed whenever either bits are ones.  Hence 1 OR 0, 1 OR 1, 0 OR 1 would produce a ‘one’

Try implementing now a solution in code.
Q:

Q:

[3] ^ [XOR Operator]
Explain & Examples

Extending the concepts further, the XOR (pronounced ‘X’ ‘OR’) produces (ONE) 1 in the truth table when both bits are different.  That is when either one of the bits is a (one) 1 and the other is a (zero) 0.
So the ^ operator compares each base 2 binary digit of two integers with the rule of:

[0][0][1][1]
[0][1][0][1]
________
[0][1][1][0]

The resultant value is computed when exclusively one of the bits are ones.  Hence 1 XOR 0, 0 XOR 1 would produce a ‘one’

Try implementing now a solution in code.
Q:

Q:

[4] ~ [NOT Operator]
Explain & Examples

Finally the NOT operator is the simplest of the operations involving base 2 binary values.
The ~ operator operates on only a single bit and provides the complement value.  The truth table for the ~ NOT operator has the rule of:

Input:    [0][1]
______   ____
Output: [1][0]

In the boolean sense, this is the ! operator where the value is flipped.  The operation reverses the current bit where the resultant value is computed by turning:  1 to 0, 0 to 1

Try implementing now a solution in code.
Q:
Write a function that takes in an integer value and prints out its complement base 2 value?
Q:
What is missing in your function to produce the resulting value in base 10?