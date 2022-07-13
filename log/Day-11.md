# #100DaysOfCode Log

## Day 11: July 13, 2022

<hr>

**Today's Progress**:

Today's lesson was HEAVY. Introduction to Objects. They make sense but had a lot of code to write so I'll keep this entry short.

For the Object lesson, I got practice in by writing objects. So we built on the country assignments and I wrote an object as such:

```javascript
const myCountry = {
  country: "Argentina",
  capital: "Buenos Aires",
  language: "Spanish",
  population: 45.38,
  neighbors: ["Colombia", "Chile", "Uruguay"],
};
```

Objects can hold any key:value pair. The key is the variable and the value is whatever you want it to be, which is amazing. It's powerful.

Then we talked about the Dot Notation vs. The Bracket Notation for accessing objects. So I was able to access the objects by writing something like: `myCountry.country` to get the name of the country. And `myCountry.neighbors` to get the array. But if I want to access an element in the array, I would have to do: `myCountry.neighbors[1]` so that was cool. To get the length, I have to do: `myCountry.neighbors.length` and it'll give me however many elements are in the array.

The bracket notation is interesting, I haven't used it much so I don't quite understand it but as far as I know, you can put any value in there.

Then we learned about Object Methods and I got to build on the country Object. I wrote some functions inside of it with a string, accessing different properties. Which got challenging at points but the more I do it, the more practice!

```javascript
const myCountry = {
  country: "Argentina",
  capital: "Buenos Aires",
  language: "Spanish",
  population: 45.38,
  neighbors: ["Colombia", "Chile", "Uruguay"],

  describe: function () {
    return `${this.country} has ${this.population} million ${this.language}-speaking people, ${this.neighbors.length} neighboring countries, and the capital is ${this.capital}.`;
  },
  checkIsland: function () {
    return (this.isIsland = this.neighbors.length === 0 ? true : false);
  },
};
```

The `describe()` function is describing what's in the object already. The `this` keyword is a cool one, I never used to understand it but now I get it. It is literally accessing "this" object and it's properties.

The `checkIsland()` function is checking if the country is an island or not with a ternary. I love ternaries!

To check my work, I printed to the console:

```javascript
console.log(myCountry);
console.log(myCountry.describe());
console.log(myCountry.checkIsland());
console.log(myCountry.isIsland);
```

Then there was a challenge, which was awesome because we went back to the BMI calculator and I got a different perspective on it, writing an actual program that does something:

```javascript
// BMI = mass / height ** 2 = mass / (height * height)
// mass in kg and height in meters
// TEST DATA: Mark weighs 78 kg and is 1.69 tall. John weighs 92 kg and is 1.95 m tall

const mark = {
  firstName: "Mark",
  lastName: "Miller",
  mass: 78,
  height: 1.69,
  calcBMI: function () {
    return (this.bmi = this.mass / this.height ** 2);
  },
};

console.log(mark);
console.log(mark.calcBMI());
console.log(mark.bmi);

const john = {
  firstName: "John",
  lastName: "Smith",
  mass: 92,
  height: 1.95,
  calcBMI: function () {
    return (this.bmi = this.mass / this.height ** 2);
  },
};

console.log(john);
console.log(john.calcBMI());
console.log(john.bmi);

if (mark.bmi > john.bmi) {
  console.log(
    `${mark.firstName}'s BMI (${mark.bmi}) is higher than ${john.firstName}'s BMI (${john.bmi})`
  );
} else if (john.bmi > mark.bmi) {
  console.log(
    `${john.firstName}'s BMI (${john.bmi}) is higher than ${mark.firstName}'s BMI (${mark.bmi})`
  );
}
```
