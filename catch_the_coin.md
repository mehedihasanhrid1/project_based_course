# 🪙 Python Pygame Assignment: Catch the Coins

## Total Marks: **100**

---

# 🎯 Learning Objectives

By completing this assignment, you will learn how to:

- Create a game window using Pygame
- Draw game objects
- Handle keyboard input
- Generate random objects
- Detect collisions
- Work with lists of objects
- Implement a scoring system
- Manage player lives
- Display Game Over screen
- Read and write files for High Score

> **Instructions:** Complete each step in order. When all the steps are completed, you will have a fully functional **Catch the Coins** game.

---

# Step 1: Create the Game Window (10 Marks)

## Definition

A **game window** is where the game is displayed. Pygame uses `display.set_mode()` to create it.

### Task

- Import the required modules.
- Initialize Pygame.
- Create a window of **500 × 600** pixels.
- Set the window title.

### Hint 💡

```python
pygame.init()

window = pygame.display.set_mode((500, 600))
pygame.display.set_caption("Catch the Coins")
```

---

# Step 2: Create the Player (10 Marks)

## Definition

The player is the object controlled by the user.

### Task

- Create a player using `pygame.Rect`.
- Place it near the bottom of the screen.
- Draw the player every frame.

### Hint 💡

```python
player = pygame.Rect(220, 540, 60, 30)
```

---

# Step 3: Move the Player (10 Marks)

## Task

Allow the player to move:

- ⬅ Left Arrow → Move Left
- ➡ Right Arrow → Move Right

Prevent the player from leaving the game window.

### Hint 💡

Use:

```python
pygame.key.get_pressed()
```

---

# Step 4: Create Falling Coins (10 Marks)

## Definition

Coins appear randomly at the top of the screen and move downward.

### Task

- Generate coins randomly.
- Store them inside a list.
- Move every coin downward.
- Remove coins after they leave the screen.

### Hint 💡

```python
coins = []
```

Create new coins using:

```python
pygame.Rect()
```

---

# Step 5: Catch Coins & Increase Score (10 Marks)

## Task

When the player catches a coin:

- Remove the coin.
- Increase the score.
- Display the updated score.

### Hint 💡

Use:

```python
colliderect()
```

---

# Step 6: Create Falling Bombs (10 Marks)

## Definition

Bombs work like coins, but they decrease the player's lives.

### Task

- Generate bombs randomly.
- Move them downward.
- Remove bombs after they leave the screen.

### Hint 💡

Create another list.

```python
bombs = []
```

---

# Step 7: Lives System (10 Marks)

## Task

- Start the game with **3 lives**.
- Every time the player touches a bomb:
  - Remove the bomb.
  - Lose one life.
- Display the remaining lives.

### Example

```
Lives: 3

↓

Lives: 2

↓

Lives: 1
```

---

# Step 8: Game Over Screen (10 Marks)

## Task

When lives become **0**:

Display:

- GAME OVER
- Final Score
- High Score
- Press **R** to Restart
- Press **Q** to Quit

### Hint 💡

Use a Boolean variable.

Example:

```python
game_over = False
```

---

# Step 9: High Score System (10 Marks)

## Definition

A **High Score** is the best score the player has achieved.

Store it inside a text file.

### Task

- Load the High Score when the game starts.
- Save a new High Score when the player beats the previous one.

### Hint 💡

Use:

```python
open()
```

Example:

```python
with open("score.txt", "r") as file:
```

---

# Step 10: Restart the Game (10 Marks)

## Task

When the Game Over screen appears:

- Press **R** → Start a new game
- Press **Q** → Exit the game

When restarting:

- Reset score
- Reset lives
- Clear all coins
- Clear all bombs
- Move the player back to the starting position

---

# Bonus Challenge (+20 Marks)

Complete **any FOUR** of the following:

⭐ Add different types of coins.

⭐ Golden Coin (+50 Points)

⭐ Silver Coin (+20 Points)

⭐ Bronze Coin (+10 Points)

---

⭐ Add sound effects.

---

⭐ Add background music.

---

⭐ Increase game speed every 100 points.

---

⭐ Display the current level.

---

⭐ Add Pause/Resume using **P**.

---

⭐ Add a Start Menu.

---

⭐ Add power-ups:

- Shield
- Double Score
- Slow Motion

---

⭐ Add different bomb sizes.

---

⭐ Add animations when collecting a coin.

---

⭐ Display FPS.

---

⭐ Add a Countdown before the game starts.

---

# Submission Requirements

Submit:

- ✅ Python (`.py`) source code
- ✅ High Score text file
- ✅ Screenshot of the game
- ✅ Short README explaining:
  - Controls
  - Features
  - Bonus features completed

---

# Marking Breakdown

| Step | Marks |
|------|------:|
| Step 1 – Game Window | 10 |
| Step 2 – Player | 10 |
| Step 3 – Player Movement | 10 |
| Step 4 – Falling Coins | 10 |
| Step 5 – Coin Collection & Score | 10 |
| Step 6 – Falling Bombs | 10 |
| Step 7 – Lives System | 10 |
| Step 8 – Game Over Screen | 10 |
| Step 9 – High Score | 10 |
| Step 10 – Restart Game | 10 |
| **Total** | **100** |

---

# ✅ Expected Outcome

After completing all the steps, your game should:

- 🪙 Generate random falling coins.
- 💣 Generate random falling bombs.
- 🎮 Allow the player to move left and right.
- 🏆 Increase the score when coins are collected.
- ❤️ Decrease lives when bombs are hit.
- 💾 Save the High Score.
- 🔄 Allow the player to restart the game.
- ❌ Allow the player to quit the game.

🎉 Congratulations! By following each step, you will have built a complete **Catch the Coins** game using **Python and Pygame**.