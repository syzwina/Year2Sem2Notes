# Shortest Path Algorithm

# Propose a deterministic algorithm that will solve a Rubik's Cube with the fewest moves.

- Data Structure
- Algorithm

1. Have a data structure to represent the state of the Rubik's Cube
	- use a directed graph
2. Represent the relationship beween states of the Rubik's Cube as the edges of the graph
	to get from one state to other must only involve one move
3. Use BFS to find shortest path from current state to solved state

