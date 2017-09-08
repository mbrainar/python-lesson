# Lesson 1

## About Python

### History

Created by Guido van Rossum and first released in 1991. Python has a design
philosophy that emphasizes code **readability** and a syntax that allows 
programmers to express concepts in **fewer lines of code**. Python is an 
**interpreted** language; which means that there is an interpreter that will 
execute instructions directly, without previously compiling a program into 
machine-language instructions.

### Philosophy

The core philosophy of the language is summarized by the document The Zen of Python

```
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

If you ever want to access this list, simply run `python -m this`

### Python versions

**Python2** released in 2000 is the most widely used interpreter. The release of 
**Python3** in 2008 has triggered the end of life of Python2. However, due to the 
wide adoption of Python2, it will not reach end of life until 2020.

To check which interpreter you are using, you can issue the command 
`python -V` in the bash terminal. Your ouput will look something like:

```
mbrainar:~/workspace $ python -V
Python 2.7.6
```

Most content in this lesson is written for 2.7, and due to syntax changes, 
will not work properly in Python3.

### Python interpreter

There are multiple ways to interact with Python. The first is the interpreter. 
To enter the interpreter, simply type `python` in the bash terminal. You will 
see a prompt that looks like:

```
mbrainar:~/workspace $ python
Python 2.7.6 (default, Oct 26 2016, 20:30:19) 
[GCC 4.8.4] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```

From here, you can start sending python commands. For example if we want to 
print out a statement like "Hello World", we use the `print` command.

```
>>> print "Hello World"
Hello World
>>> 
```

This is sometimes a useful way to check a command or execute a quick, one-time
function, but it is not typically used to interact with Python. So to exit the 
interpreter, type `quit()` and hit enter and you will be returned to the bash 
terminal.

```
>>> quit()
mbrainar:~/workspace $ 
```

### Python scripts

A better way of interacting with Python is to put your commands into a script 
and execute said script. To execute a script, simply use the command 
`python script.py` --where script.py is the script that you wish to run.

In the lesson1 directory, we have a script called hello-world.py. To run this 
script, we use the command `python lesson1/hello-world.py`. We should see 
something like the following:

```
mbrainar:~/workspace $ python lesson1/hello-world.py 
Hello World
```

Lets say we want to make a change to the script where, we are saying hello to 
a specific person, yourself. We can edit the hello-world.py file. In Cloud9, 
simply double click on the hello-world.py file in the directory structure on 
the left side of the screen. 
<!--![lesson1-directory.png](/lesson1/lesson1-directory.png)-->
We can change the print statement to read `print "Hello Matthew"`. When we rerun 
the script, we get a new result:

```
mbrainar:~/workspace $ python lesson1/hello-world.py 
Hello Matthew
```

## Python Syntax

### Indentation

Python was designed to be easily human readable. One of the ways in which this 
is accomplished is through the use of indentation. When writing Python code 
there are sections where some code is meant to be executed as a block; Python 
relies on indentation instead of explicit delimiters, for example `{ }`. 
Python doesn't care what your indentation is 
[tabs or spaces](https://www.youtube.com/watch?v=SsoOG6ZeyUI) but it has to be 
consistent throughout the code. If your indentation doesn't match, you will see 
an error that looks like 
`IndentationError: unindent does not match any outer indentation level`
Here is a sample code block using indentation:

```
if name == "Matthew":
    print "Hello", name
```

### Reserved Words

Python has reserved words; words that cannot be used as variable, object, 
or function names.

![python-reserved-words.png](/lesson1/python-reserved-words.png)

### Import Modules

Python allows you to import pieces of python code, either from another file 
that you created, or packages that someone else has written. A python module 
is simply a .py file containing python code. To import a python module that 
you wrote (this is commonly done in order to simplify .py files so they don't 
get too long), simply use `import my_module`--where the my_module.py file is 
located in the same directory as your code.

Alternatively, you can import python packages written by someone else. This is 
done similarly within your code, i.e. `import datetime`. In this case datetime 
is a built-in python module, so there are no missing dependencies. In many cases 
importing a python module will require that you install that module using pip, 
for example `pip install piglatin`. It is recommended to do this in a virtual 
environment--which is outside the scope of this lesson.


[<< Beginning](/README.md) | [Lesson 2 >](/lesson2/README.md)