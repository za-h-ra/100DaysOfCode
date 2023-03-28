# #100DaysOfCode Log

## Day 1: Monday, March 27, 2023

<hr>

**Today's Progress**:

It was information overload today. Whenever I start off my learning journey I feel like I "go big" and then tend to give up. So I spent a shit ton of time going through the first section. And I realized that maybe I time myself to spend ONE hour on a section and then cut myself off, I retain the information better. I have to remember that this isn't a sprint. I'm learning daily. Information is small doses is easily memorable than consuming it all at once. Some people are able to do it — and I'm happy for them, I love it for them — but I need to take information in small doses. But I did complete the entire "An Elixir Warmup" section and it was truly a warm up.

So here's what I learned:

- In Elixir, there's a concept of immutibility. We never modify the data structure in place. Every modification in Elixir returns a NEW data structure.
- I learned the difference between an Object-Oriented Approach and a Functional Programming Approach to writing programs. Since Elixir is a functional programming language, there's no concept of classes or instance of a class.
- A Module is a standalone object. A Module is simply a collection of methods and functions.

```elixir

defmodule Some_Module do

  def hello do
  "hello!"
  end

end
```

- `defmodule` is what defines a module and then `def` is what defines a method or function. It's similar to Ruby.
- A `"string"` is the same in Elixir as it is in other programming languages.
- We can access a method inside of a Module as `Some_Module.hello` and we don't have to call it with paranthesis.
- In Elixir, every method/function has an implicit return instead of writing the word `return`.
- It seems like arrays are also the same in elixir `["one", "two", "three"]` how it's similar to other languages (I compare it to JavaScript as I'm most familiar with JS most)
- Method arguments are the same as any function arguments in other languages. For example, if we write a `shuffle` function:

```elixir
  def shuffle(deck) do
  # some code
  end
```

So in this function, we should be able to write pass in a list of strings and they will get "shuffled." It will return back a new list of strings, it won't modify the original data structure.

- There's an important use for Elixir's documentation and built-in methods such as Enums. Enum's are functions for working with colllections (known as enumerables), which is any data type that implements the "ENUMERABLE" protocol. So one of the methods we used was:

```elixir
  def shuffle(deck) do
    Enum.shuffle(deck)
  end
```

So pretty much! Modules in Elixir are a collection of methods and NOTHING more. There will NEVER be instance variables, ever. Elixir relies on a big pool of data structures that we pass to different methods in our modules. When we want to act on the data, we take that data and pass it into a method. The method then processes the data and spits out the result back to us with new data.

And then finally, learned about Comprehensions over Lists which is pretty much...loops. It just iterates over a collection of elements.

Nested loops are a bad solution in every language. I learned the funky syntax for loops in Elixir which is with this symbol: `<-` so I'll definitely have to write more code with loops to get an understanding of "List Comprehensions."

AND THENNNN I went over Tuples `{}` which is just whatever data structure is in a curly bracket. The way I defined a Tuple is that it's an ordered list. It's like what an array is in other programming languages, it has an index and a specific place certain elements belong in.

Anyways, this is what the code was:

```elixir
defmodule Cards do

  def create_deck do
   values = ["Ace", "Two", "Three", "Four", "Five"]
   suits = ["Spades", "Clubs", "Hearts", "Diamonds"]

    for suit <- suits, value <- values do
      "#{value} of #{suit}"
    end

  end

  def shuffle(deck) do
    Enum.shuffle(deck)
  end

  def contains?(deck, card) do
    Enum.member?(deck, card)
  end

  def deal(deck, hand_size) do
    Enum.split(deck, hand_size)
  end

end


```
