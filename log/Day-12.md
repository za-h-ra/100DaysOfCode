# #100DaysOfCode Log

## Day 12: July 19, 2022

<hr>

**Today's Progress**: lol hi. I SHOULD be on like day 30 or something but lots going on. So here are the updates: I had a live-coding interview on Friday and I didn't do well in that. (Totally forgot to write a for loop properly too, what an idiot🤦🏽‍♀️) and then realized later where I messed up. It was in a google doc - so as a visual person I couldn't see what I was doing with my code in the console and crumbled under pressure while the interviewers were watching me. But it's okay, I reflected on it and I've moved on.

I'm also soon to be funemployed. BlockFi is offering to buy everyone out of the company and I'm gonna take the offer. Full on focus on technical interviews and job hunting. It was a hard decision to make and it's scary not having something lined up right after a job - but I have more skills now than I did before, and each day that I study, I get better. So keeping my head up and in positive light. The only thing I really have is to believe in myself and stay confident. ✨

SO now that we're done with the updates! Picked back up what I was working on from the JavaScript course. Reviewed:

- Iteration: The For Loop (lol after that interview, I needed to review this haha)
- Looping Arrays, Breaking and Continuing
- Looping Backwards and Loops in Loops

I never understood why, when you count a loop backwards, the syntax is usually subtracting one, but today, it clicked! Like for example:

```javascript
for (let i = array.length - 1; i >= 0; i--) {
  // some code here
}
```

The `-1` exists because if an array has 5 elements in it, it's still counting to 4 since the index starts at 0. So if the loop didn't substract it, the element in position 5 is `undefined` because there isn't an element at index 5. It's confusing to explain but my brain gets it.

So loops pretty much keep your code DRY. Instead of writing something like:

```javascript
"Play song 1";
"Play song 2";
"Play song 3";
"Play song 4";
"Play song 5";
"Play song 6";
"Play song 7";
"Play song 8";
"Play song 9";
"Play song 10";
```

And manually writing it, you could do something like this with a `for loop`.

```javascript
for (let i = 1; i <= 10; i++) {
  console.log(`Play song ${i}`);
}
```

And it would print the same thing. To explain the loop I wrote: `let i = 1` starts at one because we are working with a string and want the number `1` to print out first. Then `i <= 10` is going to be less than or equal to 10 because this is where we want the loop to stop and the condition to turn `false`. Otherwise, you'd end up with an infinite loop and crash your machine (like I did earlier, lol whoops). And `i++` is pretty much the short way of writing `i = i + 1`. So the variable `i` represents the number printed to the console, in this case.

Looping arrays is a bit different. So I have an array:

```javascript
const zahraArray = [
  "Zahra",
  "Khan",
  "Software Engineer",
  29,
  ["Katie", "Sonia", "Julie"],
  true,
];
```

And I want to log all the elements of this array to the console. Instead of writing something like:

```javascript
console.log(zahraArray[0]);
console.log(zahraArray[1]);
console.log(zahraArray[2]);
console.log(zahraArray[3]);
console.log(zahraArray[4]);
```

I would write:

```javascript
for (let i = 0; i < zahraArray.length; i++) {
  console.log(zahraArray[i]);
}
```

And it does the same thing as the longer way, to print it to the console. It's so much simpler and cleaner and effortless to write a loop. Less code, more performance.

For one the exercises, I had to work off of a previous code I built, but we used an array method in the loop to add items to an array from a loop. Here's what happened:

```javascript
function percentageOfWorld1(population) {
  return (population / 7900) * 100;
}

const populations = [329.5, 120, 35, 50];
const percentages2 = [];

for (let i = 0; i < populations.length; i++) {
  percentages2.push(percentageOfWorld1(populations[i]));
}
```

First, I wrote out the function that calculates the percentage of the worlds population with the population of the country of your choice. Then I initialized a variable `populations` that is an array with the populations of countries. Then I initialized an empty array because this is the new array that we'll be adding elements to - the percentages of the world.

SO THEN, I wrote a `for loop` that loops through the `populations` array. We take the `percentages2` array and use the `.push()` method to add the calculated percentages to the new array. We use the function we've created that will iterate through each population and calculate it and push it to the array.

And there we have it!

So then, I only had brain energy for one more long lecture on `for loops` and it was writing loops within loops. Now this confuses me so much with certain problems, so I have to sometimes draw out the problem - and a loop within a loop is what was asked in the interview....and I blanked.

So I was presented with an array that had arrays inside of it:

```javascript
const listOfNeighbors = [
  ["Canada", "Mexico"],
  ["Spain"],
  ["Norway", "Sweden", "Russia"],
];
```

The task was to print out the neighboring countries if and only if they had a neighbor. OK. So I assume I'm ignoring Spain because the array doesn't have a second country inside of it. This is what I wrote:

```javascript
for (let i = 0; i < listOfNeighbors.length; i++) {
  for (let j = 0; j < listOfNeighbors[i].length; j++) {
    if (listOfNeighbors[i].length !== 1) {
      console.log(`Neighbor: ${listOfNeighbors[i][j]}`);
    }
  }
}
```

It will only print out the neighboring countries if the length of the array is greater than 1.
But then I saw the correct solution and it was this:

```javascript
for (let i = 0; i < listOfNeighbors.length; i++) {
  for (let j = 0; j < listOfNeighbors[i].length; j++) {
    console.log(`Neighbor: ${listOfNeighbors[i][j]}`);
  }
}
```

So I definitely ended up doing something a little more complicated but the wording around the problem was confusing. So whatever, I got it either way. The "correct" solution just prints out all the countries as `Neighbor: Canada`, etc.

And that's it from me today. I'll be reviewing the `While Loop` tomorrow and completing a challenge on that.
