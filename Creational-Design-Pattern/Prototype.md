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

# Example of Prototype:
- Actually the Object.clone() method is a example of prototype design pattern.
- This method is provided by java and can clone an existing object, thus allowing any object act as prototype, Classes still needed to be Clonable but the method do the job for of cloning object.

# UML diagram for Prototype Creational design pattern:
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/4b071294-0dd0-4661-a1b8-8441e75712ac)

# Advantages of Prototype design pattern👍
1. **Object creation without coupling to specific classes:** The Prototype Design Pattern allows you to create new objects by cloning existing ones without being bound to the specific classes of the objects being cloned. This promotes decoupling between the client code and the concrete classes, making it easier to introduce new types of objects without modifying the client code.
2. **Reduces the need for subclassing:** The Prototype pattern can be a more flexible alternative to subclassing in cases where we would usually derive subclasses to create variations of objects. We can clone existing objects and modify them instead of deriving subclasses. This approach simplifies the object creation process and reduces the complexity of class hierarchies.
3. **Efficient object creation:** Creating new objects through cloning can be more efficient than creating them from scratch. Cloning avoids the overhead of initializing objects and setting their initial state. Instead, you can clone a pre-configured prototype and modify only the necessary attributes or properties.
4. **Customizable object creation:** The **Prototype** pattern allows us to create new objects with customized attributes or properties. You can clone a prototype and then modify the clone to meet specific requirements. This flexibility is especially useful when creating complex objects with many configurable parameters.
5. **Simplifies object initialization:** Object initialization can be complex, especially when dealing with dependencies and complex construction logic. The Prototype pattern simplifies object initialization by allowing us to clone a fully initialized object and then modify it as needed. This approach can help avoid complex initialization code and improve the overall readability and maintainability of the code.
6. **Supports dynamic runtime changes:** Prototypes can be modified at runtime, allowing us to change the behavior or configuration of objects on the fly. Instead of creating new objects, we can clone existing ones and apply runtime modifications to adapt to different scenarios or user preferences.
7. **Supports creating object hierarchies:** Prototypes can be used to create object hierarchies by allowing prototypes to reference other prototypes. This enables the creation of complex object structures and relationships without the need to explicitly define them in code

# Disadvantages of the Prototype Design Pattern👎:
1. **Complexity of managing prototypes:** The **Prototype** pattern introduces the need for managing a registry or a collection of prototypes. This registry can become complex to maintain, especially in applications with a large number of different prototypes. It requires careful management to ensure the correct registration and retrieval of prototypes.
2. **Deep copying challenges:** To ensure the integrity of the cloned objects, the **Prototype** pattern often requires deep copying of the attributes and internal state. This process can become complex and error-prone, especially when dealing with nested objects or complex data structures. Implementing proper deep copying logic can be a non-trivial task.
3. **Cloning limitations:** Some objects may not be easily cloneable or may not support the cloning process at all. In such cases, using the Prototype pattern becomes challenging or even impossible. Objects that contain non-serializable or non-copyable resources, such as network connections or file handles, may not be suitable for cloning.
4. **Impact on performance and memory usage:** While cloning objects can be more efficient than creating them from scratch, the Prototype pattern can introduce additional memory usage. Cloning objects, especially deep copies, can consume more memory compared to simply instantiating new objects. Additionally, maintaining a registry of prototypes can also consume memory.
5. **Potential confusion with object references:** Cloning objects may lead to unexpected behavior if the objects contain references to other objects. Changes made to one object may unintentionally affect the cloned object or other objects it references. Proper care must be taken to ensure that object references are correctly handled during the cloning process.
6. **Difficulty in applying the pattern to existing systems:** Integrating the Prototype pattern into an existing codebase or system can be challenging, especially if the codebase was not designed with prototype-based object creation in mind. Retrofitting the pattern may require refactoring existing code and making significant changes to the object creation logic.
7. **Limited compile-time type checking:** Since the Prototype pattern relies on cloning existing objects, compile-time type checking may be limited. The types of the cloned objects may not be known until runtime, which can potentially lead to errors if the cloned objects are not compatible with the client code’s expectations.

# Implemenatation: 
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/e5400e76-4487-48ec-a63a-241f38513cf5)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/417d282e-2d0b-4016-814a-195eeaf62a41)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/705f8baf-8e6b-440e-96f9-0eba559719f0)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/87f811ab-e0e5-4f3b-937b-fca69cfe018b)

# Explanation:
1. First we have a main class (Animal class) that have a a method **makeCopy()** to make copy(clone) of object.
2. We have a Sheep class to implements Animal interface and ovveride of **makeCopy()** method to make copy of object.
3. Then make **CloneFactory** class to get copied object.
4. then in client class make a instance of main class and make copy of that instance and use it.
5. we have to know that every instance of it (main instance and copy instance ) have different memory location.

  




