# Snake Game

This project is a classic **Snake Game** built using Python and the Tkinter library. Players control a snake to collect food, increasing the snake's length and score. The game ends when the snake collides with itself or the game boundaries.

## Features

- **Real-time Gameplay**: Smooth and responsive snake movement.
- **Score Tracking**: Displays the current score.
- **Game Over Screen**: Displays a message when the game ends.
- **Arrow Key Controls**: Navigate the snake using keyboard arrow keys.

## Prerequisites

Ensure you have Python installed on your system. This game requires the Tkinter library, which is bundled with most Python installations.

## How to Run

1. Copy the script into a `.py` file, e.g., `snake_game.py`.
2. Run the script using the command:
   ```bash
   python snake_game.py
   ```
3. The game window will open. Use the arrow keys to control the snake.

## Gameplay Instructions

1. Use the **arrow keys** to navigate the snake:
   - **Left Arrow**: Move left
   - **Right Arrow**: Move right
   - **Up Arrow**: Move up
   - **Down Arrow**: Move down
2. Collect the green food to increase your score.
3. Avoid colliding with the walls or the snake's body.
4. The game ends when a collision occurs.

## Code Breakdown

### 1. **Snake Class**
- Handles the creation and movement of the snake.
- Initializes with a default size of 3 body parts.
- Adds new segments when the snake eats food.

### 2. **Food Class**
- Generates food at random locations on the canvas.
- Draws a green circle to represent the food.

### 3. **Main Functions**

- **next_turn(snake, food)**: Updates the game state for each frame.
- **change_direction(new_direction)**: Changes the snake's direction based on user input.
- **check_collisions(snake)**: Checks if the snake collides with the walls or itself.
- **game_over()**: Ends the game and displays a "Game Over" message.

### 4. **Key Bindings**

The arrow keys are bound to the snake's movement using:
```python
window.bind('<Left>', lambda event: change_direction('left'))
window.bind('<Right>', lambda event: change_direction('right'))
window.bind('<Up>', lambda event: change_direction('up'))
window.bind('<Down>', lambda event: change_direction('down'))
```

## Customization

- **Game Speed**: Adjust the `SPEED` variable (default is 70ms).
- **Snake and Food Colors**: Change `SNAKE_COLOR` and `FOOD_COLOR`.
- **Game Dimensions**: Modify `GAME_WIDTH` and `GAME_HEIGHT`.

## Example Output

- **Initial Screen**:
  The snake starts as a blue rectangle with three segments, and the score is displayed at the top.

- **Gameplay**:
  Collect food (green circles) to grow the snake and increase the score.

- **Game Over Screen**:
  A red "GAME OVER" message is displayed when the game ends.

## Dependencies

- **Tkinter**: Built into Python, no external installation required.

## License

This project is open-source and available under the MIT License. Feel free to use and modify it for your purposes.
