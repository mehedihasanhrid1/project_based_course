# 🧱 Python Pygame Assignment: Break the Bricks

## Total Marks: **100**

---

# 🎯 Learning Objectives

By completing this assignment, you will learn how to:

- Create a game window using Pygame
- Draw game objects
- Handle keyboard input
- Move objects using velocity
- Detect collisions
- Create and manage multiple bricks
- Implement a scoring system
- Manage player lives
- Display Game Over and Win screens
- Save and load the High Score using a text file

> **Instructions:** Complete each step in order. When you finish all the steps, you will have a complete **Break the Bricks** game.

---

# Step 1: Create the Game Window (10 Marks)

## Definition

A **game window** is the area where your game is displayed. Pygame creates it using `pygame.display.set_mode()`.

### Task

- Import all required modules.
- Initialize Pygame.
- Create a window of **600 × 700** pixels.
- Set an appropriate window title.

### Hint 💡

```python
import pygame

pygame.init()

window = pygame.display.set_mode((600, 700))
pygame.display.set_caption("Break the Bricks")
```

---

# Step 2: Create the Paddle and Ball (10 Marks)

## Definition

- The **Paddle** is controlled by the player.
- The **Ball** bounces around the screen and breaks bricks.

### Task

- Create a paddle using `pygame.Rect`.
- Position it near the bottom of the screen.
- Create a ball in the middle of the screen.
- Draw both objects every frame.

### Hint 💡

```python
paddle = pygame.Rect(...)
ball = pygame.Rect(...)
```

---

# Step 3: Move the Paddle (10 Marks)

## Task

Allow the player to move the paddle.

- ⬅ Left Arrow → Move Left
- ➡ Right Arrow → Move Right

Prevent the paddle from leaving the game window.

### Hint 💡

Use:

```python
pygame.key.get_pressed()
```

---

# Step 4: Move the Ball (10 Marks)

## Definition

The ball should continuously move using horizontal and vertical speed values.

### Task

- Create variables for horizontal and vertical movement.
- Update the ball position every frame.
- Make the ball bounce from the left, right, and top walls.

### Hint 💡

```python
ball.x += dx
ball.y += dy
```

---

# Step 5: Paddle Collision (10 Marks)

## Task

When the ball touches the paddle:

- Reverse its vertical direction.
- Continue moving upward.

### Hint 💡

Use:

```python
colliderect()
```

---

# Step 6: Create the Bricks (10 Marks)

## Definition

Bricks are arranged in rows and columns.

Each brick disappears when hit by the ball.

### Task

- Create multiple rows of bricks.
- Store them inside a list.
- Draw all bricks on the screen.

### Hint 💡

Use nested loops.

Example:

```python
for row in range(...):
    for col in range(...):
```

---

# Step 7: Break Bricks & Update Score (10 Marks)

## Task

When the ball hits a brick:

- Remove the brick.
- Increase the score.
- Reverse the ball direction.

Display the updated score.

### Hint 💡

Use:

```python
list.remove()
```

---

# Step 8: Lives System (10 Marks)

## Task

- Start with **3 lives**.
- If the ball falls below the screen:
  - Lose one life.
  - Reset the paddle and ball position.
- If all lives are lost:
  - Display the **Game Over** screen.

### Example

```
Lives: 3

↓

Lives: 2

↓

Lives: 1

↓

Game Over
```

---

# Step 9: Win Screen & High Score (10 Marks)

## Definition

The player wins after breaking every brick.

A **High Score** stores the highest score achieved.

### Task

- Display **YOU WIN!** when all bricks are destroyed.
- Save the High Score to a text file.
- Load the High Score when the game starts.

### Hint 💡

Use:

```python
open()
```

Example:

```python
with open("highscore.txt", "r") as file:
```

---

# Step 10: Restart the Game (10 Marks)

## Task

When the game ends:

- Press **SPACE** to play again.

The game should:

- Reset the score.
- Reset lives.
- Create a new set of bricks.
- Reset the paddle.
- Reset the ball.

---

# Bonus Challenge (+20 Marks)

Complete **any FOUR** of the following:

⭐ Add multiple brick types with different points.

Example:

- 🟩 Green Brick → 10 Points
- 🟨 Yellow Brick → 20 Points
- 🟥 Red Brick → 30 Points

---

⭐ Add sound effects for:

- Paddle hit
- Brick break
- Game Over
- Win

---

⭐ Add background music.

---

⭐ Increase ball speed every 5 bricks destroyed.

---

⭐ Display the current level.

---

⭐ Add a Pause/Resume feature using **P**.

---

⭐ Add a Start Menu.

---

⭐ Add special bricks:

- 💥 Explosive Brick (destroys nearby bricks)
- ❤️ Extra Life Brick
- ⚡ Speed Brick

---

⭐ Display the total number of bricks remaining.

---

⭐ Add particle effects when a brick breaks.

---

⭐ Add multiple levels with different brick layouts.

---

# Submission Requirements

Submit the following:

- ✅ Python (`.py`) source code
- ✅ High Score text file
- ✅ Screenshot of the game
- ✅ README explaining:
  - Controls
  - Features
  - Bonus features completed

---

# Marking Breakdown

| Step | Marks |
|------|------:|
| Step 1 – Game Window | 10 |
| Step 2 – Paddle & Ball | 10 |
| Step 3 – Paddle Movement | 10 |
| Step 4 – Ball Movement | 10 |
| Step 5 – Paddle Collision | 10 |
| Step 6 – Create Bricks | 10 |
| Step 7 – Break Bricks & Score | 10 |
| Step 8 – Lives System | 10 |
| Step 9 – Win Screen & High Score | 10 |
| Step 10 – Restart Game | 10 |
| **Total** | **100** |

---

# ✅ Expected Outcome

After completing all the steps, your game should:

- 🏓 Allow the player to move the paddle.
- ⚪ Move the ball smoothly across the screen.
- 🧱 Break bricks when the ball collides with them.
- 🏆 Increase the score as bricks are destroyed.
- ❤️ Track the player's remaining lives.
- 💾 Save and load the High Score.
- 🎉 Display a **YOU WIN!** screen after all bricks are cleared.
- ❌ Display a **GAME OVER** screen when all lives are lost.
- 🔄 Allow the player to restart the game by pressing **SPACE**.

🎉 Congratulations! By following each step, you will have built a complete **Break the Bricks** game using **Python and Pygame**.