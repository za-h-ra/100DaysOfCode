# #100DaysOfCode Log

## Day 6: Thursday, July 7, 2022

<hr>

**Today's Progress**:

Well, well, it's been a weekish since I've done this but it's been hell of a weekend, with the holiday and then catching back up on life.

Today, I watched lessons:

- Truth and Falsy Values
- Equality Operators: == vs ===
- Boolean Logic
- Logical Operators
- Challenge #3

And did the lesson assignments along with the lectures.

Reviewed that with Truthy and Falsy values, there are only 5 actual falsy values:

- `Boolean(0)`
- `Boolean(undefined)`
- `Boolean("")`
- `Boolean(null)`
- `Boolean(NaN)`

And `false` is always just `false`. Everything else is `true`.

So for example:

```javascript
const money = 0;
if (money) {
  console.log("I have money!");
} else {
  console.log("I don't have any money.");
}
```

It will print out `"I don't have any money"` because `0` is a falsy value. Same with if you initalize a variable without a value `const height;` it will be falsy because it is `undefined`.

Then I reviewed equality operators. The `loose ==` and the `strict ===`. It's better to use the `===` because the loose operator with perform type coercion vs. the strict one won't.

The loose operator can't tell the difference between the string `"18"` and the number `18`, which will result in `"18" == 18 // true` (which it's not). The strict operator doesn't do that, it's specific with its type. So `"18" === 18 // false`.

The code I wrote for that was building on the country, language, population code from previous lectures:

```javascript
const numNeighbors = Number(
  prompt("How many neighbor countries does your country have?")
);
console.log(numNeighbors);

if (numNeighbors === 1) {
  console.log("Only 1 border!");
} else if (numNeighbors > 1) {
  console.log("More than 1 border!");
} else {
  console.log("No borders!");
}
```

Converted the `prompt()` to `Number(prompt())` so that the strict operator can catch that it is a `number` being stored into the console and not a string since it is strictly checking for a number.

And then to play around with logical operators, I wrote this code building on the previous:

```javascript
if (language === "English" && population < 50 && !isIsland) {
  console.log(`You should live in ${country}!`);
} else {
  console.log(`${country} does not meet your criteria`);
}
```

For Challenge #3, I was able to implement the solution as such:

```javascript
// TEST DATA:
// DATA 1: Dolphins score 96, 108, 89. Koalas score 88, 91, 110
// DATA Bonus 2: Dolphins score 91, 112, 101. Koalas score 109, 95, 123
// DATA Bonus 3: Dolphins score 97, 112, 101. Koalas score 109, 95, 106

const avgDolphins = (97 + 112 + 101) / 3;
console.log(avgDolphins);
const avgKoalas = (109 + 95 + 106) / 3;
console.log(avgKoalas);

if (avgDolphins > avgKoalas) {
  console.log("Dolphins win!");
} else if (avgKoalas > avgDolphins) {
  console.log("Koalas win!");
} else if (avgDolphins === avgKoalas) {
  console.log("It's a TIE!");
} else {
  console.log("Nobody wins.");
}

// *CHALLENGE BONUS*

if (avgDolphins > avgKoalas && avgDolphins >= 100) {
  console.log("Dolphins WINNNN🐬");
} else if (avgKoalas > avgDolphins && avgKoalas >= 100) {
  console.log("KOALAS WINNN🐨");
} else if (
  avgDolphins === avgKoalas &&
  avgDolphins >= 100 &&
  avgKoalas >= 100
) {
  console.log("It's a TIE.");
} else {
  console.log("No one wins!");
}
```
