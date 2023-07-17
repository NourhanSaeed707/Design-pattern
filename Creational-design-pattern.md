# Creational Design Pattern: 
- These patterns are designed for class instantiation. They can be either class-creation patterns or object-creational patterns.
## When Will We Need Builder Design Pattern?
- Imagine that we want to build software that accepts customers' details and stores them in a database. Customers are shown a form that accepts the below **mandatory** and **optional** fields.
- **Mandatory Fields** - First Name, Last Name, Primary Email, and Primary Mobile Number
- **Optional Fields** - Middle Name, Secondary Email, and Secondary Mobile Number
- Ideally, we create a Customer class with the **mandatory** and **optional** attributes listed above. We create a constructor that accepts the above attributes. Since some attributes are optional, we may need to pass null values to those attributes we don't want to use. The builder design pattern lets us create an object step by step without passing all the values to the constructor.

## 1. Buider:
- Builder pattern was introduced to solve some of the problems with Factory and Abstract Factory design patterns when the Object contains a lot of attributes. There are three major issues with Factory and Abstract Factory design patterns when the Object contains a lot of attributes.
1. Too Many arguments to pass from client program to the Factory class that can be error prone because most of the time, the type of arguments are same and from client side its hard to maintain the order of the argument.
2. Some of the parameters might be optional but in Factory pattern, we are forced to send all the parameters and optional parameters need to send as NULL.
3. If the object is heavy and its creation is complex, then all that complexity will be part of Factory classes that is confusing.

- We can solve the issues with large number of parameters by providing a constructor with required parameters and then different setter methods to set the optional parameters. The problem with this approach is that the Object state will be inconsistent until unless all the attributes are set explicitly. **Builder pattern solves the issue with large number of optional parameters and inconsistent state by providing a way to build the object step-by-step and provide a method that will actually return the final Object.**

## Builder Design Pattern in Java:
- Let’s see how we can implement builder design pattern in java.
1. First of all you need to create a static nested class and then copy all the arguments from the outer class to the Builder class. We should follow the naming convention and if the class name is **Computer** then builder class should be named as **ComputerBuilder**.
2. Java Builder class should have a public constructor with all the required attributes as parameters.
3. Java Builder class should have methods to set the optional parameters and it should return the same Builder object after setting the optional attribute.
4. The final step is to provide a **build()** method in the builder class that will return the Object needed by client program. For this we need to have a private constructor in the Class with Builder class as argument.
