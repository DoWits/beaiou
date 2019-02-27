# State

- Game
	- board state (all pieces state)
	- player turn
	- mirror moved in last turn

- Player (x2)
	- position
	- orientation

- Mirror (x4)
	- position
	- orientation

# Conventions

Mirrors: M1, M2, M3, M4
Players: P1, P2
Player Orientation: U | D | L | R
Mirror Orientation: +1 | -1
Piece Move: U | D | L | R

*Board Positions for Game State*  

30 31 32 33
20 21 22 23
10 11 12 13
00 01 02 03  

# Current State

### Game Table (1x2)

| Player Turn | Last Mirror Moved |
| ----------- | ----------------- |
| P1		  | 				  |
| P2		  | 	M2			  |
| P1		  | 	M1			  |
| P2		  | 				  |
| P1		  | 	M4			  |

### Piece Table(6x3)

| Piece	| 	Position | 	Orientation |
| ----- | ---------- | ------------ |
| P1	|	(0,0)	 |	U			|
| P2	| 	(3,3)	 |	D			|
| M1	| 	(1,1)	 |	+1			|
| M2	| 	(1,2)	 |	-1			|
| M3	| 	(2,1)	 |	+1			|
| M4	| 	(2,2)	 |	-1			|

# Logs

player 1: M1 Move U  
player 2: P2 Rotate L  
player 1: M2 Rotate L  
player 2:   
player 1: P1 Move U   
player 2: M2 Move L  
player 1: M3 Rotate R  
player 2: P2 Move D  
...  
...  
...  
...  
player 2: M2 Rotate L  
P2 win  

# Winning State

Args: Game state (having player's turn)
O/P: Arrow goes and hits the opponent => True

```
function winning(gamestate) {
	if able to hit:
		return True
	else:
		return False
}
```

# Minmax challenges

1. Getting to terminal state: In Tic-Tac-Toe, one of the terminating states is that all the positions are filled after 9 turns. This is not the case with DoW. So the tree could almost be infinitely deep. 

# Notes about the Game

- Maximum moves/orientations by a piece (mirror or player): 6 with 4 movements and 2 rotations
- On most occasions, it is good to change the game state. If not, it is as if you are giving the opponent two chances to play. When the opponent makes a bad move, there is a possibility to cash in by just shooting.


