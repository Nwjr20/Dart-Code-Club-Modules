#Classes  
##What are Classes and Objects?

**Classes** - A structure to hold a specific type of data, can be as simple or as complex as needed  
**Objects** - Implementations/Instances of a class - the actual data in the computer's memory  
Classes can be thought of as blueprints, and Objects as the buildings that they describe how to make  
Dart is an object-oriented language, meaning almost everything in the language is an object derived from a class  

- int is a very simple object that just holds a number value
- String is a more complex object that holds a list of characters

##How to Make a Class  
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
  Car car = new Car("Honda", "Accord", 2007);
  print(car.getYear());
  car.setYear(2019);
  print(car.getYear());
  car.drive();
}
```
There is a lot going on here, so we'll break it down  



Inheritance - subclasses, superclasses, overriding  
