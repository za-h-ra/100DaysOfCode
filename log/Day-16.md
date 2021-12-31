# #100DaysOfCode Log

## Day 16: December 31, 2021

**Today's Progress**:

It is the last day of 2021! I've offically completed Fundamentals Part 1 and Fundamentals Part 2 of this JavaScript course. Yay!

And I also officially hate `while loops`. I broke my browser so many times while writing the exercises. So I'm not sure I'm going to try to use while loops but we'll see. We'll SEE when we get to leetcode things in the new year. lol

Anyways, I learned about loops and refreshed my knowledge on that. I pretty much got it which was awesome. Some of the challenges I had to really think about but that's ok.

I did challenge #4 to end this section, which was building on that tip calculator.

Here was my solution:

```javascript
const bills = [22, 295, 176, 440, 37, 105, 10, 1100, 86, 52]
const tips = []
const totals = []

function calcTip(bill) {
  return bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2
}

for (let i = 0; i < bills.length; i++) {
  tips.push(calcTip(bills[i]))
  totals.push(bills[i] + tips[i])
}

// BONUS

function calcAverage(arr) {
  let sum = 0
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i]
  }
  return sum / arr.length
}

console.log(calcAverage(totals))
```

The bonus one, I had a little trouble with. I GOT it but I always forget that the solution needs to be returned outside of the loop. I was returned `sum / arr.length` inside of the loop so I was getting `undefined` when calling the function.

**Thoughts**:

Feeling good! I'm exicted that I finished the fundamentals. It took a little while because I wasn't fully committed but after this holiday weekend, I'll commit to being more consistent because even a little bit of the lessons help boost my knowledge.
