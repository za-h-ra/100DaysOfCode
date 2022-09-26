# #100DaysOfCode Log

## Day 15: Saturday, August 6, 2022

<hr>

**Today's Progress**:

It's already August, holy wow. Finished up my last day at BlockFi on Friday and that felt weird. It's weird to be not working again...but I know I have a hell lot of work and studying ahead to land a job.

So today I worked on the following lessons:

- Project #1: Guess My Number!
- What's the DOM and DOM Manipulation
- Selecting and Manipulating Elements
- Handling Click Events
- Implementing Game Logic
- Manipulating CSS Styles
- Challenge #1

DOM Manipulation has come up quite a bit in some of my interviews - so I figured I'd practice! This subject used to be SO scary to me, but now, I'm able to google things that I can't remember and implement what I need. So I'm excited to build something of my own towards the end of this.

The interface that I worked on during these lessons was this:

![](https://i.imgur.com/v342r40.png)

Where I had to manipulate the `input` field, the `score`, the `start guessing...` message, and the `?` box, as well as the background.

I don't like DOM manipulation because the code can get so messy. But here is the code I wrote:

```javascript
let score = 20;
let secretNumber = Math.trunc(Math.random() * 20) + 1;
let message = document.querySelector(".message");
let scoreContent = document.querySelector(".score");
let numberBox = document.querySelector(".number");
let guess = document.querySelector(".guess");
let background = document.querySelector("body");

let x = Math.trunc(Math.random() * 256);
let y = Math.trunc(Math.random() * 256);
let z = Math.trunc(Math.random() * 256);
let bgColor = `rgb(${x}, ${y}, ${z})`;

let check = document.querySelector(".check");
let reset = document.querySelector(".again");

check.addEventListener("click", () => {
  let guess = Number(document.querySelector(".guess").value);
  if (!guess) {
    message.textContent = "No number! 😕";
  } else if (guess === secretNumber) {
    message.textContent = "Correct Number! ✨";
    background.style.backgroundColor = bgColor;
    numberBox.textContent = secretNumber;
    numberBox.style.width = "30rem";
  } else if (guess > secretNumber) {
    if (score > 1) {
      message.textContent = "Too high!";
      score--;
      scoreContent.textContent = score;
    } else {
      message.textContent = "You lost the game!";
      scoreContent.textContent = 0;
    }
  } else if (guess < secretNumber) {
    if (score > 1) {
      message.textContent = "Too low!";
      score--;
      scoreContent.textContent = score;
    } else {
      message.textContent = "You lost the game!";
      scoreContent.textContent = 0;
    }
  }
});

// reset the functionality for the game

reset.addEventListener("click", () => {
  score = 20;
  secretNumber = Math.trunc(Math.random() * 20) + 1;
  message.textContent = "Start guessing...";
  scoreContent.textContent = score;
  numberBox.textContent = "?";
  guess.value = "";
  background = "#222";
  numberBox.style.width = "15rem";
});
```

This has been VERY slightly refactors. More to come. But I decided to initialize all the variables at the top to make the code more readable and keep it DRY. We wanted to keep the score at 20 so we stored it in a variable, declaring it as the `state` of the game. And then we created a `secretNumber` variable and stored a randomly generated number to it that we'll be using.

So one thing I had trouble understand was this - I declared the input value of

```javascript
let guess = document.querySelector(".guess").value;
```

And then wanted to declare it in the game as

```javascript
guess = Number(guess);

// OR

guess = Number(guess.value);
```

but the input kept popping up as `0` which I didn't understand. The `Number()` function is still converting the value to a `type Number` so I didn't quite understand why it didn't work, or let me reset the variable. Guess something I have to ask a senior engineer. So I'll provide an answer for this in a few days.

When I created the reset event listener, the `guess` worked perfectly fine. So strange.

The course didn't do this but I wanted to randomly generate a background color for when the user gets the right number. So I created three variables for RGB(X,Y,Z) as such:

```javascript
let x = Math.trunc(Math.random() * 256);
let y = Math.trunc(Math.random() * 256);
let z = Math.trunc(Math.random() * 256);
let bgColor = `rgb(${x}, ${y}, ${z})`;
```

and it worked perfectly when resetting the background. Yay! Now the color of the background is different each time the user wins. I'm gonna add a little something that when the user loses, the entire background turns into a skull. lol

But DOM manipulation is somewhat fun. I think I'm starting to appreciate it.
