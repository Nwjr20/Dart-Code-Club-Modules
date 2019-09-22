**Module 3: Logic and Control Flow**

Last lesson, we mentioned boolean variables. Booleans (in Dart written as bool) are essentially a switch with two values, true and false.

```bool b = true;
bool a = false;```

We can use special operators to compare two values and receive a bool value in the form of true or false.

**1. Comparison logic (>, <, >=, <=, ==, !=)**

Logic is the comparison of two values to see how they relate (whether or not one is bigger, smaller, the same, etc).
Here's a list of the main comparison operators. You've seen many of these in math class before.

1. Greater than > (ex. A > B)
2. Less than < (ex. A < B)
3. Greater than or equal to >= (ex. A >= B)
4. Less than or equal to <= (ex. A <= B)
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
Repeat this for the other variable (let's name it `b`).

Our Editor should look like this: 

  ```void main(){
    int a = 5;
    int b = 10;
  }```

Now, try entering a print() function that tells you if a is greater than b.
Insert another line before the closing bracket (}) and write print();

Insert (a > b) in the print function. The console will calculate whatever is in the parenthesis first, so it will check to see if a is greater than b and print the result.

Now, the Editor should look like this: 

  ```void main(){
    int a = 5;
    int b = 10;
    print(a > b);
  }```

Run your program. What was the output?
If you wrote it out correctly, you should have gotten `false`. 5 is not greater than 10, so this makes sense.

Try it out with different values and with the 6 different operators listed above. 
Get a good feel for how these operators work, because we'll be using them a lot!

**2. Logic Operators (&&, ||, !)**

We've got the comparison operators down, which give us boolean expressions (true or false). But what if we want to see if two boolean expressions are both true? What if we want to see if either one of them is true?

There are operators that do just that, called logic operators. These are:
  1. && (represents "and"): Checks to see if both of two bools are true. If so, it returns true. Otherwise, it returns false.
  2. || (represents "or"): Checks to see if at least one of two bools is true. Just like &&, it returns true or false.
  3. ! (represents "not"): Used to invert a boolean value. Therefore, !true would give you false, and !false would give you true.
These operators will return a boolean. 

Based on these, what would `((a == b) && (a > c))` represent in English?

Answer: Is a equal to b and a greater than c?

Let's try it out.

In your Editor, add another variable that equals 10 (call it c). Let's use these operators!
Replace the old print statement with `print((a > b) && (b == c));`

The Editor should now read:

  ```void main(){
    int a = 5;
    int b = 10;
    int c = 10;
    print((a > b) && (b == c));
  }```
  
What do you think the result will be? (Remember that for && to return true, both values must be true.)
Run the program.
   
The console should say `false`. b is equal to c, but a is not greater than b. Only one of the inputs is true, so && will return false.
  
Try replacing && with ||. What should the result be?

Answer: The result should be true. || requires that at least 1 input is true, and that is the case, so || will return true.

Now, what is the result if you put `!` before the (b == c)?
Your Editor should read:

  ```void main(){
    int a = 5;
    int b = 10;
    int c = 10;
    print((a > b) || !(b == c));
  }```
  
Answer: False; The `!` operator inverts (b == c), which is usually true. Now, both are false, and || will return false.

Now that you've learned about booleans, here comes the fun part!

**3. Control Flow**

You may have been wondering why we would use booleans in the first place. The answer lies within the `if` statement.

The `if` statement uses a boolean to check whether or not it should perform an action.

Let's just try it out.

In the editor, insert a line that containing `if(true) {}`. This is the most basic `if` statement you can write. Your boolean conditional goes in the parenthesis (where it currently says true) and whatever code you want to be executed goes in the curly braces (currently nothing).
Insert a line that says `print("Hello");` inside the curly braces. The Editor window should now look like:

  ```void main(){
    int a = 5;
    int b = 10;
    int c = 10;
    print((a > b) || !(b == c));
    if(true) {
      print("Hello");
    }
  }```
  
  Note that you don't need a semicolon after the if statement because the curly braces do the semicolon's job. You do, however, need semicolons for any line inside the if statement. 
  
  Run the program. `Hello` will be printed, since the conditional is always true. 
  Try replacing the `true` with a conditional that will evaluate to a boolean, such as `b == c`. In this case, that if statement will read:
    ```if(b == c) {
      print("Hello");
    }
    ```
    If the condition is true, it will be run
