# #100DaysOfCode Log

## Day 9: December 20, 2021

So I fell off. I had a feature to build at work and then after work I didn't want to look at code much but that's not an excuse. Devoting one hour to do something is do-able. So I'm here again but I'm picking back up from where I left off.

**Today's Progress**:

Yesterday I posted a blog post on Type Conversion and Coercion. This was a hard subject to explain but I believe I understand it more now and hopefully don't have to think about it too much when writing code. Also TypeScript exists now so once I learn TypeScript, not sure I'll have to worry about those buggy things that JavaScript has.

Today I worked on the Javascript Course by Jonas Schmedtmann — up to Challenge 3 and completed coding exercises for each lecture.

The main topic for each of these lectures was Boolean logic, logical operators, and how Type Conversion vs Coercion plays a part in each. 

The challenge was to test my knowledge in `if/else` statements and logical operators and I implemented the code correctly! Yay!

**Thoughts**:

Feeling good picking things back up! Just have to stay consistent and not get distracted. 

Here was the solution to my challenge: 

```javascript
let numNeighbors = Number(
  prompt('How many neighbor countries does your country have?')
)

if (numNeighbors === 1) {
  console.log('Only 1 border!')
} else if (numNeighbors > 1) {
  console.log('More than 1 border!')
} else {
  console.log('No borders')
}
```

I had to convert the `prompt` to `Number(prompt())` because with type conversion, JavaScript recognizes the answer to `prompt()` as a `string` and we needed to convert it to a number. If I compared it with a loose `==` operator, the `if/else` statements were true but when I added the strict `===` operator, the statments were false so I had to explicitly convert the value.

Testing my knowledge in Logical operators, this was my code:

```javascript

if (language === 'English' && population < 50 && country !== isIsland) {
  console.log(`You should live in ${country}`)
} else {
  console.log(`${country} does not meet your criteria`)
}
```
The country did NOT meet the criteria lol.

And then my solution to the challenge was A LOT of `if/else` statements but I know to make that simpler with a switch statement — which is up next and tomorrow's lesson! 

```javascript
let dolphinsAvg = (96 + 108 + 89) / 3
let koalasAvg = (88 + 91 + 110) / 3
console.log(dolphinsAvg, koalasAvg)

if (dolphinsAvg > koalasAvg) {
  console.log("Dolphins win!")
} else if (dolphinsAvg < koalasAvg) {
  console.log("Koalas win!")
} else if (dolphinsAvg === koalasAvg) {
  console.log("It's a tie!")
} else {
  console.log("No one wins!")
}

// BONUS 1 && BONUS 2

if (dolphinsAvg > koalasAvg && dolphinsAvg >= 100) {
  console.log("Dolphins Win!")
} else if (koalasAvg > dolphinsAvg && koalasAvg >= 100) {
  console.log("Koalas Win!")
} else if (dolphinsAvg === koalasAvg && koalasAvg >= 100 && dolphinsAvg >= 100) {
  console.log("It's a tie!")
} else {
  console.log("No one wins!")
}
```