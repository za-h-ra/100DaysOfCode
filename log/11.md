# #100DaysOfCode Log

## Day 11: December 12, 2020

<br>

**Today's Progress**: I played around with React today via
[this](https://dev.to/aspittel/a-complete-beginners-guide-to-react-2cl6). I
wanted to give it a shot because this article/tutorial was something we were
given at General Assembly to do and I didn't fully grasp it at the time so I
wanted to review it. However, I decided NOT to play around with React via
Codepen because I'm already familiar with how to use it.

I wanted to follow this tutorial but build the
[Facebook Status Widget](https://github.com/zahrakhadijha/facebook-status-widget)
on VSCode and upload the code on Github.

So I created a repo in Github, called it **facebook-status-widget** and updated
the README.

The next thing I did was install `npx create-react-app my-app` and deleted all
the unnecessary files from my react app. I followed the tutorial and it
indicated that there were going to be four components. I create a `Status`
component, `Like`, `LikeIcon` and `Comment` component.

```
src
|__ Components/
    |__Status.jsx
    |__Comment.jsx
    |__Like.jsx
    |__LikeIcon.jsx
|__ App.js
|__ App.css
|__ App.test.js
|__ index.css
|__ index.js
|__ logo.svg
|__ reportWebVitals.js
|__ setupTests.js
```

I also created a `HelloWorld` component to test out to see if my `App.js` was
working correctly and imported it into the file.

Now, just a reminder, this is me just refreshing my knowledge on how React works because I haven't used it in 3 months since I graduated from General Assembly. So I coded in the boilerplate for the components. The ```Status``` component is the main component that was going to be in the app and the rest of them are subcomponents. 

I imported the ```Status``` component into my ```App.js``` file. And then I imported the ```Comment``` component into the ```Status``` component. 

After that, I installed the ```FontAwesome``` library because I knew I needed to use it in my ```LikeIcon``` and ```Like``` component. I went into the [Font Awesome](https://fontawesome.com/how-to-use/on-the-web/using-with/react) documentation and installed the library. 

Is it smarter to install libraries before even starting the project? I have a feeling it broke my application.

Next, I went to write the code into the ```LikeIcon``` Component and as I imported into my ```Status``` component, I kept getting the following error:

![](https://i.imgur.com/MrbCScf.png)

After playing around with it for about an hourish, trying to figure out where I was going wrong. I decided to stop. My ```Like``` component wasn't importing either, giving me the same error. I tried:

1. Checking if my ```index.js``` file was working.
2. Checked the boilerplate for my ```App.js``` file but the error seemed to be in ```index.js```. I'm not really sure what ```reportWebVitals.js``` is but I don't think it has anything to do with it because my other components worked fine.

I looked at my previous React projects and they looked fine and my folder architecture was correct, too. So I'm not sure what happened!

I deleted the entire react app and decided to watch Andrei Neogie's React course on Basic React Concepts. He went over how React works, what Babel and Webpack do and how it works with the DOM. I had gaps in my knowledge so it helped.

I reinstalled ```npx create-react-app facebook-widget``` and followed along with SOME of the tutorial on the videos. They are building a Rolodex project but I want to learn to build the Facebook widget so I'll use the tutorial to do that.

And then I stopped because I wanted to spend time with my boyfriend and cook dinner 🍔🍲

**Thoughts**: I left FRUSTRATED. I'll attack this tomorrow. 

