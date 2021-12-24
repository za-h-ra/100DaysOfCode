# #100DaysOfCode Log

## Day 11: December 22, 2021

**Today's Progress**:

We started JavaScript Fundamentals Part 2! So I finished up the final lesson on the history of JavaScript — quite interesting stuff. I didn't know how JavaScript was created and the many different names it was called and how it got to where it is now.

So after finishing that up, I started the lessons on Functions in JavaScript. The purpose of functions is to avoid repeating yourself. Keep your code "DRY". And then I wrote some functions.

```javascript
// LECTURE: FUNCTIONS

function describeCountry(country, population, capitalCity) {
  let string = `${country} has ${population} million people and its capital city is ${capitalCity}`
  return string
}

console.log(describeCountry('Costa Rica', 5.094, 'San Jose'))
console.log(describeCountry('Argentina', 45.38, 'Buenos Aires'))
console.log(describeCountry('Austrailia', 25.69, 'Canberra'))

// LECTURE: Function Declarations vs Expressions

function percentageOfWorld1(population) {
  let percentage  = (population / 7900) * 100
  return percentage.toFixed(1)
}

console.log(percentageOfWorld1(325))

const percentageOfWorld2 = (population) => {
  return (population / 7900) * 100
}

console.log(percentageOfWorld2(1441))
```
Whenever I have to do match, I get tripped up though and have to think harder about the problem. But writing the functions itself, not a problem. Obviously I know how to write them. BUT! The code I wrote...there's definitely better one line solutions for them such as just returning the string in the first solution instead of initializing a variable and THEN returning it.

A learning lesson to make my code more efficient. We're onto learning about Arrow functions next!
