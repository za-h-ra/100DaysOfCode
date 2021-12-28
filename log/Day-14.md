# #100DaysOfCode Log

## Day 14: December 27, 2021

**Today's Progress**:

Reviewed Objects in JavaScript today. I completed lectures

- Introduction to Objects
- Dot vs. Bracket Notation

Objects are THE most important data structure of JavaScript. It holds so much information. So it was a nice review of the concept and then I did the lecture exercises by creating objects and accessing the `key:value` pairs.

I definitely like the dot notation better than the bracket notation - I wonder if that's just a personal preference. But I didn't spend too long today as I'm a bit tired.

Here is the exercise on writing objects:

```javascript
const myCountry = {
  country: 'Argentina',
  capital: 'Buenos Aires',
  language: 'Spanish',
  population: 45.38,
  neighbors: ['Chile', 'Venezuela', 'Uruguay'],
}

console.log(myCountry.capital)
console.log(myCountry['population'])

console.log(
  `${myCountry.country} has ${myCountry.population} million ${myCountry.language} speaking people, ${myCountry.neighbors.length} neighboring countries and a capital called ${myCountry.capital}.`
)

myCountry.population += 2
myCountry['population'] -= 2
```

I can't wait to start learning how to properly use them in a real application because I think that's where my knowledge lacks. I also want to use this knowledge to solve Data Structures & Algorithm exercises.

I also published a blog post on creating aliases which can be found [here](https://blog.zahrakhadijha.com/how-to-create-aliases-on-macos-with-terminal). So I guess today was a productive day! I think my favorite part of writing blog posts is creating the little graphics for the post. lol. But nonetheless, creating aliases was intimidating to me at some point and this blog post is just a reference for myself whenever I need to write them. 
