# #100DaysOfCode Log

## Day 12: December 23, 2021

**Today's Progress**:

I forgot to write a log for Day 12! But I worked on lessons:

- Functions Calling Other Functions
- Reviewing Functions
- Challenge #1

Functions calling other functions — isn't that recursion? Anyways, this was confusing. I know I'll need more practice with this because it's a bit trippy to have a function inside of another function doing something else.

But overall — it was a good review of functions, why we write functions and then finished off with a challenge:

```javascript
const calcAverage = (x, y, z) => {
  return (x + y + z) / 3
}

const dolphins = calcAverage(44, 23, 71)
const dolphins2 = calcAverage(85,54,41)
const koalas = calcAverage(65, 54, 49)
const koalas2 = calcAverage(23, 34, 27)

console.log(dolphins, dolphins2, koalas, koalas2)

// Check the winner 

function checkWinner(avgDolphins, avgKoalas) {

  if (avgDolphins >= 2 * avgKoalas) {
    console.log(`Dolphins win!`)
  } else if (avgKoalas >= 2 * avgDolphins) {
    console.log(`Koalas win!`)
  } else {
    console.log('No one wins!')
  }
}

checkWinner(dolphins, koalas)
checkWinner(dolphins2, koalas2) 

```

I had to think about this challenge a little bit and definitely did it slightly different than Jonas. But it works! The way I broke it down was that I made sure the average dolphin had a winner first and then I added the detail where the average had to be twice the others average.

**Thoughts**:

This was okay. I think functions calling other functions is confusing and I definitely will need more practice with this. 