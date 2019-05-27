# tennis-kata

> An elegant solution to the [Tennis Kata](http://codingdojo.org/kata/Tennis), forked from [bishboria/tennis-kata](https://github.com/bishboria/tennis-kata)

## About this Kata

This Kata is about implementing a simple tennis game. I came up with it while thinking about Wii tennis, where they have simplified tennis, so each set is one game.

The scoring system is rather simple:

1. Each player can have either of these points in one game 0 15 30 40

2. If you have 40 and you win the ball you win the game, however there are special rules.

3. If both have 40 the players are deuce:

  a. If the game is in deuce, the winner of a ball will have advantage and game ball.

  b. If the player with advantage wins the ball he wins the game

  c. If the player without advantage wins they are back at deuce.

## Usage

```
stack test
stack build
stack run tennis-kata-exe
```

## Notes

I wanted to confirm that this original code snippet:

```
score A (Game x y)          = Game (succ x) y
score B (Game x y)          = Game w z
  where
    (Game z w) = score A (Game y x)
```

could be replaced with:

```
score A (Game x y)          = Game (succ x) y
score B (Game x y)          = Game x (succ y)
```
