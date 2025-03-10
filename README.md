# 🎯 Object-Oriented Programming (OOP) in Python 🚀

## 📌 Overview
This repository contains Python projects demonstrating **Object-Oriented Programming (OOP)** concepts such as **classes, attributes, methods, constructors, inheritance, encapsulation, and polymorphism**.

---

## 📂 Assignments Included:
### **1️⃣ Assignment 1: Design Your Own Class**
📝 **Task:**  
Create a Python class representing a real-world object (Smartphone, Book, Superhero, etc.), including attributes, methods, and an inheritance layer.

✅ **Concepts Used:**
- Classes & Objects  
- Attributes & Methods  
- Constructors (`__init__`)
- Inheritance
- Encapsulation

### **2️⃣ Activity 2: Polymorphism Challenge**
📝 **Task:**  
Create multiple classes (e.g., `Car`, `Plane`, `Boat`) that share the same method (`move()`) but behave differently.

✅ **Concepts Used:**
- **Polymorphism**: Same method, different behavior across classes.

---

## 🚀 **Assignment 1: Class Design Example**
### **📚 Book Class with Encapsulation & Inheritance**
```python
# Parent Class
class Book:
    def __init__(self, title, author, price):
        self.title = title  # Public attribute
        self.author = author  # Public attribute
        self.__price = price  # Private attribute (Encapsulation)

    def get_price(self):
        return self.__price

    def book_info(self):
        return f"📖 '{self.title}' by {self.author}, Price: ${self.__price}"

# Child Class with Inheritance
class EBook(Book):
    def __init__(self, title, author, price, file_size):
        super().__init__(title, author, price)  # Inheriting from Book
        self.file_size = file_size  # New attribute

    def book_info(self):
        return f"📱 E-Book: '{self.title}' by {self.author}, Size: {self.file_size}MB, Price: ${self.get_price()}"

# Creating Objects
physical_book = Book("Python Mastery", "John Doe", 29.99)
ebook = EBook("Python Mastery", "John Doe", 19.99, 2.5)

# Output
print(physical_book.book_info())  # 📖 'Python Mastery' by John Doe, Price: $29.99
print(ebook.book_info())  # 📱 E-Book: 'Python Mastery' by John Doe, Size: 2.5MB, Price: $19.99
