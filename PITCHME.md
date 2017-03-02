#HSLIDE
<!-- .slide: data-autoslide="10000" -->

![LOGO](http://www.cakex.org/sites/default/files/National_Conservation_Training_Center.gif)

#### Python for Advanced GIS
<br>
<span style="color:gray">Markdown Presentations For Developers</span>
<br>
<span style="color:gray">on</span>
<br>
<span style="color:gray">GitHub, GitLab and Bitbucket</span>

#HSLIDE

## What is Python?

- Interpreted language (JIT compilation)
- Uses the virtual machine model
The basic idea is that we have a python *process*, which sits and waits for instructions (aka a virtual machine).  

#HSLIDE
### Major Language Elements
//<span style="color: #e49436; text-transform: none">PITCHME.md</span> into interactive, online slideshows.

- Hello, World!
- Variables and Types
- Lists
- Basic Operators
- String Formatting
- Basic String Operations
- Dictionaries, sets, and iterables

#HSLIDE
### Flow Control
- Conditions
- Loops
- Functions
- Classes and Objects
- Dictionaries
- Modules and Packages

#HSLIDE

### Typing
- Duck Typing
- Dynamic Typing
- Strongly typed
Smalltalk, Perl, Ruby, Python, and Self are all "strongly typed" in the sense that typing errors are prevented at runtime and they do little implicit type conversion, but these languages make no use of static type checking: the compiler does not check or enforce type constraint rules.

The term duck typing is now used to describe the dynamic typing paradigm used by the languages in this group. (wikipedia)

#HSLIDE

### Typing
So what does this mean?  Python very much cares that the type of the object matches the requirements of the function/method.

- String concatenation:
We want to append the value of the field to an intro string ("The temperature is :" *valTemp*).
Using the string concatenation operator (*+*) on this example will throw a run-time error.
You need to explicity convert the type for this to work.  ( *str(valTemp)* )   

#HSLIDE
## Statements
### Assignment *=*

- Assignment (token '=', the equals sign). This operates differently than in traditional imperative programming languages, and this fundamental mechanism (including the nature of Python's version of variables) illuminates many other features of the language. Assignment in C, e.g., x = 2, translates to "typed variable name x receives a copy of numeric value 2". The (right-hand) value is copied into an allocated storage location for which the (left-hand) variable name is the symbolic address. The memory allocated to the variable is large enough (potentially quite large) for the declared type. In the simplest case of Python assignment, using the same example, x = 2, translates to "(generic) name x receives a reference to a separate, dynamically allocated object of numeric (int) type of value 2." This is termed binding the name to the object. Since the name's storage location doesn't contain the indicated value, it is improper to call it a variable. Names may be subsequently rebound at any time to objects of greatly varying types, including strings, procedures, complex objects with data and methods, etc. Successive assignments of a common value to multiple names, e.g., x = 2; y = 2; z = 2 result in allocating storage to (at most) three names and one numeric object, to which all three names are bound. Since a name is a generic reference holder it is unreasonable to associate a fixed data type with it. However at a given time a name will be bound to some object, which will have a type; thus there is dynamic typing.
#HSLIDE
## Statements
### Flow Control
- The if statement, which conditionally executes a block of code, along with else and elif (a contraction of else-if).
- The for statement, which iterates over an iterable object, capturing each element to a local variable for use by the attached block.
- The while statement, which executes a block of code as long as its condition is true.
- The try statement, which allows exceptions raised in its attached code block to be caught and handled by except clauses; it also ensures that clean-up code in a finally block will always be run regardless of how the block exits.
- The with statement (from Python 2.5), which encloses a code block within a context manager (for example, acquiring a lock before the block of code is run and releasing the lock afterwards, or opening a file and then closing it), allowing Resource Acquisition Is Initialization (RAII)-like behavior.
 The pass statement, which serves as a NOP. It is syntactically needed to create an empty code block.

#HSLIDE
## Statements
### Program Constructs
- The class statement, which executes a block of code and attaches its local namespace to a class, for use in object-oriented programming.
- The def statement, which defines a function or method.
- The assert statement, used during debugging to check for conditions that ought to apply.
- The yield statement, which returns a value from a generator function. From Python 2.5, yield is also an operator. This form is used to implement coroutines.
- The import statement, which is used to import modules whose functions or variables can be used in the current program.
- The print statement was changed to the print() function in Python 3.[54]

### GitPitch turns <span style="color: #e49436; text-transform: none">PITCHME.md</span> into interactive, online slideshows.
<br>
<span style="color:gray; font-size:0.6em;">[ JUST LIKE THIS ONE ]</span>

#HSLIDE
<!-- .slide: data-autoslide="2000" -->

### No more <span style="color: #666666">Keynote.</span>
### <span class="fragment" data-fragment-index="1" data-autoslide="2000">No more <span style="color: #666666">Powerpoint.</span>
<br>
### <span class="fragment" data-fragment-index="2" data-autoslide="3500">Just <span style="color: #e49436">Markdown</span>. Then <span style="color: #e49436">Git-Commit</span>.</li>

#HSLIDE

<span style="color: #e49436">STEP 1. PITCHME.md</span>

![MARKDOWN](https://d1z75bzl1vljy2.cloudfront.net/hello-world/markdown.png)

Create GitPitch slideshow content using GitHub flavored Markdown in your favorite editor.

#HSLIDE

<span style="color: #e49436">STEP 2. GIT-COMMIT</span>

![TERMINAL](https://d1z75bzl1vljy2.cloudfront.net/hello-world/terminal.png)

Git-commit on any branch and push your PITCHME.md to GitHub, GitLab or Bitbucket.

#HSLIDE

<span style="color: #e49436">STEP 3. GET THE WORD OUT!</span>

<br>

<span style="font-size: 1.3em;"><span style="color:white">htt</span><span style="color:white">ps://git</span><span style="color: #e49436">pitch</span><span style="color: white">.com/<span style="color: #e49436">user</span>/<span style="color: #e49436">repo</span>/<span style="color: #e49436">branch</span></span>

<br>

Instantly use your GitPitch slideshow URL to promote, pitch or present absolutely anything.

#HSLIDE
<!-- .slide: data-autoslide="11000" -->

<span style="color: #e49436">GIT</span>PITCH DESIGNED FOR SHARING

![SOCIAL](https://d1z75bzl1vljy2.cloudfront.net/hello-world/gp-social.jpg)

- View any slideshow at its public URL
- Promote any slideshow using a GitHub badge
- Embed any slideshow within a blog or website
- Share any slideshow on Twitter, LinkedIn, etc
- Print any slideshow as a PDF document
- Download and present any slideshow offline

#HSLIDE
<!-- .slide: data-autoslide="12000" -->

<span style="color: #e49436">GIT</span>PITCH FEATURE RICH SLIDESHOWS

- GitHub Flavored Markdown +
- Code Block and GIST Slides
- Image and Video Slides
- Custom Logos and Backgrounds
- Multiple Themes And More
- <span style="color: #e49436">Plus...</span>
- Your Slideshow Is Part Of Your Project
- Under Git Version Control Within Your Git Repo


#HSLIDE
<!-- .slide: data-autoslide="8000" -->

### Go for it.
### Just add <span style="color: #e49436; text-transform: none">PITCHME.md</span> ;)
