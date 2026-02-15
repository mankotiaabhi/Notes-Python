# OOP and SOLID Principles (Python)

This document contains Object-Oriented Programming (OOP) concepts and
SOLID design principles with examples in Python.

------------------------------------------------------------------------

# 📘 Object Oriented Programming (OOP)

## 1️⃣ Class and Object

``` python
class Student:
    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

    def display(self):
        print(f"Name: {self.name}, Marks: {self.marks}")

s1 = Student("Abhay", 90)
s1.display()
```

------------------------------------------------------------------------

## 2️⃣ Encapsulation

``` python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private variable

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance
```

------------------------------------------------------------------------

## 3️⃣ Inheritance

``` python
class Animal:
    def speak(self):
        print("Animal sound")

class Dog(Animal):
    def speak(self):
        print("Bark")
```

------------------------------------------------------------------------

## 4️⃣ Polymorphism

``` python
class Cat:
    def sound(self):
        print("Meow")

class Dog:
    def sound(self):
        print("Bark")

animals = [Cat(), Dog()]
for a in animals:
    a.sound()
```

------------------------------------------------------------------------

# 📕 SOLID Principles (Detailed with Code)

------------------------------------------------------------------------

## S - Single Responsibility Principle (SRP)

A class should have only one reason to change.

❌ Wrong:

``` python
class Invoice:
    def calculate_total(self):
        pass

    def print_invoice(self):
        pass

    def save_to_db(self):
        pass
```

✅ Correct:

``` python
class Invoice:
    def calculate_total(self):
        pass

class InvoicePrinter:
    def print(self, invoice):
        pass

class InvoiceRepository:
    def save(self, invoice):
        pass
```

------------------------------------------------------------------------

## O - Open/Closed Principle (OCP)

Open for extension, closed for modification.

``` python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height
```

Now we can add new shapes without modifying old code.

------------------------------------------------------------------------

## L - Liskov Substitution Principle (LSP)

Child classes should be replaceable for parent class.

❌ Wrong Example:

``` python
class Bird:
    def fly(self):
        print("Flying")

class Ostrich(Bird):
    def fly(self):
        raise Exception("Ostrich can't fly")
```

✅ Correct Design:

``` python
class Bird:
    pass

class FlyingBird(Bird):
    def fly(self):
        print("Flying")

class Sparrow(FlyingBird):
    pass

class Ostrich(Bird):
    pass
```

------------------------------------------------------------------------

## I - Interface Segregation Principle (ISP)

Clients should not depend on methods they do not use.

❌ Wrong:

``` python
class Worker:
    def work(self):
        pass

    def eat(self):
        pass
```

✅ Correct:

``` python
class Workable:
    def work(self):
        pass

class Eatable:
    def eat(self):
        pass

class Human(Workable, Eatable):
    def work(self):
        print("Working")

    def eat(self):
        print("Eating")
```

------------------------------------------------------------------------

## D - Dependency Inversion Principle (DIP)

Depend on abstractions, not concrete implementations.

❌ Wrong:

``` python
class MySQLDatabase:
    def connect(self):
        print("Connected to MySQL")

class Application:
    def __init__(self):
        self.db = MySQLDatabase()
```

✅ Correct:

``` python
class Database:
    def connect(self):
        pass

class MySQLDatabase(Database):
    def connect(self):
        print("Connected to MySQL")

class Application:
    def __init__(self, database: Database):
        self.database = database

    def start(self):
        self.database.connect()

db = MySQLDatabase()
app = Application(db)
app.start()
```

------------------------------------------------------------------------


