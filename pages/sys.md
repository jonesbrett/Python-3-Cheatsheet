- [Return to Table of Contents](/../../)

## sys — System-specific parameters and functions

sys.path

A list of sting that specifies the search path for modules. As initialized upon program startup, the first item of 
this list, path[0], is the directory containing the script that was used to invoke the Python interpreter.

```python
# You can specify which directory you want to reference, ('.') references the root.
import sys
sys.path.append(".")
from bs4 import BeautifulSoup

# The code above imports the 'sys' module and set the system path to the root and imports 'BeautifulSoup' from 
# the folder called 'bs4'

#application
#|
#|--[bs4]
#|
#|--[folder]
#      |
#      |--script.py
```

- [Return to Table of Contents](/../../)
