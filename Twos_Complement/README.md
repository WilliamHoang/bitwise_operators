### Two’s Complement:
Two’s Complement is a technique for composing the negative version of a number from it’s positive binary form.  The way to convert is to:

  - [Step 1] First invert all the current bits of a number
  - [Step 2] Add one to the very end of the invert bits

Let’s see an example below that goes through the sequence of converting a number from human readable form into it’s negative binary counter part.

| Format | Value | 
|---------------------------|-----|
| Base 2:                  |00000000 00000000 00000010 00000010|
| Base 10:                  | 514  |

Let's follow the steps outlined above to convert now.

 - [Step 1] First invert all the current bits of a number:

* In this step we will toggle all the bits from a '0' to a '1' and all the bits from a '1' to a '0'.  We call this the 'One's Complement' of a binary number once we have toggled all bits.

| Format | Value | 
|---------------------------|-----|
| Base 2:                  |00000000 00000000 00000010 00000010|
| One’s Complement of 514 in Binary Format:| 11111111 11111111 11111101 11111101|  
  
 - [Step 2] Add one to the very end of the invert bits:

* In this second step we will add a single bit to the very end of the One's Complement.  The result is called the 'Two's Complement' of a number. 
  
| Format | Value | 
|---------------------------|-----|
| Base 2:  One's Complement                  |11111111 11111111 11111101 11111101|
| Two’s Complement of 514 in Binary Format:                  | 00000000 00000000 00000010 00000010|    

Why you may ask we do the two’s complement by adding one as the final step?  By adding one, positive numbers will have the left most bit set to 0 and negative numbers will have the left most bit set to 1.

Try implementing now a solution in code with the quesiton below.
>Q:  Implement a function that takes in an integer and prints out its two's complement value in binary.  What would the value be in base 10?

When you have completed, push the questions/solutions into a folder named 'Twos Complement:' in your GitHub repo.
______________________________________________________________________________________
Reference:
https://en.wikipedia.org/wiki/Two%27s_complement
