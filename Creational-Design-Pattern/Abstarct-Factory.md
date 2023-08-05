# Defination:
- if you familiar with **Factory pattern**, you will notice that we have a single factory class. This factory returns different subclasses based on input provided and **factory class** use if-condition or switch statment to achieve this. in **Abstract class** we get ride of if-condition block and have factory class for every sub-class. Then an **Abstract Factory class** that will return the sub-class based on the input factory class.
- **Abtract factory** is used when we have two or more objects which work together forming a kit or set and there can be set or kit that can be created by client code.
- if i have a bunch of objects or products that do familiar jobs or context then i use **Abstract class**.
- Abstract Factory Design Pattern, as the name suggests is an abstraction over Factory design pattern. It is one of the creational design patterns. As a factory pattern allows us to create a generic factory of one or more than one type of object, extending the same behavior abstract factory design pattern allows us to create a factory of factories, one level above the abstraction in the factory design pattern.
- Consider a real-life analogy, just like a factory can create products or objects, similarly, an industry can create multiple factories. So industry can be understood as the abstract factory pattern, and a single factory can be understood as the factory pattern.

# Implementation Abstract factory:
- We start by studing the product "sets"
- Create **Abstract factory** as abstract class or an interface
- **Abstract factory** defines abstract methods for creating products.
- Provide concrete implementation of factory for each set of products.

# Example:

