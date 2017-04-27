# CRIMINAL MASTERMIND V0.1

a board + text adventure game engine  
by masterminds for masterminds

Criminal Mastermind is a game engine for a new genre of
text adventure games where the player navigates on a self-drawn map (the board).
The computer keeps track of the game state, but ignores player location.
This means the player can express their own imagination while playing.
It is the intention that the player draws events from the story on the board while playing.
With some scripting skills, you can create your own adventure games using the engine.

The self-drawn map can be reused in later games,
colored and shared as art, or kept as a memory of the experience.

This ideas behind this experiment is:

- Make the computer keep track of dialogue, money, inventory, social points and quests
- Make the player design the topology of the world
- Evolve the world dynamically over time, changing the playing experience,
  with the intention that players draw characters they meet, events and their experiences

### How to play (Tutorial)

This game engine is currently experimental, unfinished, and only usable if you know the [Dyon](https://github.com/pistondevelopers/dyon) programming language.

Prepare your computer:

1. First, you need to install [Rust](https://www.rust-lang.org/en-US/).
2. Fork this repository to your local computer
3. Open up the Terminal window (Command Line on Windows)
4. Navigate to the project folder using `cd <dir>`
5. To run, type `cargo run --example run_game --release`

Prepare your mind:

1. Find a sheet of paper (A4 or bigger)
2. Find a pen (color pencils are optional)
3. Find something you can use to keep track of your position, (e.g. a stolen chess piece or a cursed gold coin)

Prepare the mood:

6. Wait until it's dark and cold outside
7. Crawl into some blankets with a cup of hot chocolate
8. Play some epic background music

When the game starts, it lists all major locations in the game.
These should be placed on the map.
You can draw locations any way you like, I often use slots shaped as double-circles.
Make sure that all locations have enough room for your player piece.

1. Draw each listed location as a slot with a small icon inside it, or text besides it
2. Connect locations with a network of empty slots

In the Terminal window, you get a set of choices.
The three first are "items", "empty" and "home".

- When you type "items", you get a list of your inventory. There are things you find during the game and is used to solve quests.
- When you type "empty", the game engine assumes that you have moved to an empty slot on the board. This will give you some surprises, free, rides, some money you find on the ground or some ideas of what to do.
- When you type "home", you get to a special location that first asks you whether to sleep until next day. This advances the story one day and counts down until the dead line.
If you say "no" you activate other events at your home.

The game engine rolls a dice for you,
which you use to navigate on the map.
You can choose which direction to go,
and you can stop at any location if there are enough eyes to move there.
Remember to explore the map each day to not miss important events!

Each location has an assigned character.
Their name is shown when you are having a dialogue.
Characters in the game give you a secret social score, which might unlock new events when you reach a high enough score.
Or, they can do things if you get a low enough score... you never know.

Most important: Remember to not trust anyone.

### How to modify the game

Quest:

A quest is an object that has a `finished` flag (bool).
It contains a closure for each location place, e.g.

        home: \() = {...}

## License

Licensed under either of
 * Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)
at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you shall be dual licensed as above, without any
additional terms or conditions.
