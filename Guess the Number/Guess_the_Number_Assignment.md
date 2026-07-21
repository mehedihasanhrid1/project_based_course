# 🎯 Python Assignment: Build a "Guess the Number" Game

## Total Marks: 100

### 🎯 Learning Objectives

By completing this assignment, you will learn how to: - Import and use
Python modules - Generate random numbers - Take user input - Use
conditional statements - Create loops - Handle exceptions - Count
attempts - Build a complete console game

> Complete each step in order. When all steps are finished, you will
> have a complete Guess the Number game.

## Step 1: Import the Required Module (5 Marks)

### Definition

A **module** is a Python file containing reusable code.

### Task

-   Import the `random` module.

### Hint

``` python
import random
```

------------------------------------------------------------------------

## Step 2: Generate a Random Number (10 Marks)

### Definition

`random.randint(start, end)` returns a random integer within the given
range.

### Task

-   Generate a random number between **1 and 100**.

### Template

``` python
number = # Write your code here
```

------------------------------------------------------------------------

## Step 3: Display Instructions (5 Marks)

### Task

Display a welcome message explaining the game.

------------------------------------------------------------------------

## Step 4: Take User Input (10 Marks)

### Definition

`input()` receives input from the user.

### Task

Ask the user to enter a guess.

### Template

``` python
guess = int(input("Enter your guess: "))
```

------------------------------------------------------------------------

## Step 5: Compare the Guess (15 Marks)

### Task

-   Show **Too Low!** if the guess is smaller.
-   Show **Too High!** if the guess is larger.
-   Show **Correct!** if the guess is correct.

### Template

``` python
if guess < number:
    pass
elif guess > number:
    pass
else:
    pass
```

------------------------------------------------------------------------

## Step 6: Repeat Until Correct (15 Marks)

### Definition

A `while` loop repeats code until a condition changes.

### Task

Continue asking for guesses until the correct number is entered.

### Hint

``` python
while True:
    # code
    break
```

------------------------------------------------------------------------

## Step 7: Count Attempts (10 Marks)

### Task

-   Create an `attempts` variable.
-   Increase it after every valid guess.
-   Display the total attempts when the player wins.

------------------------------------------------------------------------

## Step 8: Validate Input (15 Marks)

### Definition

Use `try` and `except` to prevent crashes from invalid input.

### Template

``` python
try:
    guess = int(input("Enter your guess: "))
except ValueError:
    print("Invalid input!")
```

------------------------------------------------------------------------

## Step 9: Winning Message (5 Marks)

Display: - Congratulations message - Secret number - Total attempts

------------------------------------------------------------------------

## Step 10: Code Quality (10 Marks)

-   Meaningful variable names
-   Proper indentation
-   Comments
-   Clean, readable code

------------------------------------------------------------------------

# Bonus (+20 Marks)

Complete any four: - Play Again feature - Difficulty levels - Very Close
hint - High score using a text file - Maximum 10 attempts - Main menu -
Performance message

------------------------------------------------------------------------

# Marking Breakdown

  Step            Marks
  ----------- ---------
  Step 1              5
  Step 2             10
  Step 3              5
  Step 4             10
  Step 5             15
  Step 6             15
  Step 7             10
  Step 8             15
  Step 9              5
  Step 10            10
  **Total**     **100**
