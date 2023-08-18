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

## Implementaion of proxy:
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/760f02d8-2a62-4b57-aafb-13b63d1b33ae)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/9c83614d-2b3b-45ae-8946-0e5856df475e)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/84a12e55-ed5a-45a2-b691-d5ca84e6b256)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/90e33eac-4870-4f84-ad51-5980074fab76)


# Example in java:
- Hibernate use proxy design pattern to load a collection of value types.
- Spring uses proxy to provide support for features like transaction, caching and general AOP support.



