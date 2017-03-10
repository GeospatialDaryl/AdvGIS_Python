# Exercise 2:

## Purpose
The purpose of this exercise is to enable you to identify a portion of your project that would benefit from automation.
In addition to defining one or more functions, you need to develop a script that performs some processing.

To get this done:
## Step 1:  Script Design
1. Develop a script file that includes and ```import``` statements, a brief commented description, and the inputs and outputs for the whole script.
2. Start to implement this script.  You should identify those parts that are most complex (such as nested loops/conditionals).
3. Build the framework from the outside in.  If you are developing a class or function based approach, build a dummy (empty, use ```pass``) version of the functions and objects you will flesh out.  At the end of the script, include an execution statement with ```if __name__```.
4. Make sure the empty, dummy script runs.  This allows you test that you are:
  + getting data in,
  + your script is formatted correctly,
  + and that any problems you have moving forward are the results of added function.

If you are working with arcpy, you probably want a start that looks like this:
```python
import arcpy

#env variables
arcpy.env.workspace = r"c:/data"
arcpy.env.snapRaster = r"c:/data/awesomesauce.img"
arcpy.env.overwriteOutput = True
#etc ...
```
At the bottom of your template, add this call to start your program:
```python
if __name__ == "__main__":
    ...start program here...
```
This allows us to reuse the functions and classes from this script as a module.

## Step 2: Implement Script
3. With that strategy, start at the inside of the loop and use print statements.
You may find it helpful to use a ```Verbose = True``` flag at the top of the script.  Then, when you have a debug or development print statement, you can turn them on and off.
```python
if Verbose: print thisValue
```
4.  Add functionality one step at a time.  For instance, if you are going to do something
  + to a feature class,
  + then do a table join,
  + then calculate based on that join,
use a dummy column in the original feature class to get the main flow working (and **tested**).


## Hints:
Execute.  Profit.
