# #100DaysOfCode Log

## Day 1: Monday, September 26, 2022

<hr>

**Today's Progress**:

Course: [JavaScript Algorithms and Data Structures Masterclass](https://www.udemy.com/course/js-algorithms-and-data-structures-masterclass/) by Colt Steele
Lecture: Analyzing Performance of Arrays and Objects (Section 3)

Listened through section 3 and learned the Big O of Objects and Arrays and the Big O of the methods.

`Objects` are unordered data structures of `key:value` pairs so we use them when we don't need our data to be ordered.

**Big O of Objects**

```javascript
-Insertion - O(1) - Removal - O(1) - Searching - O(N) - Access - O(1);
```

Insertion, removal, and access are constant time because it doesn't matter how big the input is - inserting a key:value pair, or removing it or accessing it is just one simple task.

But searching is O(N) time because in order to search through an object, JavaScript will (behind-the-scenes) go through the entire object to see if the given piece of information exists in a key or value. It has to go through the the data one-by-one to search for the value. Therefore, it's linear time, O(N). As the keys increase, the bigger the object is, the longer it will take to search through it.

`Arrays` are ordered lists! But I learned that arrays come at a cost, therefore, not very efficient to use. So if you don't need to order your data, you won't need to use an array. For optimized performance, there are other ways to store ordered data - arrays are just the free one. (I have yet to learn about the other ones).

**Big O of Arrays**

```javascript
- Insertion — it depends
- Removal - it depends
- Search - O(N)
- Access - O(1)
```

The Big O of Insertion and Removal depend on _where_ in the array we are inserting/removing elements from.

If you are inserting/removing an element from the **end of an array** the Big O will be `O(1)` because we don't care about the size of the array. We are simply adding or removing an index from the end of an array without disrupting the rest of the array.

If you are inserting/removing an element from the **beginning of an array**, the Big O is `O(N)` because! when you add an element to the beginning of an array, it assumes the index of `0`, meaning, the rest of the elements now have to be moved _one-by-one_ to the next/previous index.

For example: if we have an array

```javascript
let spotifyFavs = ["Lane 8", "ODESZA", "Big Wild", "Tep No", "Washed Out"];
```

And we remove the first element `"Lane 8"`, which is at `index 0`, we will now need to assign `"ODESZA"` which is at `index 1` to `index 0` to replace the removal of `"Lane 8"`, and so on with the rest of the elements that will now have a new index. (I hope this makes sense! It's easier to explain with a drawing!)

But the same thing happens when we add a new item to the beginning of the array. If I added, say, `"Jamie xx"` to my `spotifyFavs` array, to the beginning, our array would NOW look like:

```javascript
let spotifyFavs = [
  "Jamie xx",
  "Lane 8",
  "ODESZA",
  "Big Wild",
  "Tep No",
  "Washed Out",
];
```

With `"Jamie xx"` at `index 0` and the rest of the elements moved over and assigned a new index.

So we learn that arrays can be costly and problematic.

**Big O of Array Methods**

```javascript
- push() - O(1)
- pop() - O(1)
- shift() - O(N)
- unshift() - O(N)
- concat()- O(N)
- slice() - O(N)
- splice() - O(N)
- sort() - O(N * log N)
- forEach() / map() / filter() = O(N)

```

I can't explain why `sort()` is `O(N * log N)` yet because I have to learn it but the rest of the methods that are `O(N)` are because they care about the size of the array. As the number of elements increase, the time to use some of these methods increases as well.
