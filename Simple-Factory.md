## Defined:
- Simple factory generates an instance of an object/service for client without exposing any implementation to the client.
- In OOP, a factory is an object for creating other objects.
- Here we simply move instantiation logic to seperate class most commonly to static method of this class.
- Some do not consider a **Simple Factory** a design pattern as its simply a method that encapsulates object instantiation. Nothing complex goes on that method
- **The main essence**: Simple Factory is the simplest class which has methods for creation other class instances. For example if you need to create a tons of instances for some specific class, it’s much easier to use method which returns instances for you. That’s the main idea
## Why, When?
- Typically we want to do this if we have more than one option when instantiating object and simple logic is used to choose correct class. 
