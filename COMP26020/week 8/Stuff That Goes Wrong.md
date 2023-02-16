Non exhaustive defenition of pattern matching

```Haskel
oops True = True

main = print (oops True)
```
```Bash
$main
True
```

```Haskel
oops True = True

main = print (oops False)
```
```Bash
$main
runtime error, non exhaustive patterns in function oops
```

Non-terminating recursion, undefined recursion

```Haskel
eep 0 = 0
eep n = 1 + eep n

main = print (eep 0)
```
```Bash
$main
0
```

Local scope of x causes an infinite loop

```Haskel
yikes = let x = 1 in
 let x = 1 + x in x

main = print (yikes)
```
```Bash
$main
True
```

The last x is in the scope of x = 1 + x
it has nothing to do with x = 1

```Haskel
yikes = let x = x in x

main = print (yikes)
```
```Bash
$main
True
```

This will also run forever