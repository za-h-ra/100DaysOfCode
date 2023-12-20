# #100DaysOfCode Log

## Day 4: Wednesday, December 20, 2023

<hr>

**Today's Progress**:

### Octal System

Today, we're learning about the Octal Number System. SO many number systems. So this number sustem is less widely used. It was created similarly to the hexadecial system to compactly represent binary numbers.

The Octal System groups binary numbers into triplets, whereas the Hexadecimal system groups them in quartets.

So `11011011` would be `011 011 011` in the Octal System. It is base-8. So we have the binary system which is base-2, the decimal system, which is base-10, the hexadecimal system which is base-16, and the octal system, which is base-8.

The symbols that represent the Octal System range from `0-7` so `0 1 2 3 4 5 6 7` and the place values would be powers of 8 from right to left.

An example to represent this is:

```
1  |  5  |  6
8^2  8^1   8^0

= (1 * 8^2) + (5 * 8^1) + (6 * 8^0)
= 64 + 40 + 6
= 110
```

The octal number `156` is `110` in our decimal system. So let's convert `1000111110101` binary to octal.

First I'll group it into threes.

```
001 000 111 110 101
```

And then I'll write the corresponding Octal symbol under

```
001 | 000 | 111 | 110 | 101
 1     0     7     6     5
```

So the octal is `10765`

And now the Octal to Binary converstion of `534`

```
5  |  3  |  4
101  011  100

= 101011100
```

The binary conversion would be `101011100`. That's kind of cool. To be able to convert like that. It's like finding secrets in the numbers.

Quiz:

1. What is the octal number 37 in decimal

```
37
= (3*8^1) + (7 * 8^0)
= 24 + 7
= 31
```

2. How many unique values can a 5 digit octal number represent?

`8^5 = 32768`

3. What is the range of values that can be represented with an octal number with 3 digits?

```
8^3 = 512 - 1
= 511

Range: 0 - 511
```

### N-Base Number System

So another one, N-base Number System! The N-base number system allows us to create our own number system. However, there's limitations based on what we know from base-2, base-10, base-8, base-16.

The decimal system has ten base symbols, the binary has two, and the hexadecimal has sixteen. For an n-base number system, we would need `N` base symbols.

The binary has 0 and 1 but the hexadecimal uses letters for it's last six symbols `ABCDEF`

In the n-base system, the place values would be ascending powers of `n`. For example:

```
A   |   B   |   C
n^2    n^1     n^0

= (A * n^2) + (B * n^1) + (C * n^0)
```

The range would be `k^n - 1`. So why all of this? Because you can create your own number systems. If I had a number system, I would start with `base-4`

Decimal number `138` would be:

```
138 / 4 = 34.5  | 2
34 / 4 = 8.5  | 2
8 / 4 = 2

= 222

```

So `138` in the base-10 system is equal to `222` in base-4 system.
