# #100DaysOfCode Log

## Day 9: Monday, July 11, 2022

<hr>

**Today's Progress**:

Did some more functions practice today. Surprisingly I got tripped up on the challenge, but that's a good thing because then I'm learning.

Reviewed:

- Arrow Functions
- Functions Calling Other Functions
- Reviewing Functions
- Challange #1

I was already using arrow functions before the lessons but I did learn that the `this` keyword doesn't exist on them. So I'm interested to understand more/why.

Also learned that arrow functions are convienient for writing one-liners. Great for performance, right?!

And then functions calling other functions is always a bit confusing for me so that was a good review. The code I wrote:

```javascript
function percentageOfWorld1(population) {
  return (population / 7900) * 100;
}

const describePopulation = (country, population) => {
  const popPercentage = percentageOfWorld1(population);
  return `${country} has ${population} million people, which is about ${popPercentage}% of the world.`;
};

console.log(describePopulation("USA", 328));
```

I understood what the code was doing, but what if the function that's being called inside of another function has like 3 arguments? Something to research...because I was trying to think of using it inside of my challenge #1 but couldn't quite wrap my brain around it.

And then the code I wrote for Challenge #1 was:

```javascript
const calcAverage = (one, two, three) => {
  const avg = (one + two + three) / 3;
  return avg;
};

const dolphins = console.log(calcAverage(44, 23, 71));
const koalas = console.log(calcAverage(65, 54, 49));

const checkWinner = (avgDolphins, avgKoalas) => {
  if (avgDolphins >= 2 * avgKoalas) {
    console.log(`Dolphins Win (${avgDolphins} vs. ${avgKoalas})`);
  } else if (avgKoalas >= 2 * avgDolphins) {
    console.log(`Koala's Win (${avgKoalas} vs. ${avgDolphins})`);
  } else {
    console.log(`No one wins!`);
  }
};

checkWinner(576, 111);
```

This was not bad but I was tripping up because when I was checking to see the results of `checkWinner()` I was doing `console.log(CheckWinner()) - the result was showing up and then an `undefined` and I assume the undefined was there because the function isn't actually returning anything.

Literally was going crazy but then figured out that the function just needs to be called, not logged since the statements are already being logged inside of the function.

Anyways, tomorrow we review Arrays.

On a random note, I was reading a newsletter by Josh Comeau on Expressions vs. Statements. Since I've recently reviewed these, he had a good and clear explanation:

**Expressions** - Javascript code that produces a value.
**Statement** - A Javascript program is a sequence of statements. Each statement is an instruction for the computer to do something.
