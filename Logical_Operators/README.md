# Bitwise Logical Operators

We will explore 4 operators relating to combining values in their binary base 2 formats together.  These are similar to boolean operators and can be referenced in code.  The 4 ooperators:

  - And Operator:  &
  - OR Operator:  |
  - XOR Operator:  ^
  - NOT Operator:  ~

Let us explore each of these operators in more details now.
_____________________
### AND Operator: &
The & operator compares each base 2 binary digit from two integers with the rule of:

| Truth Table: AND Operator | Ex1 | Ex2 | Ex3 | Ex4 |
|---------------------------|-----|-----|-----|-----|
| Value A:                  | 0   | 0   | 1   | 1   |
| Value B:                  | 0   | 1   | 0   | 1   |
| Resultant Value:  A&B     | 0   | 0   | 0   | 1   |

With the AND operator, the resultant value is computed whenever both bits are ones.  Hence in the Ex4 column when 1 AND 1, where A&B, would produce a corresponding *1*.  Any other combination will produce a *0* as shown in Ex1, Ex2, Ex3.  The above is called a ‘Truth Table’ and will be used throughout to demonstrate the outcome of the operators.

Try implementing now a solution in code with the questions below.

>Q:  Given that the rightmost bit is also called the ‘least significant bit’, write a function that takes in an integer value and checks to see if it is even or odd using bit-wise operations.

>Q:  Why would using bit-wise operations be potentially faster for checking even and odds as oppose to using something like a modular operator? eg. (randInt % 2)

When you have completed, push the questions/solutions into a folder named 'AND Operator' in your GitHub repo.
_____________________
### OR Operator: |

Now you have knowledge about how the AND operator works, we will explore the | OR operator where instead of having both bits to be 1 (one), the OR operator will have the resultant bit value set to 1 (one) as long as we have one bit set to 1 (one).  So the | operator compares each base 2 binary digit from two integers with the rule of:

| Truth Table: OR Operator | Ex1 | Ex2 | Ex3 | Ex4 |
|---------------------------|-----|-----|-----|-----|
| Value A:                  | 0   | 0   | 1   | 1   |
| Value B:                  | 0   | 1   | 0   | 1   |
| Resultant Value:  A\|B   | 0   | 1   | 1   | 1   |

The resultant bit value is computed whenever either bits are set to ones.  Hence with A|B from Ex2 of 0 OR 1, Ex3 of 1 OR 0, Ex4 of 1 OR 1 would all produce a ‘one’ in the resultant bit.

Try implementing now a solution in code with the question below.

>Q:  Write a function that takes in a two integer values and prints out the resultant value when you ADD the two input values and then also when you OR the two input values.

When you have completed, push the questions/solutions into a folder named 'OR Operator' in your GitHub repo.
_____________________
### XOR Operator: ^

Extending the concepts further, XOR (pronounced ‘X’ ‘OR’) produces (ONE) 1 in the truth table when both bits are different.  That is when either one of the bits is a (one) 1 and the other is a (zero) 0.
The ^ operator compares each base 2 binary digit of two integers with the rule of:

| Truth Table: XOR Operator | Ex1 | Ex2 | Ex3 | Ex4 |
|---------------------------|-----|-----|-----|-----|
| Value A:                  | 0   | 0   | 1   | 1   |
| Value B:                  | 0   | 1   | 0   | 1   |
| Resultant Value:  A^B   | 0   | 1   | 1   | 0   |

The resultant bit value is computed when exclusively one of the A,B  bits are ones.  Hence with A^B operation from Ex2 of 0 OR 1, Ex3 of 1 OR 0 would both produce a ‘one’ in the resultant bit.  While Ex1 and Ex4 both would produce a 'zero' as the bit values between A^B do not exclusively contain '1'.

Try implementing now a solution in code with the question below.

>Q:  Extend the previous function further by adding logic for the XOR operation when two integer values are inputted along with a 2nd parameter that would denote for the type of operation to execute.  Print out the resultant value for the associated operation type.

When you have completed, push the questions/solutions into a folder named 'XOR Operator' in your GitHub repo.
_____________________

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