First 3 Live sessions are where we'll learn recursion techniques.
Will be very useful for any programming languages.
It forces you to think about recursions.

we'll do some exercise together

```Haskel
-- write stuff
```
```Bash
; write stuff
```

```Haskel
main = print "!"        -- just to make it compile

data Game = Flip Game Game | Win | Lose

-- model the rules of a game
-- either win or lose
-- or play another game, a subgame

a = (Flip Win Lose)
a = Flip Win (Flip Win Lose)
-- a game where if you flip head you win, tail you lose

c = (Flip (Flip Win Lose) (Lose))
-- flip the coin twice, and win if and only win if i have 2 heads
-- safer to keep brackets

d = (Flip (Flip Win Lose) (Flip Lose Lose))
-- stricly flip two coins

-- game to win if 2 consecutive Wins, lose if we have 2 consecutive Loses 
-- and keep playing otherwise
-- there's a possibility that it'll go forever, infinite
-- week 3 of Haskell
-- data structure, recursion
-- make a tree of possibilities ...
-- use let
twice = Flip h t
			where 
				h = Flip Win t
				t = Flip h Lose

-- it compiles, but if run, would run forever

```
```Bash
; write stuff
```

![[../../images/Pasted image 20230203122126.png]]

```Haskel
-- game where you can only win
-- 2 heads in a row, Win
-- otherwise, play forever

main = print ("!")

data Game = Flip Game Game | Win | Lose
lucky = Flip (Flip Win lucky) lucky

main = print ()
```
```Bash
; write stuff
```

```Haskel
-- given a game, the amount you get when you win
-- the amount you get for losing, output
-- expected values (but ignore issues to do with
-- floating point accuracy)
-- you may assume win >= lose
expv :: Game -> Double -> Double -> Double

-- Game (Int d)
expvl :: Game -> Int -> Double -> Double -> Double -> Double -> Double
-- assume one branch would be infinite
-- and the other of depth d


```
```Bash
; write stuff
```
