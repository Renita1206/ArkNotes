# Java
- Java is an Object Oriented Programming language
- Java is platform-independent because it uses a virtual machine. The Java programming language and all APIs are compiled into bytecodes. Bytecodes are effectively platform-independent. The virtual machine takes care of the differences between the bytecodes for the different platforms. 
- Java supports primitive data types - byte, boolean, char, short, int, float, long, and double and hence it is not a pure object oriented language.


## Heap and Stack Memory
Stack memory is the portion of memory that was assigned to every individual program. And it was fixed. On the other hand, Heap memory is the portion that was not allocated to the java program but it will be available for use by the java program when it is required, mostly during the runtime of the program.
When we write a java program then all the variables, methods, etc are stored in the stack memory. And when we create any object in the java program then that object was created in the heap memory. And it was referenced from the stack memory.

## Java vs Cpp
- C++ is only a  compiled language, whereas Java is compiled as well as an interpreted language.
- Java programs are machine-independent whereas a c++ program can run only in the machine in which it is compiled. 
- C++ allows users to use pointers in the program. Whereas java doesn’t allow it. Java internally uses pointers. 
- C++ supports the concept of Multiple inheritances whereas Java doesn't support this. And it is due to avoiding the complexity of name ambiguity that causes the diamond problem.


## Java Compilation
First, the Java source code (.java) conversion to byte code (.class) occurs with the help of the javac compiler.
Then, the .class files are loaded at run time by JVM and with the help of an interpreter, these are converted to machine understandable code.
### Java Virtual Machine (JVM)
- Provides a runtime environment where Java Byte Code can be executed
- Platform Dependent
- Loads, verifies and executes code
### Java Runtime Environment (JRE)
- Produces environment to run java application
- Consists of JVM, core classes and supporting files
- Java Classloader is the program that belongs to JRE (Java Runtime Environment). The task of ClassLoader is to load the required classes and interfaces to the JVM when required. 
### Java Development Kit (JDK)
- Includes JRE, loader, compiler, archiver and other tools for java dev

## Infinite Loop
```
// Using For Loop:
for (;;)
{
   // Business logic
   // Any break logic
}
// Using while loop:
while(true){
   // Business logic
   // Any break logic
}
// Using do-while loop:
do{
   // Business logic
   // Any break logic
}while(true);
```


##  Main Method
- The main method is always static because static members are those methods that belong to the classes, not to an individual object. So if the main method will not be static then for every object, It is available. And that is not acceptable by JVM. JVM calls the main method based on the class name itself. Not by creating the object.Because there must be only 1 main method in the java program as the execution starts from the main method. So for this reason the main method is static. 
- We can create as many overloaded main methods we want. However, JVM has a predefined calling method that JVM will only call the main method with the definition of - 
```
public static void main(string[] args)
```

## Final
In Java, the final keyword is used as defining something as constant /final and represents the non-access modifier.
- final variable: When a variable is declared as final in Java, the value can’t be modified once it has been assigned.
If any value has not been assigned to that variable, then it can be assigned only by the constructor of the class.
- final method: A method declared as final cannot be overridden by its children's classes.
A constructor cannot be marked as final because whenever a class is inherited, the constructors are not inherited. Hence, marking it final doesn't make sense. Java throws compilation error saying - modifier final not allowed here
- final class: No classes can be inherited from the class declared as final. But that final class can extend other classes for its usage.
  
## Final, Finally and Finalize
-  Final: If any restriction is required for classes, variables, or methods, the final keyword comes in handy. Inheritance of a final class and overriding of a final method is restricted by the use of the final keyword. The variable value becomes fixed after incorporating the final keyword. Example:
- Finally: It is the block present in a program where all the codes written inside it get executed irrespective of handling of exceptions. It is always executed (unless System,exit())
- Finalize: Prior to the garbage collection of an object, the finalize method is called so that the clean-up activity is implemented. 

## Super
The super keyword is used to access hidden fields and overridden methods or attributes of the parent class.
- Accessing data members of parent class when the member names of the class and its child subclasses are same.
- To call the default and parameterized constructor of the parent class inside the child class.
- Accessing the parent class methods when the child classes have overridden them.

## Static
- Static Methods and Static variables are those methods and variables that belong to the class of the java program, not to the object of the class. This gets memory where the class is loaded. And these can directly be called with the help of class names.
- Static classes - A class in the java program cannot be static except if it is the inner class. If it is an inner static class, then it exactly works like other static members of the class.
- Static methods cannot be overridden as overriding is a dynamic functionality

## Shallow vs Deep Copy
Shallow copy - The shallow copy only creates a new reference and points to the same object.
```Rectangle obj2 = obj1;```
Now by doing this what will happen is the new reference is created with the name obj2 and that will point to the same memory location.

Deep Copy - In a deep copy, we create a new object and copy the old object value to the new object. Example -
```
Rectangle obj3 = new Rectangle();
Obj3.length = obj1.length;
Obj3.breadth = obj1.breadth;
```

## String, StringBuffer, and a StringBuilder
Storage area: In string, the String pool serves as the storage area. For StringBuilder and StringBuffer, heap memory is the storage area.
Mutability: A String is immutable, whereas both the StringBuilder and StringBuffer are mutable.
Efficiency: It is quite slow to work with a String. However, StringBuilder is the fastest in performing operations. The speed of a StringBuffer is more than a String and less than a StringBuilder. (For example appending a character is fastest in StringBuilder and very slow in String because a new memory is required for the new String with appended character.)
Thread-safe: In the case of a threaded environment, StringBuilder and StringBuffer are used whereas a String is not used. However, StringBuilder is suitable for an environment with a single thread, and a StringBuffer is suitable for multiple threads.
Syntax:
```
// String
String first = "InterviewBit";
String second = new String("InterviewBit");
// StringBuffer
StringBuffer third = new StringBuffer("InterviewBit");
// StringBuilder
StringBuilder fourth = new StringBuilder("InterviewBit");
```

## Java Comparator
Consider the example where we have an ArrayList of employees like( EId, Ename, Salary), etc. Now if we want to sort this list of employees based on the names of employees. Then that is not possible to sort using the Collections.sort() method. We need to provide something to the sort() function depending on what values we have to perform sorting. Then in that case a comparator is used.

Comparator is the interface in java that contains the compare method. And by overloading the compare method, we can define that on what basis we need to compare the values. 

## Pass by value
Java always works as a “pass by value”. There is nothing called a “pass by reference” in Java. However, when the object is passed in any method, the address of the value is passed due to the nature of object handling in Java. When an object is passed, a copy of the reference is created by Java and that is passed to the method. The objects point to the same memory location. 


## Type Conversion
There are two types of conversion - 
    - Implicit - Done by system(also called widening/automatic/type promotion), no data loss
    - Explicit - Done by programmer to change type into desirable type (also called narrowing), might throw error*
        ```
        b = (int)(b * 2);
        ```  
* So, for example, typecasting an Integer to a String (String is not a subclass of Integer) results in a ClassCastException exception. Another possible exception is the ClassNotFoundException.
<a href="https://www.geeksforgeeks.org/type-conversion-java-examples/"> GFG article </a>

## Int Min and Max values
```
int a  = Integer.MAX_VALUE;
int b  = Integer.MIN_VALUE;
```
The range of int is ->  -2,147,483,647 to 2,147,483,647 [or -2^31 to 2^31-1]

## For-each loop / Enhanced for loop
```
// Loop prints out every element in int array arr
for(int i : arr)
    System.out.println(i); 
```
