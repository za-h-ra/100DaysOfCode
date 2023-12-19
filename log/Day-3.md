# #100DaysOfCode Log

## Day 3: Tuesday, December 19, 2023

<hr>

**Today's Progress**:

Continuing learning about the Essential Number System in the Computer Science Bootcamp. I learned about binary conversion into decimal numbers. One of the exercise was to figure out what `895` is in binary.

I realized that it would have to be `10 bits`.

```
512 | 256 | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1

```

It would look like this:

```
 1  |  1  |  0  | 1  | 1  | 1  | 1 | 1 | 1 | 1
512 | 256 | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1

```

This might not the proper way to do but this is how it makes sense to me so I calculated 895 by doing:

```
512 + 256 = 768

768 + 128 = 896 (that won't work because it's OVER 895) so 128 will be a 0.

768 + 64 = 832

832 + 32 = 864

864 + 16 = 880

880 + 8 = 888

888 + 4 = 892

892 + 2 = 894

894 + 1 = 895

```

AND that's how you get `1101111111`.

So then we moved onto the Hexadecimal System. SO many number systems, wow wow wow. SO we have the decimal system for our everyday counting, which is base-10 because of our 10 fingers.

The binary system is base-2 because of the ON and OFF states a transistor in a computer can have.

The problem with binary is that it's hard for humans to accurately read and write a number in binary (TRUE). So we needed to come up with a better method than to string 0's and 1's.

The **hexadecimal system** is the idea that the numbers would be in groups because it's easier for the brain to remember groups instead of an entire string of numbers.

```
0011 1000 0100
```

It's easier to remember that this is `3`, `8`, and `4` instead of expanding this out to be `001110000100`. So the hexadecimal system represents numbers for every group of **four binary bits**. Four binary bits can represent the numbers from `0000` to `1111`, or `0-15` totalling of 16 numbers, so this system would have base-16 symbols.

Since the decimal system ends at 9, the hexadecimal system uses letters `A-F` to represent `10-15` so the base symbols for this is:

```
0123456789ABCDEF
```

The place values in hexadecimal are in powers of 16 (since it's base-16).

This part is confusing and I don't understand it yet but the lesson asked to figure out what hexadecimal `XYZ` would be in the decimal system and my mind hurts. lol

```
 |  X  |  Y  |  Z  |
 |16^2 | 16^1| 16^0|

 X * 16^2 + Y * 16^1 * Z * 16^0
 256 + 16 + 0
 272 ???

```

Idk if I even did this correctly.

It was stated that Hexadecimals are numbers usually proceeded by `#` to indicate that they are base-16. This explains the color system in Hexadecimal.

The next problem was also confusing but I THINK I can explain it. So to convert hexadecimal number `#E3B` to decimal, the math would look like this:

```

|  E  |  3  |  B  |
| 16^2| 16^1| 16^0|

#E3B = E * 16^2 + 3 * 16^1 + B * 16^0

```

`E` represents a decimal number in the hexadecimal system `0123456789ABCDEF`. `E = 14` and `B = 11` so the math would continue to be:

```

(14 * 16^2) + (3 * 16^1) + (11 * 16^0)

= (14 * 256) + (3 * 16) + (11 * 1)

= 3584 + 48 + 11

= 3643

```

`3643` would be the decimal number. But I don't really understand WHY we need to understand how to calculate this.

To note: the RANGE in the hexadecimal system would be 16^n - 1. There are 16 numbers but 0 is one of them. So you have to subtract.

So quiz recap:

1. 4 Hexadecimal digits can represent 65536 values. 16^4 = 65536

<hr>

### Converting Binary to Hexadecimal

From what I'm gathering, the purpose of this conversion is that it makes it more compact to read hexadecimal instead of binary. So if I were to convert the binary `1000111110101` to hexadecimal, I would do it like this:

Divide into four groups:

```
10001 1111 0101
```

But since there are an uneven amount of numbers, you would add extra 0's to make it easier, which would look like this:

```

= 1 1 15 5
```

And then we would write the corresponding hexadecimal symbol to it, since `15` is actually represented by a letter in hexadecimal, it would look like this:

```
0001 0001 1111 0101
 1    1    F     5

 = #11F5
```

lol it represents a color!

How converting hexadecimal #F8BE into binary:

```
F = 15 = 1111
8 = 1000
B = 11 = 1011
E = 14 = 1110

= 1111 1000 1011 1110
= 111110001011110
```

And then if I were to convert that to a decimal number:

```
(15 * 16^3) + (8 * 16^2) + (11 * 16^1) + (14 * 16^0)
= (15 * 4096) + (8 * 256) + (11 * 16) + (14 * 1)
= 61440 + 2048 + 176 + 14
= 63678
```

1. What is 5A in binary

```
5(decimal) = 101(binary)
A = 10(decimal) = 1010(binary)

= 101 1010
= 1011010

```

2. What is 1011000 in hexadecimal

```
1011000

= 0101 1000
= 0101 = 5(hexadecimal)
= 1000 = 8(hexadecimal)
= #58

```
