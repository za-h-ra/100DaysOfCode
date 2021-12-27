# #100DaysOfCode Log

## Day 13: December 26, 2021

**Today's Progress**:

We're at Arrays now! I completed the Introduction to Arrays section of The Complete JavaScript Course 2022 by Jonas. And then finished off with a challenge.

Arrays and Objects are the most important Data Structures in JavaScript. So I refreshed my knowledge in writing arrays and *how* arrays work. I didn't know that you can't calculate arrays as parameters of a function. The lesson said that but I tried it anyway to see what happens and it gave me a `NaN` or coerced the strings into one big one. 

Anyways. I reveiwed the different methods of an array:
- `.pop()`
- `.unshift()`
- `.push()`
- `.shift()`
- `.indexOf()`
- `.includes()`

I may create a little cheatsheet for these to remember them each time I need to use them.

To get the last element of an array, you simply type in `array.length -1`, to check the length of an array, you type in `array.length`.

**Thoughts**:

Feeling good! For the challenge, I had to do a tip calculator again, but this time I had to put it in a function and then put the total bill in an array. This was my solution:

```javascript
function calcTip(bill) {
  return bill >= 50 && bill <= 300 ? bill * .15 : bill * .20
}

console.log(calcTip(100))

const bills = [125, 55, 44]
const tips = [calcTip(bills[0]), calcTip(bills[1]), calcTip(bills[2])]
console.log(tips)
const totals = [bills[0] + tips[0], bills[1] + tips[1], bills[2] + tips[2]]
console.log(totals)

```

My original solution to calculating the totals was `map()` through the array and calculate the totals altogether and pushing them into the array:

```javascript
let totals = []
bills.map(function(el1, idx) {
  return totals.push(el1 + bills[idx])
})
``` 

BUT! We've not gotten to that so I just added the bill and tip with the index of the array. Sticking to only what we've been learning. 😁

The above was a solution I saw on StackOverflow — it worked so I was happy but I don't fully understand it yet SO TBD.