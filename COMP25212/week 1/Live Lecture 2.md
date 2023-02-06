[[COMP25212 - Table of Contents]]
# Interconnection

## Buses
- we can load a byte, a half-word, a word
- it's important tat if we store a byte, the bus does not overwrite the neighbours of the byte
- timing - cause sometimes we don't use it, and sometimes we do, so when is it valid
- ready signal - i want to read that, now im ready to receive data
- wait signal - complements the ready signal
- privilege - can a process access some parts of the memory, i am an OS, i am an application
- success/failure - yes or no, complements the priviledge signal, if the read or write is successful or not, one of the causes of the segmentation fault

### Sharing Buses
- shared bus, scales easily but bottleneck
- crossbar bus, offers paralellism ut scales badly O($n^2$) 
	- if a 2-to-2, has a 50% chance of a collision
	- a $3/4$ chance of you getting some parallellism
	- use of multiplexers
	- the chip in COMP22712 has a 8-to-8 crossbar switch

## Network on Chip
- often rectangular grid pattern, suits silicon layout
- other topologies are available, 'irregular' ones
- speed of light limits you to send information across a chip
- bandwith is less of a problem, but latency is
- processors, subsytems are connected to some local router to communicate, often in x, y coordinates bcs of flat rectangular layout

## Bytes and Words

### Byte
- smallest addressable unit
- originally a character
- 8 bits, octet

### Word
- natural data size in an architecture
- increasingly 32 bits (4 bytes)
- halfword, 16 bits
- doubleword 64 bits
- gcc compiler defaut int size is still 32-bits even on a 64-bits processor

### Bus
- aren't always a word
- it can be wider or shorter than the thing it will be communicating

## Allignment
- misallignes operations will be slower(or malfunction)
	- keep data at appropiate address boundaries
	- can cause allignment fault in more sophisticated systems
	- in basic arm, it will return 5,6,7,4 - the same word but rotated, which would be confusing

### Code Allignment
- x86 - has variable length instructions
	- allignment infeasible
	- but compilers would try, nops galore
	- if there's a loop, there would be a sequence of nops, bcs the compilers wants to optimise the loop
	- so we waste a bit of time to get to the loop, so that we can do the loop efficiently
- RISC - fixed length

## Endianness
- Jonathan Swift - Gulliver's Travels
- this only matters if you are getting stuff from memory, of different size, but at the same size
### Little Endian - most common
- stores the MSB byte at the LSB address
- least significat at the lowest address
### Big Endian
- starts at the largest address, and counts down
- most significant at the lowest address

## Von Neumann and other architectures

### Von Neumann
- processor and memory(holds everything)
- bus bottleneck - can only do one thing at a time

### Harvard 
- stores code and data in different memory
- have separate address spaces
- AVR as used in (small) Arduinos
	- 8-bits wide data
	- 16-bits wide and 20-bits address
	- omega halfword/ mega halfword???

### Common approach
- Harcard interface physically
- Von Neumann model for the programmer, a mental model
- memory has a 'soft' partition

## System Bus Organisation

- High performance for RAM, used a lot
- Low performance for IO, rarely used

### Bus Bridge
- a mean of translating one protocol to another

| More stuff to look at
- atomicity
- semaphores

Next : [[Addresing]]


