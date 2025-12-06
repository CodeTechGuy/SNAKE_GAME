# 🐍 Snake Game 

<p align="center"> <img src="https://img.shields.io/badge/Game-Snake-%2300FF7F?style=for-the-badge&logo=python&logoColor=white" /> <img src="https://img.shields.io/badge/HTML-%23E34F26?style=for-the-badge&logo=html5&logoColor=white" /> <img src="https://img.shields.io/badge/CSS-%231572B6?style=for-the-badge&logo=css3&logoColor=white" /> <img src="https://img.shields.io/badge/JavaScript-%23F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" /> </p>

A classic Snake game implemented using fundamental web technologies (HTML, CSS, and pure JavaScript).

<img width="3092" height="1633" alt="Image" src="https://github.com/user-attachments/assets/291a2741-94d7-45bc-afc1-7ced2a0fb665" />

## 🚀 How to Play

1.  Open the `index.html` file in your web browser.
2.  Click the **"Start Game"** button.
3.  Use the **Arrow Keys** to navigate the snake and eat the red food blocks.

### 🕹️ Controls

| Key | Action |
| :---: | :--- |
| **Arrow Up** | Move Up |
| **Arrow Down** | Move Down |
| **Arrow Left** | Move Left |
| **Arrow Right** | Move Right |

## ✨ Features

* **Game Loop:** The snake's movement is managed by a constant game loop set at a fixed interval (300ms).
* **Collision Detection:** The game ends if the snake's head hits any of the **four walls** of the board.
* **Scoring & Persistence:**
    * The current score is tracked in real-time.
    * The **High Score** is saved locally in the browser's `localStorage`.
* **Time Tracking:** A game timer tracks the minutes and seconds of the current round.
* **Start/Game Over Modals:** Simple modal screens are used to control the game flow and allow for restarts.

## 💻 Project Structure

The project consists of three files defining the structure, style, and logic:

| File | Description |
| :--- | :--- |
| `index.html` | Provides the layout (board, scores, modals) and links the stylesheet and script. |
| `style.css` | Handles all styling, including variables for colors, board layout using CSS Grid, and styles for the snake (`.fill`) and food (`.food`). |
| `script.js` | The game engine. Handles dynamic board creation, snake movement logic, collision checks, food generation, score updates, and user input via keydown events. |

## 🛠 Installation

No dependencies needed.

Just clone the repo:
 ```
git clone https://github.com/CodeTechGuy/snake-game.git
cd snake-game
```


Open:
```
index.html
```

You're ready to play! 🎉


## ⚙️ Implementation Details

### Game Board
The board is created dynamically based on the container size and populated with `div.block` elements, which are stored in a JavaScript object (`blocks`) mapped by their coordinates (`"row-col"`).

### Game Logic (`script.js`) 
Movement and updates are handled inside the `render()` function, which runs on an interval:
1.  Calculates the new head position based on the current `direction`.
2.  Checks for wall collision.
3.  Checks for food consumption: If consumed, the snake is *not* shortened (`snake.pop()` is skipped), and the score is incremented.
4.  Updates the snake's position: New head is added (`snake.unshift(head)`) and the tail is removed (`snake.pop()`) unless food was just eaten.
5.  Updates the visual state by adding/removing the `.fill` class on the block elements.

## 🙌 Author

Made with ❤️ by Vishal Prajwal S

If you like this project, please ⭐ star the repo — it helps a lot!
