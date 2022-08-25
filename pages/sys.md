- [Return to Table of Contents](/../../)

## Sys.Path.Append

Sys.path is a list of directories where the Python interpreter searches for modules. If you need to specify a different directory, you can append it to the list using the .append() to the sys.path:

```python
import sys
from pprint import pprint
pprint(sys.path)

['c:\\Users\\Admin\\Desktop\\Python\\Sandbox',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\python310.zip',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\DLLs',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\lib',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\lib\\site-packages',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\lib\\site-packages\\win32',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\lib\\site-packages\\win32\\lib',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\lib\\site-packages\\Pythonwin']

 import sys
sys.path.append('c:\\Users\\Admin\\Desktop\\Python\\')
from pprint import pprint
pprint(sys.path)

['c:\\Users\\Admin\\Desktop\\Python\\Sandbox',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\python310.zip',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\DLLs',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\lib',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\lib\\site-packages',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\lib\\site-packages\\win32',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\lib\\site-packages\\win32\\lib',
 'C:\\Users\\Admin\\AppData\\Local\\Programs\\Python\\Python310\\lib\\site-packages\\Pythonwin',
 'c:\\Users\\Admin\\Desktop\\Python\\']

# You can specify which directory you want to reference, ('c:\\Users\\Admin\\Desktop\\Python\\').

sys.path.append('.') # ('.') will specify the root.


# You can make this more dynamic using the following code to go up one folder:

import sys

from os.path import dirname, abspath
d = dirname(dirname(abspath(__file__)))

sys.path.append(d)

```

- [Return to Table of Contents](/../../)
