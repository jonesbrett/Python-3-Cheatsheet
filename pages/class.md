

## Object-Oriented Programming

A class instance is also called an object. The pattern of defining classes and creating objects to represent 
the responsibilities of a program is known as Object Oriented Programming or OOP.

Instantiation takes a class and turns it into an object, the type() function does the opposite of that. When 
called with an object, it returns the class that the object is an instance of.

```python
class CoolClass:
  pass
 
cool_instance = CoolClass()
print(type(cool_instance))
# prints "<class '__main__.CoolClass'>"
```

We then print out the type() of cool_instance and it shows us that this object is of type __main__.CoolClass.

In Python __main__ means “this current file that we’re running” and so one could read the output from type() 
to mean “the class CoolClass that was defined here, in the script you’re currently running.”

## Class Variables

When we want the same data to be available to every instance of a class we use a class variable. A class variable is a variable that’s the same for every instance of the class.

You can define a class variable by including it in the indented part of your class definition, and you can access all of an object’s class variables with object.variable syntax.

```python
class Musician:
  title = "Rockstar"
 
drummer = Musician()
print(drummer.title)
# prints "Rockstar"
```

Above we defined the class Musician, then instantiated drummer to be an object of type Musician. We then printed out the drummer’s .title attribute, which is a class variable that we defined as the string “Rockstar”.

If we defined another musician, like guitarist = Musician() they would have the same .title attribute.

## Methods

Methods are functions that are defined as part of a class. The first argument in a method is always the object that is calling the method. Convention recommends that we name this first argument self. Methods always have at least this one argument.

We define methods similarly to functions, except that they are indented to be part of the class.

class Dog:
  dog_time_dilation = 7
 
  def time_explanation(self):
    print("Dogs experience {} years for every 1 human year.".format(self.dog_time_dilation))
 
pipi_pitbull = Dog()
pipi_pitbull.time_explanation()
# Prints "Dogs experience 7 years for every 1 human year."

Above we created a Dog class with a time_explanation method that takes one argument, self, which refers to the object calling the function. We created a Dog named pipi_pitbull and called the .time_explanation() method on our new object for Pipi.

Notice we didn’t pass any arguments when we called .time_explanation(), but were able to refer to self in the function body. When you call a method it automatically passes the object calling the method as the first argument.

## Methods with Arguments

Methods can also take more arguments than just self:

class DistanceConverter:
  kms_in_a_mile = 1.609
  def how_many_kms(self, miles):
    return miles * self.kms_in_a_mile
 
converter = DistanceConverter()
kms_in_5_miles = converter.how_many_kms(5)
print(kms_in_5_miles)
# prints "8.045"

Above we defined a DistanceConverter class, instantiated it, and used it to convert 5 miles into kilometers. Notice again that even though how_many_kms takes two arguments in its definition, we only pass miles, because self is implicitly passed (and refers to the object converter).


Constructors

There are several methods that we can define in a Python class that have special behavior. These methods are sometimes called “magic,” because they behave differently from regular methods. Another popular term is dunder methods, so-named because they have two underscores (double-underscore abbreviated to “dunder”) on either side of them.

The first dunder method we’re going to use is the __init__() method (note the two underscores before and after the word “init”). This method is used to initialize a newly created object. It is called every time the class is instantiated.

Methods that are used to prepare an object being instantiated are called constructors. The word “constructor” is used to describe similar features in other object-oriented programming languages but programmers who refer to a constructor in Python are usually talking about the __init__() method.

class Shouter:
  def __init__(self):
    print("HELLO?!")
 
shout1 = Shouter()
# prints "HELLO?!"
 
shout2 = Shouter()
# prints "HELLO?!"

Above we created a class called Shouter and every time we create an instance of Shouter the program prints out a shout. Don’t worry, this doesn’t hurt the computer at all.

Pay careful attention to the instantiation syntax we use. Shouter() looks a lot like a function call, doesn’t it? If it’s a function, can we pass parameters to it? We absolutely can, and those parameters will be received by the __init__() method.

class Shouter:
  def __init__(self, phrase):
    # make sure phrase is a string
    if type(phrase) == str:
 
      # then shout it out
      print(phrase.upper())
 
shout1 = Shouter("shout")
# prints "SHOUT"
 
shout2 = Shouter("shout")
# prints "SHOUT"
 
shout3 = Shouter("let it all out")
# prints "LET IT ALL OUT"

Above we’ve updated our Shouter class to take the additional parameter phrase. When we created each of our objects we passed an argument to the constructor. The constructor takes the argument phrase and, if it’s a string, prints out the all-caps version of phrase.


class Circle:
  pi = 3.14
  
  def __init__(self, dimeter):
    print("New circle with diameter: {}".format(dimeter))

teaching_table = Circle(36)



Attribute Functions

Instance variables and class variables are both accessed similarly in Python. This is no mistake, they are both considered attributes of an object. If we attempt to access an attribute that is neither a class variable nor an instance variable of the object Python will throw an AttributeError.

class NoCustomAttributes:
  pass
 
attributeless = NoCustomAttributes()
 
try:
  attributeless.fake_attribute
except AttributeError:
  print("This text gets printed!")
 
# prints "This text gets printed!"

What if we aren’t sure if an object has an attribute or not? hasattr() will return True if an object has a given attribute and False otherwise. If we want to get the actual value of the attribute, getattr() is a Python function that will return the value of a given object and attribute. In this function, we can also supply a third argument that will be the default if the object does not have the given attribute.

The syntax and parameters for these functions look like this:

hasattr(object, “attribute”) has two parameters:

    object : the object we are testing to see if it has a certain attribute
    attribute : name of attribute we want to see if it exists

getattr(object, “attribute”, default) has three parameters (one of which is optional):

    object : the object whose attribute we want to evaluate
    attribute : name of attribute we want to evaluate
    default : the value that is returned if the attribute does not exist (note: this parameter is optional)

Calling those functions looks like this:

hasattr(attributeless, "fake_attribute")
# returns False
 
getattr(attributeless, "other_fake_attribute", 800)
# returns 800, the default value

Above we checked if the attributeless object has the attribute fake_attribute. Since it does not, hasattr() returned False. After that, we used getattr to attempt to retrieve other_fake_attribute. Since other_fake_attribute isn’t a real attribute on attributeless, our call to getattr() returned the supplied default value 800, instead of throwing an AttributeError.

Self

Since we can already use dictionaries to store key-value pairs, using objects for that purpose is not really useful. Instance variables are more powerful when you can guarantee a rigidity to the data the object is holding.

This convenience is most apparent when the constructor creates the instance variables, using the arguments passed in to it. If we were creating a search engine, and we wanted to create classes for each separate entry we could return. We’d do that like this:

class SearchEngineEntry:
  def __init__(self, url):
    self.url = url
 
codecademy = SearchEngineEntry("www.codecademy.com")
wikipedia = SearchEngineEntry("www.wikipedia.org")
 
print(codecademy.url)
# prints "www.codecademy.com"
 
print(wikipedia.url)
# prints "www.wikipedia.org"

Since the self keyword refers to the object and not the class being called, we can define a secure method on the SearchEngineEntry class that returns the secure link to an entry.

class SearchEngineEntry:
  secure_prefix = "https://"
  def __init__(self, url):
    self.url = url
 
  def secure(self):
    return "{prefix}{site}".format(prefix=self.secure_prefix, site=self.url)
 
codecademy = SearchEngineEntry("www.codecademy.com")
wikipedia = SearchEngineEntry("www.wikipedia.org")
 
print(codecademy.secure())
# prints "https://www.codecademy.com"
 
print(wikipedia.secure())
# prints "https://www.wikipedia.org"

Above we define our secure() method to take just the one required argument, self. We access both the class variable self.secure_prefix and the instance variable self.url to return a secure URL.

This is the strength of writing object-oriented programs. We can write our classes to structure the data that we need and write methods that will interact with that data in a meaningful way.

