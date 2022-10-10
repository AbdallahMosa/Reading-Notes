# Intro to OOP
   - As the name suggests, Object-Oriented Programming or OOPs refers to languages that use objects in programming. Object-oriented programming aims to implement real-world entities like inheritance, hiding, polymorphism, etc in programming. The main aim of OOP is to bind together the data and the functions that operate on them so that no other part of the code can access this data except that function.
 
###  OOPs Concepts:
  1. Class 
  2. Objects
  3. Data Abstraction 
  4. Encapsulation
  5. Inheritance
  6. Polymorphism
  7. Dynamic Binding
  8. Message Passing
 
 #### Class
   - A class is a user-defined data type. It consists of data members and member functions, which can be accessed and used by creating an instance of that class. It represents the set of properties or methods that are common to all objects of one type. A class is like a blueprint for an object.
   - For Example: Consider the Class of Cars. There may be many cars with different names and brands but all of them will share some common properties like all of them will have 4 wheels, Speed Limit, Mileage range, etc. So here, Car is the class, and wheels, speed limits, mileage are their properties.  
    
 #### Objects
   - It is a basic unit of Object-Oriented Programming and represents the real-life entities. An Object is an instance of a Class. When a class is defined, no memory is allocated but when it is instantiated (i.e. an object is created) memory is allocated. An object has an identity, state, and behavior. Each object contains data and code to manipulate the data. Objects can interact without having to know details of each other’s data or code, it is sufficient to know the type of message accepted and type of response returned by the objects. 
   - For example “Dog” is a real-life Object, which has some characteristics like color, Breed, Bark, Sleep, and Eats.
   ![alt](https://media.geeksforgeeks.org/wp-content/uploads/20200901221937/Object-660x185.png)
   
# Thinking Recursively in Python
  - Problems (in life and also in computer science) can often seem big and scary. But if we keep chipping away at them, more often than not we can break them down into smaller chunks trivial enough to solve
  - A recursive function is a function defined in terms of itself via self-referential expressions.

  - This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result. All recursive functions share a common structure made up of two parts: base case and recursive case.

# Python Testing with pytest: Fixtures and Coverage
  ### Fixtures 

  - In the simplest terms, a test is meant to look at the result of a particular behavior, and make sure that result aligns with what you would expect. Behavior is not     something that can be empirically measured, which is why writing tests can be challenging.

  “Behavior” is the way in which some system acts in response to a particular situation and/or stimuli. But exactly how or why something is done is not quite as          important as what was done.

  You can think of a test as being broken down into four steps:

   1. Arrange

   2. Act

   3. Assert

   4. Cleanup
   
   ```python
   import pytest


class Fruit:
    def __init__(self, name):
        self.name = name

    def __eq__(self, other):
        return self.name == other.name


@pytest.fixture
def my_fruit():
    return Fruit("apple")


@pytest.fixture
def fruit_basket(my_fruit):
    return [Fruit("banana"), my_fruit]


def test_my_fruit_in_basket(my_fruit, fruit_basket):
    assert my_fruit in fruit_basket
   ```
   
 #### Coverage
   - Coverage.py is a tool for measuring code coverage of Python programs. It monitors your program, noting which parts of the code have been executed, then analyzes the source to identify code that could have been executed but was not.

 -  Coverage measurement is typically used to gauge the effectiveness of tests. It can show which parts of your code are being exercised by tests, and which are not.
 Capabilities of Coverage.py
 1. By default it will measure line (statement) coverage.
 2. It can also measure branch coverage.
 3. It can tell you what tests ran which lines.
 4. It can produce reports in a number of formats: text, HTML, XML, LCOV, and JSON.
 5. For advanced uses, there’s an API, and the result data is available in a SQLite database.
 
# Sources 
  1. [Introduction of Object Oriented Programming](https://www.geeksforgeeks.org/introduction-of-object-oriented-programming/)
  2. [Thinking Recursively in Python](https://realpython.com/python-thinking-recursively/)
  3. [fixtures](https://docs.pytest.org/en/6.2.x/fixture.html)
  4. [Coverage](https://coverage.readthedocs.io/en/6.5.0/)
