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
- The Clone method implemented similarly in all classes. This method create an object of the current class and transfers all old objects's attributes to the new one, Even the private fields can be copied because most of programming language allow objects to access the private fields of other objects of same class.

# UML diagram for Prototype Creational design pattern:
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/4b071294-0dd0-4661-a1b8-8441e75712ac)

# Advantages of Prototype design pattern:
1. **Object creation without coupling to specific classes:** The Prototype Design Pattern allows you to create new objects by cloning existing ones without being bound to the specific classes of the objects being cloned. This promotes decoupling between the client code and the concrete classes, making it easier to introduce new types of objects without modifying the client code.
2. **Reduces the need for subclassing:** The Prototype pattern can be a more flexible alternative to subclassing in cases where we would usually derive subclasses to create variations of objects. We can clone existing objects and modify them instead of deriving subclasses. This approach simplifies the object creation process and reduces the complexity of class hierarchies.
3. **Efficient object creation:** Creating new objects through cloning can be more efficient than creating them from scratch. Cloning avoids the overhead of initializing objects and setting their initial state. Instead, you can clone a pre-configured prototype and modify only the necessary attributes or properties.
4. **Customizable object creation:** The **Prototype** pattern allows us to create new objects with customized attributes or properties. You can clone a prototype and then modify the clone to meet specific requirements. This flexibility is especially useful when creating complex objects with many configurable parameters.
5. **Simplifies object initialization:** Object initialization can be complex, especially when dealing with dependencies and complex construction logic. The Prototype pattern simplifies object initialization by allowing us to clone a fully initialized object and then modify it as needed. This approach can help avoid complex initialization code and improve the overall readability and maintainability of the code.
6. **Supports dynamic runtime changes:** Prototypes can be modified at runtime, allowing us to change the behavior or configuration of objects on the fly. Instead of creating new objects, we can clone existing ones and apply runtime modifications to adapt to different scenarios or user preferences.
7. **Supports creating object hierarchies:** Prototypes can be used to create object hierarchies by allowing prototypes to reference other prototypes. This enables the creation of complex object structures and relationships without the need to explicitly define them in code


