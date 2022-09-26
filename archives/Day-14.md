# #100DaysOfCode Log

## Day 14: Tuesday, July 26, 2022

<hr>

**Today's Progress**:

My brain is so foggy and fried today. So maybe consuming one course for 8 hours isn't for me. I think I can only take in information in small chunks for maximum result. So tomorrow, I'll do it differently and break up the course as I was doing before.

But the progress made in my job search: I have an interview on Thursday - a live coding. And I have an in-person 5 hour interview on Monday. EEEEEP. I'm NERVOUS. But thankfully my anxiety hasn't been bad today so I've been able to focus a bit more.

So I did the entire section 5 of Jonas' course, which was mainly on setting up my development environment, installing node.js, etc. And then reviewing how to break down problems - which I needed to kind of re-watch in order to think like a programmer. In interviews, especially when someone is watching me, I forget to break the problem down because I'm too nervous that I have to perform. lol so it was good.

Also reviewed best practices for how to efficiently learn to code. How to debug problems, and how to use MDN, Stackoverflow and Google.

And then at the end of the lesson, I wrote some code, which is actually a little more detailed and specific than the solution given when he goes over the code:

The challenge was:

```javascript
Given an array of forecasted maximum temperatures, the thermometer displays a string with the given temperatures. Example: [17, 21, 23] will print "... 17oC in 1 days ... 21oC in 2 days ... 23oC in 3 days ..."
```

The code I wrote:

```javascript
// TEST DATA 1: [17, 21, 23]
// TEST DATA 2: [12, 5, -5, 0, 4]

const printForecast = (arr) => {
  let str = "";
  for (let i = 0; i < arr.length; i++) {
    str += `... ${arr[i]}°C in ${i + 1} ${i + 1 !== 1 ? "days" : "day"} `;
  }
  return str + "...";
};

console.log(printForecast([12, 5, -5, 0, 4]));
```

Which prints exactly how the example asks it to print. I accounted for the `...` at the beginning and at the end of the array. And then I also added a ternary conditional in the `str` template literal in the loop to account for `1 day` or a number of `dayS`. I'm sure this could be written more efficiently but it worked and printed the result I wanted.
