# 🐍 Python OOP Concepts: Polymorphism & Abstraction

A beginner-friendly Python repository demonstrating essential **Object-Oriented Programming (OOP)** concepts, focusing on **Polymorphism**, **Method Overriding**, and **Abstraction using Abstract Base Classes (ABC)**.

## 📌 Topics Covered

### 1. Polymorphism & Method Overriding
- Defining a common base class interface.
- Overriding methods in child classes.
- Using a single function with different object types.

### 2. Abstract Base Classes (ABC)
- Defining abstract classes with Python's `abc` module.
- Requiring subclasses to implement methods with `@abstractmethod`.
- Preventing instantiation of abstract or incomplete classes.

## 📂 Repository Structure

```text
Python-OOP-Concepts/
├── polymorphism.py
├── abstraction.py
└── README.md
```

## 💻 Code Examples

### 1. Polymorphism & Method Overriding

```python
class Animal:
    def speak(self):
        return "Sound of the animal"


class Dog(Animal):
    def speak(self):
        return "Woof!"


class Cat(Animal):
    def speak(self):
        return "Meow!"


def animal_speak(animal):
    print(animal.speak())


dog = Dog()
cat = Cat()

animal_speak(dog)
animal_speak(cat)
```

**Output:**

```text
Woof!
Meow!
```

**Explanation:** `Dog` and `Cat` override the `speak()` method inherited from `Animal`. The same `animal_speak()` function works with both objects, demonstrating polymorphism.

### 2. Abstraction Using Abstract Base Classes

```python
from abc import ABC, abstractmethod


class Vehicle(ABC):
    @abstractmethod
    def start(self):
        pass


class Car(Vehicle):
    def start(self):
        return "Car engine started"


class Bike(Vehicle):
    def start(self):
        return "Bike engine started"


car = Car()
bike = Bike()

print(car.start())
print(bike.start())
```

**Output:**

```text
Car engine started
Bike engine started
```

**Explanation:** `Vehicle` defines a required `start()` method. `Car` and `Bike` provide their own implementations. An abstract class with unimplemented abstract methods cannot be instantiated.

## 🔍 Polymorphism vs Abstraction

| Feature | Polymorphism | Abstraction |
|---|---|---|
| Purpose | Common interface, different behavior | Defines required behavior |
| Main focus | How objects respond | What subclasses must implement |
| Python features | Overriding, duck typing | `ABC`, `@abstractmethod` |
| Example | `Dog.speak()`, `Cat.speak()` | `Vehicle.start()` |

## 🚀 Getting Started

1. Download or clone this repository.
2. Ensure Python 3.8+ is installed.
3. Run the examples:

```bash
python polymorphism.py
python abstraction.py
```

The commands above assume you saved the corresponding examples in those `.py` files.

## 🎯 Learning Outcomes

By practicing these examples, you will learn how to:
- Override parent class methods in Python.
- Use polymorphism with different object types.
- Create abstract base classes and abstract methods.
- Explain the difference between polymorphism and abstraction.

## 📚 References

- [Python Tutorial – Classes](https://docs.python.org/3/tutorial/classes.html)
- [Python `abc` Module](https://docs.python.org/3/library/abc.html)

---

⭐ If you find this repository useful, consider giving it a star!
