# Module 4: Functions

Functions are pieces of code that have an input and an output. Today, we will be looking at the different types of functions in Dart!

## Types of Functions
1. void
2. String
3. int
4. float
5. and more!


The syntax of declaring a function is as follows...

`return-type functioname(arugments){return data}`



Lets take a look at some of this in action...


```void main(){
print("Hello world");}
```


As seen above, this is a main method which does not return anything, we know this from the word `void` in the function which means that it will not return anything.



Another example...

```String say_hi(String name){return "Hi $name";}```

The code above takes a parameter name, and returns a string that greets the name that was put in as a parameter. Notice that the return type and stated return type in the function definition is the same! This means that our code works and will compile correctly!


## What will not work...


Before, we took a look at what works when using function return types... now lets take a look at what will break our code!


int say_hi(int age){return "You are $age years old";}

This code will not work because the return type does not match what was stated in the function definition.



## Project Time!

Now, lets make a fun project to play heads or tails an insane amount of times!




Important notes:



var list = ['a','b','c','d','e'];

var randomItem = (list..shuffle()).first;