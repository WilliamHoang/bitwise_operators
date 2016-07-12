# Binary Digits
In this unit, we will explore binary digits and learn how to use the various operations available on the bits through code.  The areas of focus will be   

  - Logical Operators   
  - Two's Complement
  - Shift Operators

But before we begin, let's explore what are binary digits and their relevance to computer engineering.
_____________________
### Fundamentals of Computing:  Bits
When we talk about binary digits, the fundamental unit is a *bit* and that is the smallest unit of data in a computer.  The computer only interacts with bits at the hardware level and thus it is the purest form of data to work with.  A bit can encompass 2 unique values, one at a time.  A particular bit can hold either a **zero** or a **one** usually denoted as a '0' or '1'.  Another way to look at zero or one is to reference it as 'false' or 'true' relatively. 

Let’s explore what this looks like:

| Binary | Zero| One|
|---------------------------|-----|----|
|bit values: digits | 0 | 1|
| bit values: boolean                 | false |true|

When we write code, it is all eventually compiled into instructions for computers to interpret and understand.  Those instruction sets are operating on what we call binary data and in its most elemental form they are either '0' or '1'.  

### Bit Patterns
We see above that if we have 1 bit then that bit can contain either a '0' or '1'.  This is where 1-bit can hold 2 potential  values or patterns. But what happens when we have 2 bits instead of 1 bit?  Let us explore how this looks like below.
 * 1-bit -
    Two patterns:  
    - Pattern 1:  [0]
    - Pattern 2:  [1]
    
    This is when the bit is either a '0' or '1'
 * 2-bits - Four patterns:  
    - Pattern 1:  [0][0]
    - Pattern 2:  [0][1]
    - Pattern 3:  [1][0]
    - Pattern 4:  [1][1]
    
    This is when the 2-bits is either a '00', '01', '10', '00'

The idea here is that each additional bit will double the number of possible combinations or patterns.  1 bit above will give us two pattern combinations and if we increase the bit by one more to two bits, then the combination will increase from two patterns to four patterns.  

| # bits | Unique Patterns| 
|-------------------|-----|
|1-bit | 2 |
|2-bits               | 4 |
|n-bits               | 2^(n) |

The bits are like storages and as we increase the number of bits, the number of unique patterns will exhibit 2 exponent (n) formula with 'n' being the number of bits.  Why do you think it is 2 to the exponent and not another value like 4 exponent to the 'n'?

### Computer Architecture:  N-Bit Processor
We see that above when we double the number of bits, the unique pattern sets will be exponential.  Often we reference the computation power of a computer but the number of bits.  For example, we reference a computer as 32-bit architecture or 32-bit memory address where a 32-bit processor will hold 32 separate storage units where each unit can hold a '0' or '1' in its position.

In the examples in thie unit we will reference a 32-bit range and what that may look like is:

 - 32-bits
 -      [][][][][][][][] [][][][][][][][] [][][][][][][][] [][][][][][][][]
We often call this 4-bytes where each byte is represented as 8-bits.  There are other common names for n-bits but usually we reference by the number of *bytes*.  

| # bits | names| 
|-------------------|-----|
|1-bit | bit |
|4-bits               | nibble |
|8-bits               | byte |
|16-bits               | word |

### Bit Computation:  Binary to Digits
Now let's look at how all of the binary digits are converted and represented overall.  We will focus on 8-bits here where it looks like:
 - 8-bits - empty
 -      [][][][][][][][]

Imagine now if we populate the 8-bits with some values:
 - 8-bits:  0 value
 -      [0][0][0][0][0][0][0][0]
 
This is not interesting either as the storage here is holding 'zero' throughout.  But what is interesting is that this is the representation of what a numerical '0' would look like from a computer's perspective.  How 5 would be represented in binary now is:
 - 8-bits:  5 value
 -      [0][0][0][0][0][1][0][1]
 
Let us explore further on how this is computed now with the equation below:

 -      digital value = [bit value at position x]*2^(bit position x) + [bit value at position x+1]*2^(bit position x+1) ... + [bit value at position n]*2^(bit position n)
 
