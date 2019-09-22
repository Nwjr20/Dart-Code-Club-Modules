Module 3: Logic and Control Flow

Last lesson, we mentioned boolean variables. Booleans (in Dart written as bool) are essentially a switch with two values, true and false.
We can use special operators to compare two values and receive a bool value in the form of true or false.

1. Logic

Logic is the comparison of two values to see how they relate (whether or not one is bigger, smaller, the same, etc.)
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

In the main() function, define 2 variables, making one equal to 5 and the other 10. We can make our first value by entering int a = 5; 
Repeat this for 2
