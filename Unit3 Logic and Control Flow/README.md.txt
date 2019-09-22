Module 3: Logic and Control Flow

Last lesson, we mentioned boolean variables. Booleans (in Dart written as bool) are essentially a switch with two values, true and false.
We can use special operators to compare two values and receive a bool value in the form of true or false.

1. Comparison logic

Logic is the comparison of two values to see how they relate (whether or not one is bigger, smaller, the same, etc).
Here's a list of the main comparison operators. You've seen many of these in math class before.

1. Greater than > (ex. A > B)
2. Less than < (ex. A < B)
3. Greater than or equal to >= (ex. A >= B)
4. Less than or equal to >= (ex. A <= B)
5. Equal to == (ex. A == B)
6. Not equal to != (ex. A != B)

A few things to remember about logic operators.
  - For any operator with equal to as part of it, the equals sign comes SECOND.
  - == is not the same as =. The double equals is for comparison and the single equals sets the variable. Two very different things!
  - Any logic operator will give you a boolean value as a result (ex. (10 > 5) would give you true).
  - You can only compare two values at a time. For example, (A > B > C) would give you an error. 
    A > B resolves to a true/false, and you can't compare a word to a number.)

Open up DartPad (https://dartpad.dartlang.org/) and let's try some comparison operators.

In the main() function, define 2 variables, making one equal to 5 and the other 10. We can make our first value by entering `int a = 5;`
Repeat this for the other variable (the name doesn't matter).

Our Editor should look like this: 
  void main(){
    int a = 5;
    int b = 10;
  }

Now, try entering a print() function that tells you if a is greater than b.
Insert another line before the closing bracket (}) and write print();

Insert (a > b) in the print function. The console will calculate whatever is in the parenthesis first, so it will check to see if a is greater than b and print the result.

Now, the Editor should look like this: 
  void main(){
    int a = 5;
    int b = 10;
    print(a > b);
  }

Run your program. What was the output?
If you wrote it out correctly, you should have gotten `false`. 5 is not greater than 10, so this makes sense.

Try it out with different values and with the 6 different operators listed above. 
Get a good feel for how these operators work, because we'll be using them a lot!

