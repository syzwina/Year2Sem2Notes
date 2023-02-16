# Caches - Part 2

associativity of caches
- fully associative cache
	- flexible
- direct-mapped cache
	- simple
	- faster
- set-associative cache
	- have two (half-size) direct-mapped cache in parallel
	- energy penalty, since we need to make more reads than a traditional direct-mapped cache
	- reducing conflict - reminding me of hash conflicts ngl

cache lines
- a program runs at average 7 instructions before branching
- reduces tag overhead

size
- small caches dont work really well w direct-mapped
- as you get larger, you can afford tor educe the associativity
use
- do we expect locality
- this determines the cache line size
- TLB - translation look-aside buffers
	- does things in parallel 'lookaside'
power
- higher associativity, more activity, more power
- the more sets you have, the more power per access, more lookups
levels of cache
- level 0, level 1, level 2, level 3
- terminologies : 'level 2 cache is private per-core, in a quad-core system'

cache sharing between cores
	- can allow information sharing between processors
	- each process in a multiple cores may as well be using the same 'virtual address'
	- TLB, this means that when you switch context, L1 cache is just junk by then
	- L2 cache is using the real addresses, so it's not fully junk, so it can stay
	- L3 is shared primarily, just to offer some flexibility if one of the cores need to do a lot of caching, so there's like a soft bound, or maybe we're doing some multiprocessing between cores

cache replacement policy
- round robin - easy
- LRU, least recently used - 'i expect a forest and i got it' - Jim
	- hard to implement in hardware
	- good results
	- is this really necessary?
- random - works reasonably well
	- predictability
	- randomness in hardware, pseudo random
		- it doesnt have to be very good
- other

cache write policy
- write through cache
	- modify cache
	- and modify the next cache
	- and modify memory
	- v v v slow
	- get more write backlogs
	- 3 reads to 1 write
	- a lot of energy penalty
	- altho simple and works
	- you can dump the cache whenever
- copy back cache/ write back cache
	- deals w reads from the L1 cache
	- but you now have an outdated copy in memory
	- not paying as much energy penalty
	- problem comes when you do a cache replacement of context switch
	- something needs to know that this is the only copy of the data, so before overwriting it, we need to update memory with it
	- we need to distinguish if our cache entry is changed or not, 'dirty'

	- if it is dirty, we need to write back before we flush
	- it is complicated
	- hardware 
	- efficient but complicated

paging
- somewhat like caching
- which pages are there and which are not

copy back/ flushing
- expensive
- don't do context switching too much

write misses
- if we want to write to something
- but that thing is not in cache
- do we just write it in memory directly
- or do we, fetch it 1st
- and then modify it in the cache and make it dirty
- 'if im writing something, i'll probably will want to read it back'
