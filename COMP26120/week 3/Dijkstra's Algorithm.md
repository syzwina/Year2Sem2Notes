just watch the first video of week 3 to understand Dijkstra's algorithm in action easier - https://online.manchester.ac.uk/webapps/blackboard/content/listContent.jsp?course_id=_72777_1&content_id=_13877942_1

![[../../images/Pasted image 20230214001543.png]]

D, discovered but not yet processed nodes
F, finish nodes

idea: we explore nodes and examine the outgoing edges

Dijkstra's algorithms takes advantage of the fact that 
the predicate of a shortest path, is itself a shortest path
so, when we traverse the outgoing nodes and compare their distances
we can optimise it better

we are going to see if we can make any improvements between s and its outgoing neighbours

we only explore the node w the minimum distance estimation

D is a priority queue where it is ranked according to the distance estimation on the node
so to get the next node to explore, we pop on the top of the priority queue

we only add to the queue when we reach it, so only reachable nodes are explored
this is good for memory

we relax on all outgoing edges from a particular node

![[../../images/Pasted image 20230214162028.png]]

todo: go look at heap implementation for complexity

![[../../images/Pasted image 20230214162039.png]]

E, number edges
V, number of vertices
