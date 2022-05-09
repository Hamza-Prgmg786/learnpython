# Welcome to Python

## Catalogue

- [Comments](#Comments)
- [Variables](#Variables)
- [Constants](#Constants)
- [Keywords](#Keywords)
- [Data_Types](#Data_Types)
- [Operators](#Operators)
- [Program_Control_Flow](#Program_Control_Flow)
- [Array](#Array)
- [Functions](#Functions)
- [Reference](#Reference)
- [Object_Oriented_Programming](#Object_Oriented_Programming)
- [Numbers](#Number)
- [Python_Casting](#Python_Casting)
- [Python_Lists](#Python_Lists)

## Comments

Single-line comments

```
# ...
```

Multi-line comments

```
"""
This is a comment
written in
more than just one line
"""
```

## Variables

Give a name to a space in memory.

```
variable_Name = value;

a = 10;
name = "Steve Jobs"
```

## Constants

Unchangeable data in the program.

```
To work around this, you use all capital letters to name a variable to indicate that the variable 
should be treated as a constant. For example:

Defining constant_name value;
 
# DAY = 7
```

## Keywords

Python keywords reserved and not available for re-definition or overloading.

![avatar](/python_keywords.png)

## Data_Types

A variable is a named location used to store data in the memory. 

#### 1. Integer

Python int variable requires minimum 24 bytes on 32-bit / 64-bit system.
It may vary as per hardware.
```
import sys
sys.getsizeof( int() ) # prints 24
sys.getsizeof(0) # prints 24
sys.getsizeof(1) # prints 28
sys.getsizeof(-2) # prints 28
```
It is helpful to think of variables as a container that holds data that can be changed later
in the program. 

Represent integers like 1, 10.
```
number = 10
```

#### 2. Floating point

Python int variable requires minimum 24 bytes on 32-bit / 64-bit system.
It may vary as per hardware.
```
import sys
sys.getsizeof( float() ) # prints 24
sys.getsizeof(0.0) # prints 24
```

Represent decimals like 1.23, -2.332.
```
number = 1.23
```

#### 3. String

```
a = "Hello, World!"
print(a)
```

#### 5. Boolean

Represent True and False.

```
import sys
sys.getsizeof( bool() ) # prints 24
sys.getsizeof(True) # prints 28
sys.getsizeof(False) # prints 24
```

```
print(10 > 9)
print(10 == 9)
```

```
+ - * / % ++ -- += >= || ! && ...
```

```
pre-increment/decrement: a=2; b=++a; // Do b=a first and ++a, the result is a=3; b=3;
```

```
post-increment/decrement: a=2; b=a++; // Do a++ first and b=a, the result is a=3; b=2;
```

## Program_Control_Flow

#### 1. Selection statements

If condition:
```
a = 10
b = 5
if b > a:
  ...
elif a == b:
  ...
else:
  ...
```

Conditional Operator ?:
```
c = a > b ? a : b; // a > b is true then return a, false return b.
```

Switch condition:
```
Python does not have this. 
So, to get around this, we use Python’s built-in dictionary construct to implement cases and decided what to do when a case is met. 
We can also specify what to do when none is met.
```

#### 2. Iteration statements

While loop:
```
# expression can be any condition

while expression:
  statement
 } 
```

## Array

Arrays are used to store multiple values in one single variable:
```
x = ["A", "B", "C", "D"]
```

#### 1. What is an Array

An array is a special variable, they can hold more than one value at a time.
```
x1 = "A"
x2 = "B"
x3 = "C"
x4 = "D"
```

#### 2. Accessing the elements of an Array.
```
x1 = x[0]
```

#### 3. Get the length of the array.
```
x1 = len(x)
```

#### 4. Looping Array Elements.
```
for x1 in x:
  print(x1)
```

#### 5. Adding Array Elements.
```
x.append("E")
```

#### 6. Removing Array Elements.

pop() method to remove an element from the array.
```
x.pop(1)
```

remove() method to remove an element from the array.
```
x.remove("A")
```

#### 7. Array Methods.

Python has a set of built-in methods that you can use on lists/arrays.
```
append()  -> Adds an element at the end of the list.
clear()   -> Removes all the elements from the list
copy()    -> Returns a copy of the list.
count()   -> Returns the number of elements with the specified value.
extend()  -> Add the elements of a list (or any iterable), to the end of the current list.
index()   -> Returns the index of the first element with the specified value.
insert()  -> Adds an element at the specified position.
pop()     -> Removes the element at the specified position.
remove()  -> Removes the first item with the specified value.
reverse() -> Reverses the order of the list.
sort()    -> Sorts the list.
```

## Functions

Encapsulate a piece of frequently used code to reduce repetitive use of code.
```
def add(num_1, num_2): // num_1 and num_2 are parameters
   sum = num_1 + num_2
   return sum
}

if __name__ == '__main__':
   a = 10
   b = 20
   sum = add(a, b) // a and b are arguments
}
```

#### 1. Arbitrary Arguments, *args.

if you do not know how many arguments that will be passed into your function.
Add a * before the parameter name in the function definition.
This way the function will receive a tuple of arguments, and can access the items accordingly:

```
def my_function(*children):
  print("The children are " + kids[2])

my_function("Steve", "Robert", "Sarah")
```

#### 2. Default Parameter Value.

If we call the function without argument, it uses the default value:

```
def my_function(child = "Steve"):
  print("My Name is" + child)

my_function("Sarah")
my_function("Robert")
my_function()
```

#### 3. Passing a List as an Argument.

You can send any data types of argument to a function (string, number, list, dictionary etc.).
It will be treated as the same data type inside the function.

```
def my_function(child):
  for x in child:
    print(x)

childrens = ["Steve", "Robert", "Sarah"]

my_function(childrens)
```

#### 4. Recursion.

Python also accepts function recursion, which means a defined function can call itself.

Recursion is a common mathematical and programming concept. 
It means that a function calls itself. 
This has the benefit of meaning that you can loop through data to reach a result.

```
def recursion(k):
  if (k > 0):
    result = k + recursion(k - 1)
    print(result)
  else:
    result = 0
  return result

print("\n\nRecursion")
recursion(6)
```

## Object_Oriented_Programming.

#### 1. The __init__() Function.

To understand the meaning of classes we have to understand the 
built-in __init__() function.
All classes have a function called __init__(), which is always executed 
when the class is being initiated.
Use the __init__() function to assign values to object properties 
or other operations that are necessary to do when the object is being created.:


```
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

p1 = Person("Steve", 70)

print(p1.name)
print(p1.age)
```

#### 2. Object Methods with self Parameter.

```
class Person:
  def __init__(object, name, age):
    object.name = name
    object.age = age

  def myfunc(nme):
    print("My name is " + nme.name)

p1 = Person("Steve", 70)
p1.myfunc()
```

#### 3. Inheritance with super(), Properties, Methods.

```
super()        -> Python also has a super() function that will make the child 
                  class inherit all the methods and properties from its parent:
```

```
Properties()   -> In the example below, the year should be a variable, 
                  passed into the Student class when creating student objects. 
                  To do so, add another parameter in the __init__() function:
```

```
Methods()      -> If you add a method in the child class with the same name as 
                  a function in the parent class, the inheritance of the parent 
                  method will be overridden.
```

```
class Student(Person):
  def __init__(self, fname, lname, year):
    super().__init__(fname, lname)
    self.graduationyear = year

  def welcome(self):
    print("Welcome", self.firstname, self.lastname, "to the class of", self.graduationyear)
```    

#### 4. Constructors & Destructors.

Constructor and destructor function automatically executed in Python. 
Constructor when an object of a class is created and Destructor when an object exit from the scope:

Constructors;

```
class Test:

    def __init__(self, number):
        print("Constructor of class Test...")
        self.number = number
        print("The value is :", number)


S = Sample(100)

Output:

Constructor of class Test...
The value is : 100
```

Destructors;

```
class Test:
    number = 0

    def __init__(self, variable):
        Test.number += 1
        self.variable = variable

        print("Object value is = ", variable)
        print("Variable value = ", Test.number)

    def __del__(self):
        Test.number -= 1

        print("Object with value %d is deleted" % self.variable)


S1 = Test(10)

Output:

Object value is = 10
Variable value = 1
Object with value 10 is deleted
```

## Numbers.
There are three numeric types in Python:

1) int
2) float
3) complex

Variables of numeric types are created when you assign a value to them:
```
x = 1    # int
y = 2.8  # float
z = 1j   # complex

To verify the type of any object in Python, use the type() function:

print(type(x))
print(type(y))
print(type(z))
```

#### 1. Int.

Int, or integer, is a whole number, positive or negative, 
without decimals, of unlimited length.

Integers:
```
x = 1
y = 35656222554887711
z = -3255522

print(type(x))
print(type(y))
print(type(z))
```

#### 2. Float.

Float, or "floating point number" is a number, positive or negative, 
containing one or more decimals.

```
x = 1.10
y = 1.0
z = -35.59

print(type(x))
print(type(y))
print(type(z))
```

Float can also be scientific numbers with an "e" to indicate the power of 10.

```
x = 35e3
y = 12E4
z = -87.7e100

print(type(x))
print(type(y))
print(type(z))
```

#### 3. Complex.

Complex numbers are written with a "j" as the imaginary part:

```
x = 3+5j
y = 5j
z = -5j

print(type(x))
print(type(y))
print(type(z))
```

#### 4. Type Conversion.

You can convert from one type to another with the int(), float(), and complex() methods:

```
x = 1    # int
y = 2.8  # float
z = 1j   # complex

#convert from int to float:
a = float(x)

#convert from float to int:
b = int(y)

#convert from int to complex:
c = complex(x)

print(a)
print(b)
print(c)

print(type(a))
print(type(b))
print(type(c))
```
#### 5. Random Number.

Python does not have a random() function to make a random number, 
but Python has a built-in module called random that can be used to 
make random numbers:

```
Import the random module, and display a random number between 1 and 9:

import random

print(random.randrange(1, 10))
```

## Python Casting.

Specify a Variable Type.

Python is an object-orientated language, and as such it uses 
classes to define data types, including its primitive types.

Casting in python is therefore done using constructor functions:

1) int() ; constructs an integer number from an integer literal, a float literal
(by removing all decimals), or a string literal (providing the string represents a whole number).
2) float() ; constructs a float number from an integer literal, a float literal or a string literal
(providing the string represents a float or an integer).
3) str() ; constructs a string from a wide variety of data types, including strings, integer 
literals and float literals.

Integers:

```
x = int(1)   # x will be 1
y = int(2.8) # y will be 2
z = int("3") # z will be 3
```

Floats:

```
x = float(1)     # x will be 1.0
y = float(2.8)   # y will be 2.8
z = float("3")   # z will be 3.0
w = float("4.2") # w will be 4.2
```

Strings:

```
x = str("s1") # x will be 's1'
y = str(2)    # y will be '2'
z = str(3.0)  # z will be '3.0'
```

## Python Lists.


Lists are used to store multiple items in a single variable.

Lists are one of 4 built-in data types in Python used to store collections
of data, the other 3 are Tuple, Set, and Dictionary, all with different qualities and usage.

Lists are created using square brackets:

```
list = ["Capgemini", "Altran", "Sogeti"]
print(list)
```

#### 1. List Items.

List items are ordered, changeable, and allow duplicate values.

List items are indexed, the first item has index [0], the second item has index [1] etc.

#### 2. Ordered.
```
When we say that lists are ordered, it means that the items have a defined order,
and that order will not change.

If you add new items to a list, the new items will be placed at the end of the list.
```

#### 3. Changeable.
```
The list is changeable, meaning that we can change, add, and remove items in a 
list after it has been created.
```

#### 4. Allow Duplicates.
```
Since lists are indexed, lists can have items with the same value:

list = ["Capgemini", "Altran", "Sogeti", "Capgemini", "Altran", "Sogeti"]
print(list)
```

#### 5. List Length.
```
list = ["Capgemini", "Altran", "Sogeti"]
print(len(list))
```

#### 6. List Items - Data Types.
```
List items can be of any data type:

list1 = ["Capgemini", "Altran", "Sogeti"]
list2 = [1, 5, 7, 9, 3]
list3 = [True, False, False]


More Examples;

list = ["abc", 34, True, 40, "male"]
```

#### 7. Types.
```
From Python's perspective, lists are defined as objects with the data type 'list':

<class 'list'>

What is the data type of a list?

list = ["Capgemini", "Altran", "Sogeti"]
print(type(list))
```

#### 7. The list() Constructor.
```
Using the list() constructor to make a List:

mylist = list(("Capgemini", "Altran", "Sogeti")) 
# note the double round-brackets

print(mylist)
```

#### 7. Python Collections (Arrays).
```
There are four collection data types in the Python programming language:

List is a collection which is ordered and changeable. Allows duplicate members.

Tuple is a collection which is ordered and unchangeable. Allows duplicate members.

Set is a collection which is unordered, unchangeable*, and unindexed. No duplicate members.

Dictionary is a collection which is ordered** and changeable. No duplicate members.
```
