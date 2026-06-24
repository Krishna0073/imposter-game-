# Imposter Word Game 🎭

A fun terminal-based multiplayer Imposter Word Game built with Python.

## About the Game

In this game, most players receive the same secret word, while one or more players are secretly chosen as imposters.

The goal of the normal players is to identify the imposters through discussion.

The goal of the imposters is to blend in without knowing the secret word. To help them slightly, they receive a hint related to the secret word.

---

## Features

* Supports multiple players
* Supports multiple imposters
* Random secret word generation
* Hint system for imposters
* Hidden role reveal system
* Secure player-by-player viewing
* Discussion phase
* Final imposter reveal
* Easy to customize with your own words and hints

---

## How It Works

1. Enter the number of players.
2. Enter the number of imposters.
3. Each player takes turns viewing their role.
4. Normal players see the secret word.
5. Imposters see:

   * "YOU ARE THE IMPOSTER"
   * A hint related to the secret word.
6. After all players view their roles, a discussion round begins.
7. Players try to identify the imposters.
8. The game reveals the imposters and the secret word.

---

## Requirements

* Python 3.x

No external libraries are required.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/imposter-word-game.git
```

Move into the project directory:

```bash
cd imposter-word-game
```

Run the game:

```bash
python imposter_game.py
```

---

## Example Gameplay

```text
Enter number of players: 5
Enter number of imposters: 1

Player 1, take the device.
Press ENTER to reveal your role...

YOUR SECRET WORD IS:
>>> Pizza <<<

Press ENTER to hide your role...
```

Imposter View:

```text
YOU ARE THE IMPOSTER

Hint: Food item
```

Final Reveal:

```text
IMPOSTER REVEALED

Player 3 was an IMPOSTER!

Secret Word: Pizza
```

---

## Project Structure

```text
imposter-word-game/
│
├── imposter_game.py
├── README.md
└── LICENSE
```

---

## Customizing Words

Modify the `word_bank` dictionary inside the Python file:

```python
word_bank = {
    "Pizza": "Food item",
    "Tiger": "Wild animal",
    "Football": "Popular sport"
}
```

Add as many words and hints as you like.

---

## Future Improvements

* Graphical User Interface (Tkinter)
* Mobile/Web Version
* Difficulty Levels
* Categories (Movies, Sports, Countries, etc.)
* Timer-Based Discussion Round
* Score Tracking System
* Online Multiplayer Support

---

## Author

Created as a fun Python mini-project for learning programming, game logic, loops, conditions, lists, and randomization.

Enjoy playing! 🎉
