# #100DaysOfCode Log

## Day 7: December 7, 2020

<br>

**Today's Progress**: I feel like I didn't work on much today but in actuality, I started working on a project and spent a few hours being stuck on how to create an animation for my heading text. 

I'm creating and building a landing page that leads people to a form that collects data. I had an idea to use both my passion for design and development and send out post cards to my friends! But to collect their addresses, I want to create a small website for them to do it because

1. This will help me with form validation
2. I want to see if I can export the information and then spread some art into the world.

So I spent a few hours being stuck on trying to figure how to animate every single letter for my hero text. I wanted each letter to appear one by one slowly onto the page.

I tried using ```@keyframes``` at first and changed the opacity. And then I realized you needed to add a ```span``` tag to EACH letter. I did that and felt like it was too much so I started googling a simpler way to do this with Javascript. AAANNNDDD I found a way! But I was hoping to not follow tutorials and get comfortable doing it on my own but I ended up watching [Dev Ed](https://www.youtube.com/channel/UClb90NQQcskPUGDIXsQEz5Q)'s channel on how to add a ```span``` tag to my ```h1``` text one by one. Even though I followed a tutorial, I learned that there is a way to do this and a way to animate text by using Javascript & CSS. 

This was the code:

```
const heading = document.querySelector('.primary-title')
const text = heading.textContent
const splitText = text.split('')

heading.textContent = '' // avoid repeating

for (let i = 0; i < splitText.length; i++) {
	heading.innerHTML += '<span>' + splitText[i] + '</span>'
}

let char = 0
let timer = setInterval(onTick, 50)

function onTick() {
	const span = heading.querySelectorAll('span')[char]
	span.classList.add('fade')
	char++
	if (char === splitText.length) {
		complete()
		return
	}
}

function complete() {
    clearInterval(timer)
    timer = null
}
```

and then my CSS

```
.primary-title {
	font-family: 'Homemade Apple', cursive;
	color: var(--heading-text-color);
}

span {
	opacity: 0;
	transition: all 1s ease;
}

span.fade {
	opacity: 1;
}
```

But now I just want to scratch it and start over with something else...

**Links**: What the landing page looks like so far

![](https://i.imgur.com/q9qyut0.gif)