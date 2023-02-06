# Functions that outputs a function
addConst is a function that returns a function

```Haskel
addConst n m = n + m
addThree = addConst 3

main = print (addThree 7)
```
```Bash
$main
10
```

or we can think of it as
as function w two arguments

```Haskel
addConstB n = \m -> n + m       -- explicitly returns a function
								-- \m -> n + m is a function literal
								-- m is the argument
								-- n + m is the value of the function at that argument

main = print (addConstB 3 8)    -- addConstB at 3 and 8
```
```Bash
$main
11
```

```Haskel
addConstC = \n -> (\m -> n + m)     -- addConstC is just an identifier now
									-- addConstC returns a function on n
									-- which then returns a function on m
main = print (addConstC 3 8)
```
```Bash
$main
11
```

# Functions that takes functions as input

```Haskel
thriceFromZero f = f(f(f(0)))

main = print (thriceFromZero(addConst 3))
```
```Bash
$main
9
```

Anonymous Function

```Haskel
thriceFromZero f = f(f(f(0)))

main = print (thriceFromZero(\n -> 2*n + 1)) -- anonymous function / function literal
											 -- looks like recursion to me
```
```Bash
$main
7
```

Shadowing, the latest definition of a variable is the one that matters

```Haskel
h n = (\n -> n)

main = print (h 1 2)    -- h 1 of  2
						-- either output n is the input of n
						-- or output n is the input of the function literal
						-- 2 is the most recent definition of n
```
```Bash
$main
2
```

```Haskel
h n = (\m -> n)

main = print (h 1 2)    -- now the most reent definition of n is 1
```
```Bash
$main
1
```

Recursive Functions

```Haskel
repFromZero 0 f = 0
repFromZero n f = f(repFromZero (n-1) f)

main = print (repFromZero 3 (\x -> x+1))  -- lambda function
```
```Bash
$main
3
```

```Haskel
repFromZero 0 f = 0
repFromZero n f = f(repFromZero n-1 f)    -- forgetting the brackets

main = print (repFromZero 3 (\x -> x+1))
```
```Bash
$main
lots of errorsss
```

Haskel is a Typed Language