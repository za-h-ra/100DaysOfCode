# #100DaysOfCode Log

## Day 9: December 10, 2020

<br>

**Today's Progress**: So the main course I'm working through is Jonas Schmedtmann's [The Complete JavaScript Course 2020: From Zero to Expert!](https://www.udemy.com/course/the-complete-javascript-course/). So I'll be writing my logs about this course because it gives me actual practice with code and thinking in a computational way.

Today I worked through his lessons:

* How to think like a Developer: Become a Problem Solver!
* Using Google, StackOverflow and MDN
* Debugging (Fixing Errors)
* Debugging with the Console and Breakpoints
* Coding Challenge #1

I rewatched the first two lessons because I was slightly distracted yesterday and I think he explains breaking problems down really well. I never really understood how to breakdown problems and how to think about them in a way a computer would. And I'm not quite sure I fully understand how to do it but I know practice makes perfect. So I worked on the following code challenge:

![](https://i.imgur.com/CiJcKhM.png)

And my thoughts were kind of scattered. I broke this problem down like so:

```
Sub-problem:
// Create a function
// Takes in array, which is temp array
// Turn array into string
// What is the # of days? Is it the index + 1?
// Compute index + 1
// Print string with dots in front of it and at the end of it
```

But then I got to trying to actually write the code and I didn't do it so well but I know I need more practice with challenges like this!

I wrote it this way:

```
const temps = [17, 21, 23]
const temps2 = [12, 5, -5, 0, 4]

function printForecast(arr) {

    for (let i = 0; i < arr.length; i++) {
    let day = Number([i]) + 1
    let temp = `... ${arr[i]}C in ${day} days ...`
    console.log(temp)
    }
}

printForecast(temps2)
```

BUT BEFORE I did this. I was googling things and came across the ```.join()``` method on MDN. And I decided to write my function this way first:

```
const temps = [17, 21, 23]
const temps2 = [12, 5, -5, 0, 4]

function printForecast(arr) {

    let tempArr = arr.join(" ... ")
    console.log(tempArr)
}

printForecast(temps2)
```

I felt like I could've done it with the ```join()``` method if I kept thinking about it but I spent an hour on this challenge and decided to do a walk-through of the solution. It gave me insight on how to think about it. Should I try the problems on Hackerrank? Or LeetCode? Maybe CodeWars? Idk.

