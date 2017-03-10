#HSLIDE
<!-- .slide: data-autoslide="10000" -->


<img src="http://www.cakex.org/sites/default/files/National_Conservation_Training_Center.gif" width="200">
<img src="https://www.python.org/static/img/python-logo.png" width="400">

#### Python for Advanced GIS
<br>
<span style="color:gray">NCTC Advanced GIS</span>
<br>
<span style="color:gray">Daryl Van Dyke</span>

#HSLIDE
## Major Language Elements
- Hello, World!
- Variables and Types
- Lists
- Basic Operators
- String Formatting
- Basic String Operations
- Dictionaries, sets, and iterables

#HSLIDE
## What is Python?

- Interpreted language (JIT compilation)
- Uses the virtual machine model
The basic idea is that we have a python *process*, which sits and waits for instructions/compiled binary code (aka a virtual machine).

#HSLIDE
## What is Python?

HelloWorld.py
```python
print "Hello World!"
print "Hello Again"
print "I like typing this."
print "I'd much rather you 'not'."
print 'I "said" do not touch this.'
```

#HSLIDE
## Flow Control - a basic code block
Flow control is handled by 'blocks'.
In Python, blocks are semantically derived from indents.
The standard is 4 spaces.

#HSLIDE
## Flow Control - a basic code block
In other words, the units of program - the chunks of execution - all have the same indent level.

#HSLIDE
## A Simple Program
```python
#!/usr/bin/python
# That was a shebang (or hashbang) - it tells a \*nix system
#  what program to use to run the script.
#  Windows will ignore it.
#  This is a comment.  Use them, alot.
#  Tell yourself what you are doing, and why
#  They *must* have a hash sign in column 1.
def helloWorld():
     #  comments make other programmers take you seriously
     print "Hello World!"
     print "Hello Again"
     print "I like typing this."

helloWorld()
```

#HSLIDE
## A Simple Program
```python
#  This is a function.  We'll look at them more closely...
#  but notice how the function definition _ends_ with the
#  move back to the 1st Column.  This ends the function
#  block.
def helloWorld():
     #  this function prints stuff
     print "Hello World!"
     print "Hello Again"
     print "I like typing this."

helloWorld()
```

#HSLIDE
## A Simple Program
```python
def helloWorld():
     #  this function prints stuff
     print "Hello World!"
     print "Hello Again"
     print "I like typing this."
#  with the function defined, we can call it.
helloWorld()
#   Because the function needs no inputs, we don't hand it any.
#   We can see this in both the declaration and the call.
```

#HSLIDE
## A Simple Program
```python
#!/usr/bin/python
def helloWorld():
    """
    This is a docstring.  They all have three
    quotes at beginning and end.  They show up magically
    in in-line help (the text that pops up.)
    """
     #  comments make other programmers take you seriously
     print "Hello World!"
     print "Hello Again"
     print "I like typing this."

helloWorld()
```
#HSLIDE
## A Simple Program
```python
#!/usr/bin/python
def helloWorld():
    """ Function helloWorld()
    inputs:   <>
    returns:  <>   """
     #  dood, refactor this later for realz.  2016/01/30
     print "Hello World!"
     print "Hello Again"
     print "I like typing this."
#  The function block ends by closing out of the indent (4 spaces).
#  That makes this the first line of code that actually does something
#      active, other than just define the function object in the compiler.
helloWorld()
```
#HSLIDE
### What is evaluation?
1. Interpreter starts reading through the program.
2. Interpreter sees the `def` keyword - this means that the next line will standardize indent size for this code block.
3. So it keeps reading until it gets to the bottom of the code block (indents back).
4. At that point, it compiles an object (everything is an object) that is a function.
#HSLIDE
### What is evaluation?
5. It then continues along until it gets to the call to that function, on the first column.
6. The call matches the object name, so any arguments in the parenthesis are passed to the object.
7. The function is evaluated with the input data, if any.
#HSLIDE
### What is evaluation?
8. Anything returned by the function (with the `return` keyword) is handed back to the calling block.
9. If there is an assignement, e.g. `output = thisFunction(input)`, the LHS variable is mapped to the object in memory.
10. Otherwise, if there is no assignement, anything returned goes to standard out.

#HSLIDE
## What is Python?

HelloWorld_v1.py
```python
#!/usr/bin/python
# Let's do a better version
def helloWorld(inputText):
     #  comments make other programmers take you seriously
     print "Hello World!"
     print "Hello Again"
     print "I like typing this."
     print inputText
     return "I printed "+inputText+" just like you asked!"
#  so what happens with these?
helloWorld()
output = helloWorld("you do you...")
output = helloWorld(1+1)  # equivalent to helloWorld(1L+1L)
```
#HSLIDE
##

#HSLIDE
## Major Language Elements

- Hello, World!
- Variables and Types
- Lists
- Basic Operators
- String Formatting
- Basic String Operations
- Dictionaries, sets, and iterables

#HSLIDE
## Lists and Iterators
Lists are one of the most common data structures in Python.
- Compound data type
- make on with square brackets ```listNum = [1,2,3]``` or empty ```listE = []```
- lists are **mutable**

#HSLIDE
## List Indexing
Call it by it's position, 0-index.
```python
>>> listE = ["ABBA", 3, False]
>>> listE[0]
'ABBA'
>>> listE[-1]
False
>>> listE[0:1]
['abba']
>>> listE[0:2]
['abba', 3]
>>>
```
#HSLIDE
## List Indexing and Mutability
```
>>> listE[0] = "Iron Maiden"
>>> listE
['Iron Maiden', 3, False]
>>>
```
#HSLIDE
## ```list``` has some awesome methods!
Remember, any list is an instance of the List class.
Learning Python is a process of collecting memories of all these methods, and connecting them to problems.
##  Check the Docs alot!

#HSLIDE
## Commonly Used Methods
```python
>>> listE.append("this String")
>>> listE
['Iron Maiden', 3, False, 'this String']
>>> len(listE)
4
>>> #Nested list
>>> listF = ["Oh NO!", "This is too much!", True]
>>> listE.append(listF)
>>> listE
['Iron Maiden', 3, False, 'this String', ['Oh NO!', 'This is too much!', True]]
>>>
```
#HSLIDE
## More common ```list``` methods and functions



#HSLIDE
## A Simple Program - Shell mode
```python
>>> # Fibonacci series:
... # the sum of two elements defines the next
... a, b = 0, 1
>>> while b < 10:
...     print b
...     a, b = b, a+b
...
1
1
2
3
5
8
```
```print```, ```while```, multiple assignement

#HSLIDE
## Flow Control 1: ```if```
```python
>>> x = int(raw_input("Please enter an integer: "))
Please enter an integer: 42
>>> if x < 0:
...     x = 0
...     print 'Negative changed to zero'
... elif x == 0:
...     print 'Zero'
... elif x == 1:
...     print 'Single'
... else:
...     print 'More'
...
More
```
#HSLIDE
## ```if``` Bonus Round
```elif``` - chains of if
```else``` - optional end to if-then chain

Other languages have a ```switch``` or ```case``` logical block.
Python uses ```if ... elif ... elif ... (else)``` structure.

#HSLIDE
## ```for```
```for``` in Python iterates over iterable objects (containers).
Not based on arithemic or logical conditions.
```python
>>> # Measure some strings:
... words = ['cat', 'window', 'defenestrate']
>>> for w in words:
...     print w, len(w)
...
cat 3
window 6
defenestrate 12
```
#HSLIDE
## ```range()``` function
```range()``` generates arithmetic progressions.
Can have 1, 2, or 3 arguments.
1.  implicit start 0, argument is # of entries generated.
This will **not** include the #.
```python
>>> range(10)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

#HSLIDE
## ```range()``` function
2.  1st argument start, 2nd argument "stop" position.
Python "stops" before it gets to the value.
```python
>>> range(5, 10)
[5, 6, 7, 8, 9]
```

#HSLIDE
## ```range()``` function
3.  Start, Stop, and Step
Like 2, but it specifies a step-size
```python
>>> range(0, 10, 3)
[0, 3, 6, 9]
>>> range(-10, -100, -30)
[-10, -40, -70]
```

#HSLIDE
## Putting them together...
remember ``len()```?
```python
>>> a = ['Mary', 'had', 'a', 'little', 'lamb']
>>> for i in range(len(a)):
...     print i, a[i]
...
0 Mary
1 had
2 a
3 little
4 lamb
```

#HSLIDE
## ```break``` and ```continue```
```break``` steps out 1 logical block from the enclosing ```for`` or ```while``` loop.
```python
>>> for n in range(2, 10):
...     for x in range(2, n):
...         if n % x == 0:
...             print n, 'equals', x, '*', n/x
...             break
...     else:
...         # loop fell through without finding a factor
...         print n, 'is a prime number'
...
2 is a prime number
3 is a prime number
4 equals 2 * 2
5 is a prime number
```

#HSLIDE
### Typing
- Duck Typing
- Dynamic Typing
- Strongly typed

Python is "strongly typed" = it does not do implicit type conversion.
Type error = Crash (an Exception)

This is not "static typing" - we can change the type of a variable by re-referencing it, and the compiler doesn not check ahead of time.

The term 'duck typing' is now used to describe the dynamic typing paradigm used by the languages in this group.

#HSLIDE
### Typing
So what does this mean?  Python very much cares that the type of the object matches the requirements of the function/method.

- String concatenation:
We want to append the value of the field to an intro string (```"The temperature is :"``` and ```valTemp```).
Using the string concatenation operator (```+```) on this example will throw a run-time error.
You need to explicity convert the type for this to work.  ( `str(valTemp)` )

#HSLIDE
### Typing
Confession:
Failing to explicity handle type conversion is my most common 1st run error.
Especially as you move between languages frequently.

#HSLIDE
## Statements
### Assignment ```=```
- We recall:
1.  All python things are objects.
2.  All objects have classes - that is, **they are an instance of a class.**
- Python has two fundamental flavors of objects.  Mutable and immutable.
- Mutable objects can be changed in place, immutable cannot.
- When we 'change' immutable objects, we are really re-building that object and transferring the symbol name to that object.
<img src="https://i.stack.imgur.com/M3iZD.png">


- Assignment (token `=`, the equals sign).
- Different than other C-style languages (C, Java, C++, etc).
- Assignment in C, e.g., `x = 2`, translates to "typed variable name x receives a copy of numeric value 2".  The memory for this element (determined by data type and width) is allocated, the data are copied over, and the *variable name* is an alias or symbolic address for that memory location.  Therefore, pointers, addresses, referencing, de-referencing, and pointer arithmetic.

#HSLIDE
## Statements
### Assignment *=* ... in Python
- ```x = 2``` - *in Python* - means:
"(generic) name x receives a reference to a separate, dynamically allocated object of numeric (int) type of value 2."
<img src="http://archive.oreilly.com/oreillyschool/courses/Python1/images/lessons/ModuleVsObjectSpace.jpg">
***This is termed binding the name to the object.***

#HSLIDE
### Assignment
 To be technical - they aren't variables.  They are names bound to objects.

 Names may be subsequently rebound at any time to objects of greatly varying types...
 -strings,
 -procedures,
 -complex objects with data and methods, etc.

#HSLIDE
### Assignment
OK - what happens?

```x = 2; y = 2; z = 2```

#HSLIDE
### Assignment
```x = 2; y = 2; z = 2```
three names and one numeric object,
to which all three names are bound.

#HSLIDE
### Assignement
Since a name is a generic reference holder it is unreasonable to associate a fixed data type with it.
However at a given time a name will be bound to some object, which will have a type;
***thus there is dynamic typing.***

#HSLIDE
### Assignment
Since it is just a name, pick a good one.  While you can do all of the above, why not?
Well, there are very good (and very advanced) reasons to do this... object polymorphism, for one.
Class inheritance and class hierarchies, another.

#HSLIDE
### Assignment - Read PEP-8
Python Enhancement Proposals are how the Python community suggests, and vets, language enhancements.
I read PEP-8 probably every 3 or 4 years, and now I find my code looks *pretty much like professional Python code*...
but I should do more comments.

#HSLIDE
### Assignment - PEP-8
YES:
```python
# Aligned with opening delimiter.
foo = long_function_name(var_one, var_two,
                         var_three, var_four)
```
#HSLIDE
### Assignment - PEP-8
```python
# More indentation included to distinguish this from the rest.
def long_function_name(
        var_one, var_two, var_three,
        var_four):
    print(var_one)
```

#HSLIDE
### Style - PEP-8
```python
# Yes: easy to match operators with operands
income = (gross_wages
          + taxable_interest
          + (dividends - qualified_dividends)
          - ira_deduction
          - student_loan_interest)
```

#HSLIDE
### Style - PEP-8
I like to use 'variable names' like this in my code:
*type*Name
```listFC```
```intNumFeat``
```boolTestLoop``
```objLASFile```
etc...
This convention ***does nothing real** - but I find it very helpful.


#HSLIDE
## Statements
### Flow Control p. 1
- The if statement, which conditionally executes a block of code, along with else and elif (a contraction of else-if).
- The for statement, which iterates over an iterable object, capturing each element to a local variable for use by the attached block.
- The while statement, which executes a block of code as long as its condition is true.
## Statements
### Flow Control p. 2
- The try statement, which allows exceptions raised in its attached code block to be caught and handled by except clauses; it also ensures that clean-up code in a finally block will always be run regardless of how the block exits.
- The with statement (from Python 2.5), which encloses a code block within a context manager (for example, acquiring a lock before the block of code is run and releasing the lock afterwards, or opening a file and then closing it), allowing Resource Acquisition Is Initialization (RAII)-like behavior.
 The pass statement, which serves as a NOP. It is syntactically needed to create an empty code block.

#HSLIDE
## Statements
### Program Constructs
- The ```class``` statement, which executes a block of code and attaches its local namespace to a class, for use in object-oriented programming.
- The ```def``` statement, which defines a function or method.
- The ```assert``` statement, used during debugging to check for conditions that ought to apply.

#HSLIDE
## Statements
### Program Constructs
- The ```yield``` statement, which returns a value from a generator function. From Python 2.5, yield is also an operator. This form is used to implement coroutines.
- The ```import``` statement, which is used to import modules whose functions or variables can be used in the current program.
- The ```print``` statement was changed to the print() function in Python 3.

### GitPitch turns <span style="color: #e49436; text-transform: none">PITCHME.md</span> into interactive, online slideshows.
<br>
<span style="color:gray; font-size:0.6em;">[ JUST LIKE THIS ONE ]</span>

#HSLIDE
## Scope
Scope is the technical term for how variables are visible in a programming language.  It's critical we have a clear understanding of how & why this works, so we can:
- predict how our code should work,
- and debug it when it doesn't.

#HSLIDE
## Scope
Python has
1. function scope,
2. module scope, and
3. global scope.

#HSLIDE
## Scope - when we 'create a variable'
Names enter scope at the start of a context (function, module, or globally),
and exit scope when a non-nested function is called or the context ends.
If a name is used prior to variable initialization, this raises a runtime exception.

#HSLIDE
## Scope - when we 'call a variable'
 If a variable is simply accessed (not assigned to) in a context, name resolution follows the LEGB rule:
 1. Local,
 2. Enclosing,
 3. Global,
 4. Built-in.

However, if a variable is assigned to, it defaults to creating a local variable, which is in scope for the entire context. Both these rules can be overridden with a global or nonlocal (in Python 3) declaration prior to use, which allows accessing global variables even if there is an intervening nonlocal variable, and assigning to global or nonlocal variables.

#HSLIDE
## Scope - forward refernce ok
As a simple example, a function resolves a variable to the global scope:
```python
>>> def f():
...     print(x)
...
>>> x = 'global'
>>> f()
global
```
We have initialized `x` before assigning a value.  As long as Python can resolve the symbol (how?) before execution, it's ok.

#HSLIDE
## Scope - it can be tricky
```python
>>> def f():
...     x = 'f'
...     print(x)
...
>>> x = 'global'
>>> print(x)
global
>>> f()
f
>>> print(x)
global
```
#HSLIDE
## Scope - What about now?
```python
>>> def f():
...     print(x)
...     x = 'f'
...
>>> x = 'global'
>>> f()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "<stdin>", line 2, in f
UnboundLocalError: local variable 'x' referenced before assignment
```
#HSLIDE
## Scope - Contrast with R
```r
> a=1
> b=2
> f<-function(x)
+ {
+     a*x + b
+ }
> g<-function(x)
+ {
+     a=2
+     b=1
+     f(x)
+ }
```
#HSLIDE
## Scope - Contrast with R
```r
> a=1
> b=2
> f<-function(x)
+ {
+     a*x + b
+ }
> g<-function(x)
+ {
+     a=2
+     b=1
+     f(x)
+ }
> g(2)
[1] 4
>
```

#HSLIDE
## Scope - Same in Python
```python
>>> a = 1
>>> b = 2
>>> def f(x):
	return a*x + b

>>> def g(x):
	a = 2
	b = 1
	f(x)

>>> g(2)
>>> def g(x):
	a = 2
	b = 1
	print f(x)
```
Answer?

#HSLIDE
## Scope - Same in Python
```python
>>> a = 1
>>> b = 2
>>> def f(x):
	return a*x + b

>>> def g(x):
	a = 2
	b = 1
	f(x)

>>> g(2)
>>> def g(x):
	a = 2
	b = 1
	print f(x)
>>> g(2)
4
>>>
```
#HSLIDE
### Flow Control
- Conditions
- Loops
- Functions
- Classes and Objects
- Dictionaries
- Modules and Packages

#HSLIDE
##  Objects and Classes
All Python 'things' are **instances** of an object.
A **Class** is a blueprint for a data model.  It defines a 'thing' that has:
- initilization (```__init__```) method
- additional methods (functions bound to the object)
- and attributes ("slots" that hold data, and are addressable by name.

#HSLIDE
## Classes and Objects
When we want to make one of these, we "instantiate it",
or "make an instance".

A class can have attributes (variables) that are unique to that instance,
or it can have variables shared by all instances of that class.

#HSLIDE
## Class & Object Nomenclature
class 'variable'    == class attribute
class 'function'    == class 'function'
instance 'variable' == an object's unique attributes
instance 'function' == an object's method, almost always common to all instances.

#HSLIDE
## Why Classes?
Classes are blueprints, or ***data models***
They allow us to organize code in a way that makes logical sense.
Classes are ***awesomesauce**.
The classic tests are 'is a' and 'has a'.
'is a ' -->  class instance
'has a ' --> class attribute

#SLIDE
## UML (Universal Markup Language)
There is a standard way of drawing ('marking up') classes.
This should be awesome, a way of using the graphic tools to model information and then generate code.
I haven't seen it work that way yet, but probably my fault.

#HSLIDE
## UML (Universal Markup Language)
<img src="http://agilemodeling.com/images/models/classDiagramStudentAddress.jpg">

#HSLIDE
So - the classic example.  Things that are dogs.

#HSLIDE
### The Dog Class
```python
class Dog:

    kind = 'canine'         # class variable shared by all instances

    def __init__(self, name):
        self.name = name    # instance variable unique to each instance
```
#HSLIDE
## The ```__init__``` method:
```python
class Dog:

    kind = 'canine'         # class variable shared by all instances

    def __init__(self, name):
        self.name = name    # instance variable unique to each instance
```
- Always called when an object is instantiated
- Always has *at least one* argument (***self***)
- Is how we pass arguments into the creation of the class.

#HSLIDE
## The ```__init__``` method:
***Import concept:***
Defining what you need for ```__init__``` is a critical part of the data modeling.
Think carefully.

#HSLIDE
```python
class Dog:
    kind = 'canine'         # class variable shared by all instances
    def __init__(self, name):
        self.name = name    # instance variable unique to each instance

>>> d = Dog('Fido')
>>> e = Dog('Buddy')
```
#HSLIDE
So now we have two instances of the Dog Class.
One called (name-bound) to ```d```, the other to ```e```.

#HSLIDE
# Class Variables vs. Instance Variables
```python
>>> d.kind                  # shared by all dogs
'canine'
>>> e.kind                  # shared by all dogs
'canine'
>>> d.name                  # unique to d
'Fido'
>>> e.name                  # unique to e
'Buddy'
```
#HSLIDE
## Careful with those class variables...
```python
class Dog:

    tricks = []             # mistaken use of a class variable

    def __init__(self, name):
        self.name = name

    def add_trick(self, trick):
        self.tricks.append(trick)

>>> d = Dog('Fido')
>>> e = Dog('Buddy')
>>> d.add_trick('roll over')
>>> e.add_trick('play dead')
>>> d.tricks                # unexpectedly shared by all dogs
['roll over', 'play dead']
```
#HSLIDE
## You probably wanted this...
```python
class Dog:

    tricks = []             # mistaken use of a class variable

    def __init__(self, name):
        self.name = name

    def add_trick(self, trick):
        self.tricks.append(trick)

>>> d = Dog('Fido')
>>> e = Dog('Buddy')
>>> d.add_trick('roll over')
>>> e.add_trick('play dead')
>>> d.tricks                # unexpectedly shared by all dogs
['roll over', 'play dead']
```
#HSLIDE
## Too much for now...
File these away:
***Class inheritance:***
If Fido 'is a' Dog, and a Dog 'is a' Mammal, and a Mammal 'is an' Animal.
Can we do that with classes?  Oh sure!

#HSLIDE
```python
class Animal:
    def __init__(self, strSpineType)
        self.spine = strSpineType
    def move(self, moveType):
        self.move = "unknown"
        print "I don't know!"
Class Dog(Animal):
    # here, the move method 'overrides' the base class one.
    #Cool, huh?
    def move(self, moveType):
        i = 10
        while i > 0:
          self.move = "crawl"
          i = i - 1
```
#HSLIDE
## Name Mangling
In a nutshell, in Java we can 'lock down' methods and attributes so they are *unavailable* outside the class.
Python doesn't support that, we have a convention.  If something is **not** to be messed with outside of the class, use an underscore up front.
```self._numWidgets```
This means that 'the object manages this attribute, don't mess with it.

#HSLIDE
## The Object as a Bucket
"Gosh Daryl, that seems complicated.  What if I just want a container to dump information into?"
```python
class Dog:
    pass  #remember pass?  It allows an empty block

fido = Dog()  #tell me about this dog...
fido.fleas = False
fido.food = "hungry"
fido.legs = 3
```


#HSLIDE
<!-- .slide: data-autoslide="2000" -->

### No more <span style="color: #666666">Keynote.</span>
### <span class="fragment" data-fragment-index="1" data-autoslide="2000">No more <span style="color: #666666">Powerpoint.</span>
<br>
### <span class="fragment" data-fragment-index="2" data-autoslide="3500">Just <span style="color: #e49436">Markdown</span>. Then <span style="color: #e49436">Git-Commit</span>.</li>

#HSLIDE
### ArcPy is not vanilla python...
In addition to the esri help which describes all of the parameters of a function and how to access them from Python you can also get Python syntax (the structure of the language) for a tool like this :

1. Run the tool interactively (e.g. buffer) with your input data, output data and any other relevant parameters (e.g. distance to buffer)

2. Go to the Geoprocessing -> Results window and right click the completed tool run.

3. Pick "Copy Python Snippet"

4. Paste the code into PythonWin or the Python code window to see how you would code the same operation you just ran in Desktop in Python.

#HSLIDE
### ArcPy is not vanilla python...


#HSLIDE
### ArcPy is not vanilla python...




#HSLIDE
### Go for it.
### Just add <span style="color: #e49436; text-transform: none">PITCHME.md</span> ;)
