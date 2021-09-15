# #100DaysOfCode Log

## Day 4: Monday, September 13, 2021

**Today's Progress**:

I dove deeper into what the Critical Rendering Path is and what it does/how it works. It's really interesting stuff. I watched this [video](https://www.youtube.com/watch?v=PkOBnYxqj3k&t=2067s) and it was added knowledge to the two lectures I had watched earlier about how web pages are rendered.

While those other lectures were more high-level stuff, this one went into detail specifically on the rendering engine. The basic Rendering Engine flow is `Parsing --> Render Tree --> Layout --> Paint`

How the Parser works is important. The tree looks like: `Bytes --> Characters --> Tokens --> Nodes --> DOM` and HTML5 is received incrementally when a web page runs because this allows the browsers to fetch the CSS while it's loading up the HTML. The information arrives in packets/chunks (HTML bytes) while it gives the illusion that the web page is loading within nanoseconds.

What I thought was interesting and didn't know about is that Tokens are the HTML tags. So example, let's say we have HTML code that looks like:

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>WEB  PERFORMANCE</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>

  <h1>Hello World!</h1>
  <p>My name is <span>Zahra</span>

	<script src="index.js"></script>
  </body>
</html>
```

The token would be:

- `Start Tag: h1`
- `Hello` (string)
- `World` (string)
- `Start Tag: p`
- `My name is` (string)
- `Start Tag: span`
- `Zahra` (string)

And these would become nodes which is how the DOM tree would be constructed incrementally.

**The first packet:**

```
<!DOCTYPE html>
<html lang="en">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
```

**The second packet**

```
<link rel="stylesheet" href="style.css">
```

**The third packet**

```
<h1>Hello World!</h1>
<p>My name is <span>Zahra</span>
```

So this arrives in chunks. Unlike HTML parsing though, CSS is **not** incremental. The styling would come at once so breaking up styles in smaller files is good for performance rather than adding everything in a `styles.css`

There's SO much to learn! I'm excited to continue learning about this topic. I'm going to construct a blog post about everything I'd learn/gathered from watching those lectures.
