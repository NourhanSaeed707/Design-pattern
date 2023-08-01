# Defination:
- We have a complex object that is costly to create. To create more instances of such class, we use an existing instance as a **Prototype**.
- **Prototype** will allow us to make copies (clone = copy) of existing obejct and save us from recreate objects from scratch.
- Prototype allows us to hide the complexity of making new instances from the client. The concept is to copy an existing object rather than creating a new instance from scratch, something that may include costly operations. The existing object acts as a prototype and contains the state of the object. The newly copied object may change same properties only if required. This approach saves costly resources and time, especially when object creation is a heavy process.
- Prototype is a creational design pattern that let us duplicates existing objects without having our code depend on their classes. For example this pattern could be used to create multiple instances of the same object with unique attributes.

# When use Prototype: 
- Prototype patterns are required, when object creation is time consuming, and costly operation, so we create objects with the existing object itself. One of the best available ways to create an object from existing objects is the clone() method. Clone is the simplest approach to implement a prototype pattern. However, it is your call to decide how to copy existing object based on your business model.

# Implement a Prototype:
- We start by creating a class which will be a prototype.
- The class must implement Cloneable interface.
- Class should override clone method and return copy of itself.
- The method should declare CloneNotSupportedException in throws clause to give subclasses chance to decide on whether to support cloing.
- Clone method implementation should consider the deep copy **(we will create all objects that are needed by our prototype object)** and shallow copy **(is simply copy the object's properties into the new copy)** and choose whatever is applicable.
- The Clone method implemented similary in all classes. This method create an object of the current class and transfers all old objects's attributes to the new one, Even the private fields can be copied because most of programming language allow objects to access the private fields of other objects of same class. 

