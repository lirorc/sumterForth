# sumterForth
An ugly and incomplete forth-like interpreter in scheme

Calling `(forth)` in the repl will call forth the interpreter.

Word definitions end with `df` instead of `;`.

You can define a word like so ->   `: add1 1 + df`

`2 add1` will remove the 2 from the stack and put 3.

`21 12 > if "North" else 12 21 < if "South" else "Canada?" then then` will -hopefully- work.

Use .s instead of .S , dup instead of DUP and so on. The code is very incomplete so most things won't work.

If you need a loop, you have to use recursion.. which you can;

`: show dup 0 = if "DONE" else dup . 1 - show then df`

`show 999999999` should print 999999999 999999998 999999997 etc.

`: sum swap dup 0 = if drop "DONE" else swap + sum then df`

`0 12 23 34 45 sum` should consume those numbers and put 114 to stack

`: fact dup 0 = if drop "DONE" else dup rot * swap 1 - fact then df`

`: fac 1 swap fact df`

`5 fac` should consume 5 and leave 120

You can pause the forth interpreter by typing `pause`, or you can `exit` and destroy the stack and defined words.

Q: Why forth

A: Because it's simple

Q: Why lisp

A: Because it's pretty
