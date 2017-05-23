# Python Practice



#### 00.pythonIntro.py

```
import sys
######################################################
# sys commands
# sys.copyright
# sys.path
# sys.platform
# sys.version
######################################################
print(sys.version)

import os
######################################################
# os commands
# os.name # name of the operating system
# os.chdir(path) # change the current directory to path
# os.getcwd() # return a string representing the current working directory
# os.listdir(path) # return a list containing the names of the entries
#                  # in the directory given by path
######################################################

#current directory
os.getcwd()

#change directory
os.chdir("M:/Classes(Spring2017)/G460_134SHD/01.practice/0213_data/tmax_ann_ascii")
cwd = os.getcwd()
os.listdir(cwd)

# run a script
C:\Python27\ArcGIS10.3\python.exe M:\Classes(Spring2017)\G460_134SHD\01.practice\00.python\test.py

#getting help
#help(os.listdir)
```

#### 01\_var&str.py

```
# -*- coding: cp1252 -*-
# https://docs.python.org/2/tutorial/introduction.html
# this is the first comment
theNum = 1 # the second comment
theText = "# this is not a comment because it's inside" 

# using python as a calculator
30 - 5 * 3
19 / 4  # int / int -> int
19 / 4.0 # int / float -> float
19 // 4.0 # explicit floor division discards the fractional part
19 % 4 # the % operator returns the remainder of the division

7 ** 2 # 7 squared
3 ** 4 # 3 to the power of 4

# variable
width = 30
height = 4 * 8
print('width')
print(width)
# in interactive mode, the last printed expression is assigned to the variable _
tax = 11.5 / 100
price = 110.50
price * tax
price + _
round(_, 2)

# strings
'spam eggs'  # single quotes
'doesn\'t'  # use \' to escape the single quote...
"doesn't"  # ...or use double quotes instead
'"Yes," he said.'
"\"Yes,\" he said."
'"Isn\'t," she said.'

# If you don’t want characters prefaced by \ to be interpreted as special characters,
# you can use raw strings by adding an r before the first quote:
print 'C:\some\name'  # here \n means newline!
print r'C:\some\name'  # note the r before the quote - similar to ' in Excel?

# String literals can span multiple lines.
# One way is using triple-quotes: """...""" or '''...'''.
# End of lines are automatically included in the string,
# but it’s possible to prevent this by adding a \ at the end of the line.
# help(round)
print """
    round(...)
         round(number[, ndigits]) -> floating point number

         Round a number to given precision in deciman digits (default 0 digits).
         This always returns a floating point number. Precision may be negative.
"""

print """hi
there
"""
print """hi\
there
"""

# Strings can be concatenated (glued together)
# with the + operator, and repeated with *
3 * "ha" + " con" + "cate" + "nate"

# Two or more string literals (i.e. the ones enclosed between quotes) next to each other
# are automatically concatenated.
"moo"   "kie"   'is''here'
# This only works with two literals though,
# not with variables or expressions.
prefix = 'Py'
prefix 'thon'  # can't concatenate a variable and a string literal
('ha' * 3) 'nope' # syntax error
# if you want to concatenate variables or a variable and a literal, use +
prefix = 'Py'
prefix + 'thon'
# This feature is particularly useful when you want to break long strings.
# enclose the whole expression in an outer set of parenthesis --
# then the expression is allowed to span multiple lines
thisQ = ('I\'d rather be hated for who I am, '
         'than loved for who I am not.')
thatQ = ("I cannot give you the formula for success, "
         "but I can give you the formula for failure, "
         "which is: try to please everybody.")

# Strings can be indexed (subscripted), with the first character having index 0.
# There is no separate character type; a character is simply a string of size one
word = 'Python'
word[0]  # character in position 0
word[5]  # character in position 5
# Indices may also be negative numbers, to start counting from the right.
# Note that since -0 is the same as 0, negative indices start from -1.
word[-1]  # last character
word[-2]  # second-last character
word[-6]
# In addition to indexing, slicing is also supported.
# While indexing is used to obtain individual characters,
# slicing allows you to obtain a substring.
word[0:2]  # characters from position 0 (included) to 2 (excluded)
word[2:5]  # characters from position 2 (included) to 5 (excluded)
# Note how the start is always included, and the end always excluded.
# This makes sure that s[:i] + s[i:] is always equal to s.
word[:2] + word[2:]
word[:4] + word[4:]
word[:2]   # character from the beginning to position 2 (excluded)
word[4:]   # characters from position 4 (included) to the end
word[-2:]  # characters from the second-last (included) to the end
word[:-2]
# One way to remember how slices work is to think of the indices
# as pointing between characters,
# with the left edge of the first character numbered 0.
#  +---+---+---+---+---+---+
#  | P | y | t | h | o | n |
#  +---+---+---+---+---+---+
#  0   1   2   3   4   5   6
# -6  -5  -4  -3  -2  -1
# Python strings cannot be changed — they are immutable (an object with a fixed value).
# Therefore, assigning to an indexed position in the string results in an error.
word[0] = 'J' # TypeError: 'str' object does not support item assignment
word[2:] = 'py' # TypeError: 'str' object does not support item assignment
# If you need a different string, you should create a new one.
'J' + word[1:]
newPy = word[:2] + 'py'
# The built-in function len() returns the length of a string.
s = 'supercalifragilisticexpialidocious'
len(s)
```



