# What is Adapter?
- Adapter pattern works as a bridge between two incompatible interfaces. This type of design pattern comes under structural pattern as this pattern combines the capability of two independent interfaces.
- This pattern aslo called as **"Wrapper"**

## Implementation 1:
# UML
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/e23d2de9-9ce4-45cd-bfec-19dc38d76d2a)

- we have a client class, target interface that the client needs, Adaptee class that have functionality that client needs.
- and we have Adapter class to combine between target and Adaptee by implements target and extends from Adapter class.

## Implementation 2:
- we have client class, **target** interface that the client needs,**Adaptee** class that have functionality that client needs.
- and we have **objectAdapter** class that implements target interface and instead of inherit from Adaptee class w have a inner object of Adaptee inside this **objectAdapter**, and this preferred way to implement.
- So we using composition instead of inheritance.




