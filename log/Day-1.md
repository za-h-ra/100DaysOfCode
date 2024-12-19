# #100DaysOfCode Log

## Day 1: Wednesday, December 18, 2024

**Today's Progress**:

I've been out of the "coding for fun after work" habit for quite some time. It's made me feel extremely stagnant in my career. So I wanted to start up again. And also because I'd really love a job in New York City at a hybrid company.

So today, I started off with 30 minutes of learning about Big O Notation. I'll continue the rest of the section tomorrow.

**Big O** is pretty much classifying and comparing the efficiency of code. The official definitely is that it is a way to formalize fuzzy counting. It allows us to talk formally about how the runtime of an algorithm grows as the input grows.

We use Big O to measure which code is "better." In this case, better has a focus on which code is FAST. So we focus on speed.

Writing good and efficient code that doesn't take up a ton of memory.

Some examples:

```javascript

function addUpTo(n) {
    let total = 0; // 1 assignment
        for (let i = 1; i <= n; i++>) {
            // 1 assignment
            // n comparisons
            // n additions & n assignments which happen 1 time each per n.
            total += i; // n additions
        }
    return total;
}

```

For this algorithm, the runtime would be `O(n)` because regardless of the exact number, the # of operations grows proportionally with N. If I were to have an input of `addUpTo(60)`, `N` would grow as many times as the number and the loop would run 60 times.

Whereas, we have the same problem solved differently, more efficiently.

```javascript
function addUpTo(n) {
  return (n * (n + 1)) / 2;
}

// 1 multiplication
// 1 addition
// 1 division
```

There are 3 operations. So no matter what, if `addUpTo(60)` is the input, there will always be 3 operations no matter the size of `N`. So it's efficient because it's constant. The runtime is `O(1)`.

I'll re-explain these concepts once I get futher into the course.
