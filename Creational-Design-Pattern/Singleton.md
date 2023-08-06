# Defination:
- A Singleton class has only one instanc. accessible globally through a single point (via method/field).
- Main problem this pattern solve is to ensure that only a single instance of this class exists.
- Any state you add in your singleton becomes part of "globale state" of your application 
- Singleton Pattern says that just"define a class that has only one instance and provides a global point of access to it".
- In other words, a class must ensure that only single instance should be created and single object can be used by all other classes.

## There are two forms of singleton design pattern:
- **Early Instantiation (Eager Singleton):** Create singleton as soon as class is loaded.
- **Lazy Instantiation (Lazy Singleton):** Singleton is created when it is first required.

## Advantage of Singleton design pattern:
- Saves memory because object is not created at each request. Only single instance is reused again and again.
## Usage of Singleton design pattern:
- Singleton pattern is mostly used in multi-threaded and database applications. It is used in logging, caching, thread pools, configuration settings etc.

# How to create Singleton design pattern?
- To create the singleton class, we need to have static member of class, private constructor and static factory method.
- ***Static method:*** it gets memory only because its static, it contains instance of the Singleton class.
- ***Private Constructor:*** it prevent instantiate Singleton class from outside the class. So we can't inherit from this class.
- ***Static factory method:*** This provides the global point of access to Singleton object and returns the instance to the caller.

## Example of Early Instantiation (Eager Singleton):
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/a16ffb03-d69f-4621-88e7-4b88c91da193)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/6bc8552b-df04-430d-8e80-0a896a62d862)

# Explanation:
- We start by creating a EagerRegistry class (Early Singleton class),Then create a private constructor that mean this class can't be inherited
- Then create a static method to create a instance (object) of EagerRegistry (Singleton class).
- Then create a static method to return a instance of EagerRegistry (Singleton class).
- in client class we create a two object of EagerRegistery and call **getInstance()** function to get a instance of EagerRegister.
- and System.out.println(eagerRegistry == eagerRegistry2); will return true if two objects point to the same object and it will return true because **eagerRegistry** and **eagerRegistry2** create a instance of **EagerRegistery**.




