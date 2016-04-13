#Python - Importing Libraries and Modules

##Objectives

* Understand how to look for, import and use Python libraries

##Importing a Module

As Python code gets larger and mode complex, developers may choose to group related code into individual files, called **modules**. Just like any script, a module can define functions, classes and variables.

Using modules makes code easier to work with because it adds an extra layer of organization.

To import a module, just use the `import` keyword followed by the name of the file you'd like to load. There is no need to use the `.py` extension.

```python
import musician
from musician import *
```
The first line imports the musician.py file itself. The second line imports all the classes and functions contained in that musician.py file. However, if you are only going to use a few attributes (functions, variables, classes) from a module, you should specify which ones to import.

```python
import musician
from musician import songs, play_music
```

##Importing a Library

Once a module is available for public use, it is then generally referred to as a library. Libraries are Python scripts written to accomplish common tasks, and are widely shared by developers.

Using libraries requires three steps:
1. Install pip, which is a tool that helps get and manage Python packages. You will only need to do this once. To install pip on a Mac, you can use easy_install in the command line
```python
>>>sudo easy_install pip
```

2. Install the library in your environment using the `pip` command. You will need to install any new libraries you want to use. If you don't have a library installed, when you try to use it, you'll get an NameError message: `NameError: name 'library_name' is not defined`. This message generally just means that you need to install that package locally.
```python
>>pip install library_name
```
3. Import the library at the top of your Python script.
```python
import library_name
```

An example of a basic Python library is- **random.py**. Since many developers would want a way to generate random numbers, someone created and published code with a variety of methods that accomplishes this goal. You can find documentation on this library <a href="https://docs.python.org/2/library/random.html">here</a> to learn about all the different functions you can call from it.

To use any of the methods in `random.py`, just import the `random` library, and then call the method by using dot notation:

```python
import random
print random.randint(1,3)
```

There are a lot of libraries to explore, including [this list](http://pythontips.com/2013/07/30/20-python-libraries-you-cant-live-without/) of 20 common ones including Pyglet, a library for 3D animation and NumPy which allows for complext mathematical operations. Before writing methods or functions to do something routine, check to see if a library exists - it will make your life a lot easier.

##Conclusion
Modules allow Python developers to keep code in distinct files, seperated by functionality. When those modules are shared with others, they are called libraries. This code is easy to import and easy to use in your own scripts.
