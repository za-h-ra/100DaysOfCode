# #100DaysOfCode Log

## Day 10: July 12, 2022

<hr>

**Today's Progress**: So today was the day for arrays! I actually haven't written arrays in a while, not even at work so it was good to review them and the methods. I've seen them in the code at work, but personally have no written it.

Anyways, the lessons:

- Introduction to Arrays
- Basic Array Operations(Methods)
- Challenge #2

With each day I study, I try to study up to the challenge unless the lessons are super long and I know I'll get fatigued with information.

Arrays are a data structure. It stores data, kind of like a big container that can take variables and process them later. Also a good way to keep your code DRY (don't repeat yourself).

Arrays aren't primitive values, which means that we can change/mutate them. Arrays can hold values of different types (`number`, `expressions`, `string`, `boolean`, other arrays, etc.)

As practice, I wrote an array:

```javascript
const zahra = ["Zahra", "Khan", 29, 2037 - 1993, "Software Engineer", friends];

console.log(zahra);
console.log(zahra.length);
```

The `.length` is a built-in method that gives you the number of elements in an array. The `.length -1` gives you the last element in an array. To access an element in an array, I would do: `zahra[0] ` since arrays start at `index 0`. And the result would be `"Zahra"` since that's the first element in my array.

Some array methods learned:

- `.push()` adds elements to the end of an array. Returns the length of the new array.
- `.unshift()` adds elements to the beginning of an array. Returns the length of the new array.
- `.pop()` removes elements from the end of an array. Returns the removed element.
- `.shift()` removes elements from the beginning of an array. Returns the removed element.
- `.indexOf()` tells you which position an element in an array is in. Returns the position of the element.
- `.includes()` checks to see if an array includes a specfic element. Returns `true` or `false`.

Since these methods are functions, they return a value.

So to practice some methods, the code I wrote was:

```javascript
const neighbors = [
  "Belize",
  "Costa Rica",
  "Chile",
  "Argentina",
  "Guatemala",
  "Peru",
];

neighbors.push("Utopia");
console.log(neighbors);
neighbors.pop();
console.log(neighbors);
if (!neighbors.includes("Germany")) {
  console.log("Probably not a central European country");
}

console.log(neighbors.indexOf("Chile"));
neighbors[2] = "Panama";
console.log(neighbors);
```

I guess I could've written the last one as:

```javascript
neighbors.indexOf("Chile") = 'Panama'
console.log(neighbors)
```

But it works and I know there are better ways of doing things so I'm learning!!

For challenge #2, I built the tip calculator again, but this time using a function and arrays!

```javascript
// TEST DATA: 125, 555, 44

const calcTip = (bill) => {
  const tip = bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2;
  return tip;
};

console.log(calcTip(100));

let bills = [125, 555, 44];

let tips = [calcTip(bills[0]), calcTip(bills[1]), calcTip(bills[2])];
console.log(tips);

const totals = [bills[0] + tips[0], bills[1] + tips[1], bills[2] + tips[2]];

console.log(totals);
```

I could've written it more simply for performance and purposes of Big-O:

```javascript
const calcTip = (bill) =>
  bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2;
```

A one-liner would've been more efficient code.

Initially for the totals, I wrote:

```javascript
const totals = [
  bills[0] + calcTip(bills[0]),
  bills[1] + calcTip(bills[1]),
  bills[2] + calcTip(bills[2]),
];
```

Not fully realizing that the purpose of the `tips` array is to make my life simpler with the values in it. lol. So then I changed it because it's so redudent to do the math in another array when it's already been done.

Tomorrow, we review Objects! A very important topic!
