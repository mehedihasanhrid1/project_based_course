# 🎮 Python Assignment: Catch the Coins Game
**Course:** Python Programming with Pygame  
**Total Marks:** 100  
**Difficulty:** Intermediate  
**Estimated Time:** 3–5 Hours

---

# 📌 Objective

Create a **Catch the Coins** game using **Python** and **Pygame**. The player controls a basket (or catcher) that collects falling coins while avoiding bombs. The game should track the player's score, lives, and highest score.

---

# 🎯 Learning Outcomes

By completing this assignment, students will learn:

- Working with the Pygame library
- Game loop implementation
- Keyboard input handling
- Collision detection
- Random object generation
- File handling (High Score System)
- Functions and modular programming
- Game state management

---

# 📝 Task Description

Develop a game where:

- The player moves left and right.
- Coins randomly fall from the top.
- Bombs also randomly fall.
- Collecting coins increases the score.
- Hitting bombs decreases lives.
- The game ends when all lives are lost.
- The highest score is saved permanently in a text file.

---

# ✅ Requirements

## Task 1 — Create the Game Window (10 Marks)

Create a game window with:

- Width: **500**
- Height: **600**
- Window title:
  ```
  Catch the Coins
  ```

The game should run at **60 FPS**.

---

## Task 2 — Create the Player (10 Marks)

Create a player object using `pygame.Rect`.

Requirements:

- Positioned near the bottom of the screen.
- Can move:
  - Left Arrow ⬅
  - Right Arrow ➡
- Cannot move outside the game window.

---

## Task 3 — Falling Coins (15 Marks)

Create coins that:

- Spawn randomly from the top.
- Fall downward continuously.
- Disappear after leaving the screen.
- Increase the player's score when collected.

### Bonus

Instead of adding a fixed score, award a **random value between 10 and 20**.

---

## Task 4 — Falling Bombs (15 Marks)

Create bombs that:

- Spawn randomly.
- Fall slightly faster than coins.
- Remove one life when touching the player.
- Disappear after collision.

---

## Task 5 — Score System (10 Marks)

Display:

- Current Score

The score should increase whenever a coin is collected.

---

## Task 6 — Lives System (10 Marks)

The player starts with:

```
Lives = 3
```

Every bomb collision decreases one life.

When lives become **0**, the game should stop.

---

## Task 7 — High Score System (15 Marks)

Implement a permanent high score system.

Requirements:

- Create a file named:

```
coinscore.txt
```

- If the file does not exist:
  - Create it.
  - Store `0`.

- At game over:
  - Compare current score with the saved high score.
  - Save the new score if it is greater.

Display the High Score during gameplay.

---

## Task 8 — Game Over Screen (10 Marks)

When the game ends:

Display:

- GAME OVER
- Final Score
- High Score

Also display:

```
Press R to Play Again

Press Q to Quit
```

---

## Task 9 — Restart Function (5 Marks)

Pressing **R** should:

- Reset score
- Reset lives
- Remove all coins
- Remove all bombs
- Move player back to starting position
- Start the game again

---

# 📋 Functional Requirements Checklist

Your game must include all of the following:

- Game window
- Player movement
- Falling coins
- Falling bombs
- Collision detection
- Random scoring (10–20)
- Score display
- Lives display
- High score saved in a file
- Game over screen
- Restart option
- Quit option

---

# 💡 Hints

### Creating the Player

```python
player = pygame.Rect(x, y, width, height)
```

---

### Random Object Position

```python
random.randint(start, end)
```

---

### Collision Detection

```python
rect1.colliderect(rect2)
```

---

### Saving High Score

```python
with open("coinscore.txt", "w") as file:
    file.write(str(high_score))
```

---

### Reading High Score

```python
with open("coinscore.txt", "r") as file:
    high_score = int(file.read())
```

---

### Drawing Shapes

Rectangle

```python
pygame.draw.rect(...)
```

Ellipse

```python
pygame.draw.ellipse(...)
```

Circle

```python
pygame.draw.circle(...)
```

---

# 📂 Project Structure

```
CatchTheCoins/
│
├── main.py
└── coinscore.txt
```

---

# ⭐ Bonus Features (Extra Credit)

Implement **any two** of the following:

- Sound effects
- Background music
- Pause feature (P key)
- Increasing difficulty over time
- Animated player
- Different coin values
- Power-up items
- Countdown timer
- Background image
- Custom player sprite

---

# 📤 Submission Requirements

Submit a ZIP file containing:

- `main.py`
- `coinscore.txt`
- Any assets used (images, sounds, fonts)
- A screenshot of the game running

---

# 📊 Marking Rubric

| Criteria | Marks |
|-----------|------:|
| Game Window & FPS | 10 |
| Player Movement | 10 |
| Coin System | 15 |
| Bomb System | 15 |
| Score System | 10 |
| Lives System | 10 |
| High Score File Handling | 15 |
| Game Over & Restart | 10 |
| Code Quality & Readability | 5 |
| **Total** | **100** |

---

# 🚫 Important Rules

- Use **Python** and **Pygame** only.
- Write clean, well-organized code.
- Use meaningful variable names.
- Divide your program into functions whenever possible.
- Your program should run without errors.
- Comment important sections of your code.

---

# 🎯 Expected Output

Your final game should allow the player to:

- Move left and right
- Catch falling coins
- Avoid bombs
- Earn random points
- Lose lives on bomb collisions
- Save the highest score permanently
- Restart the game after losing
- Quit the game using the keyboard
