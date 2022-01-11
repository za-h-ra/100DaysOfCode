# #100DaysOfCode Log

## Day 17: January 10, 2022

**Today's Progress**:

I'm back! The first week of January was a blur - trying to get back into routine and such after NYE. But I'm back and want to work on my consistency with finishing the JavaScript course.

So I got to Section 5. I skipped some sections because my developer environment, VSCode and prettier are already setup, thanks to these lectures from when I watched them last year!

But I did spend 30min - 1 hour on the challenge that came with this section. It took me a little bit to solve it because I had to fully think about what I was doing.

The problem was:

`Given an array of forecasted maximum temperatures, the thermometer displays a string with the given temperatures. Example: [17, 21, 23] will print "... 17oC in 1 days ... 21oC in 2 days ... 23oC in 3 days ..."`

And my solution:

```javascript
let numbers1 = [17, 23, 21]
let numbers2 = [12, 5, -5, 0, 4]

function printForecast(arr) {
  let str = ''
  for (let i = 0; i < arr.length; i++) {
    str += `... ${arr[i]}°C in ${i + 1} days `
  }
  console.log(str + '...')
}

printForecast(numbers2)
```

I had to create a function that took an array and logs a string to the console.

- I knew that first I had to turn the array into a string so I declared a variable equal to an empty string.
- Then I looped through the array to print out each element in the array because they would be printed as strings.
- Once looped through the array, I created a string that has the elements of the array.
- Then I had to print the days, which means the index of the array + 1 `${i +1}`.
- Then outside of the loop, I logged the string to the console.

That's my thought process for solving this. And I'm glad I didn't run to the solution so quickly and really sat down to think about it. The tricky part was also printing the last `...` dots to the end of the array and I realized, I could just concatenate that. lol.
