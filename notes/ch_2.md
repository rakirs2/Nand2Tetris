# Boolean Arithmetic

This chapter is dedicated to "how computers count". For starters, we just need to define basic calculations.

## 2.1 Operations
- Add
- subtract
- sign conversions ( going from + to - and vice versa)
- comparisons
- multiplication
- division

## 2.2 Binary number representations

- look at the "general notes" for representing binary

### Fixed word size
If you've ever heard of computers being "8 bit or 16 bit," it generally refers to the limitations of the words size.

One of the fundamental questions about computers is how do we take a "word size" and convert it into something meaningful for humans.

- How do we represent positive and negative (and 0)
- How do we represent decimals

A question you should ask is what is the implication of a large vs a small word size and if you've ever heard of 32 and 64 bit architectures/problems caused by them.

### 2.3 Binary Addition arithmetic

- used example in the book of (1 0 0 1 + 0 1 0 1)
- Overflow example ( 1 0 1 1 + 0 1 1 1)

### 2.4 Signed Binary Numbers
An n-bit binary system can code 2<sup>n</sup> different things. THe question we should ask ourselves is which bit is the bit that matters for a sign.

By convention if we have an 8 bit system we use 7 bits for the 'absolute value' and 1 bit for the sign. 

Should 1 be positive or negative?

We use 1 as a  negation because of a really cool feature called a radix complement or the "two's complement" method.

Simply put, we want any negative number to be able to be written as 2<sup>n</sup> - |number| to get our value.

so 2<sup>4</sup>-7 = 9
```
9 = 1001
7 = 0111
9+7 = 0000
```

### 2.5 Specs for the chapter
These are the chips you'll be adding. For the most part, self explained. The goal of this section is to get to creating your own "ALU." At one point, I said all computers are, well, for computation. This is a small, small part of that.

### 2.8 Reflections


## Glossary

### Arithmetic Logic Unit - ALU

### Central Processing Unit - CPU

### Least Significant Bits (LSB) - bits with least value (right most)

### Memory Address - reference to a specific piece of information on a computer

### Most Significant BIts (MSB) - bits of the highest value (left most)

### Overflow - when the result of an operation requires more data than the word size

### nbit - any number bit binary number

### radix complement

### word size - the number of bits that a computer sues to represent a bit of information

