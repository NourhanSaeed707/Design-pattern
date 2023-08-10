# What is Adapter?
- Adapter pattern works as a bridge between two incompatible interfaces. This type of design pattern comes under structural pattern as this pattern combines the capability of two independent interfaces.
- This pattern aslo called as **"Wrapper"**.

# There are two types of Adapter;
1. Class Adapter (Two way adapter)
2. Object Adapter
# What do we mean by term "Two way adapter" in Adapter design pattern?
- The object of adapter class can stand in for the real object and it can also work where object object of "Target" interface is expected. 

## Implementation 1:
# UML
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/e23d2de9-9ce4-45cd-bfec-19dc38d76d2a)

- we have a client class, target interface that the client needs, Adaptee class that have functionality that client needs.
- and we have Adapter class to combine between target and Adaptee by implements target and extends from Adapter class.

## Implementation 2:
- we have client class, **target** interface that the client needs,**Adaptee** class that have functionality that client needs.
- and we have **objectAdapter** class that implements target interface and instead of inherit from Adaptee class w have a inner object of Adaptee inside this **objectAdapter**, and this preferred way to implement.
- So we using composition instead of inheritance.

# Implementation:
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/76cab885-4f12-4252-8ee3-d9c7239630b1)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/5b160e7e-bf5d-4251-9ded-3a18f20e4b0a)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/45ef4148-1ce6-4288-b1e8-c3b581845148)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/02c41948-abe8-4e13-9048-bc4debf77d08)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/00d26c3e-0e5a-48ec-b2e9-7836c5418e67)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/35ddcfea-b564-4683-ba97-60d628a5c8f7)

# Explanation Adapter class:
- We have a client class **(BusinessCardDesigner)**, Adaptee class **(Employee)** that have functionality tha client class needs, we have a target interface that client needs **(Customer)**, we have Adapter class **(EmployeeClassAdapter)** that implements **Customer** and inherit from **Employee**.
- Then we have a 3 methods that implements Customer class and we have call inside it methods from Employee class to help us to implement method
- Then in main class we instantiate a object from **(EmployeeClassAdapter)** and instance from  **(BusinessCardDesigner)** and call a **(designCard())** that expects a Customer class

# Implementation Object Adapter:
- This best way to use constructor to define adaptee.
- we using composition instead of inheritace.
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/47fe3de4-7e20-4e5e-a882-b042e52eaa74)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/fc545cc5-461c-4f0e-852b-6b7ac3ffb018)

# Example Adapter in java:
- java.io.InputStreamReader and java.io.OutputStreamWriter classes are example of Object Adapter.
- These classes adapt existing InputStream/OutputStream object a Reader/Writer interface.

# Pitfalls:
- One of the drawbacks of using the adapter pattern is that it introduces additional overhead and complexity to your code. The adapter class acts as an intermediary between the two interfaces, which means that it has to perform extra operations to convert the data, handle exceptions, and delegate calls




