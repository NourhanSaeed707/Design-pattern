# Defination:
- Bridge is a structural design pattern that lets you split a large class or a set of closely related classes into two separate hierarchies abstraction and implementation—which can be developed independently of each other.
- is used to decouple the interfaces from implementation and hiding the implementation details from the client programs.
- There are 2 parts in Bridge design pattern : 
1. Abstraction
2. Implementation

# UML:
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/78057544-3989-4175-bf2e-dcc899bb8933)
## Example:
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/c07745dc-ff47-43bb-a704-f83a9fff5d17)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/f6e55358-dd9c-4261-aa2a-0cf005bb9077)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/63971d7f-877c-45a3-a640-f50f19b7dd1d)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/9713f7f0-a5d4-4f37-80df-8252f9bf243d)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/be39ac67-a56a-458e-8d75-022cf9b586c6)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/02ad9cac-7ff9-458b-a3ed-0eda4e1a77fb)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/9dd233ea-b4b9-4f45-b9ed-19724a722064)

# Explanation:
- We have a abstraction **(FifoCollection)** and Implementor **(LinkedList)**,  have a refined Abstraction **(Queue)** that implements **(FifoCollection)** and inside **Queue** we hava a object from Implementor **(LinkedList)** that mean of composition.
- Then we have a two concrete implementor. that implements Implemenor **(LinkedList)** that classes are **SinglyLinkedList** and **ArrayLinkedList**

# Example in java:
- java.sql.DriverManager class with The java.sql.Driver interface form a bridge patter
