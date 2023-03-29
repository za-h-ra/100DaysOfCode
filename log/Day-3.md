# #100DaysOfCode Log

## Day 3: Wednesday, March 29, 2023

<hr>

**Today's Progress**:

OK Case statements in Elixir are way too cool. So I learned about saving and loading up data. It looks strange and I'm not sure I fully get it but here's me trying to re-explain it.

To save a file to Elixir/Erlang, we have to save it to the Erlang environment (????) like so:

```elixir
    def save(deck, filename) do
        binary = :erlang.term_to_binary(deck)
        File.write(filename, binary)
    end
```

I'm learning that the `:erlang` invokes the object into erlang code. It takes the `deck` argument and turns it into an object that can be saved to the file system. And then `File.write(filename, binary)` takes the argument of the filename we want to invoke and takes the object we are trying to save.

I tried to do some outside research on `term_to_binary` and `binary_to_term` but a lot of erlang documentation came up so I guess I'll just see WHEN I need this specific solution. 🤷🏽‍♀️

But I think `case statements` are cool in Elixir. So we wrote some error handling for loading up a file. We load a file by writing `File.read(filename)` however, if there's an error, it'll throw up a computer error, but not a human readable error.

In JavaScript (pseudocode), it would be written something like this:

```javascript
if (statusCode === OK) {
  return data;
} else if (statusCode === error) {
  return "That file does not exist";
}
```

Something like that. But in Elixir, as a case statement, it's written:

```elixir

    case status do
        :ok -> :erlang.binary_to_term binary
        :error -> "That file does not exist"
    end
```

I find it cool and simple to read because it's one block of code. I do want to learn what the symbol `:` means in Elixir and what `->` means and how this syntax is used. I guess we'll get there.
