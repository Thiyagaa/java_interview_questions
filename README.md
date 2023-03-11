## Java Interview Questions


|No.  |Topic  |
|---------|---------|
|1     |  [JVM](#jvm-architecture--core)       |
|2     |         |
|3     |         |
|4     |         |
|5     |         |
|6     |         |
|7     |         |
|8     |         |
|9     |         |
|10     |         |

## JVM Architecture & Core

### Q. What is a JVM, and how does it work?

![JVM Architecture](./images/jvm/1662305841379.png)

Credits: [LinkedIn](https://www.linkedin.com/pulse/jvm-architecture-how-internally-work-ali-as-ad/)

### Q. What are the different components of the JVM?

JVM is generally categorized based on the functionality into the below three components.
>
    ClassLoader
    Runtime Data Area (Memory Area)
    Execution Engine 

### Q. What is a class loader, and how does it work?

A class loader is a component of the Java Virtual Machine (JVM) that loads Java classes into memory at runtime. The JVM uses a hierarchical class loader system to load classes from different sources, such as the local file system or remote servers.

The class loader is responsible for three key tasks:

**Loading**:
The class loader is responsible for locating the bytecode of a class and reading it into memory. It searches for the bytecode in the classpath, which is a list of directories and JAR files where Java classes are stored. If the class has already been loaded, the class loader will simply return the existing class object.

**Linking**: After a class has been loaded, it goes through a linking process that includes three stages: verification, preparation, and resolution. Verification checks that the bytecode is valid and does not violate the Java security model. Preparation allocates memory for static fields and initializes them to default values. Resolution replaces symbolic references with direct references to other classes or methods.

**Initialization**: Finally, the class loader is responsible for initializing the class by executing its static initializer block, which is a block of code that initializes static fields or performs other initialization tasks.

### Q. What are the different class loader?

There are three types of class loaders in Java:

**Bootstrap Class Loader**: It is responsible for loading core Java classes from the \lib\rt.jar file located in the JDK installation directory. It is the parent of all class loaders and is implemented in native code.

**Extension Class Loader**: It is responsible for loading classes from the extensions directory (usually located at jre/lib/ext). It is a child of the Bootstrap Class Loader and is implemented in Java code.

**Application Class Loader**: It is responsible for loading classes from the application classpath. It is a child of the Extension Class Loader and is implemented in Java code.

When a class is requested, the class loader searches for it in its local cache. If the class is not found, it delegates the task to its parent class loader. This process continues until the class is found or the Bootstrap Class Loader is reached.

If none of the class loaders can find the class, a ClassNotFoundException is thrown. Class loaders can also be used to load classes from other sources, such as network locations or databases, by creating custom class loaders.

Class loaders in Java use a delegation model to load classes. Each class loader delegates the task of loading classes to its parent class loader. This ensures that classes are loaded in a hierarchical manner, with higher-level class loaders responsible for loading classes with greater visibility.


### Q. How does garbage collection work in the JVM, and what are the different types of garbage collectors?

### Q. What is bytecode, and how is it executed in the JVM?

### Q. How does the JVM handle multi-threading and concurrency?

### Q. What is the PermGen space, and how is it different from the Metaspace?

### Q. What are the different types of memory areas in the JVM, and how are they used?

### Q. What is Just-In-Time (JIT) compilation, and how does it work in the JVM?

### Q. What is the purpose of the JVM's runtime data area, and what are some of the data structures used within it?

### Q. How does the JVM handle method dispatch (i.e., how does it determine which method to call when a method is invoked)?

### Q. What is the purpose of the Class file format, and how is it structured?

### Q. What are some of the performance tuning options available in the JVM, and how do they work?

### Q. How does the JVM handle exceptions, and what is the role of the exception table?

### Q. What is the purpose of the JIT code cache, and how does it affect performance?

### Q. How does the JVM handle dynamic class loading and unloading?

### Q. What is the difference between a native method and a regular Java method, and how does the JVM handle them differently?

### Q. What is the difference between a static method and an instance method, and how does the JVM handle them differently?

### Q. What is the purpose of the Java Native Interface (JNI), and how is it used in the JVM?

### Q. What is the difference between a value type and a reference type, and how does the JVM handle them differently?

### Q. How does the JVM handle object instantiation, and what is the purpose of the object header?

### Q. What is the difference between static and dynamic linking, and how does the JVM handle both?

### Q. What is the purpose of the Java Instrumentation API, and how is it used in the JVM?
