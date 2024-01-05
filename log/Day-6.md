# #100DaysOfCode Log

## Day 6: Thursday, January 4, 2024

<hr>

**Today's Progress**:

We took a break. But it's okay. I knew this commitment would be a bit broken but I'm going to pick up from where I left off and continue my progress from here on out.

So today, the focus is on Binary Arithmetic with a re-review of **Sign Magnitude** because I don't get it.

Signed numbers are essentially a way to represent negative numbers. Since in decimal numbers, we have the minus sign. In Binary, we only have `0`'s and `1`'s so we needed a way to represent negatives.

An example:

`11000` = `24` in decimal. But if we want to represent `-24`, we would do it by adding `100` to `11000` which would be `10011000` WHICH IS WHAT I DON'T GET. How is that `-24`?

How would one know if `10011000` is going to be `-24`?? Isn't that `152` in decimal?

So now the problem is asking me to convert `01101101` from binary to decimal:

```javascript

01101101 = 109???

| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
   0     1    1    0   1   1    0  1

= 64 + 32 + 8 + 4 + 1
= 109
```

Does that not equal `109`?

But the way it seems like it's done is:

First we have to seperate the `0` from the beginning.

```javascript
0 1101101
0 means it's a positive number.
The magnitude is 109

```

Ok so I DID get that correctly. It makes sense but the negative ones **do not** make sense.

Quiz:

What is -43 in sign magnitude?

I know that `101011` is`43` in binary. I guess, since this is 6 bits, I would have to add `10101011` - which seems correct. I guess we would never start off reading a negative binary but only when we need to convert a negative _decimal_ to binary is when we add the `1` bit in front of it. I THINK?

Anyways, moving onto One's Complement.

### One's Complement

One's complement is another way to representing signed numbers. A number's representation in one's complement has the same number of bits as the original number, plus a bit called the sign bit on the extreme left. It denotes that the number is negative if it is set to `1` and positive if it's set to `0`.

To represent a negative number, the other bits hold the complement of the original number in binary. To represent a positive number, the bits hold the number as it is in binary.

The complement of a binary number is the number with all the individual bits inverted. The complement of the number `1010001` is `0101110`. WILD.

To write the number -25 in one's complement, we have to write the binary 25 first:

```javascript
11001;
```

But this only has 5 bits. So we fill in 0's on the left to get 8 bits.

```javascript
00011001;
```

But since we want to write a negative number, we have to take the complement:

```javascript

00011001 -> 11100110

```

BUT THAT COULD REPRESENT A WHOLE DIFFERENT NUMBER IN BINARY - WHAT? 🤯

Quiz:

1. What is the representation of -39 in one's complement?

```javascript

39 = 100111
```

But since it's only 6 bits, we have to add `0`'s in front of it and then inverse it:

```javascript
39 = 00100111

00100111 = 11011000

```

2. What is the range of values that can be represented by a 10-bit one's complement number?

```javascript
-511 to 511
```

Explanation: 1 bit is reserved for the sign, so we have 9 bits left over `2^9-1 = 511`.

3. How many values can be represented by 4-bit one's complement number?

So it's `15`.

```javascript
8 + 4 + 2 + 1 = 15
```

But for some reason, I ended up subtracting `1` because I thought I was calculating the range. But in the explanation, it says to figure it out by doing the following:

```javascript
2^3 - 1 = 7

-7 - 7

7 + 7 + 1 = 15
```

I guess that makes sense. But my way worked too.

---

And NOW - moving onto Two's Complement.

### Two's Complement

Two's complement is the most widely used representation of signed numbers. Unlike one's complement, **two's complement** has a unique representation for 0. Two's complement also has a sign bit on the extreme left.

The range of two's complement is larger than one's complement. The 0 comes from the positive side representation, so the range of `n-bit` two's complement number is: `-2^n-1 to 2^n-1 - 1`. _n_ is usually a power of 2.

To represent a number in two's complement, we follow the steps below:

1. Write the number in binary
2. Take the complement of the number
3. Add 1 to the number

Let's write the number -28 in two's complement. First the binary of 28 is:

```javascript
11100;
```

But the binary representation only has 5 bits, and the closest power of 2 is 8. So we will in 0's on the left to get 8 bits. It'll look like:

```javascript

00011100 = 28

```

So then

```javascript
00011100 --> 11100011
```

And finally we have to add 1. So

```javascript
11100011;

becomes;

11100100;
```

lol what. 🤯❓ ❓ ❓

In modern computer systems, this seems to be the most widely used representation for signed numbers. I'm just thinking - when will I need to know this in my Software Engineering career. Hmm..💭 I guess it's good to know and be aware of it but I think it's okay to not understand it fully either.

So to convert FROM Two's Complement to Decimal:

1. Extract the sign bit (1 for negative, 0 for positive)
2. Take the complement of the number
3. Add 1 to the number

Let's convert `11111111` from two's complement to decimal:

```javascript

1 1111111

This means the number is negative since the left number is 1.
```

Then the complement becomes:

```javascript
11111111 ---> 00000000

and we add 1 so it becomes

00000001
```

The number `11111111` is two's complements representation of -1. I think I'm getting it, I THINK.

Let's convert `01011011` to decimal.

```javascript
0 1011011

This means the number is a positive number since the left number is 0.
```

Then the complement becomes:

```javascript
01011011 ---> 10100100
```

If I'm remembering correctly, positive numbers stay the same without adding a `1`? So this would be `164`, no?

Let's see - OK. So the mistake I made was that, it actually didn't need to be converted to a complement since it was already a positive number. So I should have left it at:

```javascript
01011011 which equals 91
```

It was `91`. Now I know.

Quiz:

1. What is the two's complement representation of 54?

Since we don't change it, with 8-bits, it would be:

```javascript
00110110 --> 54
```

2. What is the range that a 4-bit two's complement number can represent?

```javascript
2^3 - 1 = 7

-7 to 7

```

But the actual correct answer was: `-8 to 7` because:

```javascript
-2^n-1 = -8 and 2^n-1 -1 = 7

```

This is a lot of math.

That's all for today. Tomorrow I'm going to read up on _why_ two's complement works and do Arithmetic with Signed Numbers.
