# #100DaysOfCode Log

## Day 7: Friday, July 8, 2022

<hr>

**Today's Progress**:

Some heavy lessons today but it was mainly review because I'm familiar with logic statements. So I did lessons from Jonas' course:

- The Switch Statement
- Statements and Expressions
- The Conditional (Ternary) Operator
- Coding Challenge #4
- JavaScript Releases: ES5, ES6+ and ESNext

Reviewed the `switch` statement, which I truthfully forgot how to use. And then saw how the `switch` statement was written as an `if/else`. SO repetitive, so I understand why you'd use the `switch` in certain cases.

I wrote this, building on previous code:

```javascript
const language = "English";

switch (language) {
  case "Chinese":
  case "Mandarin":
    console.log("MOST number of native speakers!");
    break;
  case "Spanish":
    console.log("2nd place in number of native speakers");
    break;
  case "English":
    console.log("3rd place");
    break;
  case "Hindi":
    console.log("Number 4");
    break;
  case "Arabic":
    console.log("5th most spoken language");
    break;
  default:
    console.log("Great language too! :D");
}
```

At first, it was printing all of the statements after the `case "English":` because I forgot to add the `break;` lol but now I understand why you need to `break` after each statement!

If I were to write this as an `if/else` statement, it would come out to:

```javascript
if (language === "Chinese" || language === "Mandarin") {
  console.log("MOST number of native speakers!");
} else if (language === "Spanish") {
  console.log("2nd place in number of native speakers");
} else if (language === "English") {
  console.log("3rd place");
} else if (language === "Hindi") {
  console.log("Number 4");
} else if (language === "Arabic") {
  console.log("5th most spoken language");
} else {
  console.log("Great language, too! :D");
}
```

It's so repetitive so the `switch statement` definitely looks better. And it's a preference thing too so I'm able to use it if I feel like it. To develop my own coding style.

Then reviewed the difference between a statement and an expression.

An expression produces a value:

```javascript
3 + 4;
1991;
true && false && !false;
```

these all produce a boolean value.

And a statement does not. It's like a sentence.

```javascript
if (23 > 10) {
  const str = "23 is bigger!";
}
```

The statement doesn't produce a value but the `str` does.

Template literals are the only ones that can take an expression only because they produce a value.

Then I reviewed the Ternary Operator, which is used quite often in React. But I actually love the ternary operator. So for Challenge #4, I had to build a tip calculator using a ternary.

```javascript
// TEST DATA: Test for bill values 275, 40, 430
const bill = 430;
let tip = bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2;

console.log(
  `The bill was ${bill}, the tip was ${tip}, and the total value is $${
    bill + tip
  }`
);
```

The syntax for a ternary conditional is:

```javascript
condition ? true : false;
```

Then reviewed a bit of JavaScript history and why it's good to know about old JavaScript.

SO finished Fundamentals Part 1!
