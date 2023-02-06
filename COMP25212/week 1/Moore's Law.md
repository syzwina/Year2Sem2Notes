**Moore's law** is the observation that the number of transistors in a dense integrated circuit (IC) doubles about every two years.

- growth in number of transistors would have to stop soon
- shrinking of transistors can't continue for long because we're reaching atomic level

# Reducing component size broadly results in:
- **More components** (at roughly the same price).
	Although the number of components is still increasing the rate of increase is beginning to slow down.
- **Faster processing**.
	For many years this was largely a consequence of increasing the clock speed. 
	Although apparently simple required architectural developments which are explored in the second half of this module.  
	Since about 2005 increasing clock speed has been impractical so processing increases have been gained by increasing parallelism.
	This has significant consequences for software; it is visited throughout the module.
- **Lower energy** (per component).
	However the increasing number of components has made power management _the_ limiting factor in many systems.

# Dennard Scaling
The **power consumption** of chips stayed roughly constant as their density and speed increased.
aka MOSFET Scaling

Unfortunately this is no longer true and power has become a dominating factor in SoCs.

# Power matters because:
-   In portable equipment high power consumption shortens battery life.
-   In ‘tethered’ computing high power consumption causes cooling problems.

Dark Silicon : In high performance devices it is necessary to ration power by keeping some subsystems switched off at any given time.

# Architectural Impliactions
Amdahl/Case Law
- a ‘balanced’ computer system needs about 1 megabyte of memory and 1 megabit/s of I/O per MIPS of CPU performance

A major issue to note in the evolution over this time is that the processors and memory have scaled differently.
-   Processors have got a bit bigger and a lot faster.
-   Memory has got a lot bigger and a **bit** faster.

# Memory Wall
These memories are now up to 10× faster whereas processors are over 1000× faster.
![[../../images/Pasted image 20230202153015.png]]
**Latency** : The _delay_ from starting an operation to perceiving the result.
**Bandwidth** : The _rate_ at which data can be moved.

Increase in speed:
- Used to be: increasing circuit speed
- Now: increasing paralellism
	- instruction paralellism
	- multi-threaded software

# Speed of light
- $3 ×10^8 m.s-1$
- one foot (30 cm) per nanosecond

period 1ns = frequency 1 GHz

The most noticeable consequence is probably the need to ‘balance’ the delays on PCB (Printed Circuit Board) tracks, commonly visible on memory buses. You may be able to see this on your PC motherboard where tracks may be artificially lengthened to match those which have to be longer.
![[../../images/Pasted image 20230202153717.png]]
[source](https://resources.pcb.cadence.com/blog/on-board-as-in-life-timing-is-everything-almost-pcb-trace-length-staying-in-the-sweet-spot-2)
Another consequence is the distance on a silicon chip. 
At frequencies of (say) 3 GHz a signal cannot cross a large chip within a clock cycle. 
This causes designers to subdivide a chip into smaller timing regions. 
Single _buses_ are impractical at such speeds and there is an increasing tendency to employ **Network on Chip** (NoC) for interconnection.
The latency and bandwidth restrictions _off chip_ are, of course, much more challenging.

Next:  [[Live Lecture 2]]