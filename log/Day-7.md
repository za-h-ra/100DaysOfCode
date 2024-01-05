# #100DaysOfCode Log

## Day 7: Friday, January 5 2024

<hr>

**Today's Progress**:

I read up on why two's complement works and I still don't really get it so I think when I need it - I'll watch some videos on it but for now, it's nice to know it exists.

So then I went over how to do addition and subtraction with signed numbers.

```javascript

  01000101  = 69
+ 00001100  = 12
-----------------
  01010001  = 81

```

So does having two `1`'s equal to `0`? And then the `1` is carried over to the next number? This is how I think it works in my brain.

Quiz:

1. What is `00011001 + 01000101`, considering the numbers to be two's complement?

Here's how I would approach it:

```javascript

  00011001  = 25
+ 01000101  = 69
-----------------
  01011110  = 94
```

Which ended up being correct. So I think I'm getting the addition part.

2. What is `0011001 - 01000101`, considering the numbers to be two's complement?

I got it wrong at first. Did the math on paper and came up with `10010100` but then figured it out by doing the following:

```javascript

   111 11      ( the carryover)
  00011001 = 25
+ 10111011 = -69 (we have to convert to the inverse)
----------------
  11010100
```

Ok so that makes sense.

---

Moving onto the next module: **Using Binary to Represent Information**.

### Text Representation

So we're going to learn how to represent text in a binary system. Computer scientists came up with a standardized way to map text to decimal numbers and then to binary. HOW. These people are so smart.

One of the standard is **ASCII** which I'm familiar with. It uses 70bits to map the English alphabet (upper and lower case letters), digits, and some special characters.

I typed in `"Hi World"` in the ASCII to Binary Converter and this is what it gave me:

```javascript


Character  |  ASCII Code |  Binary
------------------------------------
    H           72          1001000
    i	        105	        1101001
                32	        0100000
    W	        87	        1010111
    o	        111	        1101111
    r	        114	        1110010
    l	        108	        1101100
    d	        100	        1100100

```

But because the 7-bit encoding limited the ability to assign mathematical symbols and characters from other languages, computer scientists came up with unicode to represent larger number of bits to encode characters. SO whenever I create an HTML documentation, the top always says `utf-8`. I googled it and learned that `utf-8` uses the least amount of memory. The definition, according to MDN is:

```
UTF-8 (UCS Transformation Format 8) is the World Wide Web's most common character encoding. Each character is represented by one to four bytes. UTF-8 is backward-compatible with ASCII and can represent any standard Unicode character.
```

Interesting.

Then there's -

### Color Representation

A **pixel** is the most basic unit in digital graphics. It is represented as a dot or a square on a monitor display screen that can represent only one solid color.

A one-bit pixel can only take two values, 0 or 1. If we encode a sequence of rows and columns of dots, each with its color value, we have a computer image, which would be a `raster image` which is a 2D grid made up of tiny pixels.

I always thought it was interesting how colors got shown on a screen so learning about that - each pixel on a classic screen (at the hardware implementation level) consists of three dots of colored phosphor: red, green, and blue. Mixing red, green and blue in varying proportions can result in MANY different colors.

We represent 256 shades ranging from 0 to 255. So with each color of red, green, and blue we can set the intensity to any of the values between 0 and 255 and come up with all the colors we need.

### Image Representation

The most common images in digital computers are:

- Black and white images
- Greyscale images
- Colored images

A black and white image is just two colors per pixel. `0` represents the color black and `1` represents the color white. The total number of pixels in an image could be found by multiplying the number of horizontal pixels with the number of vertical pixels.

A greyscale image requires 8-bits at most from memory.

A colored image is represented by three arrays or an RGB image. It stacks three arrays on top of each other of red, blue, and green. It each pixel requires 24-bits. So for an image that has 36 pixels, it would be (`24 * 36 = 864 bits`) or `108` bytes. So that's why in the early days of computing, there were only black and white digital images because only one-bit pixels were used. They required less storage.

Quiz:

1. What is the total number of pixels in an image containing 20 horizontal and 45 vertical pixels?

```javascript
20 x 40 = 900
```

`900` pixels.

2. How many bits are required to store an RGB image containing 20 horizontal and 45 vertical pixels?

```javascript
20 x 40 = 900

900 x 24 bits = 21,600 bits
```

`21,600` bits.

Quiz:

1. What is the ASCII code’s binary representation of the letter A?

```javascript
01000001 = 65 for capital A.
```

2. What is Unicode?

```
A standard for encoding characters from languages across the globe
```

3. What is a pixel?

```
The smallest unit of an image that can be displayed on a screen.
```

4. What is a raster image made of?

```
Pixels - each pixel is assigned a particular color value.
```

5. What are the three primary colors used to represent a color in digital systems?

```
Red, Green, and Blue
(RBG)
```

Tomorrow, we'll start on a new module. The Anatomy of a Computer.
