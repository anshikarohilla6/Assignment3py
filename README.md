# Assignment3py
#name-Anshika
#course- BCA(AI&DS)
#section-A
#roll number-2501060113
#serial number-44
(a) Difference between Method Overriding and Method Overloading
Method Overriding

Occurs between parent and child classes.

Child class provides a new definition for a method that already exists in the parent class.

Same method name and same parameters.

Used to modify or extend parent class behavior.

Example (Method Overriding)
class Animal:
    def sound(self):
        print("Animal makes sound")

class Dog(Animal):
    def sound(self):   # overriding
        print("Dog barks")

d = Dog()
d.sound()
Method Overloading

Occurs within the same class.

Same method name but different parameters.

Python does not support true overloading like Java/C++;
however, we can use default arguments or *args to mimic it.

Example (Method Overloading-like behavior)
class Math:
    def add(self, a=0, b=0, c=0):
        return a + b + c

m = Math()
print(m.add(5, 10))      # 15
print(m.add(5, 10, 20))  # 35
(b) Role and Types of Constructors in Python
Role of Constructor

A constructor is a special method used to initialize objects when a class is created.

In Python, the constructor is defined using the __init__() method.

It sets initial values to data members and allocates resources.

Types of Constructors in Python
1. Default Constructor

No parameters (except self).

Used when we don’t want to initialize variables at creation time.

Example:
class Student:
    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

s = Student("Rahul", 90)
print(s.name, s.marks)

