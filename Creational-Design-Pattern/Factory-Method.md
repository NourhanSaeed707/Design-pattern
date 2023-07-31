## Defination: 
- **The Factory Method** Design Pattern is a creational pattern that provides an interface for creating objects but allows subclasses to decide which class to instantiate. It is a pattern that promotes loose coupling between classes and promotes code reuse.
- We want to move the object creation logic from our code to separate class and that like "Simple Factory", But Factory Method add something to this design pattern more than Simple Factory, that We use this pattern when we don't know in advance which class we may need to instantiate beforehand and allow other new classes to be added to system and handle their creation without affecting client code.
- We let subclasses decide which object to instantiate by overriding the factory method.

## Example of Factory Method in java:
- the java.util.Collection (or java.util.AbstractCollection) has an abstract method called **iterator()** This an example of factory method.
- you might want to display each element. The easiest way to do this is to employ an iterator, which is **an object** that implements either the Iterator or the ListIterator interface.

## Pitfalls:
- More complex to implement. More classes involved and need unit testing.
- You have to start with **Factory method** from the beginning. it's not easy to refactor existing code into factory method pattern.
- Sometimes this pattern forces you to subclass just to create appropriate instance.

## Example:
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/edb8e0a5-5235-4703-9169-bc899e1261ad)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/387afbf3-1e12-44ad-bc82-5c7f01d23116)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/670ae295-0856-438c-b7f8-55e54f6b2bb1)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/7c8d6ae0-f291-4773-8378-b5261f95d331)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/e96823cf-952f-4127-b53e-b13d02876d89)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/2c4fda19-5f97-4e28-bd9b-cd29dc5e9ec5)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/957e519b-c95b-40d0-b28d-859b8b515cb9)

# Explanation:
- Here we have a product class **(Message)** and there are two other classes **(JsonMessage, TextMessage)** these classes are **concrete classes**, that inherit from product class(Message).
- We make a make a creator class **(MessageCreator)** that have a factory method **(createMessage)** that other concrete classes **(JSONMessageCreator, TextMessageCreator)** will override on it so that every class of it can instantiate a instance of it.
- In **JSONMessageCreator** class a methd that override on factory method and instantiate a instance from JsonMessage.
- In **TextMessageCreator** class a methd that override on factory method and instantiate a instance from TextMessage.
- In client class i have two methods main method and printMessage(), a printMessage method take a object of** MessageCreator** and return a message
- in Main method we make a instance of **JSONMessageCreator** and **TextMessageCreator** in printMethod.
- in this we achieve a factory method by create a creator class and put in it a factory method that every concrete creator class can override on it, so that we let user decide which class to instantiate.







