# Why

![[../../images/Pasted image 20230213143240.png]]

![[../../images/Pasted image 20230213143357.png]]

- represent the build sequence as a list

![[../../images/Pasted image 20230213143456.png]]

Directed : edges are directed
Acyclic : no cycles

we can use DFS 
	- to produce a topological ordering
	- and to detect cycles in the graph

	Node can be Open, Done or New

if we traverse deeper and deeper
and we find an Open node
that means we have a cycle in our graph

![[../../images/Pasted image 20230213144653.png]]

Function F, returns the status of the node u

prepend - opposite of appending

```
procedure DFSREC(F, u) 
	if F(u)=N then 
	F(u)←O //Startprocessingnode 
	forall v with (u, v) ∈ E do 
		F ← DFSREC(F, v) 
	F(u)←D //Doneprocessingnode 
	else if F(u)=O then 
		Error: found cycle 
return F 

procedure DFS(s) 
	forall nodes u 
		F(u)←N 
return DFSREC(F, s)
```

![[../../images/Pasted image 20230213145145.png]]

![[../../images/Pasted image 20230213145213.png]]

