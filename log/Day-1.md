# #100DaysOfCode Log

## Day 1: Thursday, November 30, 2023

<hr>

**Today's Progress**:

Reviewed Big O Notation. Big O Notation is a comparison between algorithms that determines which one is the "best" one. But how do we measure which algorithm is the best one?

It's based on Time Complexity and Space Complexity.

Time complexity isn't measured in seconds or minutes, it's measured by the number of operations the code has. The reason for this is — different machines might run the algorithm slower or faster but the number of operations in the code remain constant.

For example:

```
function addUpTo(n) {
    return n * (n + 1) / 2
}
```

This function has `1 division`, `1 addition`, `1 multiplication` in total 3 operations. So no matter how big `n` is - the operations remain 3. The computer will have to only perform 3 operations for this problem.

But if you have this problem

```
function addUpTo(n) {
    let total = 0;
    for (let i = 1; i <= n; i++) {
        total += 1l
    }
    return total;
}
```

With this one - since it's a `for loop`, depending on what `n` is, the number of operations can be as low as `2n` or as high as `5n + 2` but the thing is that they will grow as `n` grows. The `for loop` will run as many times as `n` will run which will make the number of operations...A LOT. Which would make this solution inefficient.

Performance matters when you're dealing with big datasets so Big O Notation is important.
