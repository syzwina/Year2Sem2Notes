```Haskel
b = False || (True && True)
main = print (b)
```
```Bash
$main
True
```

Literals: capital letters
Identifiers: lowercase letters

```Haskel
b = False || (False && True)
main = print (b)
```
```Bash
$main
False
```

Integers

```Haskel
n = 1 + 7
main = print (n)
```
```Bash
$main
8
```

```Haskel
b = False || (True && True)
n = 1 + 7

b2 = n == 7

main = print (b)
```
```Bash
$main
False
```

```Haskel
b = False || (True && True)
n = 1 + 7

b2 = n /= 7

main = print (b)
```
```Bash
$main
True
```

```Haskel
b = False || (True && True)
n = 1 
+ 7      -- must be in one line

b2 = n == 7

main = print (b)
```
```Bash
$main
gets an error
```

```Haskel
b = False || (True && True)
n = 1 
 + 7      -- must be in one line, but if have one whitespace in beginning, it works

b2 = n == 7

main = print (b)
```
```Bash
$main
False
```

Pairs

```Haskel
b = (0,1) == (0,0)

main = print (b)
```
```Bash
$main
False
```

If Else -  so not instructions, but definition of mathematical cases

```Haskel
b = (0,1) == (0,0)

v = if b then 5 else 6

main = print (b)
```
```Bash
$main
6
```

```Haskel
b = (0,1) == (0,0)

v = 7 * (if b then 5 else 6) -- Haskel treats everything as data

main = print (b)
```
```Bash
$main
42
```

Functions

```Haskel
add7 n = n + 7

main = print (add7 8)
```
```Bash
$main
15
```

```Haskel
small 0 = True
small 1 = True
small n = False

main = print (small 5)
```
```Bash
$main
False
```

Ordering Matters

```Haskel
small 0 = True
small n = False
small 1 = True

main = print (small 1)
```
```Bash
$main
gets a warning
False
```

Function on Pairs with Pattern Matching

```Haskel
addUp (0,n) = n
addUp (m,0) = m
addUp (m,n) = m + n

main = print (addUp(5,6))
```
```Bash
$main
11
```

Best to think of Pairs as Single things
Best to think of addUp as a function w One argument which happens to be a pair

```Haskel
first (e,__) = e 
main = print (first(5,6))
```
```Bash
$main
5
```

Recursive Definitions

```Haskel
fib 0 = 0
fib 1 = 1
fib n = fib (n-2) + fib (n-1)

main = print (fib 6)
```
```Bash
$main
8
```

