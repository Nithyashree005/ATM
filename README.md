# ATM
🔹 1. Recognize the Draw Scenario
A game ends in a draw when:

The board is completely filled, AND

No player has won yet.





🔹 2. Create a New Method isBoardFull()
This method checks every cell of the board:

public static boolean isBoardFull(char[][] board) {
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            if (board[i][j] == ' ') {
                return false; // If any empty cell exists, board is not full
            }
        }
    }
    return true; // All cells are filled
}





🔹 3. Add the Draw Check Inside the Game Loop
After placing a move and checking for a win:

if (won(board, player)) {
    // Player wins
} else if (isBoardFull(board)) {
    // It's a draw
}
✅ This ensures:

If no one wins after a move,

And the board is full,

Then it's declared a draw.





🔹 4. Print the Final Result
If the board is full and no win:

System.out.println("It's a draw!");
Also, set:

gameover = true;
So the loop ends.






🔹 5. Full Flow in Game Loop
In order:

Print board

Take input

Validate input

Place move

Check won(board, player)

If not won, check isBoardFull(board)

If full, print "It's a draw!"

If not full, switch player

