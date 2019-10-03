# Dependency Injection

Dependency injection is a technique whereby one object (or static method) supplies the dependencies of another object. 
In Java, before we can use methods of other classes, we first need to create the object of that class (i.e. class A needs to create an instance of class B).

So, transferring the task of creating the object to someone else and directly using the dependency is called dependency injection.

There are basically three types of dependency injection:
##### Constructor injection:
The dependencies are provided through a class constructor.

##### Setter injection: 
The client exposes a setter method that the injector uses to inject the dependency.

##### Interface injection: 
The dependency provides an injector method that will inject the dependency into any client passed to it. Clients must implement an interface that exposes a setter method that accepts the dependency.

So now its the dependency injection’s responsibility to:

- Create the objects
- Know which classes require those objects
- And provide them all those objects

If there is any change in objects, then DI looks into it and it should not concern the class using those objects. This way if the objects change in the future, then its DI’s responsibility to provide the appropriate objects to the class.

### Benefits of using DI
- Helps in Unit testing.
- Boiler plate code is reduced, as initializing of dependencies is done by the injector component.
- Extending the application becomes easier.
- Helps to enable loose coupling, which is important in application programming.

### Disadvantages of DI
- It’s a bit complex to learn, and if overused can lead to management issues and other problems.
- Many compile time errors are pushed to run-time.
- Dependency injection frameworks are implemented with reflection or dynamic programming. This can hinder use of IDE automation.

### Libraries and Frameworks that implement DI

- Spring (Java)
- Google Guice (Java)
- Dagger (Java and Android)
- Castle Windsor (.NET)
- Unity(.NET)

https://www.freecodecamp.org/news/a-quick-intro-to-dependency-injection-what-it-is-and-when-to-use-it-7578c84fa88f/
