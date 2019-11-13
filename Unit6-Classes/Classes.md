# Classes  
## What are Classes and Objects?

**Classes** - A structure to hold a specific type of data, can be as simple or as complex as needed  
**Objects** - Implementations/Instances of a class - the actual data in the computer's memory  
Classes can be thought of as blueprints, and Objects as the buildings that they describe how to make (Cardboard box analogy)  
Dart is an object-oriented language, meaning almost everything in the language is an object derived from a class  

- int is a very simple object that just holds a number value
- String is a more complex object that holds a list of characters

## How to Make a Class  
```dart
class Car{
  String _make;
  String _model;
  int _year;
  
  Car(this._make, this._model, this._year);
  
  String getMake(){
    return _make;
  }
  String getModel(){
    return _model;
  }
  int getYear(){
    return _year;
  }
  
  void setMake(String make){
    _make = make;
  }
  void setModel(String model){
    _model = model;
  }
  void setYear(int year){
    _year = year;
  }
  
  void drive(){
    print("Vroom");
  }
}

void main() {
  Car myCar = new Car("Honda", "Accord", 2007);
  print(car.getYear());
  car.setYear(2019);
  print(car.getYear());
  car.drive();
}
```
There is a lot going on here, so we'll break it down piece by piece:  
  - The first line `Class Car {` is a class definition, which just states the name of the class being created
  - The 3 variables at the top are *attributes* of the class - variables that store data that we *know* about the object. These variable names start with an _ character, meaning they are private and only accessible from within the class.
  - The line `Car(this._make, this._model, this._year);` is a *constructor* - this is a method that is called when an object is created, and allows the object to be created with specific values placed into its attributes.
  - The next 6 methods are *getters* and *setters* - these allow access to and mutation of the data inside the class's private attributes (encapsulation)
  - The last method, `void drive()` is just a method that is a member of the class. These methods are usually something that the objects of the class do, in this simple case calling `drive()` on an object of type `Car` prints the word "Vroom"
  - The line in the `main()` method `Car myCar = new Car("Honda", "Accord", 2007);` creates an *Object* of type Car. This object is created like any other variable, with a type, name, and value.
  - The methods defined in the Car class can then be called on the object to access and change the data, or just print something to the screen.
  
  
## Activities

Pick something in the room and make a class describing it, then create a few objects of that type in the `main()` method  
Include private attributes, a constructor, getters/setters, and other methods




