# Creational Design Patterns

These design patterns are all about class instantiation or object creation. These patterns can be further categorized into Class-creational patterns and object-creational patterns. While class-creation patterns use inheritance effectively in the instantiation process, object-creation patterns use delegation effectively to get the job done.
    
Creational design patterns are the Factory Method, Abstract Factory, Builder, Singleton, Object Pool, and Prototype.

Use case of creational design pattern -
1) For creating multiple instances of a class 

### More info on following patterns:

#### 1. Object Pool Design Pattern

Object pool pattern is a software creational design pattern which is used in situations where the cost of initializing a class
instance is very high.Basically, an Object pool is a container which contains some amount of objects. So, when an object is 
taken from the pool, it is not available in the pool until it is put back.
Objects in the pool have a lifecycle:

-Creation
-Validation
-Destroy.

#### 2. Factory Design Pattern

Factory method is a creational design pattern, i.e., related to object creation. In Factory pattern, we create object without
exposing the creation logic to client and the client use the same common interface to create new type of object.
The idea is to use a static member-function (static factory method) which creates & returns instances, hiding the details of 
class modules from user.

A factory pattern is one of the core design principles to create an object, allowing clients to create objects of a 
library in a way such that it doesn’t have tight coupling with the class hierarchy of the library.

#### 3.Prototype 

Prototype pattern is one of the creational pattern refers to creating duplicate object while keeping performance in mind.

It implementing a prototype interface which tells to create a clone of the current object. This pattern is used when creation
of object directly is costly. For example, an object is to be created after a costly database operation. We can cache the 
object, returns its clone on next request and update the database as and when needed thus reducing database calls.
