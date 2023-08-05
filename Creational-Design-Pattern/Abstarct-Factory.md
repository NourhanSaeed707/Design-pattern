# Defination:
- if you familiar with **Factory pattern**, you will notice that we have a single factory class. This factory returns different subclasses based on input provided and **factory class** use if-condition or switch statment to achieve this. in **Abstract class** we get ride of if-condition block and have factory class for every sub-class. Then an **Abstract Factory class** that will return the sub-class based on the input factory class.
- **Abtract factory** is used when we have two or more objects which work together forming a kit or set and there can be set or kit that can be created by client code.
- if i have a bunch of objects or products that do familiar jobs or context then i use **Abstract class**.

# Implementation Abstract factory:
- We start by studing the product "sets"
- Create **Abstract factory** as abstract class or an interface
- **Abstract factory** defines abstract methods for creating products.
- Provide concrete implementation of factory for each set of products.
