# Defination:
- Provide a surrogate or placeholder to another object to controll access to it (Like a gate for object).
- In proxy pattern, we create object having original object to interface its functionality to outer world.
- A real world example can be a cheque or credit card is a proxy for what is in our bank account. It can be used in place of cash, and provides a means of accessing that cash when required. And that’s exactly what the Proxy pattern does – **“Controls and manage access to the object they are protecting“.**

# UML:
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/2722c858-b000-4ff1-970a-0e37e04ae046)

## Implement a proxy:
- We start by implementing proxy
- Proxy must implement same interface as real subject
- We can create actual object later when required or ask for one in constructor.
- In method implementations of proxy we implement proxy's function before delegating to real object.




