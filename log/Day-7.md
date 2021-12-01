# #100DaysOfCode Log

## Day 7: November 30, 2021

**Today's Progress**:
Learned about Operator Precedence and I think it's really interesting (my next blog post topic!!!) But I also didn't quite understand it fully. Like I get it but I think I need to write more ~ math ~ that have examples with it so I can see how it fully works.

And then I did Challenge #1 in The Complete JavaScript Course by Jonas Schmedtmann. I implemented the code correctly so that's a plus!

**Thoughts**:
So obviously this JavaScript section is review for me. Yes, there is ALWAYS something new to learn, which is why I'm going to dig deeper into Operator Precedence and write about it.

Here was the coding challenge solution that I wrote:

**CHALLENGE # 1**

Mark and John are trying to compare their BMI (Body Mass Index), which is calculated using the formula:
BMI = mass / height ** 2 = mass / (height * height) (mass in kg and height in meter).
Your tasks:
1. StoreMark's and John's mass and height in variables
2. Calculate both their BMIs using the formula (you can even implement both versions)
3. Createa Boolean variable 'markHigherBMI' containing information about whether Mark has a higher BMI than John.

Test data:
Data 1: Marks weights 78 kg and is 1.69 m tall. John weights 92 kg and is 1.95 m tall.
Data 2: Marks weights 95 kg and is 1.88 m tall. John weights 85 kg and is 1.76 m tall.

Data 1:
```
let markMass = 78
const markHeight = 1.69
let johnMass = 92
const johnHeight = 1.95
```
Data 2:
```
let markMass = 95
const markHeight = 1.88
let johnMass = 85
const johnHeight = 1.76
```

Solution:
```
const markBMI = markMass / markHeight ** 2
console.log(markBMI)

const johnBMI = johnMass / johnHeight ** 2
console.log(johnBMI)

let markHigherBMI = markBMI > johnBMI
console.log(markHigherBMI)
```

I just commented out the data # 1 when I wanted to test data # 2.

Now time for bed, I'm SLEEPY.