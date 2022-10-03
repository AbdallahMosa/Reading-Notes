# READ 2 
 
 ## In Tests We Trust — TDD with Python
 
 ### What is test-driven development?
   TDD is a software development technique based on very short recurrent cycles 
    

### AAA Testing
The AAA pattern is a pattern for structuring tests. It breaks each test down into three parts – Arrange, Act, and Assert – where each part is a step leading to the next. The arrange step sets up the test’s input values. The act step prompts the primary function being tested. And finally, the assert step verifies that the output of the function is what was expected.

![image](https://www.whizlabs.com/wp-content/uploads/2016/04/TDD.png)


## What does the if __name__ == “__main__”: do?

The condition if __name__ == ‘__main__’ is used in a Python program to execute the code inside the if statement only when the program is executed directly by the Python interpreter. When the code in the file is imported as a module the code inside the if statement is not executed.

### What are the Advantages of using if __name__ == “__main__” statement?
1. Using the main in our file, we can restrict some data from exporting to other files when imported.
1. We can restrict the unnecessary data, thus making the output cleaner and more readable.
1. We can choose what others may import or what they may not while using our module.

## Introduction to Recursion
### What is Recursion?
Recursion is a powerful algorithmic technique in which a function calls itself (either directly or indirectly) on a smaller problem of the same type in order to simplify the problem to a solvable state.

### Why should we use recursion? 
1. Conciseness: recursion logic is generally shorter
1. Immutability: if you need your recursion logic to not mutate the same variable over and over
1. Elegance: it is more fun for some programmers to solve a problem using recursion
1. Repeatability: this is related to conciseness - recursion logic tends to be easier to manage when putting repetitive code together to solve the same problem over and over. This can be tedious in an object oriented paradigm, but becomes a bit more straightforward in a recursion paradigm

