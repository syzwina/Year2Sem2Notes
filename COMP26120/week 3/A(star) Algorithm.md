![[../../images/Pasted image 20230214162544.png]]

Dijkstra's Algorithm is still quite long
- explore **all nodes**
- only considers the weight of the edge

A* Algorithm 
- cuts down on the search using a heuristic approach
- considers weight of the edge + how far are we from the goal node
	- so A* algorithm will prioritise paths that are taken roughly in the right direction
	- it'll prioritise paths that take us closer to goal node

`heuristic(u) =  D(u) + Eucladian distance to Munich/100` 
we will be ranking stations that are closer to Munich higher in the Priority Queue

- we terminate once we found goal node
	- this will cut out a lot of searching time

![[../../images/Pasted image 20230214163243.png]]

this is why we do 
`Eucladian distance to Munich/100` 
instead of just
`Eucladian distance to Munich

Admissible
- so the heuristic, must be $\le$ than the actual distance estimate, never overestimated

Monotonicity
- not actually required, A* algorithm will actually work without this
- altho, this is a nice feature to have

![[../../images/Pasted image 20230214163834.png]]

Observations:
- A* Algorithm completely avoided Hamburg and Bonn
- exactly same complexity as Dijkstra's Algorithm
	- however, in real-use we are going to do bettwe with A* Algorithm than Dijkstra's Algorithm
	- because we terminated way earlier
	- and in memory, because we're not storing many nodes in memory

![[../../images/Pasted image 20230214173851.png]]

