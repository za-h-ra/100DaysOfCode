# #100DaysOfCode Log

## Day 8: Sunday, July 10, 2022

<hr>

**Today's Progress**:

Made it to JavaScript Fundamentals Part 2. But I didn't want to overdo it on a Sunday since I don't normally code on the weekends. BUT. I reviewed

- Activating Strict Mode
- Functions
- Function Declarations vs. Expressions

Learned that `'use strict'` catches bugs in the code and will warn you of errors.

Reviewed functions and anonymous functions. I actually still don't quite understand the purpose of an anonymous function? I know it's a function without a name but what's the point? Maybe I'll learn deeper later on.

Then learned the difference between Function Declarations vs. Expressions and I definitely like writing Function Expressions more. Especially Arrow functions - I know that's the next lesson but since I'm familiar with them....they just look so much prettier!

So the code I wrote today was:

```javascript
// FUNCTIONS
const describeCountry = (country, population, capitalCity) => {
  return `${country} has ${population} million people and its capital city is ${capitalCity}.`;
};

console.log(describeCountry("United Kingdom", 40, "London"));
console.log(describeCountry("United States", 326.5, "Washington"));
console.log(describeCountry("Costa Rica", 20, "San Jose"));

// FUNCTION DECLARATIONS vs. EXPRESSIONS

function calcAge1(birthYear) {
  return 2037 - birthYear;
}
console.log(calcAge1(1993));

function percentageOfWorld1(population) {
  return (population / 7900) * 100;
}

console.log(percentageOfWorld1(329.5));

const percentageOfWorld2 = (population) => {
  return (population / 7900) * 100;
};

console.log(percentageOfWorld2(50));
```

In summary, functions are like a machine, they can receive data and return data, which is powerful.
