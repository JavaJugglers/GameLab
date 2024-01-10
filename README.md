# Project Background

I've undertaken an exciting journey to recreate the classic single-player computer game "2048," originally designed by Gabriele Cirulli. This game, influenced by "1024" from Veewo Studio, captivates players with its simple yet challenging puzzle mechanics. In this project, I focused on building the core logic of 2048.

### Game Overview

2048 is played on a 4x4 grid where each cell can be empty or hold a tile with a power-of-2 value. The game starts with one tile, randomly placed, with a value of either 2 or 4. Players use arrow keys to tilt the board, causing tiles to slide and merge under specific rules, thus altering the board and scoring points. The game's objective is to create a tile with the value 2048.

### Implementation Details

#### Constructors
- **Model(int size):** Initializes a game board of a specified size.
- **Model(int[][] rawValues, int score, int maxScore, boolean gameOver):** Constructs a game state from given parameters, reflecting a specific game situation.

#### Key Methods
- **emptySpaceExists(Board b):** Checks for any empty space on the board.
- **maxTileExists(Board b):** Determines if a tile with the maximum value (2048) exists.
- **atLeastOneMoveExists(Board b):** Evaluates if any valid moves are left.
- **tilt(Side side):** Manages the movement and merging of tiles based on the direction of tilt (arrow key input).

### Game Mechanics

1. **Tile Merging:** Tiles with the same value merge into a tile of double value. Merged tiles cannot merge again in the same move.
2. **Move Strategy:** Players use arrow keys to slide tiles. Tiles slide as far as possible in the chosen direction until they are blocked by another tile or the board's edge.
3. **Scoring:** Each merge adds the new tile's value to the player's score.
4. **Game Over Conditions:** The game ends when no moves are possible or a tile with 2048 appears.

### Design Patterns

The project applies the Model-View-Controller (MVC) and Observer design patterns, segmenting the game's logic, user interface, and the intercommunication between these components.

### Challenges and Learning

This project presented an excellent opportunity to work with a complex codebase, fostering skills in reading, understanding, and modifying existing code. Implementing the `tilt` method was particularly challenging, requiring a deep understanding of the game's mechanics and careful consideration of different game states and tile movements.

### Testing

Comprehensive unit and integration tests were provided to ensure the correctness of each component and their interaction. These tests played a crucial role in validating the game's logic and mechanics.

### Conclusion

Developing the 2048 game logic was both challenging and rewarding. It enhanced my understanding of complex game mechanics, object-oriented programming, and working within established codebases. This experience has significantly contributed to my growth as a software developer.
