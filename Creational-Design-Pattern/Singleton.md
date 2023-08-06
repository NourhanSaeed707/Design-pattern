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


