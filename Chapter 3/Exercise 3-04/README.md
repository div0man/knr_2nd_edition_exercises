# Exercise 3-4

## Task

In a two's complement number representation, our version of `itoa` does not
handle the largest negative number, that is, the value of `n` equal to
-(2<sup>wordsize-1</sup>). Explain why not. Modify it to print that value
correctly, regardless of the machine on which it runs.

## Answer

In a two's complement number system, the absolute of minimum value is for 1
greater than the maximum positive value therefore converting largest negative
value into positive one results in overflow.

At first I thougt it's simplest to borrow 1 from any negative number, perform
everything as before, and put the 1 back at the end. However, this is not so
simple when the nuber would end with a 0, so it's simplest to just deal with the
edge case immediately.
