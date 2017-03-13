#  ArcPy Cheat Sheet and Basic ArcPy

##  1.  Creating Basic Workflows

1.  Use the python interface in ArcPy
Try to open the python interface.  

<img src="http://desktop.arcgis.com/en/arcmap/10.3/analyze/executing-tools/GUID-15634547-7DA4-4AA4-85F0-20F78B071574-web.png">

Note how when you drag a Feature Class object from the Table of Contents (dragging a Layer object) to the interface, you are creating a character string.  The FC gets it's name automatically wrapped in quotes, and we can refer to that object (the Layer object) by that name.

This is an important sublety, because there is a difference between:
```pointCritters``` <-- this is a object on it's own, it can be addressed using the dot-methods and dot-attributes
```'pointCritters'``` <--- this is a String.  It can be sliced, or used to address the layer object inside of the ArcMap ArcPy interface.

In a stand-alone script, this won't work the same way.  

2.  Know the difference between a Layer and a Feature Class.  

In ArcMap, we don't really deal with Feature Classes.  Any time we add data to ArcMap, we are creating a layer file with default values.  It can be confusing to switch from ArcMap to scripting, because we expect that Arc is doing this for me.  In scripting, some operations (like Buffer) can be done on a FC directly.  Other operations require a Layer instead.

3.  Use the Results tab!  It's awesome!
When assembling a work flow, how do we figure out what is going on?  We run through the work flow with one Layer.

Often, I build a single "avenue" that moves a FC from beginning to end.  Then, I can open up the Results tab, and R-Clik "Copy As Python Snippet".  Paste each of those into a text file, and clean it up.
