# #100DaysOfCode Log

## Day 5: Sunday, December 24, 2023

<hr>

**Today's Progress**:

Slacked for a few days because of holiday things but! getting back to it on Christmas Eve. Learned about Binary Arithmetic today.

The reason why we learn conversion techniques between the decimal system and binary system is because humans have to give input to computers in decimal numbers and computers only understand the binary world. So there will always be two things computers need to do:

1. Represent numbers in binary
2. Perform arithmetic operations on those binary representations.

### Sign Magnitude

A numbers representation in sign magnitude has the same number of bits as the original number, plus a bit called the sign bit on the extremely left (**MSB: Most Significant Bit**).

The **sign bit** denotes that the number is negative if it is set to 1 and positive if it is set to 0.

So for example, let's represent a number using an 8-bit sign magnitude. The number `-24` in signed magnitude:

First write the binary representation of 24

```
1 1 0 0 0 = 24
```

But `10011000` is `-24`.

But HOW? I'm confused about sign magnitude because couldn't `10011000` represent `152`? I don't understand I don't understand.

The next lessons are on One's Complement and Two's Complement so maybe it'll make more sense but this is all I've got for now.
