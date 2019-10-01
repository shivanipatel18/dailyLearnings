# Singleton Class

A singleton class is a class that can have only one object (an instance of the class) at a time. The Singleton's purpose is to control object creation, limiting the number of objects to only one. Since there is only one Singleton instance, any instance fields of a Singleton will occur only once per class, just like static fields.

Singleton class 
```
// File Name: Singleton.java
public class Singleton {

   private static Singleton singleton = new Singleton( );

   /* A private Constructor prevents any other
    * class from instantiating.
    */
   private Singleton() { }

   /* Static 'instance' method */
   public static Singleton getInstance( ) {
      return singleton;
   }

   /* Other methods protected by singleton-ness */
   protected static void demoMethod( ) {
      System.out.println("demoMethod for singleton");
   }
}
```

Main program file where we will create a singleton object :−

```
// File Name: SingletonDemo.java
public class SingletonDemo {

   public static void main(String[] args) {
      Singleton tmp = Singleton.getInstance( );
      tmp.demoMethod( );
   }
}
```

#### Pros of Singleton

###### Instance control:
Singleton prevents other objects from instantiating their own copies of the Singleton object, ensuring that all objects access the single instance.

##### Flexibility: 
Since the class controls the instantiation process, the class has the flexibility to change the instantiation process.

##### Easy to implement: 
Easy to create and we could use it anywhere for the lifetime of the app The advantage of Singleton over global variables is that you are absolutely sure of the number of instances when you use Singleton. However, you can still change your mind and manage any number of instances. Having a very versatile design pattern that can work well for many different applications and processes.

#### Cons of Singleton

- They are a global mutable shared state. Their state is automatically shared across the entire app, and bugs can often start occurring when that state changes unexpectedly. The disadvantages of Singleton over a global mutable shared state can give you a real headache if the state changes unexpectedly and also keep your code tightly coupled. It will make difficult to test when your code is not loosely coupled so it will cause a lot problems to maintain.

- The relationships between Singletons and the code that depends on them is usually not very well defined. Since Singletons are so convenient and easy to access.

- Managing their life-cycle can be tricky. Since Singletons are alive during the entire lifespan of an application, managing them can be really hard, and they usually have to rely on optionals to keep track of values. This also makes code that relies on Singletons really hard to test, since you can’t easily start from a “clean slate” in each test case.
