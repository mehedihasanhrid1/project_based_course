# 🎮 Pygame Project: Catch the Coins

## Project Assignment

Build a complete **Catch the Coins** game using Python and Pygame.

You will build the project step by step. **Do not copy a complete solution.** Each step gives you instructions and code comments describing what you need to write.

### Game Features

Your final game should include:

- A player that moves left and right.
- Falling coins.
- Falling bombs.
- Score system.
- Lives system.
- Collision detection.
- Random coin and bomb generation.
- High-score system using a text file.
- Game Over screen.
- Restart option.
- Quit option.

---

# Step 1: Import Libraries and Initialize Pygame

Create the beginning of your Python program.

### Your Task

Write the required imports and initialize Pygame.

```python
# Import the pygame library
# Import the random library
# Import the sys library

# Initialize pygame
```

### Requirements

- Use `pygame`.
- Use `random`.
- Use `sys`.
- Initialize Pygame before creating the game window.

---

# Step 2: Create the Game Window and Game Variables

Set up the basic configuration of the game.

### Your Task

Create:

- Window width and height.
- Pygame display window.
- Window title.
- Game clock.
- Normal font.
- Large font.
- Player rectangle.
- Empty coins list.
- Empty bombs list.
- Score variable.
- Lives variable.
- Game-over variable.

```python
# Set the game window width to 500
# Set the game window height to 600

# Create the Pygame window using the width and height
# Set the window title to "Catch the Coins"

# Create a Pygame clock
# Create a normal font with size 36
# Create a large font with size 60

# Create the player rectangle
# Player position: x = 220, y = 540
# Player size: width = 60, height = 30

# Create an empty list to store coins
# Create an empty list to store bombs

# Set the initial score to 0
# Set the initial lives to 3
# Set game_over to False
```

---

# Step 3: Create the High Score Loading Function

The game must remember the highest score between different game sessions.

Create a function named:

```python
# Define a function named load_high_score()
```

### Function Requirements

Inside the function:

```python
# Try to open "coinscore.txt" in read mode
# Read the content of the file
# Convert the content into an integer
# Return the stored high score

# If an error occurs:
#     Open "coinscore.txt" in write mode
#     Write "0" into the file
#     Return 0
```

### Concepts

- Function
- `try`
- `except`
- File reading
- File writing
- `return`

---

# Step 4: Create the High Score Saving Function

Create a function named:

```python
# Define a function named save_high_score(high_score)
```

### Function Requirements

```python
# Open "coinscore.txt" in write mode
# Convert high_score into a string
# Write the high score into the file
```

After creating both high-score functions:

```python
# Call load_high_score()
# Store the returned value in a variable named high_score
```

---

# Step 5: Create the Game Reset Function

Create a function named:

```python
# Define a function named reset_game()
```

This function will be called when the player wants to play again.

### Function Requirements

```python
# Use global for:
# score
# lives
# coins
# bombs
# game_over

# Reset score to 0
# Reset lives to 3
# Empty the coins list
# Empty the bombs list
# Move the player back to x position 220
# Set game_over to False
```

### Important

Do not reset the high score. The high score must remain saved.

---

# Step 6: Create the Main Game Loop

Now create the main game loop.

### Your Task

Create an infinite loop that continuously runs the game.

```python
# Create an infinite while loop

# Limit the game to 60 frames per second
# Fill the screen with a dark background
```

The game loop will contain most of the remaining game logic.

---

# Step 7: Handle Pygame Events

Inside the main game loop, handle user and window events.

### Your Task

Use Pygame's event system.

```python
# Loop through all Pygame events

# Check if the user closes the game window
# If the window is closed:
#     Quit pygame
#     Exit the Python program

# Check whether the game is over AND the event is a keyboard event

# If the R key is pressed:
#     Call reset_game()

# If the Q key is pressed:
#     Quit pygame
#     Exit the Python program
```

### Required Events

You need to use:

- `pygame.event.get()`
- `pygame.QUIT`
- `pygame.KEYDOWN`
- `pygame.K_r`
- `pygame.K_q`

---

# Step 8: Detect Keyboard Input

Get the current keyboard state.

```python
# Get the current state of all keyboard keys
# Store the result in a variable named keys
```

This variable will be used to control the player.

---

# Step 9: Add Player Movement

The player should only move while the game is running.

### Your Task

Create a condition that checks whether the game is **not over**.

Inside that condition:

```python
# Check whether the LEFT arrow key is pressed
# Make sure the player is not already at the left edge
# Move the player 7 pixels to the left

# Check whether the RIGHT arrow key is pressed
# Make sure the player is not already at the right edge
# Move the player 7 pixels to the right
```

### Requirements

- Left movement speed: `7`
- Right movement speed: `7`
- Player cannot move outside the window.

---

# Step 10: Generate Falling Coins

Coins should appear randomly from the top of the screen.

### Your Task

```python
# Generate a random number between 1 and 25
# If the generated number is 1:
#     Create a new coin rectangle
#     Give it a random x position
#     Start its y position above the screen
#     Give it a width of 25
#     Give it a height of 25
#     Add the coin to the coins list
```

### Requirements

- Use `random.randint()`.
- Coin x-position must be random.
- Coin should start above the screen.
- Store each coin in the `coins` list.

---

# Step 11: Generate Falling Bombs

Bombs should also appear randomly.

### Your Task

```python
# Generate a random number between 1 and 45
# If the generated number is 1:
#     Create a new bomb rectangle
#     Give it a random x position
#     Start its y position above the screen
#     Give it a width of 30
#     Give it a height of 30
#     Add the bomb to the bombs list
```

### Requirements

- Use `random.randint()`.
- Bomb x-position must be random.
- Bomb should start above the screen.
- Store each bomb in the `bombs` list.

---

# Step 12: Move Coins and Detect Coin Collisions

Now process every coin currently in the game.

### Your Task

```python
# Loop through a copy of the coins list

# Move each coin downward by 5 pixels

# If the coin moves below the bottom of the screen:
#     Remove the coin from the coins list

# Otherwise, check whether the coin collides with the player

# If the coin collides with the player:
#     Remove the coin
#     Increase the score by a random number between 10 and 20
```

### Important

Use a safe way to loop through the list while removing items from it.

### Concepts

- List slicing
- `for` loop
- `remove()`
- Collision detection
- Random score

---

# Step 13: Move Bombs and Detect Bomb Collisions

Now process every bomb.

### Your Task

```python
# Loop through a copy of the bombs list

# Move each bomb downward by 6 pixels

# If the bomb moves below the bottom of the screen:
#     Remove the bomb

# Otherwise, check whether the bomb collides with the player

# If the bomb collides with the player:
#     Remove the bomb
#     Decrease lives by 1
```

---

# Step 14: Handle Game Over and High Score

Continue inside the bomb collision logic.

### Your Task

After decreasing the player's lives:

```python
# Check whether lives are less than or equal to 0

# If the player has no lives remaining:
#     Check whether the current score is greater than the high score

#     If the current score is greater:
#         Update high_score with the current score
#         Save the new high score using save_high_score()

#     Set game_over to True
```

### Important

The high score should only be updated when the current score is greater than the existing high score.

---

# Step 15: Draw the Player

After the game logic, draw the player on the screen.

### Your Task

```python
# Draw the player as a rectangle
# Use the player rectangle
# Use a blue/light-blue RGB color
```

Use:

- `pygame.draw.rect()`

---

# Step 16: Draw the Coins

Draw every coin currently stored in the coins list.

### Your Task

```python
# Loop through all coins

# Draw each coin as an ellipse
# Use the coin rectangle as the drawing area
# Use a yellow RGB color
```

Use:

- `pygame.draw.ellipse()`

---

# Step 17: Draw the Bombs

Draw every bomb currently stored in the bombs list.

### Your Task

```python
# Loop through all bombs

# Draw each bomb as a circle
# Use the center of the bomb rectangle
# Use a radius of 15
# Use a red RGB color
```

Use:

- `pygame.draw.circle()`
- `bomb.center`

---

# Step 18: Display the Score, Lives, and High Score

Create text showing the current game information.

### Your Task

Create three text surfaces:

```python
# Create text showing the current score
# Format: Score: <score>

# Create text showing the remaining lives
# Format: Lives: <lives>

# Create text showing the high score
# Format: High Score: <high_score>
```

Use the normal font.

### Display Requirements

```python
# Display the score near the top-left corner

# Display the lives near the top-right corner

# Display the high score near the top-center area
```

Use:

- `font.render()`
- `win.blit()`
- f-strings

---

# Step 19: Create the Game Over Screen

When `game_over` becomes `True`, show a Game Over screen.

### Your Task

Create a condition:

```python
# Check if game_over is True
```

Inside it, create five text elements:

```python
# Create a large "GAME OVER" text

# Create text telling the player to press R to play again

# Create text telling the player to press Q to quit

# Create text showing the final score

# Create text showing the high score
```

### Required Messages

The screen should communicate:

- `GAME OVER`
- `Press R to Play Again`
- `Press Q to Quit`
- `Final Score: ...`
- `High Score: ...`

### Display Position

Place the messages approximately in the middle of the screen, similar to:

```text
             GAME OVER

       Press R to Play Again
            Press Q to Quit

          Final Score: ...

           High Score: ...
```

You may adjust the exact positions if needed.

---

# Step 20: Update the Display

At the very end of the main game loop:

```python
# Update the Pygame display
```

Use the appropriate Pygame display-update function.

This is necessary so that all drawings and text appear on the screen.

---

# Step 21: Final Game Flow

Your completed program should follow this general flow:

```text
Start Program
      ↓
Initialize Pygame
      ↓
Create Window
      ↓
Load High Score
      ↓
Create Game Objects
      ↓
Start Game Loop
      ↓
Handle Events
      ↓
Check Keyboard
      ↓
Move Player
      ↓
Generate Coins
      ↓
Generate Bombs
      ↓
Move Coins
      ↓
Check Coin Collision
      ↓
Update Score
      ↓
Move Bombs
      ↓
Check Bomb Collision
      ↓
Update Lives
      ↓
Check Game Over
      ↓
Draw Player
      ↓
Draw Coins
      ↓
Draw Bombs
      ↓
Display Score / Lives / High Score
      ↓
Display Game Over Screen if necessary
      ↓
Update Display
      ↓
Repeat
```

---

# Step 22: Final Testing Checklist

Before submitting your project, test every feature.

### Game Setup

- [ ] Pygame initializes correctly.
- [ ] Game window opens.
- [ ] Window title is correct.
- [ ] Game runs at approximately 60 FPS.

### Player

- [ ] Player appears at the bottom.
- [ ] Left Arrow moves the player left.
- [ ] Right Arrow moves the player right.
- [ ] Player cannot leave the screen.

### Coins

- [ ] Coins appear randomly.
- [ ] Coins fall downward.
- [ ] Coins disappear when they leave the screen.
- [ ] Player can catch coins.
- [ ] Catching a coin increases the score.

### Bombs

- [ ] Bombs appear randomly.
- [ ] Bombs fall downward.
- [ ] Bombs disappear when they leave the screen.
- [ ] Player can collide with bombs.
- [ ] Bomb collision decreases lives.

### Score

- [ ] Score starts at 0.
- [ ] Coin collection increases the score.
- [ ] Score is displayed on screen.

### Lives

- [ ] Lives start at 3.
- [ ] Bomb collision decreases lives.
- [ ] Game ends when lives reach 0.

### High Score

- [ ] `coinscore.txt` is created automatically.
- [ ] High score can be loaded.
- [ ] High score can be saved.
- [ ] A new high score replaces the old one.
- [ ] High score remains available after restarting the program.

### Game Over

- [ ] Game Over screen appears.
- [ ] Final score is displayed.
- [ ] High score is displayed.
- [ ] R restarts the game.
- [ ] Q quits the game.

---

# Step 23: Submission Requirements

Submit the following:

### 1. Python File

Your completed Python program:

```text
catch_the_coins.py
```

### 2. High Score File

The program should generate:

```text
coinscore.txt
```

### 3. Screenshot

Provide a screenshot showing your completed game running.

---

# Important Instructions

- Do not skip any step.
- Do not copy a complete solution from another source.
- Write the code yourself based on the instructions.
- Keep your code properly indented.
- Use meaningful variable and function names.
- Test the program after completing each major section.
- If you encounter an error, identify which step caused it and fix it before continuing.

## Goal

By completing this assignment, you should be able to demonstrate your understanding of:

- Python variables
- Lists
- Functions
- `global`
- Conditional statements
- Loops
- File handling
- Exception handling
- Random numbers
- Pygame events
- Keyboard input
- Pygame drawing
- Rectangles
- Collision detection
- Game loops
- Score and life systems
- Basic game-state management
