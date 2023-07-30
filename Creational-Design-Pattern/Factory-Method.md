## Defination: 
- **The Factory Method** Design Pattern is a creational pattern that provides an interface for creating objects but allows subclasses to decide which class to instantiate. It is a pattern that promotes loose coupling between classes and promotes code reuse.
- We want to move the object creation logic from our code to separate class and that like "Simple Factory", But Factory Method add something to this design pattern more than Simple Factory, that We use this pattern when we don't know in advance which class we may need to instantiate beforehand and allow other new classes to be added to system and handle their creation without affecting client code.
- We let subclasses decide which object to instantiate by overriding the factory method.

## Example of Factory Method in java:
- the java.util.Collection (or java.util.AbstractCollection) has an abstract method called **iterator()** This an example of factory method.

## Pitfalls:
- More complex to implement. More classes involved and need unit testing.
- You have to start with **Factory method** from the beginning. it's not easy to refactor existing code into factory method pattern.
- Sometimes this pattern forces you to subclass just to create appropriate instance.
