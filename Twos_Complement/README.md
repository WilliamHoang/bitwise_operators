### Two’s Complement:
Two’s Complement is a technique for composing the negative version of a number from it’s positive binary form.  The way to convert is to:

  -[1] First invert all the current bits of a number
  -[2] Add one to the very end of the invert bits

Let’s see an example below that goes through the sequence of converting a number in human readable form into it’s negative binary counter part.

| Format | Value | 
|---------------------------|-----|
| Base 2:                  |00000000 00000000 00000010 00000010|
| Base 10:                  | 514  |

Let's follow the steps outlined above.
  -[1] First invert all the current bits of a number
| Format | Value | 
|---------------------------|-----|
| Base 2:                  |00000000 00000000 00000010 00000010|
| One’s Complement of 514 in Binary Format:| 11111111 11111111 11111101 11111101|  
  
  -[2] Add one to the very end of the invert bits
  
| Format | Value | 
|---------------------------|-----|
| Base 2:                  |11111111 11111111 11111101 11111101|
| Two’s Complement of 514 in Binary Format:                  | 11111111 11111111 11111101 xxxxxxxxx|    

Why you may ask we do the two’s complement by adding one as the final step?  By adding one, positive numbers will have the left most bit set to 0 and negative numbers will have the left most bit set to 1.

Try implementing now a solution in code with the quesiton below.
>Q:

When you have completed, push the questions/solutions into a folder named 'Twos Complement:' in your GitHub repo.
______________________________________________________________________________________
Reference:
https://en.wikipedia.org/wiki/Two%27s_complement
