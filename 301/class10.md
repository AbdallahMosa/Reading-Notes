# reading class 10

## What is a 'call'?
as  a function that can be used in another line of code

## How many 'calls' can happen at once?
one at a time.
## What does LIFO mean?
LIFO = Last In First Out.
## Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.



![class10](https://user-images.githubusercontent.com/109727654/188285623-ca879824-d50a-40a8-bf63-df8bb8011754.png)


## What causes a Stack Overflow?
A stack overflow is when you've used up more memory for the stack than your program was supposed to use. In embedded systems you might only have 256 bytes for the stack, and if each function takes up 32 bytes then you can only have function calls 8 deep - function 1 calls function 2 who calls function 3 who calls function 4 .... who calls function 8 who calls function 9, but function 9 overwrites memory outside the stack. This might overwrite memory, code, etc.


## What is a 'reference error'?
The ReferenceError object represents an error when a variable that doesn't exist (or hasn't yet been initialized) in the current scope is referenced.
## What is a 'syntax error'?
A syntax error in computer science is an error in the syntax of a coding or programming language, entered by a programmer. Syntax errors are caught by a software program called a compiler, and the programmer must fix them before the program is compiled and then run
## What is a 'range error'?
The RangeError object indicates an error when a value is not in the set or range of allowed values.
## What is a 'tyep error'?
The TypeError object represents an error when an operation could not be performed, typically (but not exclusively) when a value is not of the expected type.
## What is a breakpoint?
The point at when the code ends
## What does the word 'debugger' do in your code?
A debugger is a tool that is typically used to allow the user to view the execution state and data of another application as it is running. Debuggers allow users to halt the execution of the program, examine the values of variables, step execution of the program line by line, and set breakpoints on lines or specific functions that, when hit, will halt execution of the program at that spot. In this view, seeing how the program is viewed by their computer, the user can discover how a program flows, identify incorrect code and data, and find semantic errors in the program.
