# Module 3: Logic and Control Flow

Last lesson, we mentioned boolean variables. Booleans (in Dart written as bool) are essentially a switch with two values, true and false.

```dart
bool b = true;
bool a = false;
```

We can use special operators to compare two values and receive a bool value in the form of true or false.

**1. Comparison logic (>, <, >=, <=, ==, !=)**

Logic is the comparison of two values to see how they relate (whether or not one is bigger, smaller, the same, etc).
Here's a list of the main comparison operators. You've seen many of these in math class before.

1. `>` - Greater than (ex. `A > B`)
2. `<` - Less than (ex. `A < B`)
3. `>=` - Greater than or equal to (ex. `A >= B`)
4. `<=` - Less than or equal to (ex. `A <= B`)
5. `==` - Equal to (ex. `A == B`)
6. `!=` - Not equal to (ex. `A != B`)

A few things to remember about logic operators.
  - For any operator with equal to as part of it, the equals sign comes SECOND.
  - == is not the same as =. The double equals is for comparison and the single equals sets the variable. Two very different things!
  - Any logic operator will give you a boolean value as a result (ex. (`10 > 5`) would give you `true`).
  - You can only compare two values at a time. For example, (`A > B > C`) would give you an error. 
    `A > B` resolves to a true/false, and you can't compare a word to a number.)

Open up DartPad (https://dartpad.dartlang.org/) and let's try some comparison operators.

In the `main()` function, define 2 variables, making one equal to 5 and the other 10. We can make our first value by entering `int a = 5;`
Repeat this for the other variable (let's name it `b`).

Our Editor should look like this: 

  ```dart
  void main(){
    int a = 5;
    int b = 10;
  }
  ```

Now, try entering a `print()` function that tells you if a is greater than b.
Insert another line before the closing curly brace (`}`) and write `print();`

Insert `(a > b)` in the print function. The console will calculate whatever is in the parenthesis first, so it will check to see if a is greater than b and print the result.

Now, the Editor should look like this: 

  ```dart
  void main(){
    int a = 5;
    int b = 10;
    print(a > b);
  }
  ```

Run your program. What was the output?
If you wrote it out correctly, you should have gotten `false`. 5 is not greater than 10, so this makes sense.

Try it out with different values and with the 6 different operators listed above. 
Get a good feel for how these operators work, because we'll be using them a lot!

**2. Logic Operators (&&, ||, !)**

We've got the comparison operators down, which give us boolean expressions (true or false). But what if we want to see if two boolean expressions are both true? What if we want to see if either one of them is true?

There are operators that do just that, called logic operators. These are:
  1. `&&` (represents "and"): Checks to see if both of two bools are true. If so, it returns `true`. Otherwise, it returns `false`.
  2. `||` (represents "or"): Checks to see if at least one of two bools is true. Just like `&&`, it returns true or `false`.
  3. `!` (represents "not"): Used to invert a boolean value. Therefore, `!true` would give you `false`, and `!false` would give you `true`.
These operators will return a boolean. 

Based on these, what would `((a == b) && (a > c))` represent in English?

<details>
  <summary>Answer:</summary>
  <p>
    <code>((a == b) && (a > c))</code> would be equivilent to asking "Is a equal to b and a greater than c?".
  </p>
</details>

Let's try it out.

In your Editor, add another variable that equals 10 (call it c). Let's use these operators!
Replace the old print statement with `print((a > b) && (b == c));`

The Editor should now read:

  ```dart
  void main(){
    int a = 5;
    int b = 10;
    int c = 10;
    print((a > b) && (b == c));
  }
  ```
  
What do you think the result will be? (Remember that for `&&` to return true, both values must be true.)
Run the program.
   
The console should say `false`. b is equal to c, but a is not greater than b. Only one of the inputs is true, so `&&` will return false.
  
Try replacing `&&` with `||`. What should the result be?

<details>
  <summary>Answer: </summary> 
  <p> 
    The result should be true. <code>||</code> requires that at least 1 input is true. That is the case, so <code>||</code> will return <code>true</code>.
  </p>
</details>

Now, what is the result if you put `!` before the `(b == c)`?
Your Editor should read:

  ```dart
  void main(){
    int a = 5;
    int b = 10;
    int c = 10;
    print((a > b) || !(b == c));
  }
  ```
  
<details>
  <summary>Answer:</summary>
  <p>
    False; The <code>!</code> operator inverts <code>(b == c)</code>, which is usually <code>true</code>. Now, both are <code>false</code>, and <code>||</code> will return <code>false</code>.
  <p>
</details>

Now that you've learned about booleans, here comes the fun part!

**3. Control Flow**

You may have been wondering why we would use booleans in the first place. The answer lies within the `if` statement.

**if**

The `if` statement uses a boolean to check whether or not it should perform an action.

Let's just try it out.

In the editor, insert a line that containing `if(true) {}`. This is the most basic `if` statement you can write. Your boolean conditional goes in the parenthesis (where it currently says true) and whatever code you want to be executed goes in the curly braces (currently nothing).
Insert a line that says `print("Hello");` inside the curly braces. The Editor window should now look like:

  ```dart
  void main(){
    int a = 5;
    int b = 10;
    int c = 10;
    print((a > b) || !(b == c));
    if(true) {
      print("Hello");
    }
  }
  ```
  
  Note that you don't need a semicolon after the if statement because the curly braces do the semicolon's job. You do, however, need semicolons for any line inside the if statement. 
  
  Run the program. `Hello` will be printed, since the conditional is always true. 
  Try replacing the `true` with a conditional that will evaluate to a boolean, such as `b == c`. In this case, that if statement will read:
    ```dart
    if(b == c) {
      print("Hello");
    }
    ```
    If the condition is true, `Hello` will be printed. If the condition is false, nothing will be printed because the instructions inside the curly braces are skipped over.
    
You can even put a compound conditional (such as `(a > b) || !(b == c)`) in the if statement! As long as it evaluates to a boolean, you can use it in an `if` statement.
    
**else**

What if you want to run something if the condition is not true? We can use what's called an `else` statement. This goes after the second curly brace of an `if` statement. It looks something like this:

```dart
  if(b == c){
    print("Hello");
  }
  else {
    print("Goodbye");
  }
  ```
    
Note that an else statement does not use a condition. It always runs if the `if` statement condition is false.
Test it out and see what you can do with it.

**else if**

What if you want to run another if statement after the first one was not met? You'd use `else if`. It goes where you'd put an `else` statement, but you have to give it a condition.
For example:
```dart
  if(b == c){
    print("Hello");
  }
  else if(a > b){
    print("Oh no!");
  }
  ```
  
After the `else if`, you can chain on more `else if` and `else` statements to check multiple conditions, and only one of them will be run!
```dart
  if(b == c){
    print("Hello");
  }
  else if(a > b){
    print("Oh no!");
  }
  else{
    print("Goodbye")
  }
  ```
Experiment with the control flow of `if`, `else`, and `else if` statements to see what complex decisions you can translate into code!


