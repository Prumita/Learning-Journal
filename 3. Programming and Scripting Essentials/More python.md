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

Another example of class!
```
#Employee class encapsulates properties and methods
# of "employee" objects: could be used for a HR Application
class Employee:
  #__init__ constructor - a "dunder method"
  # which "initialises" an object when a new instance
  # of a class is created, by setting its properties
  def __init__(self, name, ni_number):
    self.name = name
    self.ni_number = ni_number
    self.salary = 0
    self.department = 0
```
a "dunder method" is a specific, special way to write it so Python knows it's a special python method. Initialises a new instance of an object.

So that's initially setting us up, so we're going to then create an instance. Which apparently can be called instanciating a particular object of the class.

So we've only got the constructor, the init, which we set up our properties in. And then we can seperately define methods:

```
  def set_salary(self, salary_amount):
    self.salary = salary_amount
  def set_department(self, department):
    self.department = department
```

Sorry lost the thread there a bit. But we can obviously make these things more complicated and we can put restrictions on it.
So we can use if, else if etc to check the minimum and only set it if it meets the criteria to stop naff stuff being passed in.

Static Class Members! So where are the min and max salaries going to come from?

```
So we can go:
class Employee:
  # static members - allows us to set min and max salaries
  min_salary = 12000
  max_salary = 110000
```

This is in the class, not the constructor, so it's in every single instance of that class. There is a hard coded value for everyone. The constructor is about how a particular instance is made and can't be overruled.

```
@staticmethod
def get_max_salary():
  return Employee.max_salary

print("Max salary is " + str(Employee.get_max_salary()))
Max salary 110000
```

The @staticmethod is called a decorator 

When should we use one? When the task doesn't rely on instance level data. So it comes from a static or class level. If the data is for everything to do with the class rather than an instance you use the static method and that gives you access to the static property.
