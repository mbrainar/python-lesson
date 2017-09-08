# Lesson 3

## Conditionals

Conditionals let us check the state of something (like a variable) and based on 
the result, perform an action. When checking a condition, there are several 
operators.

* `==` If the values of two operands are equal, then the condition becomes true.
* `!=` If values of two operands are not equal, then condition becomes true.
* `>` If the value of left operand is greater than the value of right operand, 
then condition becomes true.
* `<` If the value of left operand is less than the value of right operand, 
then condition becomes true.
* `>=` If the value of left operand is greater than or equal to the value of 
right operand, then condition becomes true.
* `<=` If the value of left operand is less than or equal to the value of right 
operand, then condition becomes true.

### If Statement

A basic conditional will use an `if` statement to see if the provided condition 
evaluates True or False. If the condition evaluates True, then the code block 
which follows the `if` statement will execute. Here indentation is important; 
the code that is intended to be executed following the `if` statement, must be 
indented. Also, the colon (:) following the `if` statement is required.

```
name = "Matthew"
if name == "Matthew":
    print "Hello",name

print "Finished"
```

### Else statement

But what happens if the condition evaluates False. In the example above, what if 
`name = "Drew"`. In that case, nothing would happen, it would move on to 
the next non-indented line in the code, and in this case print ONLY "Finished". 
We can build onto our conditional by adding an `else:` statement; when we do 
this, anything that is indented following the `else:` statement will be executed. 

```
name = "Drew"
if name == "Matthew":
    print "Hello",name
else:
    print "Hello",name
    print "You seem like a nice person"

print "Finished"
```

### Elif Statement

Sometimes a True and a False option is all we need, but sometimes we need more 
complicated conditionals. For example, what if we wanted to check that name is 
either "Matthew", "Drew", or "Craig", and based on the result perform a unique 
action. We can use the `elif` statement, which essentially says "else if" with 
another condition. 

```
name = "Craig"
if name == "Matthew":
    print "Hello",name
    print "I bet you drive a Sonata"
elif name == "Drew":
    print "Hello",name
    print "I bet you drive an Accord"
elif name == "Craig":
    print "Hello",name
    print "I bet you drive a Fusion"
else:
    print "Hello",name
    print "I don't know what car you drive."

print "Finished"
```

It is important to note that a conditional will execute top down--starting with 
the `if` statement, then sequentially any `elif` statements, and finally ending 
with the `else:` statement.

### Complex Conditionals 

### Negative Conditions

In some cases, you may want to see if your condition is false. You can write 
your `if` statement to evaluate true, then `pass` in the code block, then use 
the `else:` statmement to execute what you want to. The `pass` will simply tell 
the interpreter that it doesn't want to do anything; if it is omitted, the 
interpreter will realize that there should be something indented in the code 
block following the `if` statement.

```
today = "Thursday"
if today == "Sunday":
    pass
else:
    print "Get to work, this is not the sabbath"
```

As you can see above, that is 4 lines of code. The more efficient way is to 
negate the condition. Below we can do it in 2 lines. 

```
today = "Thursday"
if today != "Sunday":
    print "Get to work, this is not the sabbath"
```

#### In Operator

The in operator gives us an easy way to check if something is in something else. 
For example, I may want to know if a value appears in a list. Or I can use the 
`in` operator to see if a letter appears in a string.

```
lucky_things = ['underwear', 'rabbits foot', 11]
if "charm" in lucky_things:
    print "Is it made out of a marshmallow?"
```

We can also negate the `in` operator with the `not` operator.

```
alphabet = "abcdefghijklmnoqrstuvwxyz"
if "p" not in alphabet:
    print "Where's the P? Running down your leg?"
else:
    print "You really know your ABCs"
```

## Loops

Loops allow you to perform the same action multiple times without writing the 
same lines of code over and over again.

### For Loop



### While Loop

A while loop will continue to run as long as the given condition is true. Be 
careful with while loops as they are easy to get into an infinite loop by 
creating a condition that never evaluates negative.


[<< Beginning](/README.md) | [< Lesson 2](/lesson2/README.md) | 
[Lesson 4 >](/lesson4/README.md)