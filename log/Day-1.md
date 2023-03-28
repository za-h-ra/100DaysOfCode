# #100DaysOfCode Log

## Day 1: Monday, March 27, 2023

<hr>

**Today's Progress**:

Completed "An Elixir Warmup" in The Complete Elixir and Phoenix Bootcamp. I learned about Enums, Lists, data structures in elixir, and most importantly, immutibility. There's no concept of modifying things in Elixir, you simply use the data strucutres you have and it results in new ones.

The written code so far:

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
