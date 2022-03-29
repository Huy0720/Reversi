# Reversi
This game was built for our Computational Thinking For Design 1D project in Python, where we are required to write our own python-based computer game that has a text-based user interface.

Group 10 Team Members:
- Raphael Yee
- Kailin Chen
- Anushree Rawat
- Nguyen Thai Huy

## Description
Reversi is a strategy board game played on an 8x8 or 4x4 board. 

The game is played using identical game pieces called discs (denoted as tiles in the documentation), which are white on one side and black on the other. 

The game begins with four disks placed in a square in the middle of the grid, two facing white-side-up, two black-side-up, so that the same-colored disks are on a diagonal. 
Players take turns placing disks on the board by inputting the coordinate in (x,y) format, where x denotes the horizontal position while y indicates the vertical position. 

During a play, any disks of the opponent's color that are in a straight line and bounded by the disk just placed and another disk of the current player's color are turned over to the current player's color.

The objective of the game is to capture as many disks as possible until there is no valid move available. The player with the most pieces on the board at the end of the game wins; the game can also end in a draw when 2 players end up with the same number of disks.

We implemented a local variation of the game that we grew up playing as kids. The game ends as long as the player has no valid moves (not both). This removes the need for timed moves and allows us to shorten the length of each game.

## Key Notes
**Using Matplotlib to display the board**

One bug we encountered is that the game is unplayable when run as a python file. This is because Matplotlib runs its own event loop which blocks the main thread. This is circumvented by running the game in an iPython notebook as Jupyter/browser runs its own event loop.

**Check_valid_moves**

To check every single tile on the board is inefficient because we really only need to check adjacent tiles to the already played tiles on the board. If we had more time, we can consider implementing a better check_valid_moves function. Improving this function will also allow us to build a possible “AI” that won’t take too long to compute look-aheads / simulate game moves in the future before picking the best move.

**Why use a class?**

We imagined a fictitious scenario where Magnus Carlsen would play multiple Reversi games on our Jupyter notebook at once. :P 

Thank you for reading :) We had fun implementing this game.

## Dependencies
- Setup pip install -r requirements.txt
- Matplotlib ( to display the game board)
