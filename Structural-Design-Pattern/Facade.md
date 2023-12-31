# Defination:
- Client has to interact with a large number of interfaces and classes in a subsystem to get result, and this interaction because client needs some functionality that is provided by this particular subsystem, So if you want to make any changes to these classes or interfaces you have to make sure that your client is going to work with these changes, So client gets tightly coupled with those interfaces and classes, Facade solves this problem.
- Facade pattern hides the complexities of the system and provides an interface to the client using which the client can access the system, This pattern involves a single class which provides simplified methods required by client and delegates calls to methods of existing system classes.
- **Facade** provides a simple and unified interface to a subsystem, Client interacts with just **Facade** now to get some result.
- Facade NOT just one to one method forwarding to other classes.

# Implement a Facade:
- We start by creating class that will serve as a facade.
- We determine the overall "use cases/tasks" that subsystem is used for.
- We write a method that exposes each "use case" or task.
- This method take care of working with different classes of subsystem.

#  Example to understand more Facade:
- You need to first validate all the user information, check that the email is not already taken, and then finally save the user to the database.
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/f1a11403-d720-4e44-b38d-ffa6c67602fb)
- This is a three step process that you most likely will need to use in many places across your application. The idea behind the facade pattern is to take all these steps and put them behind a single interface/function.
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/32a40d1f-f50d-452b-b316-d82615b850ad)
- By doing this we can clean up our code so that everywhere we need to save our user it just looks like this.
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/437c4484-02fe-4770-8ffe-8fe12278421b)
- This has two primary benefits.
1. Your code is much easier to read since instead of having to read five lines of code to understand what is going on we only need to read one line. This becomes an even larger benefit if the underlying code is longer or more complex.
2. Your code is easier to change since all the code for saving the user is in one single place. If we need to modify this code to add an additional step to also validate the username is not taken it is trivial since we just need to add that code in one single place. If we did not use the facade pattern, though, we would need to add that code to every single place we save a user which could be all over your application.

# UML:
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/80e879ab-529f-4b1c-9331-501ded35fbfd)

## Example:
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/abc83acd-0d56-4943-a471-03129a0762df)
![image](https://github.com/NourhanSaeed707/Design-pattern/assets/64387352/3227e249-9fe4-4167-8a0a-fb8f916272e2)

## Explanation:
- Here before we create a EmailFacade class client was calling a function to send email.
- So to use Facade we create a class EmailFacade and move logic of **sendOrderEmailWithoutFacade() function** inside a method inside **EmailFacade class** so in the client we only make a instance of **EmailFacade** and call a method to send email so by that we make facade deal with the logic and client only call facade.

# Example of Facade in java:
- java.net.URL class is greate example of facade, This class provide a simple method called as openStream() and we get an input stream to the resource pointed by URL object.


