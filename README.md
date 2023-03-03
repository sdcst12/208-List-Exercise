# Creating a Game

### Introduction
Trying to capitalize on the success of board games like Chess, game designers would like to develop a turn based strategy game that is more accessible to a larger audience. The game will use a chessboard, and have multiple different pieces, like Chess, with the goal of capturing the King, like in Chess.  Our task is to bring it to life.

[image]https://www.regencychess.co.uk/images/how-to-set-up-a-chessboard/how-to-set-up-a-chessboard-1a.jpg[/image]
We will use the chessboard and it's coordinate system to identify squares.  Note that each row has a letter and each column has a number.  * a1: indicates the square in the bottom left
* h8: indicates the square in the top right

#### Game Pieces
We will use chess pieces to denote the following:
Queen : 6 points
Rook : 5 points
Knight: 4 points
Bishop: 3 points
King: 2 points
Pawn: 1 point

#### Game Setup
Each player sets up their pieces in any order they want, in any locations on the first 2 rows nearest them.  White, for example, places all their pieces in rows A and B, Black places all their pieces in G and H.

#### Objective
Kill the enemy king

#### Game Play
Each player takes turns.  A piece can move any distance diagonally or down rows or columns.  It may jump over its own pieces provided that they are of lesser points value, but not enemy players. If it lands on an enemy tile, a battle is determined to have occurred.

#### Battle Resolution
Pawns may not make attacks into the AB or GH ranks.  There is no reward for a pawn reaching the last row of the board.
If an attacker is of equal points value or higher, the defender is eliminated and the attacker takes the square.
If an attacker is 1 rank below the defender, then both pieces are eliminated.
If an attacker is 2 or more ranks below the defender, the attacker is eliminated and the defender is reduced in power by 1 rank and replaced with the appropriate piece. 3 point pieces are eliminated if attacked by a pawn.

## Task 1
Create a dictionary variable to keep track of pieces for each player and their location on the board
You could use this variable. Is it the best one? Can you think of a better one?
```
pieces = [
  0 : {
    6 : ['a2'],
    5 : ['a1','c1'],
    4 : [],
    3 : [],
    2 : ['a3'],
    1 : []
    },
  1 : {
    6 : [],
    5 : [],
    4 : [],
    3 : [],
    2 : [],
    1 : []
    }
   ]
```
## Task 2
Create a function to display the contents of the board 

## Task 3
Have a user be able to place their 16 pieces on the board. We will worry only about white for now, but if you want to, you can also add blacks pieces.  It would be best to take turns, with white placing first followed by black.

## Task 4
Create a function that checks to see where valid squares are for a piece that is selected.  This should be a list so that when a user selects a piece to move, we can check their target square to see if it is an empty square or contains an enemy  that can be attacked.  Display this list.
