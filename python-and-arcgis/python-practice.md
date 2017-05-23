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





