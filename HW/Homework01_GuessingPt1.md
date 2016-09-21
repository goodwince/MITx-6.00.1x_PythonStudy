###The Guessing game Part 1! 

Create a program that has a variable answer and allows user to input a number. If the user inputs the correct number it returns "Correct". If the user guesses incorrectly it prints "Incorrect". Remember that input returns a string and we want our answer to be an integer.

Code start: 
```
answer = 6
```

Console Window: 

``` 
Enter a number: 
```

Say you type ```5```. The program prints "Incorrect the number is 6". 
Say you type ```6```. The program prints "Correct the number is 6".



<b>Hint</b>: I added Input to the examples of how to use in our summary "ReadMe" file. 

###Part 1.2
What fun is a guessing game if you know the number? Now that you've managed to do the above.  For the next portion you are going to do something new. Generating a random number. 

At the top of your code on its own line add. ```import random``` and in place of the "6" write ```random.randint(1,10)```. 

```random.randint(start, end)``` means generate a random number from start to end. In our case that means a number from 1 to 10. Now run your code!






