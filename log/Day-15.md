# #100DaysOfCode Log

## Day 15: December 29, 2021

**Today's Progress**:

I forgot to write my github log on this day BUT. I completed the lecture on Object Method, which was an explanation of how you can access values in an object. It was pretty straight forward. So I completed the lesson with some exercises and Challenge #3. 

This was my solution:

```javascript
const mark = {
  firstName: 'Mark',
  lastName: 'Miller',
  mass: 78,
  height: 1.69,
  calcBMI: function () {
    this.BMI = this.mass / this.height ** 2
    return this.BMI
  },
}

const john = {
  firstName: 'John',
  lastName: 'Smith',
  mass: 92,
  height: 1.95,
  calcBMI: function () {
    this.BMI = this.mass / this.height ** 2
    return this.BMI
  },
}

if (mark.calcBMI() > john.calcBMI()) {
  console.log(`${mark.firstName}'s BMI (${mark.BMI}) is higher than ${john.firstName}'s (${john.BMI})`)
} else if (john.calcBMI() > mark.calcBMI()) {
  console.log(`${john.firstName}'s BMI (${john.BMI}) is higher than ${mark.firstName}'s (${mark.BMI})`)
}

```

**Thoughts**:

It's cool build on previous exercises with new fundamentals because it shows you how the code becomes more efficient. I haven't practiced writing functions inside of objects but it's good to know it's a possibility!