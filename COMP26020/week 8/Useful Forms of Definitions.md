```Haskel
small 0 = True
small 1 = True
small n = False

smallB n = case n of
 0 -> True                           -- don't forget that one whitespace before 0
 1 -> True                           -- here as well
 n -> False                          -- and here

main = print (smallB 1)
```
```Bash
$main
True
```

Guard Expression

```Haskel
sideOfFive n 
 | n - 5 > 0 = 1
 | n - 5 < 0 = -1
 | n - 5 == 0 = 0

main = print (sideOfFive 6)
```
```Bash
$main
1
```

```Haskel
sideOfFive n 
 | d > 0 = 1
 | d < 0 = -1
 | d == 0 = 0
 where d = n - 5

main = print (sideOfFive 6)
```
```Bash
$main
1
```

```Haskel
sideOfFive n 
 | d > 0 = 1
 | d < 0 = -1
 | otherwise = 0
 where d = n - 5

main = print (sideOfFive 6)
```
```Bash
$main
1
```

```Haskel
sideOfFive n 
 | d > 0 = 1
 | d < 0 = -1
 | otherwise = 0
 where d = n - 5

main = print (sideOfFive 6)
```
```Bash
$main
1
```

Let Expression

```Haskel
y = let x = 10 + 10 in x + x

main = print (y)
```
```Bash
$main
40
```

Let also has the phenomenon of shadowing

```Haskel
z = let x = 10 in              
 let x = 20 in x                 -- notice the single whitespace before let

main = print (z)
```
```Bash
$main
20
```

Let is an expression
it allows us to make a local definition
it is not a sequential operation

it is not that, x is set to 10, then the same x is set into 20
we are just defining mathematical values, by means of writing expressions

```Haskel
w = let x = 5 in              
 let f = \n -> x in                 -- notice the single whitespace before let
 let x = 6 in
 f 0

main = print (w)
```
```Bash
$main
5
```

we get 5 because, in Haskel, a function is a methematical object like any other
f is defined as a function that sends n to x
and is defined in a context where x is just 5
so, by definition
f is a function that sends n to 5

```Haskel
w = let x = 5 in              
 let f = \n -> x in                 -- notice the single whitespace before let
 let x = 6 in
 x

main = print (w)
```
```Bash
$main
6
```

here, the most recent definition of x is 6
f is still defined as n to 5, as when f is defined
the most recent definition of x is 5

this makes reasoning about Haskel code easier than reasoning about code in other languages