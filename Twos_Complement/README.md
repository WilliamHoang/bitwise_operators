Two’s Complement:
Two’s Complement is a technique for composing the negative version of a number from it’s positive binary form.  The way to convert is to:

[1] First invert all the current bits of a number
[2] Add one to the very end of the invert bits

Let’s see an example below that goes through the sequence of converting a number in human readable form into it’s negative binary counter part.

514 —> Decimal Format

00000000 00000000 00000010 00000010  —> Binary Format of 514

[1] First invert all the current bits of a number
11111111 11111111 11111101 11111101  —> One’s Complement of 514 in Binary Format
[2] Add one to the very end of the invert bits
000000…..—> Two’s Complement of 514 in Binary Format

Why you may ask we do the two’s complement by adding one as the final step?  By adding one, positive numbers will have the left most bit set to 0 and negative numbers will have the left most bit set to 1.
______________________________________________________________________________________
Reference:
https://en.wikipedia.org/wiki/Two%27s_complement