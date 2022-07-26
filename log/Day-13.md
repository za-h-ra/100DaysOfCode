# #100DaysOfCode Log

## Day 13: July 25, 2022

<hr>

**Today's Progress**:

lol I hate the `while` loop because I always end up in an infinite loop if my server is running. 🥲

Now is the time to start grinding and creating a structure for success. I finished JavaScript Fundamentals Part 2 of the course. Each section of the course is about 4-5 hours long. If I spend about 8 hours studying, I can finish this course in two weeks. Maybe. But will THAT much knowledge stick? I mean it has to since I'll have the time now.

Anyways - today I worked on:

- The While Loop
- Challenge #4

The difference between the `while` loop and the `for` loop is that the `while` loop doesn't need a counter. It only needs a condition to be `true` in order to run. The syntax is:

```javascript
while (condition) {
  statement;
}
```

So in the lesson, we created a `while` loop that would roll the dice until we rolled a `6`. So the loop will run until it hits the number 6. This is how we achieved that:

```javascript
// you initialize the variable for the while loop OUTSIDE of the loop
let dice = Math.trunc(Math.random() * 6) + 1;

while (dice !== 6) {
  console.log(`You rolled a ${dice}!`);
  dice = Math.trunc(Math.random() * 6) + 1;
  if (dice === 6) console.log(`Loop is about to end...`);
}
```

I get it, but personally I don't like it. So for one of the exercises I had to write some code I wrote previously, but this time using a `while` loop instead of a `for` loop. This is the code:

```javascript
function percentageOfWorld1(population) {
  return (population / 7900) * 100;
}
const populations = [329.5, 120, 35, 50];
const percentages3 = [];

let i = 0;
while (i < populations.length) {
  percentages3.push(percentageOfWorld1(populations[i]));
  i++;
}

console.log(percentages3);
console.log(populations);
```

I used my `percentagesOfWorld1()` function to calculate the populations. I have an array of populations and an empty array where I'll add the percentages that I'll get from the loop.

So I declared `let i = 0` outside of the `while` loop. While `i` is less than the length of the `populations` array, I want my `while` loop to run. In the loop, I want to add (`push`) the calculated percentages to my `percentages3` array. So I use the `push` method on the empty array and call the `percentagesOfWorld1(populations[i])` function which iterating through the populations array and calculate each instance of the array to gather the percentage.

And then I did challenge #4 which was building on the tip calculator with all the loop knowledge we have now. This was one quite challenging but actually fun to think about:

```javascript
// TEST DATA: 22, 295, 176, 440, 37, 105, 10, 1100, 86, and 52

const bills = [22, 295, 176, 440, 37, 105, 10, 1100, 86, 52];
let tips = [];
let totals = [];

const calcTip = (bill) => {
  const tip = bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2;
  return tip;
};

for (let i = 0; i < bills.length; i++) {
  // console.log(bills[i]);
  tips.push(calcTip(bills[i]));
  totals.push(tips[i] + bills[i]);
}

console.log(tips);
console.log(totals);

const calcAverage = (arr) => {
  let sum = 0;
  // console.log("----SUM----", sum);
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  console.log(sum);
  return sum / arr.length;
};

console.log(calcAverage(totals));
```

Here's my code and thought process. SO I have an array called `bills` with the test data. I created two empty arrays called `let tips = []` and `let totals = []` and then used the `calcTip(bill)` function we created previously to calculated the tips based on the cost of the bill.

I created a `for` loop that iterates through the `bills` array. I logged `bills[i]` to the console to make sure that the loop was working and it logged each element of the array to the console. Then, I used the `tips` array and added each calculated tip to it by using our `calcTip` function and iterating through each `bills` cost in the array. So I used the `push()` method to add the calculated tips to the `tips` array. Then I logged the `tips` array to the console OUTSIDE of the loop to make sure that the array had elements in it. It had the correct calculations.

So next, I did the same with our `totals` array. I added the total cost of the bill WITH the tip to the `totals` array by using the `push()` method and then simply adding each item from the `tips[i]` array and each item from the `bills[i]` array together. Then I logged the `totals` array to the console to make sure I was getting the correct sum of each tip + bill.

Then, finally, I was given a bonus, which made me think a bit. I had to calculate the average cost of the `totals` array. I created a function called `calcAverage()` that would receive an array. First the sum of the array would start with `0` because we are adding each sum. So I declared `let sum = 0` and logged to the console to make sure it worked. lol. Then I wrote a `for` loop iterating through the `arr` that the function would receive. As it receives the array and goes through each iteration, it would add each iteration to the `sum` variable. So I re-initalized the sum variable to `sum += arr[i]` which is the same as `sum = sum + arr[i]` which is ALSO the same as whatever the sum is PLUS the next iteration of the array. Logged it to the console outside of the loop to make sure that the `sum` was receiving the correct information. And then I returned the `sum` variabled divided by the length of the array, since that would give me the average.

I used the `totals` array to calculate the average cost in the function and got the correct calculation.

WHEW!

Tomorrow will be a heavier lesson because I want to finish a full section. Today, earlier in the day, it was filled with lots of career emails and connecting with people. So that took up quite a bit of time. But here we are. I have an interview on Thursday so I need to properly prep for that too.
