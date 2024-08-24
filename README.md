# Tic_Tac_Toe
This HTML and JavaScript code implements a simple Tic Tac Toe game. The HTML sets up the structure with a 3x3 grid of buttons, which serve as the game board, and a "Restart Game" button to reset the game. The grid is styled using CSS to be visually appealing, with each cell having a size of 100x100 pixels, a white background, a black border, and a hover effect that changes the background color to a light shade. The game is designed to be interactive, allowing users to play by clicking on the cells to place their 'X' or 'O'.

The JavaScript code handles the core functionality of the game. It starts by selecting all cells using document.querySelectorAll and initializing the game state. A variable isXTurn is used to keep track of whose turn it is, with 'X' starting first. The winPatterns array defines all possible winning combinations of cell indices.

The checkWin function iterates through these win patterns to determine if any player has achieved a winning combination. If a winning condition is detected, an alert announces the winner, and all click event listeners on cells are removed to prevent further moves.

The handleClick function is called whenever a cell is clicked. It first checks if the cell is already filled; if not, it places the current player's mark ('X' or 'O') in the cell. After making a move, it calls checkWin to see if the move resulted in a win. If a win is detected, it alerts the winner and disables further clicks. If no win is found, it then checks if the board is full using the checkTie function.

The checkTie function determines if the game has ended in a tie by checking if all cells contain a mark. If all cells are filled and no winner is found, it alerts a tie.

The startGame function resets the board by clearing all cell contents and re-enabling click events on each cell to allow a new game to start. This function is called initially to set up the game and whenever the "Restart Game" button is clicked.

In summary, this code creates a fully functional Tic Tac Toe game where two players can take turns clicking cells to place their marks, with automatic win and tie detection, and a restart feature to play multiple rounds.
