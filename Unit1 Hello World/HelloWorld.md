# Module 1 - Hello, World!

**1. Navigate to https://dartpad.dartlang.org/**
  Familiarize yourself with this screen. The left side of the site is the code Editor, and the right side is the Console output. 
  When you hit the `Run` button, the code in the Editor will execute and its output will be displayed to the Console.
  
 **2. Clearing the `main()` function**
   Clear all the code from the word 'for' to the first closed curly bracket '}'. 
   The remaining code should look like this:
    ```void main() {
    
    } ```
    
    The block of code surrounded by `void main() { }` is known as the `main()` function. 
    Don't worry about the definition of function just yet - you will learn about it later.
    
    The `main()` function is the start point for all Dart projects. When you hit the `Run` button, the code inside 
    the curly brackets after 'main()' is run first, even if there is code written above the function.
    
    If you hit `Run` now, the display in the Console should be blank.
    
 **3. Hello, World! **
   Inside the curly brackets of the `main()` function, place the following line of code:
   `print("Hello, World!");`
   The entire Editor should now look like this:
   ```
   void main() {
    print("Hello, World!");
   }```
   
   `print()` is another function that displays a String to the Console.
   A String is a sequence of typed characters - letters, numbers, etc. (Anything on the keyboard is a character) that is enclosed by
   single or double quotation marks.
   
   At the end of the line, you placed a semicolon - `;`. 
   This tells the computer that the current line of code is over, and to move on to the next line for execution of the program.
   
   If you hit `Run`, the String `"Hello World"` will display in the Console.
   
   Try displaying other messages to the Console - Test out the limitations of what you can place inside `print()`
