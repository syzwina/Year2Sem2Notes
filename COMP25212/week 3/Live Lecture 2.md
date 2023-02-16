# Memory Management

glue of caching and main memory

# Virtual Memory

threads: share an address space

process: does not share an address space

a process can have multiple threads

# Pages

divided into triand
typical size, 4kb on average

bigger pages waste space

4kb page, 12 bits worth of address
32 bit machine
2^20 = about a million



2^10 = about a thousand
2^39 = about a billion

## Multi-Level Tables

5-levels on a 64-bit
2-levels on a 32-bit

## TLB

highly associative
only use about 3-pages per process, maybe one for your stack

when a table hit occur
- permissions are compared
- if the process is not allowed to look into that part of memory
- send a bus failure signal

# MMU

# TCM - tightly coupled memory

an SRAM actually
- applicable to a real-time controller
- hardware can not give you predictability
- so if you're working w real-time controller, you might want to deal w memory a bit more manually
- altho would be less efficient in general, but we can avoid worst cases

paging - would be better of fully associative bcs stuff can get haphazard 

# Main Memory

## SRAM

all your levels of cache
buffers
packet receiver - quick data coming in quickly

## RAM

## Multi-Port SRAM

- speed penalty, not worth it

