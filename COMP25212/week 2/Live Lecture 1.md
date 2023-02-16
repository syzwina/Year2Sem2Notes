# Caches - Part 1
locality
	- if i use something in some space, i'll probably want to use it again
	- spatial locality, memory
	- temporal locality, if you use something now, you would probably want to use it again in the near future
working set
	- keeping the things that you want and probably want again nearby
Hit & Miss
	- $T_{ave} = T_{hit} + P_{miss} x T_{miss}$  



Fully associativity, means you can put naything anywehere
so you'll need to search the whole cache for something
	- you can also have 2 copies of the same data in the cache

making it less associative allows you to reduce the comparisons needed to check for something

CAM - content addressable memory
	here's the data, where it is
	reverse of ram, here's the address, what's the data
	network routing uses this as well
	fully associative 

fully associative will have more hits, but is more expensive to implement
direct-mapped cache will have more miss, but is cheaper when you have a hit

set-associative

cache misses, 3C's
Compulsary Misses
	- when you initially start a program
	- cache is empty/everything in cache is invalid
Capacity Misses
	- cache is full
	- need to reject some stuff
	- direct-mapped is ez,, ust remove whatever that is there and replace w new data
	- fully associative is a bit difficult
Conflict Misses
	- thrashing, within  a loop, when we use purely direct-mapped

