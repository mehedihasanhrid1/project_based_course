# 🎮 Python Pygame Assignment
# Assignment: Space Defender 🚀👾

**Course:** Python with Pygame  
**Total Marks:** 100  
**Difficulty:** Beginner → Intermediate

---

# 🎯 Learning Outcomes

After completing this assignment, students will be able to:

- Initialize and use Pygame
- Create a game window
- Draw game objects using `pygame.draw`
- Handle keyboard input
- Generate random enemies
- Detect collisions
- Work with lists
- Use functions
- Save and load data using text files
- Build a complete arcade-style game

---

# 📖 Project Scenario

Earth is under attack!

Enemy spaceships are entering the screen from the top.

Your mission is to protect Earth by controlling your spaceship and shooting down enemies before they reach the bottom.

The game ends when all lives are lost.

Your highest score should be saved so players can try to beat their record.

---

# 🕹 Game Requirements

Your game should include:

- A player spaceship
- Enemy spaceships
- Bullets
- Score system
- Lives system
- High Score system
- Restart option
- Game Over screen

> **Important:**  
> Every game object must be created using **pygame.draw()** functions only.
>
> ❌ No image files.
>
> ✅ Use:
>
> - `pygame.draw.rect()`
> - `pygame.draw.circle()`
> - `pygame.draw.polygon()`
> - `pygame.draw.line()`

---

# Step 1 — Import Libraries & Initialize Pygame
**Marks: 5**

## Objective

Import required libraries.

Initialize Pygame.

### Required Libraries

- pygame
- random
- sys

### Template

```python
import ______
import ______
import ______

pygame._______()
```

### Hint

Use the function that starts every pygame module.

---

# Step 2 — Create the Game Window
**Marks: 8**

## Objective

Create a game window.

Requirements

- Width = 500
- Height = 700
- Title = Space Defender

### Template

```python
WIDTH = _____
HEIGHT = _____

window = pygame.display.__________((WIDTH, HEIGHT))

pygame.display.____________("Space Defender")
```

---

# Step 3 — Create Fonts and Clock
**Marks: 5**

## Objective

Create

- Game clock
- Normal font
- Large font

### Template

```python
clock = pygame.time._______()

font = pygame.font.SysFont(None, ____)

big_font = pygame.font.SysFont(None, ____)
```

---

# Step 4 — Create the Player
**Marks: 8**

## Objective

Create the player rectangle.

Requirements

- Width = 50
- Height = 40

Suggested Position

```
x = 225
y = 620
```

### Template

```python
player = pygame.Rect(
    _____,
    _____,
    _____,
    _____
)
```

---

# Step 5 — Create Game Variables
**Marks: 8**

## Objective

Create variables for

- Enemies
- Bullets
- Score
- Lives
- Game Over

### Template

```python
enemies = []

bullets = []

score = ____

lives = ____

game_over = ______
```

---

# Step 6 — Create the High Score System
**Marks: 12**

## Objective

Create

- load_high_score()
- save_high_score()

Store the score inside

```
highscore.txt
```

### Template

```python
def load_high_score():

    try:

        with open("____________", "r") as file:

            return int(file.read())

    except:

        with open("____________", "w") as file:

            file.write("0")

        return 0
```

---

# Step 7 — Create reset_game()
**Marks: 8**

## Objective

Reset

- Score
- Lives
- Enemy list
- Bullet list
- Player position
- Game Over status

### Template

```python
def reset_game():

    global ______________________

    score = ____

    lives = ____

    enemies = []

    bullets = []

    player.x = _____

    game_over = ______
```

---

# Step 8 — Create the Main Game Loop
**Marks: 5**

## Objective

Create the game loop.

### Template

```python
while ______:

    clock.tick(60)
```

---

# Step 9 — Handle Events
**Marks: 8**

## Objective

Handle

- Quit
- Shoot Bullet (Space)
- Restart (R)
- Quit Game (Q)

### Template

```python
for event in pygame.event.get():

    if event.type == __________:

        pygame.quit()

        sys.exit()
```

---

# Step 10 — Move the Player
**Marks: 8**

## Objective

Move

⬅ Left Arrow

➡ Right Arrow

Prevent the player from leaving the screen.

### Template

```python
keys = pygame.key.get_pressed()

if keys[____________]:

    player.x -= 7

if keys[____________]:

    player.x += 7
```

---

# Step 11 — Fire Bullets
**Marks: 8**

## Objective

Create bullets when the player presses SPACE.

Requirements

- Bullet starts from the center of the spaceship.
- Store bullets in a list.

### Template

```python
if event.key == __________:

    bullets.append(
        pygame.Rect(...)
    )
```

---

# Step 12 — Generate Enemy Spaceships
**Marks: 8**

## Objective

Randomly generate enemies.

Requirements

- Random X position
- Start above the screen
- Store in a list

### Template

```python
if random.randint(1, _____) == 1:

    enemies.append(
        pygame.Rect(...)
    )
```

---

# Step 13 — Move Bullets & Detect Collision
**Marks: 10**

## Objective

For every bullet

- Move upward
- Remove when outside the screen
- Destroy enemy on collision
- Increase score

### Template

```python
for bullet in bullets[:]:

    bullet.y -= ____

    if bullet.bottom < 0:

        __________

    for enemy in enemies[:]:

        if bullet.colliderect(enemy):

            __________

            score += 10
```

---

# Step 14 — Move Enemies & Reduce Lives
**Marks: 10**

## Objective

For every enemy

- Move downward
- Remove if outside screen
- Lose one life
- End game when lives reach zero

### Template

```python
for enemy in enemies[:]:

    enemy.y += ____

    if enemy.top > HEIGHT:

        enemies.remove(enemy)

        lives -= ____

        if lives <= 0:

            game_over = ______
```

---

# Step 15 — Draw Everything
**Marks: 8**

## Objective

Draw

- Player spaceship
- Enemy spaceships
- Bullets
- Score
- Lives
- High Score

### Hint

Use only

```python
pygame.draw.rect()

pygame.draw.circle()

pygame.draw.polygon()

pygame.draw.line()

font.render()
```

---

# Step 16 — Create the Game Over Screen
**Marks: 8**

## Objective

Display

- GAME OVER
- Final Score
- High Score
- Press R to Restart
- Press Q to Quit

### Template

```python
if game_over:

    over_text = big_font.render(
        "GAME OVER",
        True,
        (255,80,80)
    )
```

---

# Step 17 — Update the Display
**Marks: 3**

## Objective

Refresh the screen every frame.

### Template

```python
pygame.display.__________()
```

---

# 🌟 Bonus Challenge (+10 Marks)

Complete **ONE** or more of the following:

- 💥 Explosion animation using circles
- ⭐ Power-up that shoots three bullets
- ❤️ Heart icons instead of text lives
- 🎵 Background music
- 🔊 Laser sound effects
- 🚀 Speed increases every 20 points
- 🛡 Temporary shield power-up
- 🌌 Animated star background
- 🎯 Boss enemy every 100 points
- ⚡ Rapid-fire mode for 5 seconds

---

# 📊 Marking Breakdown

| Step | Task | Marks |
|------|------|------:|
|1|Import & Initialize|5|
|2|Game Window|8|
|3|Clock & Fonts|5|
|4|Player|8|
|5|Variables|8|
|6|High Score|12|
|7|Reset Game|8|
|8|Main Loop|5|
|9|Events|8|
|10|Player Movement|8|
|11|Shoot Bullets|8|
|12|Enemy Generation|8|
|13|Bullet Collision|10|
|14|Enemy Movement|10|
|15|Drawing Objects|8|
|16|Game Over Screen|8|
|17|Display Update|3|

**Total: 100 Marks**

---

# 📁 Submission Requirements

Submit the following files:

```
main.py
highscore.txt
```

Also include:

- 📸 One screenshot of the running game
- 🎥 *(Optional)* 30–60 second gameplay video

---

# ✅ Expected Output

Your completed game should:

- Open a game window.
- Allow the spaceship to move left and right.
- Shoot bullets using the Space key.
- Randomly generate enemy spaceships.
- Destroy enemies using bullets.
- Increase the score for every enemy destroyed.
- Reduce lives when enemies escape.
- Save the highest score.
- Show a Game Over screen when lives reach zero.
- Allow the player to restart by pressing **R** or quit by pressing **Q**.

---

# 💡 Tips

- Build the game **step by step**.
- Test your program after completing each step.
- Save your work frequently.
- Read error messages carefully—they often tell you exactly what needs to be fixed.
- Use functions to keep your code organized.
- Draw every object using **pygame.draw()** instead of image files.

Good luck, Commander! 🚀👾