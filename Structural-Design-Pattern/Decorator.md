# Defination:
- Decorator is a structural design pattern that lets you attach new behaviors to objects by placing these objects inside special wrapper objects that contain the behaviors.
- is used to modify the functionality of an object at runtime. At the same time other instances of the same class will not be affected by this, so individual object gets the modified behavior.

# Implement a Decorator:
- We start with our component.
- Component define interface that needed or already used by client.
- Concrete Component implements component.
- We define our decorator, Decorator implements component and also needs reference to concrete component.
- In decorator methods we provide additional behaviour on top that provided by concrete component instance.
- Decorator can be abstract class, and depend on subclasses tp provided functionality.

# Example:
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/843f6f73-5525-4c8e-8da6-5482ca1c1b47)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/f32decbe-fe20-4c13-8033-fb38c0ba5522)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/74ad9d04-39f0-4521-803c-b6a0713d55e0)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/607c3526-956a-4a16-8943-7173a867ea7c)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/ad6158a3-0aa0-46a6-b71d-10fb7bad1230)

# Exaplanation:
- First we make a component class **(Message)** and Concrete component **(TextMessage)** that implements **Message interface**.
- Then we implement a Decorator class **(HtmlEncodedMessage)** to implement a component and we get a instance from message and initialize it in constructor and implement the method of Message component in **(HtmlEncodedMessage)** and add a behviour on it StringEscapeUtils.escapeHtml4().
- then we implement client and call a decorator **(HtmlEncodedMessage)**.

# Example of Decorator in java:
- java.io.BufferedOutputStream, This improves i/o performance by reducing number of writes.
