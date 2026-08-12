# 🎯 Python Project: Guess the Number Game

## Project Assignment

Build a complete **Guess the Number Game** using Python.

In this game, the computer randomly selects a number between **1 and 10**. The player repeatedly enters guesses until the correct number is found.

The game should provide feedback after every valid guess:

- The guess is too low.
- The guess is too high.
- The guess is correct.

The program should also count how many attempts the player needed and allow the player to start another round.

**Do not copy a complete solution.** Build the project step by step using the requirements below.

---

# Step 1: Import the Required Module

Import Python's `random` module.

```python
# Import random
```

You will use this module to generate the secret number.

---

# Step 2: Create the Main Game Function

Create a function named:

```text
guessTheNumber()
```

Place the complete game logic inside this function.

The function should handle:

- Game introduction
- Random number generation
- User guesses
- Attempt counting
- Input validation
- Guess feedback
- Winning condition
- Replay functionality
- Ending the game

---

# Step 3: Create the Game Introduction

When the function starts, display:

```text
================================
     GUESS THE NUMBER GAME
================================
```

Use `print()` statements.

---

# Step 4: Display the Game Instructions

Tell the player:

- The computer has selected a number.
- The number is between `1` and `10`.
- The player needs to guess the correct number.

Display a message similar to:

```text
I have selected a number between 1 and 10.
Try to guess the correct number!
```

---

# Step 5: Create the Main Game Loop

The player should be able to play multiple rounds.

Create an outer:

```text
while True
```

loop.

Each iteration of this loop represents a new round.

---

# Step 6: Generate a Random Target Number

At the beginning of every round, generate a random number between `1` and `10`.

Use:

```python
random.randint(1, 10)
```

Store the result in:

```text
target
```

### Important

Generate a new target number for every new round.

---

# Step 7: Create the Attempt Counter

Create:

```text
attempts
```

Set it to:

```text
0
```

This variable counts how many guesses the player makes during the current round.

---

# Step 8: Announce the New Round

Display:

```text
A new number has been selected.
```

Do not display the target number.

---

# Step 9: Create the Guessing Loop

Inside the main game loop, create another:

```text
while True
```

loop.

This inner loop should continue until the player correctly guesses the target.

### Game Structure

```text
Main Game Loop
    ↓
Generate Target
    ↓
Set Attempts = 0
    ↓
Guessing Loop
    ↓
Check Guess
    ↓
Correct?
   ↙ ↘
 No   Yes
 ↓     ↓
Try    Win
Again  ↓
       End Round
```

---

# Step 10: Ask the Player for a Guess

Inside the guessing loop, ask:

```text
Enter your guess (1-10):
```

Use `input()` and convert the result to an integer.

Store the value in:

```text
guess
```

---

# Step 11: Increase the Attempt Counter

Every time the player enters a guess, increase:

```text
attempts
```

by `1`.

The counter should track the number of submitted guesses in the current round.

---

# Step 12: Validate the Guess Range

The valid range is:

```text
1 to 10
```

Check whether:

```text
guess < 1
```

or:

```text
guess > 10
```

If either condition is true, the guess is invalid.

---

# Step 13: Handle Invalid Guesses

For an invalid guess, display:

```text
Please enter a number between 1 and 10.
```

Then use:

```text
continue
```

to return to the beginning of the guessing loop.

The round should not end.

---

# Step 14: Compare the Guess with the Target

After validating the range, compare:

```text
guess
```

with:

```text
target
```

There are three possible results:

```text
guess < target
guess > target
guess == target
```

Use:

```text
if
elif
else
```

to handle them.

---

# Step 15: Handle a Guess That Is Too Low

If:

```text
guess < target
```

display:

```text
Your guess is too low. Try again.
```

The guessing loop should continue.

---

# Step 16: Handle a Guess That Is Too High

If:

```text
guess > target
```

display:

```text
Your guess is too high. Try again.
```

The guessing loop should continue.

---

# Step 17: Handle the Correct Guess

If:

```text
guess == target
```

the player has won the round.

Display:

```text
Congratulations!
```

Then display:

```text
You guessed the correct number: [target]
```

---

# Step 18: Display the Attempt Count

After a correct guess, display:

```text
You needed [attempts] attempt(s) to win.
```

Use the current value of `attempts`.

---

# Step 19: End the Guessing Loop

After the correct guess, use:

```text
break
```

to exit the inner guessing loop.

Do not break the loop after a low or high guess.

---

# Step 20: Ask Whether the Player Wants to Play Again

After the guessing loop ends, ask:

```text
Would you like to play again? (yes/no):
```

Store the response in:

```text
play_again
```

---

# Step 21: Convert the Replay Response to Lowercase

Use:

```python
.lower()
```

on the replay response.

This makes responses such as:

```text
YES
Yes
yes
```

consistent.

The same applies to:

```text
NO
No
no
```

---

# Step 22: Handle the `no` Response

Check:

```text
play_again == "no"
```

If true:

1. Display a thank-you message.
2. Display a game-ended message.
3. Break the outer game loop.

---

# Step 23: Display the Ending Messages

When the player chooses not to continue, display:

```text
Thank you for playing!
Game ended. See you next time!
```

---

# Step 24: Start Another Round

If the player does not enter `no`, display:

```text
Starting a new round...
```

Then allow the outer loop to continue.

The next round must:

- Generate a new target.
- Reset `attempts` to `0`.
- Start a new guessing loop.

---

# Step 25: Call the Game Function

After defining the function, call:

```python
guessTheNumber()
```

This starts the game when the program runs.

---

# Step 26: Understand the Complete Game Flow

Your program should follow this structure:

```text
Import random
      ↓
Define guessTheNumber()
      ↓
Display Title
      ↓
Display Instructions
      ↓
Outer while loop
      ↓
Generate Target
      ↓
Set Attempts = 0
      ↓
Inner while loop
      ↓
Ask for Guess
      ↓
Increase Attempts
      ↓
Validate Range
      ↓
Compare Guess
      ↓
 ┌───────────────┬───────────────┬───────────────┐
 ↓               ↓               ↓
Too Low       Too High         Correct
 ↓               ↓               ↓
Try Again     Try Again       Show Result
                                ↓
                              break
                                ↓
                       Ask Play Again
                                ↓
                       ┌────────┴────────┐
                       ↓                 ↓
                      yes                no
                       ↓                 ↓
                 New Round          End Game
```

---

# Step 27: Understand the Main Variables

| Variable | Purpose |
|---|---|
| `target` | Stores the randomly selected number |
| `attempts` | Counts the player's guesses |
| `guess` | Stores the player's current guess |
| `play_again` | Stores the replay decision |

---

# Step 28: Understand the Main Python Concepts

This project should demonstrate:

### `import`

Imports the `random` module.

### Function

Organizes the game inside:

```text
guessTheNumber()
```

### `random.randint()`

Generates a random integer between two limits.

### `input()`

Receives input from the player.

### `int()`

Converts the player's input into an integer.

### `while`

Creates the repeated game rounds and guessing process.

### `if / elif / else`

Compares the guess with the target.

### `continue`

Skips the remaining code in the current guessing-loop iteration and asks for another guess.

### `break`

Ends the guessing loop after a correct answer and ends the main loop when the player chooses to stop.

### `.lower()`

Normalizes the replay response.

---

# Step 29: Test the Game Introduction

Verify that:

- [ ] The game title appears.
- [ ] The title formatting is correct.
- [ ] The range `1-10` is explained.
- [ ] The player is told to guess the number.

---

# Step 30: Test Random Number Generation

Verify that:

- [ ] A target is generated.
- [ ] The target is between `1` and `10`.
- [ ] The target is hidden from the player.
- [ ] A new target is generated for a new round.

---

# Step 31: Test Valid Guesses

Try valid numbers such as:

```text
1
5
10
```

Verify that:

- [ ] Input is accepted.
- [ ] Attempts increase.
- [ ] The guess is compared with the target.

---

# Step 32: Test a Guess That Is Too Low

Enter a number lower than the target.

Verify:

```text
Your guess is too low. Try again.
```

Also verify that the player can guess again.

---

# Step 33: Test a Guess That Is Too High

Enter a number higher than the target.

Verify:

```text
Your guess is too high. Try again.
```

Also verify that the player can guess again.

---

# Step 34: Test the Correct Guess

Enter the correct number.

Verify that:

- [ ] Congratulations is displayed.
- [ ] The target number is displayed.
- [ ] The attempt count is displayed.
- [ ] The guessing loop ends.

---

# Step 35: Test Invalid Numbers

Try:

```text
0
11
20
-5
```

Verify that:

```text
Please enter a number between 1 and 10.
```

is displayed and the program asks for another guess.

---

# Step 36: Test Replay With `no`

After winning, enter:

```text
no
```

Verify that:

- [ ] The thank-you message appears.
- [ ] The game-ended message appears.
- [ ] The outer loop ends.
- [ ] The program finishes.

---

# Step 37: Test Replay With `yes`

After winning, enter:

```text
yes
```

Verify that:

- [ ] The new-round message appears.
- [ ] A new target is generated.
- [ ] Attempts reset to `0`.
- [ ] The player can make guesses again.

---

# Step 38: Test Different Letter Cases

Test:

```text
YES
Yes
yEs
NO
No
nO
```

Verify that `.lower()` allows the replay decision to be handled consistently.

---

# Step 39: Final Game Testing Checklist

### Game Setup

- [ ] `random` is imported.
- [ ] `guessTheNumber()` is defined.
- [ ] `guessTheNumber()` is called.
- [ ] The game starts successfully.

### Random Number

- [ ] Target is randomly generated.
- [ ] Target is between `1` and `10`.
- [ ] Target remains hidden.
- [ ] A new target is generated for each round.

### Input

- [ ] Player can enter a guess.
- [ ] Input is converted to an integer.
- [ ] Valid guesses are processed.
- [ ] Invalid range values are detected.

### Guess Logic

- [ ] Too-low message works.
- [ ] Too-high message works.
- [ ] Correct-guess message works.
- [ ] Guessing continues until correct.

### Attempts

- [ ] Attempts start at `0`.
- [ ] Attempts increase after each submitted guess.
- [ ] Final attempts are displayed.
- [ ] Attempts reset for every new round.

### Replay

- [ ] `yes` starts another round.
- [ ] `no` ends the game.
- [ ] `.lower()` is used.
- [ ] A new target is generated after replay.

---

# Step 40: Expected Gameplay Flow

A normal game should look conceptually like:

```text
================================
     GUESS THE NUMBER GAME
================================
I have selected a number between 1 and 10.
Try to guess the correct number!

A new number has been selected.

Enter your guess (1-10): 4
Your guess is too low. Try again.

Enter your guess (1-10): 8
Your guess is too high. Try again.

Enter your guess (1-10): 6

Congratulations!
You guessed the correct number: 6
You needed 3 attempt(s) to win.

Would you like to play again? (yes/no): yes

Starting a new round...
```

The exact target and attempt count will vary because the target is randomly generated.

---

# Step 41: Submission Requirements

Submit:

### 1. Python File

```text
guess_the_number.py
```

### 2. Screenshot

Provide a screenshot showing:

- The game title.
- At least one incorrect guess.
- A successful guess.
- The attempt count.
- The replay question.

If possible, also show the new-round flow.

---

# Step 42: Code Quality Requirements

Before submitting:

- [ ] Use meaningful variable names.
- [ ] Keep the game inside `guessTheNumber()`.
- [ ] Use proper indentation.
- [ ] Keep the nested loops organized.
- [ ] Use `break` only where necessary.
- [ ] Use `continue` for invalid range values.
- [ ] Keep output messages clear.
- [ ] Keep the code readable.
- [ ] Avoid unnecessary duplicate logic.

---

# Important Instructions

- Do not copy the complete solution.
- Build the program step by step.
- Keep the target number hidden from the player.
- Generate a new target for every round.
- Make sure the target is always between `1` and `10`.
- Validate guesses before comparing them with the target.
- Continue asking for guesses until the correct number is found.
- Count the player's attempts.
- Reset the attempt count for every new round.
- Use `.lower()` for the replay response.
- Make sure `yes` starts another round.
- Make sure `no` ends the game.
- Test all guess outcomes.
- Test both replay options before submission.

---

# Learning Objectives

By completing this project, you should understand:

- Python modules
- `import`
- Functions
- Function calls
- `random.randint()`
- Random number generation
- Variables
- User input
- `input()`
- `int()`
- String methods
- `.lower()`
- `while` loops
- Nested loops
- `if`
- `elif`
- `else`
- Comparison operators
- `continue`
- `break`
- Boolean conditions
- Counters
- Input validation
- Game logic
- Replay systems
- Program flow
- Basic console-game architecture
