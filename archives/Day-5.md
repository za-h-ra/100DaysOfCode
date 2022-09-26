# #100DaysOfCode Log

## Day 5: Wednesday, June 29, 2022

<hr>

**Today's Progress**:

Did a small lesson today on Type Conversion vs. Coercion. I wrote a blog post about this a while ago but it's easy to get confused with this topic. So I did some exercises and figured out what the result was for each:

```javascript
console.log("9" - "5");
console.log("19" - "13" + "17");
console.log("19" - "13" + 17);
console.log("123" < 57);
console.log(5 + 6 + "4" + 9 - 4 - 2);
```

`"9" - "5"` is equal to `4` because javascript automatically subtracts the integers even if they are a `string`.

`"19" - "13" + "17"` is equal to `617` because javascript will run from left to right, subtracting `19 - 13` first and then it will concatenate the "17" as a string, resulting in the `617` being a `string`.

`"19" - "13" + 17` is equal to `23` because this will just be a mathematical equation. Javascript will subtract the first two integers and then it will add `17` because `17` is a number, not a string.

`"123" < 57` is false. I have to review this once more but does Javascript think that `123` is an integer and that's why it's actually comparing the two values?

`5 + 6 + "4" + 9 - 4 - 2` is equal to `1143`. Crazy right?! It's because Javascript will add `5 + 6` which is `11` and then it will concatenate `4` to `11` making it `114` and now that `114` is a string, the `9` will actually be concatenated to `114` making it `1149`. After that, `1149` will actually be subtracted as an integer, so `1149 - 4` is `1145` and then `- 2` is `1143` making it an integer again. WHAT AN EXPLANATION.

You can also turn a string into a number by using the `Number()` function.
