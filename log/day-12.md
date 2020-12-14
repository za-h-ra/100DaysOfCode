# #100DaysOfCode Log

## Day 12: December 13, 2020

<br>

**Today's Progress**: I played around with React again today. I was going to attempt to create the Facebook Status Widget but decided to just refresh my knowledge on React via Andrei Neogoie's course. We are building a monster rolodex application but it's a good refresher on how to make API calls, what ```fetch``` and ```promise``` does and what ```React.Component``` means. 

I needed this refresher because I remember using React Hooks for most of my time at General Assembly so I forgot how to use React Classes.

I had a lot of gaps in my knowledge with React even though I knew how to use it. But I didn't quite understand some things and this course is helping fill in the blanks. 

So what I learned today is how to store data is ```state``` and how to ```map()``` through it. I remember the ```map()``` so that's exciting. I just remember learning it a little differently so this perspective is still interesting. So this is how I did it initally:

```
class App extends Component {
    constructor() {
        super()

        this.state = {
            monsters: [
                {
                    name: 'Frankenstein',
                    id: 'asc1'
                },
                {
                    name: 'Dracula',
                    id: 'asc2'
                },
                {
                    name: 'Ursula',
                    id: 'asc3
                }
            ]
        }
    }
```

I never really understood the ```key``` error that popped up in console but the lessons explained that as well, which is why there is an ```id``` added to the objects. And then I mapped through it to make it appear on the screen:

```
{this.state.monsters.map(monster => (<h1 key={monster.id}> {monster.name} </h1>))}
```

It was a very light lesson, but I'll continue to learn more tomorrow.🙂