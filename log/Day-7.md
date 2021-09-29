# #100DaysOfCode Log

## Day 7: Tuesday, September 28, 2021

**Today's Progress**:

This weekend, I published the article on How Browsers Render a Website ([see link!](https://blog.zahrakhadijha.com/how-browsers-work-to-render-websites)). What I learned from this topic is how to write performant code and it made me realize why my portfolio site is slow 😅 so that's definitely something to work on.

Today I started up The Complete JavaScript Course 2021 by Jonas Schmedtmann. This course has incredible explanations and exercises of how JavaScript works. I started it a while ago but I never finished it so I'm picking up from where I left off. If I could focus on ONE course instead of context switching, that would help solidify my knowledge better.

So the two JavaScript things I'll be focusing on for the next three weeks are:

- The Complete JavaScript Course 2021 by Jonas Schmedtmann
- [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS/blob/1st-ed/up%20%26%20going/ch1.md) - Up & Going

**Thoughts:**

Reviewed truthy and falsy values, equality operators (`===` vs `==`) and Boolean Logic.

There are five falsy values:

1. `0`
2. `undefined`
3. `''`
4. `NaN`
5. `null`

So if you have a conditional statement that goes something like:

```
const peaches = 0

if(peaches) {
  console.log('I love a good peach!🍑')
} else {
  console.log('You need to buy some peaches!')
}

```

It assumes `0` to be a falsy value, therefore, it will print out `"You need to buy some peaches!`

The same thing will happen if I change the situation to

```
let peaches;
if(peaches) console.log('I love a good peach!🍑')
```

It will print out `undefined` because the variable `peaches` is literally undefined. Same thing would happen if `let peach = ''` an empty string would result in a falsy undefined value.

And then I reviewed the strict equal operator vs. the loose equal operator. Obviously it's always good practice to use `===` than `==` and I actually haven't seen the second option being used professionally. The difference between the two is:

1. `===`

```
let cats = '2'
if(cats === 2){
  console.log('I have cats!')
} else {
  console.log('I want cats 🥺')
}
```

This will print out false and the string `'I want cats 🥺'`

2. `==`

```
let cats = '2'
if(cats == 2){
  console.log('I have cats!')
} else {
  console.log('I want cats 🥺')
}
```

This will print out true and the string `'I have cats!'`

The `==` is not strict and will think that a string 2 is the same as the number 2. But the `===` is more strict and is able to tell the difference between the two values.
