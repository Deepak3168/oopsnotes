# oopsnotes
notes on oops 

Sure, let's go through each concept one by one, providing both the definition and example code in Python.

### OOPs Concepts:

1. **Class Definition with Example Code**:
   **Definition**: A class is a blueprint for creating objects. It defines attributes (variables) and methods (functions) common to all objects of the class.
   **Python Code**:
   ```python
   class Car:
       def __init__(self, brand, model):
           self.brand = brand
           self.model = model
       
       def display_info(self):
           print(f"Brand: {self.brand}, Model: {self.model}")

   # Creating an object of the Car class
   my_car = Car("Toyota", "Camry")
   my_car.display_info()  # Output: Brand: Toyota, Model: Camry
   ```

2. **Object Definition with Example Code**:
   **Definition**: An object is an instance of a class. It represents a real-world entity and has attributes and behaviors defined by its class.
   **Python Code**:
   ```python
   class Car:
       def __init__(self, brand, model):
           self.brand = brand
           self.model = model

   # Creating an object of the Car class
   my_car = Car("Toyota", "Camry")
   ```

3. **Inheritance Definition with Example Code**:
   **Definition**: Inheritance is a mechanism in which a new class inherits properties and behaviors from an existing class (called the base class).
   **Python Code**:
   ```python
   class Animal:
       def sound(self):
           print("Animal makes a sound")

   class Dog(Animal):
       def sound(self):
           print("Dog barks")

   # Creating an object of the Dog class
   my_dog = Dog()
   my_dog.sound()  # Output: Dog barks
   ```

4. **Types of Inheritance Definition with Example Code**:
   **Definition**: Different types of inheritance include single, multiple, hierarchical, multilevel, and hybrid.
   **Python Code**:
   ```python
   class Parent:
       def func1(self):
           print("Function 1")

   class Child1(Parent):
       def func2(self):
           print("Function 2")

   class Child2(Child1):
       def func3(self):
           print("Function 3")

   # Creating an object of the Child2 class
   obj = Child2()
   obj.func1()  # Output: Function 1
   obj.func2()  # Output: Function 2
   obj.func3()  # Output: Function 3
   ```

5. **Polymorphism Definition with Example Code**:
   **Definition**: Polymorphism allows objects of different classes to be treated as objects of a common superclass. It enables methods to do different things based on the object that calls them.
   **Python Code**:
   ```python
   class Animal:
       def sound(self):
           pass

   class Dog(Animal):
       def sound(self):
           return "Woof!"

   class Cat(Animal):
       def sound(self):
           return "Meow!"

   # Function demonstrating polymorphism
   def make_sound(animal):
       print(animal.sound())

   # Creating objects of Dog and Cat classes
   my_dog = Dog()
   my_cat = Cat()

   make_sound(my_dog)  # Output: Woof!
   make_sound(my_cat)  # Output: Meow!
   ```

6. **Types of Polymorphism Definition with Example Code**:
   **Definition**: Types of polymorphism include compile-time polymorphism (method overloading) and runtime polymorphism (method overriding).
   **Python Code**:
   ```python
   # Compile-time polymorphism (Method Overloading)
   class Add:
       def add(self, a, b):
           return a + b

       def add(self, a, b, c):
           return a + b + c

   # Creating an object of the Add class
   obj = Add()
   print(obj.add(2, 3))      # Output: 5
   print(obj.add(2, 3, 4))   # Output: 9
   ```

7. **Encapsulation Definition with Example Code**:
   **Definition**: Encapsulation is the bundling of data (attributes) and methods (functions) that operate on the data into a single unit (class).
   **Python Code**:
   ```python
   class EncapsulationDemo:
       def __init__(self):
           self.__private_var = 10  # private variable

       def get_private_var(self):
           return self.__private_var

       def set_private_var(self, value):
           self.__private_var = value

   # Usage
   obj = EncapsulationDemo()
   print(obj.get_private_var())  # Output: 10
   obj.set_private_var(20)
   print(obj.get_private_var())  # Output: 20
   ```

8. **Constructor Definition with Example Code**:
   **Definition**: A constructor is a special method that is automatically called when an object is created. It initializes the object's attributes.
   **Python Code**:
   ```python
   class MyClass:
       def __init__(self, x, y):
           self.x = x
           self.y = y

   # Creating an object of the MyClass class
   obj = MyClass(5, 10)
   ```

9. **Destructor Definition with Example Code**:
   **Definition**: A destructor is a special method that is automatically called when an object is destroyed or goes out of scope. It performs cleanup tasks.
   **Python Code**:
   ```python
   class MyClass:
       def __del__(self):
           print("Destructor called")

   # Creating an object of the MyClass class
   obj = MyClass()
   del obj  # Destructor called
   ```

10. **Self Keyword Definition with Example Code**:
   **Definition**: The `self` keyword represents the instance of the class. It is used to access attributes and methods within the class.
   **Python Code**:
   ```python
   class MyClass:
       def __init__(self, x):
           self.x = x

       def display(self):
           print(self.x)

   # Creating an object of the MyClass class
   obj = MyClass(5)
   obj.display()  # Output: 5
   ```

11. **Abstraction Definition with Example Code**:
   **Definition**: Abstraction is the concept of hiding complex implementation details and showing only the necessary features of an object.
   **Python Code**:
   ```python
   from abc import ABC, abstractmethod

   class Shape(ABC):
       @abstractmethod
       def draw(self):
           pass

   class Circle(Shape):
       def draw(self):
           print("Drawing Circle")

   # Creating an object of the Circle class
   obj = Circle()
   obj.draw()  # Output: Drawing Circle
   ```

12. **Access Specifiers Definition with Example Code**:
   **Definition**: Access specifiers define the visibility of attributes and methods within a class. They include public, protected, and private.
   **Python Code**:
   ```python
   class MyClass:
       def __init__(self):
           self.public_var = 10
           self._
