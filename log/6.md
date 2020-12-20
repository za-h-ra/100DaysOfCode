# #100DaysOfCode Log

## Day 6: December 6, 2020

<br>

**Today's Progress**: To keep my learning fresh, I spent an hour on a code challenge today via [Jonas' course](https://www.udemy.com/course/the-complete-javascript-course/)! I want to stick to coding everyday, even if it's a small amount. So today I worked on the following code challenge:

![Code Challenge](https://i.imgur.com/VDNX2Vx.png)

This is a challenge I've done twice before: once when learning about functions and another time when learning about arrays. But this time, the goal was to use a ```for loop``` so I did. 

At first, I thought I was supposed to write a nested for loop but I was using ```console.log``` to look at what I was doing and quickly realized that it was okay to just loop over the array once and ```push()``` into two seperate arrays.

My solution was: 

```
for (let i = 0; i < bills.length; i++) {
	tips.push(calcTip(bills[i]))
	totals.push(bills[i] + calcTip(bills[i]))
}
```

but the instructor did it the following way to avoid repitition. No need to calculate twice, so it made sense:

```
for (let i = 0; i < bills.length; i++) {
    const tip = calcTip(bills[i])
    tips.push(tip)
    totals.push(tip + bills[i])
}
```

It's interesting to learn about better and efficent ways of doing things and definitely helps me think about code in a better way as well.

I tackled the bonus as well but I messed up and wrote the ```sum``` inside of the loop instead of returning it outside of the loop.

```
function calcAverage(arr) {
    let sum = 0

    for (let i = 0; i < arr.length; i++) {
        sum += arr[i]
        sum / arr.length
    }

}
```

My way KIND OF worked in my head and when I was testing it in the ```console``` but it looked weird. So I decided to look at the solution and realized that you have to return the ```sum``` variable OUTSIDE of the loop. Whoops. I've always gotten confused about this but practice makes perfect. 

The actual solution:

```
function calcAverage(arr) {
    let sum = 0

    for (let i = 0; i < arr.length; i++) {
        sum += arr[i]
    }

    return sum / arr.length
}
```

**Thoughts:** I really love this course. I feel like I'm learning a lot and the knowledge IS sticking. I'm not just following a tutorial, I'm actually tackling challenges on my own and yes, some are difficult and take more time but that's the whole point! It's so rewarding figuring it out. Now to apply to some jobs...


**Links**: Here is the link to the entire solution
<br>

![Final Solution](https://i.imgur.com/7v4eDHg.png)