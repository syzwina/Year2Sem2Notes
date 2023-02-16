we use graphs to represent **entities and the relationships between them**
graphs allow us to reason the connections
graphs can help us visualise the information
	some choices to visualisation can help
	use visualisation algorithms

# Directed Graphs

![[../../images/Pasted image 20230213125158.png]]

## Path

![[../../images/Pasted image 20230213125336.png]]

## Spanning Subgraphs

![[../../images/Pasted image 20230213125542.png]]

- the nodes does not need all of the nodes to be connected
- if we want all the vertices to be connected, we're want a spanning tree

## Operations

![[../../images/Pasted image 20230213130010.png]]

## Adjacency List

![[../../images/Pasted image 20230213130143.png]]

### Space and Time Complexity of Adjacency List

![[../../images/Pasted image 20230213130343.png]]

## Adjacency Matrix

![[../../images/Pasted image 20230213130705.png]]

### Space and Time Complexity of Adjacency Matrix

![[../../images/Pasted image 20230213130742.png]]

## Deciding on Representation

![[../../images/Pasted image 20230213131118.png]]

Adjacency List
- a large social network
	- sparse graph
	- needs quick SUCCS operation to get list of friends
