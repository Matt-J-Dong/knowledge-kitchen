---
title: Number Systems
---

Numbers are numbers. Binary numbers, decimal numbers, hexadecimal numbers, octal numbers, and any other kind of numbers you're likely to hear about are no different from 'ordinary' numbers, except in the way in which they are written.

- Binary numbers are numbers written with combinations of two glyphs: 0 and 1.
- Octal numbers are written with combinations of eight glyphs: 0, 1, 2, 3, 4, 5, 6, and 7
- Decimal numbers are written with combinations of ten glyphs: 0, 1, 2, 3, 4, 5, 6, 7, 8, and 9
- Hexadecimal numbers are written with combinations of sixteen glyphs: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, a, b, c, d, e, and f

## Decimal numbers

The number system most ordinary humans grow up learning is called the decimal [numeral system](https://en.wikipedia.org/wiki/Numeral system), also known as the base-10 number system for reasons explained below.

### Glyphs

Numbers in the decimal system are written using any of 10 different glyphs or characters: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9. All numbers are written using some combination of these glyphs.

For example, the number `ninety three` is written in decimal as combination of a 9 and a 3:
93

The number `[one hundred twelve](https://en.wikipedia.org/wiki/112)` is written, from right to left, as a combination of a 2, a 1, and another 1:
112

Did you need a university professor to explain that to you?

### Base 10

The meaning of each of the ten glyphs in a decimal number depends upon their placement.

- The glyph all the way on the very right side of any decimal number indicates how many `1`'s there are.
- The glyph at the second-from-right position of any decimal number indicates how many `10`'s there are.
- The glyph at the third-from-right position of any decimal number indicates how many `100`'s there are.
- The glyph at the fourth-from-right position of any decimal number indicates how many `100`'s there are.
- etc...

You'll notice that the meaning of each of these positions are based on powers of 10:

- 10<sup>0</sup> = 1
- 10 <sup>1</sup> = 10
- 10<sup>2</sup> = 100.
- 10<sup>3</sup> = 1000
- etc...

Given the following number, you can see that it has a 1 at the very right-most position (indicating a one), another 1 at the second-from left position (indicating one ten), and third 1 at the third-from-left position (indicating one 100). Add those together, and you get one hundred and eleven.
111

### Terminology

Digit

- a digit is any one of the ten glyphs in any decimal number
- the word comes from latin `digitus`, meaning 'finger' or 'toe'
  ** most people have 10 fingers and toes
  ** one might imagine that counting up to ten on fingers is relatively easy for most people

### In code

In most programming languages, decimal is the default number system for all numeric [literals](../variables-literals-expressions/#variables-vs-literals):

`int x = 5; // java example assigning the value 5 to the variable x`

## Binary numbers

The number system most computer scientists love to talk about is called the binary numeral system, also known as the base-2 number system for reasons explained below.

### Glyphs

Numbers in the binary system are written using any of 2 different glyphs or characters: 0, 1. All numbers are written using some combination of these glyphs.

For example, the number `ninety three` is written in binary as combination of 0s and 1s:
`1011101`

The number `one hundred twelve`' is written, from right to left, as a combination of bunch of 0s and 1s:
`10111011110000`

### Base 2

There are two different glyphs in use in numbers written in binary style.

The meaning of each of the two glyphs in a binary number depends upon their placement.

- The glyph all the way on the very right side of any decimal number indicates how many `1`'s there are.
- The glyph at the second-from-right position of any decimal number indicates how many `2`'s there are.
- The glyph at the third-from-right position of any decimal number indicates how many `4`'s there are.
- The glyph at the fourth-from-right position of any decimal number indicates how many `8`'s there are.
- etc...

You'll notice that the meaning of each of these positions are based on powers of 2:

- 2<sup>0</sup> = 1
- 2 <sup>1</sup> = 2
- 2<sup>2</sup> = 4.
- 2<sup>3</sup> = 8
- etc...

Given the following number, you can see that it has zero ones at the very right-most position, one two at the second-from left position, and one four at the third-from-left position, one eight at the fourth-from-left position... keep going with powers of 2 for each glyph, and you will find that all the numbers add up to two hundred and twenty two.
`1011101111000011011110`

### Terminology

Bit

- the word '`bit`' is a [portmanteau](https://en.wikipedia.org/wiki/Portmanteau) of the words 'binary' and 'digit'
- since the term 'digit' has its root in the number ten, a new term was needed to talk about characters with binary numbers
- the term 'bit' was first coined in 1949 by [Claude Shannon](https://en.wikipedia.org/wiki/Claude_E._Shannon), the 'father of information theory'.

### In code

In most programming languages, binary numeric literals can be written prefixed with "0b"
`int x = 0b101; // java example assigning the value 5 to the variable x`

### History

- In Western civilization, [zero was not considered a number](https://www.scientificamerican.com/article/history-of-zero/) until introduced from Arabic culture by Fibonacci circa 1200
- Binary arithmetic and binary logic were [established by Gottfried Wilhelm Leibniz in 1703](http://www.leibniz-translations.com/binary.htm)

### Raison d'être

The binary number system correlates nicely with electronic signals in computer circuits

- Claude Shannon proposed that calculations in binary could be performed natively by electronic circuits
- computer circuits are composed of a multitude of electronic switches which are either on or off

Not coincidentally, Claude Shannon noted that this binary system lends itself to [Boolean logic](https://en.wikipedia.org/wiki/Boolean_algebra)

- in Boolean logic, devised by George Boole in 1847, all logical propositions can be decomposed into two combinations of two values: true or false

## Octal

Octal numbers work the same way, but they are base-8. Octal numbers are all composed of combinations of 8 different glyphs whose meaning depends upon their position in the number. The value of each position increases by powers of 8 with every step to the left.

## Hexadecimal

Hexadecimal numbers work the same way, but they are base-16.

### Glyphs

Hexadecimal numbers are all composed of combinations of 16 different glyphs: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, a, b, c, d, whose meaning depends upon their position in the number. The value of each position increases by powers of 16 with every step to the left.

We use a,b,c,d,e,f as glyphs in hexadecimal is in order to have a single character to represent the decimal numbers 10,11,12,13,14,15 which are each two characters long.

### In code

In most programming languages, hexadecimal numeric literals can be written prefixed with `0x`

`int x = 0x5; // java example assigning the value 5 to the variable x`
