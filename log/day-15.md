# #100DaysOfCode Log

## Day 15: December 16, 2020

<br>

**Today's Progress**: Today I worked on my React book app. 

1. I went back to the General Assembly recordings and watched the Intro to React lesson. And then with the knowledge from the video, I re-did one of the assignments. 

    It's interesting to look at your assignment back then and how you wrote code then versus how much it's improved now. I often feel like I don't know anything but then I'm put in a situation where I'm implementing something and I know more than I thought I did. 

    So I wanted to review how ```props``` work but I didn't want to watch a course on Udemy because I feel like they don't go into detail of little things. I wanted to go back to the lessons from GA. And it helped me understand how to pass data from one component to the other. 

2. I went back to one of the assignments which was to re-create a mockup of a book-app. But to re-create it, we had to create a component architecture and use ```props``` to pass down data. For me, these small lessons help me focus on the little details. 

    So in my ```<Book />``` component, I wrote the following code:


```
export default function Book(props) {
	return (
		<BookContainer>
			<BookTitle>{props.title}</BookTitle>
			<BookContent>
				<BookImage src={props.img} />
				<BookText>{props.description}</BookText>
			</BookContent>
		</BookContainer>
	)
}
```

I understand now that the ```{ }``` in React is a way render Javascript and the HTML code is ```JSX``` not HTML. 

I used styled-components to style the application. I didn't even know what styled-components were at the time and it's interesting to use them. I still have unanswered questions about the library though and I think I'll fully understand it by using it more often.

**Link** [Here is the Github Repo for the project](https://github.com/zahrakhadijha/my-book-app)
<br>
<br>
My app actually looks like more like this than the actual clone because I added the books I really like and wanted to add 3 pieces of information instead of 2.

![](https://i.imgur.com/llyo1vB.png)
