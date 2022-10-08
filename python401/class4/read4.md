# Reading and Writing Files in Python

 ### There are two types of files that can be handled in python, normal text files and binary files (written in binary language, 0s, and 1s).
   1. Text files: In this type of file, Each line of text is terminated with a special character called EOL (End of Line), which is the new line character (‘\n’) in python by default.
   1. Binary files: In this type of file, there is no terminator for a line, and the data is stored after converting it into machine-understandable binary language.
  
 
 ### File Access Modes
 
 1. Read Only (‘r’) : Open text file for reading. The handle is positioned at the beginning of the file. If the file does not exists, raises the I/O error. This is also the default mode in which a file is opened.
 2. Read and Write (‘r+’): Open the file for reading and writing. The handle is positioned at the beginning of the file. Raises I/O error if the file does not exist.
 3. Write Only (‘w’) : Open the file for writing. For the existing files, the data is truncated and over-written. The handle is positioned at the beginning of the file.
 4. Write and Read (‘w+’) : Open the file for reading and writing. For an existing file, data is truncated and over-written. The handle is positioned at the beginning of the file.
 5. Append Only (‘a’): Open the file for writing. The file is created if it does not exist. The handle is positioned at the end of the file. The data being written will be inserted at the end, after the existing data.
 6. Append and Read (‘a+’) : Open the file for reading and writing. The file is created if it does not exist. The handle is positioned at the end of the file. The data being written will be inserted at the end, after the existing data.
 
 
 ### Opening a File
  ```python
File_object = open(r"File_Name","Access_Mode")
```


## Python Exceptions: An Introduction

### What Is an Exception in Python? 
   - An exception is the result of an unpredicted event that occurs while your program is running, and prevents the program from doing what it should. As a result, the program throws an exception code.
### Different Exceptions in Python 
  - Python consists of several built-in exceptions we may leverage in our programs. We experience them when our code is syntactically correct but during the execution of our program, an unexpected event disrupted the normal flow of the program's instruction. When confronted with these errors our programs crash unless they are handled.
  -  
![Exceptions](https://miro.medium.com/max/640/1*yKRseWKBjdccXRoFsjIIQw.png)

## ex ZeroDivisionError

  -  We encounter a ZeroDivisionError when a number is divided by 0:
```python
a = 50
b = 0
print(a / b)
>>>> ---------------------------------------------------------------
ZeroDivisionError                  Traceback (most recent call last)
<ipython-input-3-bb264fdb44b0> in <module>()
      2 b = 0
      3 
----> 4 a / b
ZeroDivisionError: division by zero
```
## ex AttributeError
   -  We encounter an AttributeError when an invalid attribute reference is made:
  ```python
age = 6
# remembers i'm actually 60 so tries this...
age.append(0)
>>>> ---------------------------------------------------------------
AttributeError                     Traceback (most recent call last)
<ipython-input-1-67f5d41da6a1> in <module>()
      1 age = 6
      2 
----> 3 age.append(0)
AttributeError: 'int' object has no attribute 'append'
```
## Catching and handling Exceptions
  - There are several philosophies on how to deal with a possible exceptional case. Python programmers typically embrace the philosophy in which a raised error may be caught by a surrounding context that handles an exception appropriately.

   The sentiment behind this philosophy is that extra time shouldn’t be spent trying to safeguard every exceptional case during execution. This only holds when there is a mechanism for coping with a problem after it occurs.
 - try: This is the primary code to be executed — where we expect an error to occur in our code.
-  except: This is the program's response to any Exceptions in the try clause — where we define the type of Exception we think will occur.

-Our interpreter will stop executing when it encounters an Exception. If we’ve provided code in our except condition, this instead will be executed when the designated error is raised in our try clause.
```python
x = 400
y = int(input("Enter a number: "))
try:
    ratio = x / y
except ZeroDivisionError:
    y = y + 2
    ratio = x / y
    print(ratio)
>>>> Enter a number: 0 
200.0
```

## References 
- [Reading and Writing to text files in Python](https://www.geeksforgeeks.org/reading-writing-text-files-python/)
- [An Introduction To Exception Handling in Python](https://medium.com/geekculture/an-introduction-to-exception-handling-in-python-8a5b9c98d47f#4281)
