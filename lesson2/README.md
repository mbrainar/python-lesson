# Lesson 2

## Variables

Variables are reserved memory locations for storing values. Memory is reserved, 
when the value is assigned to the variable. The memory allocated varies based 
on a the data type.

### Assignment operator

To assign a value to a variable, simply define the name of the variable, use 
the `=` operator to assign the value. A basic example could look like:

```
name = "Matthew"
lucky_number = 11
```

Variables can be created from other variables; for example 

```
matthew_anniversary = "December 15, 2007"
drew_anniversary = matthew_anniversary
```

To simplify the example above, you can also assign variables together; for 
example:

```
drew_anniversary = matthew_anniversary = "December 15, 2007"
```

Since you can assign the value of one variable to another variable, you can also 
manipulate the data before assigning it to the new variable. 

```
whole = 100
half = whole / 2
```

### Data Types

Data types determine whether an object can do something, or whether it just 
would not make sense. For example, you can add 1 + 2; but you cannot add 1 + 
the letter "a". 

There are 6 standard data types:

1. Boolean

    Boolean data has 2 options, it can only be `True` or `False`.

2. Numbers

    Numbers can be one of two types:
    
    * Integer = a whole number
    
        An integer will always be a whole number. We know that dividing 5 by 2 
        results in 2.5; however, python will not convert the result to a float, 
        so it will round to the nearest whole number/integer. In a python 
        interpreter, execute `print 5 / 2`; you will see that it yields "2"
        
    * Float = a number with a decimal point
    
        A float is an number that is capable of containing decimal places. There 
        are no limits to how many decimal places that it can hold. If you want 
        to assign a variable a float value, simply add the decimal, if you want 
        a whole number with the ability to contain decimals, trail the number 
        with ".0". In a python interpreter, execute `print 5.0 / 2` and you will 
        see that it yields "2.5"
    
    Numbers can be manipulated with any mathematical operation. Use `+` to add, 
    `-` to subtract, `*` to multiply, and `/` to divide. Less common operators 
    include the modulus `%` which will divide and return the remainder, and the 
    exponent `**` which will raise the number before the `**` to the power of 
    the number following the `**`.
    
    Integers can be converted to float by using the `float()` function; and 
    vice versa with the `int()` function.

3. Strings

    Strings are text-based alphanumerics. To create a string variable, simply 
    put the value in quotes. Python will accept single quotes or double quotes; 
    just make sure that they are the same on both sides of the value. 
    
    ```
    name = "Matthew"
    car = 'Sonata'
    ```
    
    Strings can contain numerics in text form as well. We can simply put quotes 
    around a number. When we do this, it is no longer a number, so we cannot 
    add a string and an integer. 
    
    ```
    a = 10
    b = "10"
    print a + b
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    TypeError: unsupported operand type(s) for +: 'int' and 'str'
    ``` 
    
    We do have the ability to convert an integer or float to a string using the 
    `str()` function. 
    
    Strings can be combined together through concatenation. For example, using 
    the strings above, we could create a sentance:
    
    ```
    print name + " drives a " + car
    Matthew drives a Sonata
    ```
    
    We could achieve the same results using comma concatenation (note, this only 
    works in print statements, not variable assignment operations): 
    `print name,"drives a",car`
    
    
4. List

    A list is a sequence of items. To create a list, we use a comma 
    separated list enclosed within square brackets, for example: 
    `the_a_list = ['Matthew', 'Drew', 'Craig']`. A list is a mutable 
    object; meaning that we can manipulate the list in place by adding, 
    removing, or changing items.
    
    Lists do not need to be homogeneous data types; this is an important 
    concept later. It is acceptable to mix data types in a list, for example: 
    `lucky_things = ['underwear', 'rabbits foot', 11]`
    
    To access an item in a list, you specify its location in square brackets. 
    It is important to remember that when counting items in a list, the first 
    item is in location 0. If we wanted to get the 2nd item in our list above 
    we would `print lucky_things[1]`.
    
5. Tuple

    A tuple is like a list, with the following differences:
        
        * It is immutable; it cannot be manipulated after its creation-- 
        think of it as read-only.
        * It is enclosed in parenthesis, for example: 
        `the_d_list = ('Kathy Griffin')`
    
    
6. Dictionary

    A dictionary is a key:value mapping. To create a dictionary, we create 
    a "key" to identify the location, and a "value" that we want to store, and 
    enclose them in curly brackets; for example:
    `me = {'name':'Matthew','height':6.0,'weight':195.0,'eye_color':'hazel'}`
    
    To access a value in a dictionary, we specify the key that we are looking 
    for in square brackets. If we wanted to get my eye color, we would 
    `print me['eye_color']`

**trust, but verify**

First, let's verify these data types. Run open the "data-types.py" file and add 
some values that you think are appropriate and save. Then run they file with
`python lesson2/data-types.py` and see if you are right. Your output should look 
like:

```
mbrainar:~/workspace (master) $ python lesson2/data-types.py 
<type 'bool'>
<type 'int'>
<type 'float'>
<type 'str'>
<type 'list'>
<type 'dict'>
```


### Nested Data Types

Remember when I said that mixing data types was going to be important later. 
Well here it is. Because we can mix data types, we can now nest lists inside of 
dictionaries, or dictionaries inside of lists. Here is an example of the former 
(a list within a dictionary):

```
me = {
    'name':'Matthew',
    'height':6.0,
    'weight':195.0,
    'eye_color':'hazel',
    'lucky_things' = ['underwear', 'rabbits foot', 11]
    }
```

Here is an example of the latter (a list of dictionaries):

```
us = [
    {'name':'Matthew','eye_color':'hazel'},
    {'name':'Drew','eye_color':'brown'},
    {'name':'Craig','eye_color':'unknown'}
]
```

[<< Beginning](/README.md) | [< Lesson 1](/lesson1/README.md) | 
[Lesson 3 >](/lesson3/README.md)