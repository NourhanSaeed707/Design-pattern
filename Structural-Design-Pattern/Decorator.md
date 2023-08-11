# Defination:
- Decorator is a structural design pattern that lets you attach new behaviors to objects by placing these objects inside special wrapper objects that contain the behaviors.
- is used to modify the functionality of an object at runtime. At the same time other instances of the same class will not be affected by this, so individual object gets the modified behavior.

# Implement a Decorator:
- We start with our component.
- Component define interface that needed or already used by client.
- Concrete Component implements component.
- We define our decorator, Decorator implements component and also needs reference to concrete component.
- In decorator methods we provide additional behaviour on top that provided by concrete component instance.
