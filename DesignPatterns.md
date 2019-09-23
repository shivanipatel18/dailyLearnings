Types of Design Patterns
  There are mainly three types of design patterns:

A. Creational
 These design patterns are all about class instantiation or object creation. These patterns can be further categorized into 
 Class-creational patterns and object-creational patterns. While class-creation patterns use inheritance effectively in 
 the instantiation process, object-creation patterns use delegation effectively to get the job done.
    
  Creational design patterns are the Factory Method, Abstract Factory, Builder, Singleton, Object Pool, and Prototype.

Use case of creational design pattern -
1) For creating multiple instances of a class 

B. Structural
 These design patterns are about organizing different classes and objects to form larger structures and provide new 
 functionality.
  Structural design patterns are Adapter, Bridge, Composite, Decorator, Facade, Flyweight, Private Class Data, and Proxy.

Use Case Of Structural Design Pattern-

1) When 2 interfaces are not compatible with each other and want to make establish a relationship between them through an 
adapter its called adapter design pattern. Adapter pattern converts the interface of a class into another interface or classes 
the client expects that is adapter lets classes works together that could not otherwise because of incompatibility. so in these
type of incompatible scenarios, we can go for the adapter pattern.

C. Behavioral
 Behavioral patterns are about identifying common communication patterns between objects and realize these patterns.
 Behavioral patterns are Chain of responsibility, Command, Interpreter, Iterator, Mediator, Memento, Null Object, Observer, 
 State, Strategy, Template method, Visitor

Use Case of Behavioral Design Pattern-

1) Template pattern defines the skeleton of an algorithm in an operation deferring some steps to sub-classes, Template method 
lets subclasses redefine certain steps of an algorithm without changing the algorithm structure. say for an example in your 
project you want the behavior of the module can be extended, such that we can make the module behave in new and different ways
as the requirements of the application change, or to meet the needs of new applications. However, No one is allowed to make 
source code changes to it. it means you can add but can’t modify the structure in those scenarios a developer can approach 
template design pattern.

More info on following patterns:

1. Object Pool Design Pattern

Object pool pattern is a software creational design pattern which is used in situations where the cost of initializing a class
instance is very high.Basically, an Object pool is a container which contains some amount of objects. So, when an object is 
taken from the pool, it is not available in the pool until it is put back.
Objects in the pool have a lifecycle:

-Creation
-Validation
-Destroy.

2. Factory Design Pattern

Factory method is a creational design pattern, i.e., related to object creation. In Factory pattern, we create object without
exposing the creation logic to client and the client use the same common interface to create new type of object.
The idea is to use a static member-function (static factory method) which creates & returns instances, hiding the details of 
class modules from user.

A factory pattern is one of the core design principles to create an object, allowing clients to create objects of a 
library in a way such that it doesn’t have tight coupling with the class hierarchy of the library.



3.Prototype 

Prototype pattern is one of the creational pattern refers to creating duplicate object while keeping performance in mind.

It implementing a prototype interface which tells to create a clone of the current object. This pattern is used when creation
of object directly is costly. For example, an object is to be created after a costly database operation. We can cache the 
object, returns its clone on next request and update the database as and when needed thus reducing database calls.
