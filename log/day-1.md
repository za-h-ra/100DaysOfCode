# #100DaysOfCode Log

## Day 1: December 1, 2020
<br>

**Today's Progress**: 

1. I worked on Jonas Schmedtmann's [The Complete JavaScript Course 2020: From Zero to Expert!](https://www.udemy.com/course/the-complete-javascript-course/). I was already working through part 2 of the JavaScript Fundamentals where it was refresher knowledge on functions. However, I enjoyed his explanations on how functions work, each lecture ending with an assignment to put into practice what I've learned. So I completed the following lessons:
* Activating Strict Mode
* Functions
* Function Declarations vs. Expressions
* Arrow Functions
* Functions Calling Other Functions
* Reviewing Functions

And then ending it with a Coding Challenge to summerize and practice everything learned. 

2. I started freeCodeCamp's Responsive Web Design Certification a long time ago but I'd like to finish it for my own personal gain and knowledge. And I'd like to complete the projects. So I left off at Applied Visual Design. I worked on that today and got through 58% percent of the section. I think tomorrow, instead of going hard, I'll complete just 10 lessons so what I'm learning sticks.

**Thoughts**:

I'm feeling good—productive! I accomplished my coding goals for the day so that's a nice feeling. 

1. The coding challenge for Jonas' course was a little tough. The first part asked for an arrow function that calculated the average of 3 scores. I did that one right. And then the second part was to check which score was the winner. I got confused because the lesson taught us to Call Functions within Functions so I was writing my code like this: 

```
const calcAverage = (score1, score2, score3) => {
    const average = (score1 + score2 + score3) / 3
    return average 
}

// Dolphins 
calcAverage(44, 23, 71)

// Koalas
calcAverage(65, 54, 49)

function checkWinner(avgDolphins, avgKoalas) {
    const dolphins = calcAverage(avgDolphins)
    const koalas = calcAverage(avgKoalas)

    if (dolphins >= 2 * koalas) {
        console.log(`Dolphins win (${avgDolphins} vs. ${avgKoalas})`)
    } else if (koalas >= 2 * dolphins) {
        console.log(`Koalas win (${avgKoalas} vs. ${avgDolphins})`)
    }
}

console.log(checkWinner(46, 56))
```

But in the console, it was throwing ```undefined``` at me. So I made a second attempt at it by re-reading the challenge and what it was asking for. I did it right the second time but I was getting confused about the ```undefined``` result once again and realized my mistake.

2. The freeCodeCamp exercises were really helpful. I know how to use CSS but it was helpful because I've always gotten confused about the ```position``` property and how to use it. But NOW it makes sense to me. I'll need to put this into practice intentionally in order to full grasp but I do believe I get it now! 

**Link**: Some exercises I did today:

 ![Functions Exercise](https://i.imgur.com/gxgjjnK.png)
<br>
 ![Function Declarations](https://i.imgur.com/zRKj6vL.png)
<br>
![Function Expression](https://i.imgur.com/noKYoHi.png)
<br>
![Functions Calling Other Functions](https://i.imgur.com/YT0TwRi.png)

Attempt #1 at the Coding Challenge:

![Attempt1](https://i.imgur.com/p421OMy.png)

Attempt #2 at the Coding Challenge:
![Attempt2](https://i.imgur.com/l437WMp.png)