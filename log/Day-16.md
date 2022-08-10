# #100DaysOfCode Log

## Day 16: August 8, 2022

<hr>

**Today's Progress**:

I forgot to log Day 16! So here it is! Things took an interesting turn. I completed some lessons in Jonas' course:

- Implementing Highscores
- Refactoring Our Code: The DRY Principle

But throughout these lessons, I kind of wanting to just implement the code myself so I gave myself that challenge. Before moving onto Project #2 - I wanted to figure out how to use `localStorage` to store the highscores.

So this was the challenge - because it's not me following a tutorial but implementing my own solutions. So first, let's start with the refactoring - I refactored the code to make it look/function better.

```javascript
let score = 20;
let highscore = 0;
let highscoreContent = document.querySelector(".highscore");
let secretNumber = Math.trunc(Math.random() * 20) + 1;
let guessRef = document.querySelector(".guess");
let check = document.querySelector(".check");
let reset = document.querySelector(".again");

const displayMessage = (message) => {
  document.querySelector(".message").textContent = message;
};

const displayScore = (message) => {
  document.querySelector(".score").textContent = message;
};

const displayNum = (num, style) => {
  let selector = document.querySelector(".number");
  selector.textContent = num;
  selector.style.width = style;
};

const bgColor = (color) => {
  document.querySelector("body").style.backgroundColor = color;
};

const getBgColor = () => {
  let x = Math.trunc(Math.random() * 256);
  let y = Math.trunc(Math.random() * 256);
  let z = Math.trunc(Math.random() * 256);
  return `rgb(${x}, ${y}, ${z})`;
};
```

I think there's still some refactoring to do with the variables at the top. But I created functions for code that was reused all over the place. I tried to create a function for `secretNumber`:

```javascript
let secretNumber = Math.trunc(Math.random() * 20) + 1;

const secretNum = () => {
  return Math.trunc(Math.random() * 20) + 1;
};
```

But I was having issues because everytime I use the function, it generates a new random number whereas the `secretNumber` variable doesn't do that if I place it all over the place. So I definitely have to figure that one out.

BUT I did figure out the issue I was having previously on why my `guess` wasn't working inside of the click event. JavaScript does funky things within the global scope vs. inside of a function so because `guess` was declared outside of the global scope, it would reset to an empty value because of that. But since I wanted it to hold the guess at each click, I'd have to declare it inside of the click event. So I figured it out.

It makes sense.

I think this function could be refactored differently but I'm not sure how yet so I did it the best way I know how:

```javascript
const displayNum = (num, style) => {
  let selector = document.querySelector(".number");
  selector.textContent = num;
  selector.style.width = style;
};
```

It's used for two different use-cases.

The entire code for the game so far looks like this now:

```javascript
let score = 20;
let highscore = 0;
let highscoreContent = document.querySelector(".highscore");
let secretNumber = Math.trunc(Math.random() * 20) + 1;
let guessRef = document.querySelector(".guess");
let check = document.querySelector(".check");
let reset = document.querySelector(".again");

const displayMessage = (message) => {
  document.querySelector(".message").textContent = message;
};

const displayScore = (message) => {
  document.querySelector(".score").textContent = message;
};

const displayNum = (num, style) => {
  let selector = document.querySelector(".number");
  selector.textContent = num;
  selector.style.width = style;
};

const bgColor = (color) => {
  document.querySelector("body").style.backgroundColor = color;
};

const getBgColor = () => {
  let x = Math.trunc(Math.random() * 256);
  let y = Math.trunc(Math.random() * 256);
  let z = Math.trunc(Math.random() * 256);
  return `rgb(${x}, ${y}, ${z})`;
};

check.addEventListener("click", () => {
  let guess = Number(guessRef.value);
  if (!guess) {
    displayMessage("No number! 😕");
  } else if (guess === secretNumber) {
    displayMessage("Correct Number! ✨");
    bgColor(getBgColor());
    displayNum(secretNumber, "30rem");

    if (score > highscore) {
      highscore = score;
      highscoreContent.textContent = highscore;
    }
  } else if (guess !== secretNumber) {
    if (score > 1) {
      displayMessage(guess > secretNumber ? "Too high!" : "Too Low!");
      score--;
      displayScore(score);
    } else {
      displayMessage("You lost the game!");
      displayScore(0);
    }
  }
});

// reset the functionality for the game

reset.addEventListener("click", () => {
  score = 20;
  secretNumber = Math.trunc(Math.random() * 20) + 1;
  displayMessage("Start guessing...");
  displayScore(score);
  guessRef.value = "";
  bgColor("#222");
  displayNum("?", "15rem");
});
```

But I want to store the highscore in `localStorage` so I'm still figuring THAT out. Initially, I did it this way:

```javascript
const storedData = localStorage.getItem("scoreData");

localStorage.setItem("scoreData", highscoreContent.textContent);
```

I put it inside of the conditional

```javascript
if (score > highscore) {
  highscore = score;
  highscoreContent.textContent = highscore;
  localStorage.setItem("scoreData", highscoreContent.textContent);
}
```

Like that - and yes, it DID store the score in localStorage but I strugged to actually get the data and have it render on the page and it stay there if I refreshed the page.

So that's something I have to figure out. But its exciting because it's a solution I may want to vs someone telling me to solve it. There was an article I read that maybe I need to store all the scores inside of an array and then compare and sort them and print out the highest one. So I'm going to try it and see if that works.
