# MITx-6.00.1x_PythonStudy

## Index
- [Types](#types)
- [Math](#math)
- [Operators (Boolean Expressions)](#operators)
- [Branching (if, elif, else)](#branching)
- [Loops](#loops)
  - [While](#while-loops)
  - [For](#for-loops)



### Types
So far we have four types
- Booleans
- Strings
- Integers
- Floats

**Booleans** have either a value of ```True``` or ```False```

**Strings** are any character on our keyboard held in between a set of quotes (single or double) 

Example: ```"String abc"``` 

**Integers** are numbers just as we learned in math class (-15, 0, 3, 2675, etc)

**Floats** are decimals that we learned in math (0.0, 5.876, -3300.182, etc)
<br /><br />
###Math
(In Progress)
- Truncation with integers
- Division with floats
- Addition of floats, integers, strings

### String Manipulation
(In Progress)
<br /><br />
[](TODO: Substring, index in string, string manipulation)
### Logical Operators (Boolean Logic) & Branching <br/>

####Operators<br />
Main Operators are "<", ">", ">=" "<=", "!=", "=="

These operators are used to do comparisons between a first and second value and they evaluate to True or False. 

- "**<**" - if first value is **less than** second value <br />
- "**>**" - if first value is **great than** second value <br />
- "**<=**" - if first value is **less than or equal to** second value <br />
- "**>=**" - if first value is **greater than or equal to** second value <br />
- "**!=**" - if values **are not equal**  <br />
- "**==**" - if values **are equal** <br />

<br /><br />
####Branching<br />
All early knowledge of branching truly just refers to "if" statements.

There are really only three things to know about if statements ("if", "elif", and "else").

Example **if** statement: 
```
if True:
  print("This line is executed")
```

The above code written out means that when the boolean expression for the **if statement equals true** then we execute the code inside the if statement's branch (in this case we print "This line is executed"). 

[](TODO: image to explain branching (flowchart))

```
if False:
  print("This line is executed")
```
And the above code means that we evaluate the if expression as false and we will never hit the ```print("This line is executed")```. 

Example **else** statement.
```
if True:
  print("Branch 1")
else:
  print("Branch 2")
```
Now we have started true branching, the statement may execute "Branch 1" or it may execute "Branch 2". Note that the else statement MUST come after the if statement and CANNOT exist without the beginning if statement. 

In this particular case the if always evaluates to True so the else will never be hit. Below is a little more complex of an example:

```
letter = "x"

if letter == "y":
  print("The letter is y")
else:
  print("Not the letter y")
  
```

The code knows that we have a letter and attempts to use boolean expression to check and see if the letter happens to be "y", if letter is "y" our code branches in and executes ```print("The letter is y")```; otherwise, it executes ```print("Not the letter y")```.

In our example, it ends up printing "Not the letter y" because letter is set to "x". 

**elif statements** <br />
Having both if and else is wonderful as long as we only need two branches, but life can be made a little easier sometimes with more possible statement the "elif" which is short for "else if".

Like an else statement elif executes when the previous if expression evaluated to false, but is changed because it has an expression that must be true as well. 

Example
```
if True:
  print("Branch 1")
elif True:
  print("Branch 2")
```

This code above only executes ```print("Branch 1")```. We do not execute the elif because the first expression evaluates to true. However, if the if had been false:

```
if False:
  print("Branch 1")
elif True:
  print("Branch 2")
```
We now execute ```print("Branch 2")```, but what if our elif had been false as well? 

```
if False:
  print("Branch 1")
elif False:
  print("Branch 2")
```

We execute neither print statement because they're both false. **We only execute a branch if we make it to their statement and its expression evaluates to true**. 

Currently we have had only two branches, but now that we have elif we can create more branches. 

Below example of three branches:
```
letter = "x"

if letter == "y":
  print("The letter is y")
elif letter == "a":
  print("The letter is a")
else 
  print("The letter is not a or y")
  
```
We have variable letter set to "x", we check it with our first if statement ```letter == "y"``` and it returns false. We check with our second elif statement ```letter == "a"``` and it returns false. Then finally we land in our catchall "else" which knows because of our previous boolean expressions that the letter is neither a or y so we execute ```print("The letter is not a or y")```.

<br /><br /><br /><br />

##Loops
TODO: while/for - numbers, strings/range - range, skipping, reversal 

###While Loops
Loops are an extension of our previous if statement. As in you branch into them when its statement is deemed True. The only difference is we continuously execute the code inside it until the expression becomes False. 

```
while True:
  print("This code executes infinitely")
```

The above while loops criteria is True so it will execute ``` print("This code executes infinitely") ``` forever as it will never evaluate to false. 

Example of our infinite loop:

```
This code executes infinitely
This code executes infinitely
This code executes infinitely
This code executes infinitely
This code executes infinitely
This code executes infinitely
This code executes infinitely
This code executes infinitely
This code executes infinitely
```

To exit we will use ```ctrl+c``` (hitting the ctrl and the c key at the same time). Ctrl+c is used to exit a program early.

Here's a more useful while loop where we traverse a string. 
```
alphabet = "abcdef"
index = 0
while index < len(alphabet):
    letter = alphabet[index]
    print(letter + " - " + index)
    index += 1
```

Prints:
```
a - 0
b - 1
c - 2
d - 3
e - 4
f - 5
```

We check our index to make sure it less than the length of alphabet. Index starts at 0 which means we enter the while loop and print our first letter. Then we increment and continue doing this until ``` index < len(alphabet ``` evaluates to False. Meaning that as long as index is less than 6 we continue looping. Once index becomes 6 we exit and continue on with our program. 

###For Loops
For loops are slightly more complex while loops. If they're more complex then why introduce them? Well they are slightly more complex, but they make the code extremely more clear. 

To get an understanding of for loops we need to be introduce other method ```range(..)```. Range in what we have currently learned is used mainly on integers. 

```range(5)``` is the same thing as saying ```[0, 1, 2, 3, 4]```

You can have a start and an end.. 
```range(begin:end)``` <br />
```range(3:7)```      ==>    ```[3, 4, 5, 6]```<br />

Then we have step which is the amount we will jump over to get the next integer
```range(4, 10, 2)``` ==>   ```[4, 6, 8]```

And lastly to have not forgotten reversal. <br />
```range(10, 0, -1)``` ==>  ```10, 9, 8, 7, 6, 5, 4, 3, 2, 1```

Note that just like string manipulation it truncates before it hits the end which was 7 and stops at 6. 
range



How this makes a difference. **While vs. For**

```
index = 0
while index < 5
  print(index)
  index += 1
```
**VS**
```
for index in range(5)
  print(index)
```

Either program results in the same output

```
0
1
2
3
4
```







