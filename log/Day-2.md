# #100DaysOfCode Log

## Day 2: Monday, December 18, 2023

<hr>

**Today's Progress**:
Learning about the Essential Number Systems in Computer Science.

This course breaks it down as if you are a 5 year old, which I love.

So let's start with what a number system is: we've naturally developed systems that relate unique symbols to specific values which end up being a number system.

The "base symbols " of the decimal system are the numbers are we know it:

```
0123456789
```

And what I've never thought about but consciously am aware of is that all numbers (symbols) after 9 are a combination of the numbers that already exist from 0-9 to give him greater values. That's kind of cool.

So in the decimal number system (which is what humans use), the place value of each digit increases in the powers of 10 from right to left. This is because the decimal system uses a base of 10, meaning we have 10 base symbols (0-9) to represent numbers.

So then we have the **Binary System**. An essential component of compters is the `transistor` which has two states, `on` and `off`. Each state is represented using one of two symbols (`0` and `1`) resulting in a numbering system with base 2. So the binary system is a two-base system.

Similarly to the decimal system, the rules for representing a number in binary comes from the place values of digits. In the 0-9 decimal system, we have base at powers of 10 from right to left (because there are 10 digits??!! It never clicked before this). BUT! In the Binary System, the place value correspond to ascending powers of 2 from right to left (because there are two digits in the binary system).

For example, the binary representation of 29 would be `11101`

There are many different numbers we can represent with two bits:

```
0 0 = 0
0 1 = 1
1 0 = 2
1 1 = 3

```

We can represent four combinations of numbers from 0-3. With three bits, there would be 4 \* 2 = 8 possibilities.

```
0 0 0 = 0
0 0 1 = 1
0 1 0 = 2
0 1 1 = 3
1 0 0 = 4
1 0 1 = 5
1 1 0 = 6
1 1 1 = 7
```

The goal is to come up with an expression for the range of bits. We want an expression to calculate how many (and what) numbers we can present using `n` bits.

A single digit (n = 1) binary number can have two different values (0 or 1).

When we take the number of bits to `n = 1`, the number of possible values increases to `2 x 2 = 2^2` and when we take the number of bits to three digits, it increases to ` 2 x 2 x 2 = 2^3` because there are three times as many possibilities with a combination of two numbers.

With every increase in `n`, we are multiplying the possible combinations by 2.

`n` binary digits can represent `2^n` unique values. One of these values is always 0, so the range of numbers that we can represent is 0 to 2^n - 1.

Binary quiz recap:

1. To represent 6 digits in binary = `2^6 = 64`

2. The range of numbers that you can represent in binary using 6 digits is `0-63`. Initially, I put `0-64` but I realize that's incorrect because the number system starts at 0. So even though we have 64 numbers, the range is up to 63 because you have to subtract 1 since the binary digits start at 0.

   So the math would be `2^6 - 1 = 63` for the range.

3. How many binary digits do you need to represent the range of numbers 0-127?

   I figured that we're actually counting up to 128. So it would be 7 binary digits. So the math would be `2^7` but since we're counting the RANGE, it would be `2^n - 1 = 127`. Alternatively, we can count that the given range as 128 unique values and solve `2^n = 128`
