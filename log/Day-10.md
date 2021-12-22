# #100DaysOfCode Log

## Day 10: December 21, 2021

**Today's Progress**:

I finished JavaScript Fundamentals Part 1!!! I completed exercises up to Challenge #4. That one made me think a bit because I'm not good at math. The problem was to write a tip calculator.

`Steven wants to build a very simple tip calculator for whenever he goes eating in a restaurant. In his country, it's usual to tip 15% if the bill value is between 50 and 300. If the value is different, the tip is 20%.`

This was my solution:

```javascript
// TEST DATA:
// Test for bill values 275, 40, 430

let bill = 275
let tip = bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2

console.log(
  `The bill was $${bill}, the tip was $${tip}, and the total value $${
    bill + tip
  }`
)
```

Once I thought about, I got it. So I had to set declare the `bill` variable first and then declare the `tip` variable, which had to include the calculation.

The total of the bill has to be between 50 and 300 — I think at first I got confused because I wasn't breaking down the problem to structure the ternary statement. So I wrote it as an `if/else` statement as such:

```javascript
if (bill >= 50 || bil <= 300) {
  bill * 0.15
} else {
  bill * 0.2
}
```

But I had written an `||` instead of an `&&` and that gave me a completely different result. I read the instructions again and changed it to an `&&` because the condition was that it HAS to be between 50 and 300 otherwise it's something else completely.

Also did some lessons on `switch statements` and `ternary operators`. I used ternary A LOT at work so I'm familiar with how to write them.

**Thoughts**:

This was a great refresher into conditionals. I like the ternary operator a lot and I use it quite a bit at work so I like the one-liner. I also see the use case for `switch` statements as well because I've seen them used in `Redux`. I like the exercises in between lectures because they challenge me to write code and think about the problem. They're easy now but I'm excited for them to get a bit harder. I want to be able to do some DSA as well. BUT one thing at a time 😅
