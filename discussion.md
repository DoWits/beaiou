# State

- Game
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

# Current State

Game Table (1x2)
| Player Turn | Last Mirror Moved |
|-------------|-------------------|
| P1		  | 				  |
| P2		  | 	M2			  |
| P1		  | 	M1			  |
| P2		  | 				  |
| P1		  | 	M4			  |

Piece Table(6x3)
| Piece	| 	Position | 	Orientation |
|-------|------------|--------------|
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

