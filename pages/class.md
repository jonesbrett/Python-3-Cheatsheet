

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
