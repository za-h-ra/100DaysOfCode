# #100DaysOfCode Log

## Day 4: Tuesday, June 28, 2022

<hr>

**Today's Progress**:

Reviewed Strings & Template Literals and then `if/else` statements. But it wasn't extremely stimulating because it's review. So I ended up doing the assignments to make sure I still understood everything, and then reviewing the solutions.

For writing a template literal string, I wrote:

```javascript
let description = `${country} is in ${continent}, and its ${population} million people speak ${language}`;
console.log(description);
```

And then building off on the previous lessons, I wrote an if/else statement:

```javascript
if (population > 33) {
  console.log(`${country}'s population is above average`);
} else {
  console.log(
    `${country}'s population is ${population - 33} million below average`
  );
}
```

Pretty much checking if the population of the country is greater than 33 million (which it was) and then printing a template literal as well as doing a mathetical equation in the second string.

Challenge #2 was also building on the information created in Challenge #1, but I had to create an `if/else` statement here as well. So the code I wrote is:

```javascript
let markMass = 95;
let johnMass = 85;
const markHeight = 1.88;
const johnHeight = 1.76;

let markBMI = markMass / markHeight ** 2;
let johnBMI = johnMass / johnHeight ** 2;

console.log(markBMI, johnBMI);

let markHigherBMI = markBMI > johnBMI;
console.log(markHigherBMI);

if (markBMI > johnBMI) {
  console.log(`Mark's BMI (${markBMI}) is higher than John's BMI (${johnBMI})`);
} else {
  console.log(`John's BMI (${johnBMI}) is higher than Mark's BMI (${markBMI})`);
}
```

Based on the data of Mark and John's BMI, I checked which dude had the higher BMI and printed it to the console.

Tomorrow, I'll review:

- Type Conversion vs. Coercion
- Truthy and Falsey Values
- Equality Operators: == vs ===

Also working on some accessibility tasks for work, so that's a learning experience too.
