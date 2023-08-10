# What is Adapter?
- Adapter pattern works as a bridge between two incompatible interfaces. This type of design pattern comes under structural pattern as this pattern combines the capability of two independent interfaces.
- This pattern aslo called as **"Wrapper"**

## UML 1:
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/97be3bcc-5596-4ee1-a762-39debe71e0d7)
## Explanation of UML:
- we have a client class, target interface that the client needs, Adaptee class that have functionality that client needs.
- and we have Adapter class to combine between target and Adaptee by implements target and extends from Adapter class .

## UML 2:
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/d27d85e0-774b-40a8-a0a9-6ef9c0efd033)
## Explanation of UML:
- we have client class, **target** interface that the client needs,**Adaptee** class that have functionality that client needs.
- and we have **objectAdapter** class that implements target interface and instead of inherit from Adaptee class w have a inner object of Adaptee inside this **objectAdapter**, and this preferred way to implement




