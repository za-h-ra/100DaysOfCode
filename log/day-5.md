# #100DaysOfCode Log

## Day 5: December 5, 2020

<br>

**Today's Progress**: Today, I kept it light but I reviewed topics on
`for loops`, `nested for loops` and the `while loop` and completed the
assignments from Jonas' lectures. I also learned to loop backwards, which I
don't think I've learned before.

But the one great thing I can say about this course and learning in small
increments is that the knowledge is sticking. I also understand why certain
things are done the way they are. I didn't really understand nested for loops
before but one of Jonas' exercises was to create a nested for loop like this:

```
for (let exercise = 1; exercise < 4; exercise++) {
    console.log(`------Starting exercise ${exercise}`)

    for (let rep = 1; rep < 6; rep++) {
        console.log(`Exercise: ${exercise}: Lifting weights repetition ${rep} 🏋🏼‍♂️`)
    }
}
```

And I understood it better this way because I was able to visually see what it
was doing. I know I'm a visual learner and I have to see how things work so I
though that was cool.

I also had to do the following exercise and I think I misread it, but the
solution to it was MUCH simpler than I thought.

![Loop Exercise](https://i.imgur.com/miXtZ01.png)

The exercise asked to log **only** the neighboring countries and one of the
arrays didn't have a neighboring country. So I got stuck a little bit trying to
access an array within an array within a nested loop and how to create a
conditional that **ONLY** logs the countries with neighbors. My solution looked
like this:

```
const listOfNeighbors = [
    ['Canada', 'Mexico'],
    ['Spain'],
    ['Norway', 'Sweden', 'Russia']
]

for (let i = 0; i <= listOfNeighbors.length -1; i++) {

    for (let j = 0; j <= listOfNeighbors[i].length - 1; j++) {
        if (listOfNeighbors[i].length === 1) continue
            console.log(`Neighbor: ${listOfNeighbors[i][j]}`)
    }
}

```

but the actual solution was to just log each item in the nested array,
individually. Which I knew how to do! So the solution was:

```
for (let i = 0; i < listOfNeighbors.length; i++) {
    for (let j = 0; j < listOfNeighbors[i].length; j++) {
        console.log(`Neighor: ${listOfNeighbors[i][j]}`)
    }
}
```

It was a very "OH!" moment.

I don't like while loops much but I know I need to practice them a bit more. So
until tomorrow...

I'll complete a full challenge tomorrow and we'll see how that goes.
