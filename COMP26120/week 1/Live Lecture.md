# Simple Graph
- no parallel edges (two edges w the same origin and destination)
	(A,B)
	(A,B)
- no self-loops
	(B,B)
	we'll see self-loops in disjoint sets

# What would be the most reasonable representation of a Railway Network as a Graph?
- Undirected Graph
	no
	- circle line, anticlockwise and clockwise
	- direction is very important
- Directed Acyclic Graph
	no
	- we need cycles
- Adjacency List
	yes
- Adjacency Matrix
	no
	- if you want to get the SUCCS, it'll take bloody ages
	- you want to know what stations you can get to from that station quicly

# I want to know which stations I can get to within X stops of my current location. How would you compute this EFFICIENTLY? UNEFFICIENTLY?
- Depth First Search
	UNefficient
- Breadth First Search
	efficient

# My travelling buddy wants to know if there is a 'Ring' Line on a Train network. I don't have a visual representation, but I have Graph data!
- follow station by station on the graph and see if it loops back
- use topological sort
- Depth First Search