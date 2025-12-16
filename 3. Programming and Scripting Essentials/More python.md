Object Oriented Programming.
classes are great.

Encapsulation.
Modular.
Benefits of OOP
- Re-usability
- Organisation
- Enhanced data security

Easier to test and maintain. Build a well designed class or object that you can use again and again and again.
DRY Principle. Don't repeat yourself.

I'm very cross and moody today. I don't know why particularly, it's my last day I shoudl be thrilled.

What is OOP in Python?

It's an approach fo modelling concrete, real-world things, like cars, as well as relations between things, lime companies and employees, students and teachers, and so on.

What is a class?
It's a key term in OOP. It's a blueprint or a template of creating objects. Instances of objects can be made from a class. Define characteristics and behaviours of an object. Then you use the class to make an instance of the object.
Need to understand classes.
So for this example, our class is a Car.
So it has key attributes, colour, make, miles per gallon etc.
Behaviours are things it can do. So a car can brake, accelerate, start, change gear etc. Its an action or a function. Something you do with it.
So we define all the ays a car could be and that's the class. Then we make a specific object, and that's a specific instance of that class. So a specific car, I could use the car class to create Maximus. Bit like having a stored procedure, and hten a task being a particular instance of that stored procedure being called.
Maximus, our instance, will inherit all the behaviour etc from the car class, so he can drive, brake etc without needing to restate that.
Got an example here of class Employee. Defined within are the attributes and then the methods. So a method is showin with brackets.
So diagram is like
|class Employee|
|----------------|
|+Name|
|+NI Number|
|+Salary|
| |
|+PaySalary()|

From there can set up different employees, and set them up with the various attributes (Name, Ni Number, Salary etc). And then with the method, we would use the PaySalary method with each of the objects.
Idea is a method can manipulate or use the field data of the object. Stored procedure concept probably falls down a bit, as it's almost like a toolset of stored procedures, where you create something with top line parameters and then could use all different types of methods with those parameters to perform different things.

|Term|Definition|
|---|---|
|Classes| a blueprint or template that defines the structure and behaviour of objects|
|Objects| an instance of a class, representing individual entities with their own unique data and behaviour|
|Methods| a function that is associated with an object of a particular class|
|PRoperties| the data held by an object|

__init__ is a constructor. It's the first method that gets called. It's the first thing that is defined and sets up your instance. self creates an instance. Instance of whatever it is we're using, so we're using a class. Passing in an instance of self, passing in key attributes, then make, model, year, colour
```
class Car:
  def __int__(self, make, model, year, color):
    self.make = make
    self.model = model
    self.year = year
    self.colour = colour
    self.engine_status = False

  def start_engine(self):
    if not self.engine_status:
      print("Starting the engine...")
      self.engine_status = True
      print("Engine is now running.")
    else:
      print("Engine is already running.")
# Creating a car object
my_car = Car("Toyota","Corolla",2022,"Blue")

# Starting the engine of the car
my_car.start_engine()
```
So the self thing I think is becuase we are referencing the self, so when it's used, it'll make an instance, and that instance will reference itself.
Then we make my_car, which is an instance of the car class. That will then inherit the method that was defined in the class.

Notice at the top that the parameters in brackets are for all the values that don't have a default. engine_status is given a default of false, so it is optional in the top and does not need to be included in the brackets.
