# 🎮 Pygame Project: Break the Bricks

## Project Assignment

Build a complete **Break the Bricks** game using Python and Pygame.

You will build the project step by step. **Do not copy a complete solution.** Each step gives you instructions and code comments describing what you need to write.

### Game Features

Your final game should include:

- A paddle controlled by the player.
- A bouncing ball.
- A grid of colored bricks.
- Ball and wall collision detection.
- Ball and paddle collision detection.
- Brick collision detection.
- Score system.
- Lives system.
- High-score system using a text file.
- Game Over screen.
- You Win screen.
- Restart option.
- Random initial ball direction.

---

# Step 1: Import Libraries and Initialize Pygame

Create the beginning of your Python program.

### Your Task

Write the required imports and initialize Pygame.

```python
# Import the pygame library
# Import the random library
# Import the os library
# Import the sys library

# Initialize pygame
```

### Requirements

- Use `pygame`.
- Use `random`.
- Use `os`.
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
- Player paddle rectangle.
- Ball rectangle.
- Ball speed.
- Ball horizontal direction.
- Ball vertical direction.
- Score variable.
- Lives variable.
- Game state.
- High-score file name.

```python
# Set the game window width to 600
# Set the game window height to 700

# Create the Pygame window using the width and height
# Set the window title to "Break the Bricks"

# Create a Pygame clock
# Create a normal font with size 36
# Create a large font with size 70

# Create the paddle rectangle
# Paddle position: centered horizontally near the bottom
# Paddle size: width = 120, height = 20

# Create the ball rectangle
# Ball position: near the center of the screen
# Ball size: width = 20, height = 20

# Set the ball speed to 5
# Set the initial horizontal direction randomly to -speed or speed
# Set the initial vertical direction to -speed

# Set the initial score to 0
# Set the initial lives to 3
# Set the initial state to "PLAY"

# Set the high-score file name to "brickgame.txt"
```

### Requirements

- Window size: `600 x 700`.
- Paddle size: `120 x 20`.
- Ball size: `20 x 20`.
- Initial lives: `3`.
- Initial score: `0`.
- Initial state: `"PLAY"`.
- Game speed should be controlled by the `speed` variable.

---

# Step 3: Create the High Score Loading Function

The game must remember the highest score between different game sessions.

Create a function named:

```python
# Define a function named load()
```

### Function Requirements

Inside the function:

```python
# Check whether the high-score file exists

# If the file exists:
#     Open the file
#     Read the stored score
#     Convert the content into an integer
#     Return the stored high score

# If the file does not exist:
#     Return 0
```

### Concepts

- Function
- `os.path.exists()`
- File reading
- `int()`
- `return`

---

# Step 4: Create the High Score Saving Function

Create a function named:

```python
# Define a function named save(s)
```

### Function Requirements

```python
# Open "brickgame.txt" in write mode
# Convert the score into a string
# Write the score into the file
```

After creating both high-score functions:

```python
# Call load()
# Store the returned value in a variable named high
```

### Important

The high score should be saved only when the current score is greater than the existing high score.

---

# Step 5: Create the Brick Generation Function

The game needs a reusable function that creates the complete brick layout.

Create a function named:

```python
# Define a function named make_bricks()
```

### Your Task

Inside the function:

```python
# Create an empty list named b

# Create a list containing five different RGB colors

# Create a loop for five rows

# Create a loop for eight columns

# For every row and column:
#     Create a brick rectangle
#     Give the brick a position based on its row and column
#     Give it a width of 60
#     Give it a height of 25
#     Store the rectangle and the row color together
#     Add the brick to the list

# Return the completed brick list
```

### Requirements

- Create `5` rows of bricks.
- Create `8` bricks in each row.
- Each brick should be `60 x 25`.
- Store each brick together with its color.
- Use different colors for different rows.
- Return the completed list.

### Concepts

- Function
- Lists
- Nested `for` loops
- `pygame.Rect`
- RGB colors
- `append()`
- `return`

---

# Step 6: Create the Initial Brick Layout

After creating the brick-generation function:

```python
# Call make_bricks()
# Store the returned list in a variable named bricks
```

This list will contain all bricks currently present in the game.

---

# Step 7: Create the Ball Reset Function

Create a function that returns the paddle and ball to their starting positions.

Create a function named:

```python
# Define a function named reset_ball()
```

### Function Requirements

```python
# Use global for:
# dx
# dy

# Move the paddle back to its starting horizontal position

# Move the ball back to the center position

# Set dx randomly to -speed or speed

# Set dy to -speed
```

### Important

This function is used when the player loses a life but still has lives remaining.

---

# Step 8: Create the Main Game Loop

Now create the main game loop.

### Your Task

Create an infinite loop that continuously runs the game.

```python
# Create an infinite while loop

# Limit the game to 60 frames per second
```

The game loop will contain the event handling, player movement, ball movement, collision detection, drawing, and display update.

---

# Step 9: Handle Pygame Events

Inside the main game loop, handle user and window events.

### Your Task

Use Pygame's event system.

```python
# Loop through all Pygame events

# Check if the user closes the game window
# If the window is closed:
#     Quit pygame
#     Exit the Python program

# Check whether the user pressed SPACE
# Make sure the current state is not "PLAY"

# If SPACE is pressed:
#     Check whether the current score is greater than the high score
#     If it is greater, save the new high score

#     Reset the score to 0
#     Reset lives to 3
#     Create a fresh set of bricks
#     Reset the ball
#     Change the state back to "PLAY"
```

### Required Events

You need to use:

- `pygame.event.get()`
- `pygame.QUIT`
- `pygame.KEYDOWN`
- `pygame.K_SPACE`

---

# Step 10: Detect Keyboard Input

The paddle should be controlled using the keyboard.

Inside the `"PLAY"` state:

```python
# Get the current state of all keyboard keys
# Store the result in a variable named k
```

This variable will be used to control the paddle.

---

# Step 11: Add Paddle Movement

The paddle should move only while the game is running.

### Your Task

Create conditions for the left and right arrow keys.

```python
# Check whether the LEFT arrow key is pressed
# Make sure the paddle is not already at the left edge
# Move the paddle 8 pixels to the left

# Check whether the RIGHT arrow key is pressed
# Make sure the paddle is not already at the right edge
# Move the paddle 8 pixels to the right
```

### Requirements

- Left movement speed: `8`.
- Right movement speed: `8`.
- Paddle cannot move outside the window.
- Paddle movement should happen only when `state == "PLAY"`.

---

# Step 12: Move the Ball

Now make the ball move continuously.

### Your Task

Inside the `"PLAY"` state:

```python
# Move the ball horizontally using dx
# Move the ball vertically using dy
```

The ball's position should change every frame.

### Requirements

- Use `dx` for horizontal movement.
- Use `dy` for vertical movement.
- Do not move the ball when the game is not in the `"PLAY"` state.

---

# Step 13: Detect Wall Collisions

The ball should bounce when it reaches the left, right, or top edges of the screen.

### Your Task

```python
# Check whether the ball touches the left edge
# OR the right edge

# If it does:
#     Reverse the horizontal direction

# Check whether the ball touches the top edge

# If it does:
#     Reverse the vertical direction
```

### Requirements

- Left wall collision changes `dx`.
- Right wall collision changes `dx`.
- Top wall collision changes `dy`.
- The ball should remain inside the visible play area except when falling below the bottom.

### Concepts

- Conditional statements
- Boolean operators
- Rectangle boundaries
- Direction reversal

---

# Step 14: Detect Paddle Collision

The ball should bounce when it hits the paddle.

### Your Task

```python
# Check whether the ball collides with the paddle

# Make sure the ball is moving downward

# If both conditions are true:
#     Reverse the vertical direction
#     Randomly change the horizontal direction slightly
```

### Requirements

Use:

- `ball.colliderect(paddle)`
- `dy > 0`
- `random.choice()`

The horizontal direction should be adjusted using a random choice of:

```python
-1
0
1
```

---

# Step 15: Detect Brick Collisions

Now process every brick currently in the game.

### Your Task

```python
# Loop through a copy of the bricks list

# Check whether the ball collides with the current brick

# If the ball collides with the brick:
#     Remove the brick from the bricks list
#     Reverse the vertical direction
#     Increase the score by a random number between 10 and 20
#     Stop checking additional bricks for this frame
```

### Important

Use a safe way to loop through the list while removing bricks.

For example, loop through a copy of the list.

### Concepts

- List slicing
- `for` loop
- `remove()`
- Collision detection
- Random score

---

# Step 16: Gradually Increase Ball Speed

The game should become slightly faster as the player breaks bricks.

### Your Task

After a brick is destroyed:

```python
# Check whether the absolute horizontal speed is less than 10

# If it is:
#     Slightly increase the horizontal speed
#     Slightly increase the vertical speed
```

### Requirements

- Use `abs()` to check the horizontal speed.
- Increase the speed gradually rather than making a large change.
- Keep the ball challenging but controllable.

### Concepts

- `abs()`
- Floating-point values
- Conditional statements
- Gradual difficulty

---

# Step 17: Detect When the Ball Falls

The player loses a life if the ball falls below the bottom of the screen.

### Your Task

```python
# Check whether the top of the ball is below the bottom of the window

# If it is:
#     Decrease lives by 1

# Check whether lives have reached 0
```

If the player still has lives remaining:

```python
# Reset the ball
```

---

# Step 18: Handle Game Over

When the player loses all lives, the game should enter the Game Over state.

### Your Task

```python
# If lives reaches 0:
#     Set the state to "GAME OVER"

# Check whether the current score is greater than the high score

# If the current score is greater:
#     Update the high score
#     Save the new high score
```

### Important

The high score should only be updated when the current score is greater than the existing high score.

---

# Step 19: Detect When All Bricks Are Destroyed

The player should win when no bricks remain.

### Your Task

```python
# Check whether the number of remaining bricks is 0

# If there are no bricks:
#     Set the state to "YOU WIN"

# Check whether the current score is greater than the high score

# If the current score is greater:
#     Update the high score
#     Save the new high score
```

### Required State

Use:

```text
YOU WIN
```

---

# Step 20: Draw the Background and Bricks

After the game logic, draw the game objects.

### Your Task

First fill the screen with a dark background.

```python
# Fill the window with a dark RGB color
```

Then draw every brick.

```python
# Loop through all bricks

# Draw each brick using its stored color

# Draw a white outline around each brick
```

### Requirements

Use:

- `win.fill()`
- `pygame.draw.rect()`
- Brick color
- White outline

---

# Step 21: Draw the Paddle and Ball

Draw the player paddle and the ball.

### Your Task

```python
# Draw the paddle as a rectangle
# Use a light-blue RGB color

# Draw the ball as an ellipse
# Use a white RGB color
```

Use:

- `pygame.draw.rect()`
- `pygame.draw.ellipse()`

---

# Step 22: Display Score, Lives, and High Score

Create text showing the current game information.

### Your Task

Create three text surfaces:

```python
# Create text showing the current score
# Format: Score: <score>

# Create text showing the remaining lives
# Format: Lives: <lives>

# Create text showing the high score
# Format: High: <high>
```

### Display Requirements

```python
# Display the score near the top-left corner

# Display the lives near the top-center area

# Display the high score near the top-right corner
```

Use:

- `font.render()`
- `win.blit()`
- f-strings

---

# Step 23: Create the Game Over Screen

When the state becomes `"GAME OVER"`, show a Game Over screen.

### Your Task

Create a condition:

```python
# Check if state is "GAME OVER"
```

Inside it:

```python
# Create a large "GAME OVER" text

# Create text telling the player to press SPACE to play again

# Draw both messages approximately in the center of the screen
```

### Required Messages

The screen should communicate:

- `GAME OVER`
- `Press SPACE to Play Again`

---

# Step 24: Create the You Win Screen

When all bricks are destroyed, show a winning screen.

### Your Task

Create a condition:

```python
# Check if state is "YOU WIN"
```

Inside it:

```python
# Create a large "YOU WIN!" text

# Create text telling the player to press SPACE to play again

# Draw both messages approximately in the center of the screen
```

### Required Messages

The screen should communicate:

- `YOU WIN!`
- `Press SPACE to Play Again`

---

# Step 25: Update the Display

At the very end of the main game loop:

```python
# Update the Pygame display
```

Use the appropriate Pygame display-update function.

This is necessary so that all drawings and text appear on the screen.

---

# Step 26: Final Game Flow

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
Create Brick Layout
      ↓
Create Paddle and Ball
      ↓
Start Game Loop
      ↓
Handle Events
      ↓
Check Game State
      ↓
Move Paddle
      ↓
Move Ball
      ↓
Check Wall Collision
      ↓
Check Paddle Collision
      ↓
Check Brick Collision
      ↓
Update Score
      ↓
Check Ball Lost
      ↓
Update Lives
      ↓
Check Game Over
      ↓
Check You Win
      ↓
Draw Background
      ↓
Draw Bricks
      ↓
Draw Paddle
      ↓
Draw Ball
      ↓
Display Score / Lives / High Score
      ↓
Display Game Over or You Win Screen
      ↓
Update Display
      ↓
Repeat
```

---

# Step 27: Final Testing Checklist

Before submitting your project, test every feature.

### Game Setup

- [ ] Pygame initializes correctly.
- [ ] Game window opens.
- [ ] Window title is correct.
- [ ] Game runs at approximately 60 FPS.
- [ ] High-score file is handled correctly.

### Paddle

- [ ] Paddle appears near the bottom.
- [ ] Left Arrow moves the paddle left.
- [ ] Right Arrow moves the paddle right.
- [ ] Paddle cannot leave the screen.

### Ball

- [ ] Ball starts near the center.
- [ ] Ball moves automatically.
- [ ] Ball bounces from the left wall.
- [ ] Ball bounces from the right wall.
- [ ] Ball bounces from the top wall.
- [ ] Ball bounces from the paddle.
- [ ] Ball can fall below the screen.

### Bricks

- [ ] Five rows of bricks appear.
- [ ] Eight bricks appear in each row.
- [ ] Bricks have different row colors.
- [ ] Ball can destroy bricks.
- [ ] Destroyed bricks disappear.
- [ ] Score increases when a brick is destroyed.
- [ ] Ball speed gradually increases.

### Score

- [ ] Score starts at 0.
- [ ] Breaking a brick increases the score.
- [ ] Score is displayed on screen.

### Lives

- [ ] Lives start at 3.
- [ ] Losing the ball decreases lives.
- [ ] Ball resets when lives remain.
- [ ] Game ends when lives reach 0.

### High Score

- [ ] `brickgame.txt` is created automatically when a high score needs to be saved.
- [ ] High score can be loaded.
- [ ] High score can be saved.
- [ ] A new high score replaces the old one.
- [ ] High score remains available after restarting the program.

### Game Over

- [ ] Game Over screen appears when lives reach 0.
- [ ] `GAME OVER` is displayed.
- [ ] SPACE restarts the game.
- [ ] Score resets when the game restarts.
- [ ] Lives reset to 3.
- [ ] Bricks are recreated.

### You Win

- [ ] You Win screen appears when all bricks are destroyed.
- [ ] `YOU WIN!` is displayed.
- [ ] SPACE restarts the game.
- [ ] New bricks are created after restarting.

---

# Step 28: Submission Requirements

Submit the following:

### 1. Python File

Your completed Python program:

```text
break_the_bricks.py
```

### 2. High Score File

The program uses:

```text
brickgame.txt
```

The file is used to store the high score.

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
- Do not remove the high-score functionality.
- Make sure the game can be restarted after both Game Over and You Win.

---

## Goal

By completing this assignment, you should be able to demonstrate your understanding of:

- Python variables
- Lists
- Functions
- Global variables
- Conditional statements
- Loops
- File handling
- `os.path.exists()`
- Random numbers
- Pygame initialization
- Pygame events
- Keyboard input
- Pygame drawing
- Rectangles
- Ellipses
- Collision detection
- Ball physics
- Game loops
- Score systems
- Life systems
- High-score persistence
- Game states
- Basic game-state management
