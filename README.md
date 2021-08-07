# sumterForth
An ugly and incomplete forth interpreter in scheme

Calling `(forth)` in the repl will call forth the interpreter.

Word definitions end with `df` instead of `;`.

You can define a word like so ->   `: add1 1 + df`

`2 add1` will remove the 2 from the stack and put 3.

`5 0 > if 123 else 321 then` works now. Yay!

Use .s instead of .S , dup instead of DUP and so on. The code is very incomplete so most things won't work. 

You can pause the forth interpreter by typing `pause`, or you can `exit` and destroy the stack and defined words.
