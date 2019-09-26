### Generics 

Generics in Java is similar to templates in C++. The idea is to allow type (Integer, String, … etc and user defined types) to 
be a parameter to methods, classes and interfaces. For example, classes like HashSet, ArrayList, HashMap, etc use generics very well. We can use them for any type.

### Generic Class

Like C++, we use <> to specify parameter types in generic class creation. 

```
// A Simple Java program to show working of user defined 
// Generic classes 
   
// We use < > to specify Parameter type 
class GenericExample<T> 
{ 
    // An object of type T is declared 
    T obj; 
    GenericExample(T obj) {  this.obj = obj;  }  // constructor 
    public T getObject()  { return this.obj; } 
} 

class Main 
{ 
    public static void main (String[] args) 
    { 
        // instance of Integer type 
        GenericExample <Integer> iObj = new GenericExample<Integer>(2003); 
        System.out.println(iObj.getObject()); 
   
        // instance of String type 
        GenericExample <String> sObj =  new GenericExample<String>("Softway"); 
        System.out.println(sObj.getObject()); 
    } 
}
```

### Generic Functions:-

We can also write generic functions that can be called with different types of arguments based on the type of arguments passed 
to generic method, the compiler handles each method.
```
// A Simple Java program to show working of user defined 
// Generic functions 
   
class GenericExample 
{ 
    // A Generic method example 
    static <T> void print(T element)
    { 
        System.out.println(element.getClass().getName() + " = " + element); 
    } 
   
    public static void main(String[] args) 
    { 
         // Calling generic method with Integer argument 
        print(11); 
   
        // Calling generic method with String argument 
        print("GeeksForGeeks"); 
   
        // Calling generic method with double argument 
        print(1.0); 
    } 
}
```
