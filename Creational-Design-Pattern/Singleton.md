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
- We start by creating a EagerRegistry class (Early Singleton class),Then create a private constructor that mean this class can't be inherited and to make sure that nobody can create instance of our class outside of this class.
- Then create a static method to create a instance (object) of EagerRegistry (Singleton class).
- Then create a static method to return a instance of EagerRegistry (Singleton class).
- in client class we create a two object of EagerRegistery and call **getInstance()** function to get a instance of EagerRegister.
- and System.out.println(eagerRegistry == eagerRegistry2); will return true if two objects point to the same object and it will return true because **eagerRegistry** and **eagerRegistry2** create a instance of **EagerRegistery**.

## Example of Lazy instantiation (Lazy Singleton):
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/435a7574-1843-4ed7-a115-848b09707208)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/39a0beb1-d00d-43aa-b6de-fb5c26c5dce6)

## Explanation: 
- We first create a LazyRegistryWithDCL class, Then create a private constructor to make sure that nobody can create object of this class outside class.
- Then create a static member **LazyRegistryWithDCL instance** This variable is going to hold our Singleton instance.
- Then create a static method **getInstance()** to get instance of this class, First we have to make sure that no instance is created and make sure to handle Synchronize mechanism so we write a if condition to make sure that **INSTANCE** == NULL so that mean no instance is created, then inside use Synchronize block and as double check we have to make sure that our **INSTANCE** == NULL again beacuse it may happen that two threads might call our instance method both see that INSTANCE == NULL as soon as we hit our Synchronize block one of threads is going to get the lock and start executing the code and create instance second one is going to wait.
- **volatile**: it will indicate to these threads that they shouldn't use the cached version of this variables.

## Example of Lazy instantiation (Lazy Singleton):
- Singleton pattern using Lazy instantiation holder class (private class). This ensures that, We have a lazy intialization without worrig about synchronization. 
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/e9564a04-e198-49f8-b972-af1525eb2c30)





