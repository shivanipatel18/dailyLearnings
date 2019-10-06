# Structural Design Patterns 

These design patterns are about organizing different classes and objects to form larger structures and provide new functionality. Structural design patterns are Adapter, Bridge, Composite, Decorator, Facade, Flyweight, Private Class Data, and Proxy.

Use Case Of Structural Design Pattern-

When 2 interfaces are not compatible with each other and want to make establish a relationship between them through an adapter its called adapter design pattern. Adapter pattern converts the interface of a class into another interface or classes the client expects that is adapter lets classes works together that could not otherwise because of incompatibility. so in these type of incompatible scenarios, we can go for the adapter pattern.

#### More info on following patterns:

##### 1. Flyweight:-

This pattern provides ways to decrease object count thus improving application required objects structure. Flyweight pattern is used when we need to create a large number of similar objects (say 105). One important feature of flyweight objects is that they are immutable. This means that they cannot be modified once they have been constructed.

Why do we care for number of objects in our program?

Less number of objects reduces the memory usage, and it manages to keep us away from errors related to memory like java.lang.OutOfMemoryError.
Although creating an object in Java is really fast, we can still reduce the execution time of our program by sharing objects.

In this pattern we use a HashMap that stores reference to the object which have already been created, every object is associated with a key. When you wants to create an object, simply has to pass a key associated with it and if the object has already been created we simply get the reference to that object else it creates a new object and then returns the reference of object.

##### 2. Private Class Data:-

The private class data design pattern seeks to reduce exposure of attributes by limiting their visibility.

It reduces the number of class attributes by encapsulating them in single Data object. It allows the class designer to remove write privilege of attributes that are intended to be set only during construction, even from methods of the target class.

##### 3. Proxy:-

In proxy pattern, a class represents functionality of another class. We create object having original object to interface its functionality to outer world.

