# #100DaysOfCode Log

## Day 18: Thursday, August 11, 2022

<hr>

**Today's Progress**:

Refactored last nights JavaScript to this:

```javascript
async function getGenre() {
  let response = await fetch(
    "https://binaryjazz.us/wp-json/genrenator/v1/genre/25"
  );
  let data = await response.json();

  const html = data.map(renderToHTML).join("");
  document.querySelector("#app").innerHTML = html;

  return data;
}

getGenre().then((data) => console.log(data));

const renderToHTML = (genre) => {
  return `<p>Genre: ${genre}</p>`;
};
```

I created a function `renderToHTML(genre)` so that it can be reused in the code and then called it inside of my async `.map()` to render the data. It worked! I didn't understand it at first so I had to ask questions about it.

Today's task:

- Play around with Firebase Auth
- Create a Login / Signup Flow
- Connect it with Firebase
- Sign Up and Login a user in the UI.

So it was A LOT. It's 2:05AM and I JUST finished. I definitely need to manage my time better but I got the login/signup/logout flow working. It's not perfect but the code can be reviewed here:

[github](https://github.com/zahrakhadijha/firebase-auth/pull/6)

My brain is mush now so I'll expand on some of my learnings tomorrow because I'll be doing a code review with my mentor on it. And right now I'm using the static firebase for Web - I may implement webpack for this.
