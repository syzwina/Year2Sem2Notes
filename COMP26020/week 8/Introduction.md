# Functional Programming

Treat functions like any other data
- define without naming
- functions as inputs and outputs of other functions
	- functions that take functions as inputs are - higher order functions

Reason about functions like mathematical functions
- if f(x) = g(x) for all x, then f = g
- a function is really is, a mapping of inputs to outputs
- let x = f(10) in x + x + x = f(10) + f(10) + f(10)
	- using the same value x, 3 times must be the same as generating f(10) 3 times
	- no randomly generated values inside the function

