# #100DaysOfCode Log

## Day 3: June 27, 2022

<hr>

**Today's Progress**:

So I skipped a few days, it's been a lot going on the last few days. But today I reviewed:

- Basic Operators
- Operator Precedence
- Challenge #1

The basic operators are:

1. `+`
2. `-`
3. `*`
4. `/`
5. `**`
6. `typeof`

The comparision operators are:

1. `>`
2. `<`
3. `>=`
4. `<=`
5. `==` and `===` we didn't discuss these but I know they exist.

And then assignment operators:

1. `=`
2. `+=`
3. `*=`
4. `++`
5. `--`

So to practice the lessons I learned, I added to the code from (Day 2)[Day-2.md]

```javascript
// BASIC OPERATORS
let halfCountry = population / 2;
console.log(halfCountry);
population++;
console.log(population);

let finlandPop = 6;

console.log(population > finlandPop);

let avgPopulation = 33;
console.log(country < avgPopulation);

let description = `${country} is in ${continent}, and its ${population} million people speak ${language}`;
console.log(description);
```

And for the challenge, I was meant to calculate the BMI for two dudes, so this is the code I wrote to calculate their BMI's and then compare them to each other:

```javascript
// BMI Formula
// BMI = mass / height ** 2 = mass / (height * height) (mass in kg and height in meter)

// Data 1: Mark weighs 78 kg and is 1.69 m tall. John weighs 92 kg and is 1.95 m tall
// Data 2: Mark weighs 95 kg and is 1.88 m tall. John weighs 85 kg and is 1.76 m tall

let markMass = 95;
let johnMass = 85;
const markHeight = 1.88;
const johnHeight = 1.76;

let markBMI = markMass / markHeight ** 2;
let johnBMI = johnMass / johnHeight ** 2;

console.log(markBMI, johnBMI);

let markHigherBMI = markBMI > johnBMI;
console.log(markHigherBMI);
```

So I'm feeling good! Tomorrow I'll move on to review Strings and Template Literals and then `if/else` statements 😬
