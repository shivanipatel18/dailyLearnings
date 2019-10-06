# Memory Management

Memory management is the process of allocation and de-allocation of objects to make space for those new object allocations. Java uses an automatic memory management system called a garbage collector. Thus, we are not required to implement memory management logic in our application. Java memory management divides into two major parts:

- JVM Memory Structure
- Working of the Garbage Collector

### JVM Memory Structure
JVM memory is divided into multiple parts: Heap Memory, Non-Heap Memory, and Other.

##### Heap memory
Heap memory is the run time data area from which the memory for all java class instances and arrays is allocated. The heap is created when the JVM starts up and may increase or decrease in size while the application runs. The size of the heap can be specified using –Xms VM option. The heap can be of fixed size or variable size depending on the garbage collection strategy. Maximum heap size can be set using –Xmx option. By default, the maximum heap size is set to 64 MB.

##### Non-Heap memory
The JVM has memory other than the heap, referred to as Non-Heap Memory. It is created at the JVM startup and stores per-class structures such as runtime constant pool, field and method data, and the code for methods and constructors, as well as interned Strings. The default maximum size of non-heap memory is 64 MB. This can be changed using –XX:MaxPermSize VM option.

##### Other memory
JVM uses this space to store the JVM code itself, JVM internal structures, loaded profiler agent code and data, etc.

### Working of Garbage Collector

When a program executes in Java, it uses memory in different ways. The heap is a part of memory where objects live. It's the only part of memory that involved in the garbage collection process. It is also known as garbage collectible heap. All the garbage collection makes sure that the heap has as much free space as possible. The function of the garbage collector is to find and delete the objects that cannot be reached.

##### What does Java Garbage Collector?
JVM controls the garbage collector. JVM decides when to perform the garbage collection. We can also request to the JVM to run the garbage collector. But there is no guarantee under any conditions that the JVM will comply. JVM runs the garbage collector if it senses that memory is running low. When Java program request for the garbage collector, the JVM usually grants the request in short order. It does not make sure that the requests accept.

Every Java program has more than one thread. Each thread has its execution stack. There is a thread to run in Java program that is a main() method. Now we can say that an object is eligible for garbage collection when no live thread can access it. The garbage collector considers that object as eligible for deletion. If a program has a reference variable that refers to an object, that reference variable available to live thread, this object is called reachable.

### Types of Garbage Collection
There are five types of garbage collection are as follows:

- Serial GC: It uses the mark and sweeps approach for young and old generations, which is minor and major GC.
- Parallel GC: It is similar to serial GC except that, it spawns N (the number of CPU cores in the system) threads for young generation garbage collection.
- Parallel Old GC: It is similar to parallel GC, except that it uses multiple threads for both generations.
- Concurrent Mark Sweep (CMS) Collector: It does the garbage collection for the old generation. You can limit the number of threads in CMS collector using XX:ParalleCMSThreads=JVM option. It is also known as Concurrent Low Pause Collector.
- G1 Garbage Collector: It introduced in Java 7. Its objective is to replace the CMS collector. It is a parallel, concurrent, and CMS collector. There is no young and old generation space. It divides the heap into several equal sized heaps. It first collects the regions with lesser live data.


##### Mark and Sweep Algorithm
JRockit JVM uses the mark, and sweep algorithm for performing the garbage collection. It contains two phases, the mark phase, and the sweep phase.

- Mark Phase: Objects that are accessible from the threads, native handles, and other GC root sources are marked as live. Every object tree has more than one root objects. GC root is always reachable. So any object that has a garbage collection root at its root. It identifies and marks all objects that are in use, and the remaining can be considered garbage.

- Sweep Phase: In this phase, the heap is traversed to find the gap between the live objects. These gaps are recorded in the free list and are available for new object allocation.

There are two improved versions of mark and sweep:
- Concurrent Mark and Sweep
- Parallel Mark and Sweep


##### Concurrent Mark and Sweep
It allows the threads to continue running during a large portion of the garbage collection. There are following types of marking:

- Initial marking: It identifies the root set of live objects. It is done while threads are paused.
Concurrent marking: In this marking, the reference from the root set are followed. It finds and marks the rest of the live objects in a heap. It is done while the thread is running.
- Pre-cleaning marking: It identifies the changes made by concurrent marking. Other live objects marked and found. It is done while the threads are running.
- Final marking: It identifies the changes made by pre-cleaning marking. Other live objects marked and found. It is done while threads are paused.

##### Parallel Mark and Sweep
It uses all available CPU in the system for performing the garbage collection as fast as possible. It is also called the parallel garbage collector. Threads do not execute when the parallel garbage collection executes.

- Pros of Mark and Sweep
1. It is a recurring process.\
2. It is an infinite loop.\
3. No additional overheads allowed during the execution of an algorithm.

- Cons of Mark and Sweep
1. It stops the normal program execution while the garbage collection algorithm runs.
2. It runs multiple times on a program.
