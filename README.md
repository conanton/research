# Function_dict.ipynb Context

This python script, Function_dict.ipynb, currently in the form of a Jupyter Notebook, takes in a python script in .txt format and parses through the file to 
identify functions and their names, arguments/parameters, and comments and puts them into a dictionary. Finally, upon completion, the function will convert the
dictionary into a .json file and dump it. 

How to use:
Seeing that the file is currently a notebook, the user will need to first run the first four cells in Function_dict.ipynb to initialize the program. Using the
function is fairly simple. In a new cell, the user will input the following line:

  fndict([insert file name ending with .txt], [insert dictionary name here])

For the first input, the user will simply enter the filename (as a string) of the python script they want a dictionary for.
For the second input, the user will enter {} (empty dictionary) if they want to create a new dictionary, or they could enter an already existing dictionary 
in the form of a variable name (e.g. x) to add onto it.

An example input would look like this:
  fndict('mypyfile.txt', {})
  fndict('example.txt', dict)
  
Keep in mind that the current version of this requires that the .py file is converted to a .txt file for it to work. The input file must also be contained in the
same folder as the Function_dict.ipynb file.

The cells below the definition of the 3 functions used in the script are example usages of the program. The final cell titled "#Test Cases" lists the test cases
used and concerns with each one.

* Many of the test cases used came from the pytorch/caffe2/python repository *

Challenges:
- Code currently only scans for a select few types of commenting, so oddly-styled programs (including comments above the header of a function) may not be parsed correctly.
