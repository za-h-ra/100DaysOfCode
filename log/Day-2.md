# #100DaysOfCode Log

## Day 2: Tuesday, March 28, 2023

<hr>

**Today's Progress**:

We started on section 2: Elixir's Amazing Pattern Matching. So I followed my own advice, set a timer for 1 hour and deep-dived into the concept of Pattern Matching and Elixir's Relationship with Erlang. And there's what I learned:

Pattern Matching is the literal CORE of Elixir. We left off wondering how we can access elements/data inside of a Tuple in Elixir. So it was kind of cool learning about Pattern Matching.

Pattern Matching is used for variable assignments in Elixir. It's Elixir's replacement for variable assignments, except that you have to match the SAME data structure in order to access elements inside of it.

For example—

If we have,

```elixir
name1 = ["zahra"]
# > ["zahra"]
```

The entire list is assigned to `name1` since we didn't give it any specifications. But let's say I want to access the `string` inside of the list, THEN I would have to do this:

```elixir
[name1] = ["zahra"]
# > "zahra"
```

This works because the data structure on the left matches the data structure on the right side. So for Tuples, it works the same way:

```elixir

{hand, rest_of_deck} = { my_hand, the_rest }

# > hand = my_hand

```

So `hand` is assigned to `my_hand` and `rest_of_deck` is matched to `the_rest`. `hand` and `my_hand` is at `index 0` and `rest_of_deck` and `the_rest` is at `index 1`. So the left right has to match the right side.

It felt simple to understand this concept and I found it cool. Obviously I'm still learning to have to put it into practice a bit more.

So then we quickly reviewed Elixir's Ecosystem with Erlang. From my understanding, Elixir is the dialect of Erlang. Erlang's syntax is ugly so we use Elixir so ~us~ developers can understand it better. It's a different language but has the same underlying concepts.

How it works:

```

The Code We Write ---(get's fed into)--> Elixir ---(gets transpiled into)--> Erlang ---(gets compiled and executed)--> BEAM


```

BEAM (Bogdan/Björn's Erlang Abstract Machine): A virtual machine at the core of the Erlang Open Telecom Platform.

It's interesting to learn that Erlang was created as a solution for telecom companies.

Anyways, no actual coding today, just learning some concepts. Tomorrow, more knowledge on Pattern Matching will continue.
