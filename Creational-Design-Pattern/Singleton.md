# Defination:
- A Singleton class has only one instanc. accessible globally through a single point (via method/field).
- Main problem this pattern solve is to ensure that only a single instance of this class exists.
- Any state you add in your singleton becomes part of "globale state" of your application 
- Singleton Pattern says that just"define a class that has only one instance and provides a global point of access to it".
- In other words, a class must ensure that only single instance should be created and single object can be used by all other classes.

# There are two forms of singleton design pattern:
- **Early Instantiation:** creation of instance at load time.
- **Lazy Instantiation:** creation of instance when required.
