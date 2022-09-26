# #100DaysOfCode Log

## Day 17: August 10, 2022

<hr>

**Today's Progress**:

Had a bit of a rough day but here we are still showing up. I'm so lucky to have mentors in the industry. Today - I didn't continue the `localStorage` task. Instead - I worked on somethihng compeletly different, to practice consuming API's and getting comfortable with fetching them.

The task was to consume a public API, display the API response and then render it on the screen. I didn't have to worry about styling anything today, just making sure the functionality works. So initially I was going to use the Spotify API but it requires `OAuth` so I decided against it (for now) and do something simpler. I found a funky cute API called [Binary Jazz](https://binaryjazz.us/genrenator-api/) which displays funky genres of music. This API actually uses Spotify's database to discover random genre's of music and stories of the genres.

I decided to practice my API fetching skills by using the genre API. It generates an array of genres of random music. And the task was to render it on the screen and create a button that the user can click to generate a new set of random genres each time they click it.

This is the code I wrote, it's simple but it works!

`index.html`

```javascript
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>echo</title>
  </head>
  <body>
    <h1>echo</h1>
    <div id="app"></div>
    <button id="btn" onclick="getGenre()">Refresh</button>

    <script src="app.js"></script>
  </body>
</html>
```

`app.js`

```javascript
async function getGenre() {
  let response = await fetch(
    "https://binaryjazz.us/wp-json/genrenator/v1/genre/25"
  );
  let data = await response.json();

  const html = data
    .map((genre) => {
      return `<p>Genre: ${genre}</p>`;
    })
    .join("");
  console.log(html);

  document.querySelector("#app").innerHTML = html;

  return data;
}

getGenre().then((data) => console.log(data));
```

I did the `DOM Manipulation` inside of the async function but was given feedback to create a separate function for it so it's reuseable. So that's what I'm going to work on tomorrow!

So with the `async` function `getGenre()` I fetched the genre `API` with an array of 25 random genres.

```javascript
let response = await fetch(
  "https://binaryjazz.us/wp-json/genrenator/v1/genre/25"
);
let data = await response.json();
return data;

getGenre().then((data) => console.log(data));
```

The `response` fetches the API while `data` gets the response in a json() format. (I THINK????) Need to review the details. And then I returned the `data` and called the function. I used my `console` to see if the data was being fetched. AND IT WAS:

![img](https://i.imgur.com/cvRnDSg.png)

I could see the genres displayed in my console. So then I had to figure out a way to actually render them on the screen in my `HTML`.

So I initialized a variable `let html` and used `.map()` to loop over the array of genres. Initially I used a `for loop` and although it displayed the array in my console, it wouldn't render on the screen, so I decided to use `.map()` and it worked. Not sure why, I have to review this with someone and I'm not super comfortable using `.map()` yet but it worked so here we are.

So I wrote this code inside of the `async` function:

```javascript
const html = data
  .map((genre) => {
    return `<p>Genre: ${genre}</p>`;
  })
  .join("");
console.log(html);

document.querySelector("#app").innerHTML = html;
```

Which loops through the array of genres, called `data` and then returns a string `<p>Genre: ${genre}</p>` in a `<p>` tag. And then I added `.join("")` at the end because it was printing out the commas that it shouldn't have. I logged it to the console and I was getting the data I needed as a string:

![data](https://i.imgur.com/6mtSir6.png)

SO NOW to insert it into my HTML. This is obviously easier with React. I haven't had much practice doing it strictly with vanilla javascript so it's good I got to do this.

I used DOM manipulation:

```javascript
document.querySelector("#app").innerHTML = html;
```

I created a `div` with the `id` of `#app` in my html and decided to select that and insert the `innerHTML` and it worked!

![app](https://i.imgur.com/scQZe7l.png)

So the next step was to create a button that refreshes the page with a new set of genres everytime you click it.

The html looked like this:

```javascript
// html
<button id="btn" onclick="getGenre()">
  Refresh
</button>
```

I used the `getGenre()` function onclick so that everytime the user clicks the button, it gave you a new set of genres. So that WORKED.

Here is the [github](https://github.com/zahrakhadijha/echo) repo for it.

It felt good to solve this on my own - with obviously the help of google. 😬
