# Object Oriented Programming
Object-Oriented Programming, or OOPs, is a programming paradigm that implements the concept of objects in the program. It aims to provide an easier solution to real-world problems by implementing real-world entities such as inheritance, abstraction, polymorphism, etc. in programming. OOPs concept is widely used in many popular languages like Java, Python, C++, etc.   
  
Objects can be considered as real-world instances of entities like class, that contain some characteristics and behaviors specified in the class template. In simple language, a class can be considered as the blueprint or template, based on which objects can be created. So the Objects are considered the instance of a class, and are therefore sometimes called “instances”. The term “characteristics” refers to the “what” about the Object, and the term “behavior” refers to the “how” about the Object.  

The concept of “objects” allows the OOPs model to easily access, use and modify the instance data and methods, interact with other objects, and define methods in runtime (during the execution of the program). This gives the OOPs model significance and makes it diverse in its implementation.


## Alternate Programming Paradigms
Programming paradigms refers to the method of classification of programming languages based on their features. There are mainly two types of Programming Paradigms:
- Imperative Programming Paradigm - Imperative programming focuses on HOW to execute program logic and defines control flow as statements that change a program state. This can be further classified as:
    - Procedural Programming Paradigm: Procedural programming specifies the steps a program must take to reach the desired state, usually read in order from top to bottom.
    - Object-Oriented Programming or OOP: Object-oriented programming (OOP) organizes programs as objects, that contain some data and have some behavior.
    - Parallel Programming: Parallel programming paradigm breaks a task into subtasks and focuses on executing them simultaneously at the same time.
- Declarative Programming Paradigm - Declarative programming focuses on WHAT to execute and defines program logic, but not a detailed control flow. Declarative paradigm can be further classified into:
    - Logical Programming Paradigm: Logical programming paradigm is based on formal logic, which refers to a set of sentences expressing facts and rules about how to solve a problem
    - Functional Programming Paradigm: Functional programming is a programming paradigm where programs are constructed by applying and composing functions.
    - Database Programming Paradigm: Database programming model is used to manage data and information structured as fields, records, and files.


## Features of OOPs
- Encapsulation
    - Binding of data and methods into a single unit
    - Java classes are example of encapsulation
- Abstraction
    - Show only necessary information
    - Abstraction is achieved using interfaces or abstract classes
- Inheritance
    - One class is allowed to inherit the features(fields and methods) of another class. In Java, Inheritance means creating new classes based on existing ones. A class that inherits from another class can reuse the methods and fields of that class.
    - Allows code reusability
    - Types of inheritance are - single level, multilevel, hierarchy, hybrid
    - Super/Base/Parent Class: The class whose features are inherited is known as a superclass(or a base class or a parent class).
    - Sub/Derived/Child Class: The class that inherits the other class is known as a subclass(or a derived class, extended class, or child class). The subclass can add its own fields and methods in addition to the superclass fields and methods.
    - Java does not support multiple inheritance
    - extends keyword is used
- Polymorphism
    - Code behaves differently in different situations or contexts
    - Compile - time/static -> Method overloading
    - Run - time / Dynamic -> Method overriding


## Advantages of OOP
- OOPs is very helpful in solving very complex level of problems.
- Highly complex programs can be created, handled, and maintained easily using object-oriented programming.
- OOPs, promote code reuse, thereby reducing redundancy.
- OOPs also helps to hide the unnecessary details with the help of Data Abstraction.
- OOPs, are based on a bottom-up approach, unlike the Structural programming paradigm, which uses a top-down approach.
- Polymorphism offers a lot of flexibility in OOPs.

## Classes and Objects
- Class - A user-defined datatype that contains data members and member functions. A class is a blueprint of objects having common properties and methods
- Objects - Objects are instances of class. They have certain properties and methods.
- Classes do not consume any memory. They are just a blueprint based on which objects are created. Now when objects are created, they actually initialize the class members and methods and therefore consume memory.
- An object is necessary to be created if the base class has non-static methods. But if the class has static methods, then objects don’t need to be created. You can call the class method directly in this case, using the class name.
- Instance variables are those variables that are accessible by all the methods in the class. They are declared outside the methods and inside the class. These variables describe the properties of an object and remain bound to it at any cost.

## Constructors
Constructors are special methods whose name is the same as the class name. The constructors serve the special purpose of initializing the objects.
The different types of constructors are - 
- Default - The default constructor is the constructor which doesn’t take any argument. It has no parameters.
- Parameterized constructor -  The constructors that take some arguments are known as parameterized constructors.
- Copy constructor -  A copy constructor is a member function that initializes an object using another object of the same class. (Clones object)

## Destructors
Contrary to constructors, which initialize objects and specify space for them, Destructors are also special methods. But destructors free up the resources and memory occupied by an object. Destructors are automatically called when an object is being destroyed. A destructor cannot be overloaded.

## Interfaces
- Interfaces consists of only abstract methods
- No implementations, only method declarations
- Supports multiple inheritance
- Only static final variables
- When an interface is implemented, the subclass is required to specify all of the interface’s methods as well as their implementation.

## Abstract Classes
- An abstract class may have one or more abstract methods
- Does not support multiple inheritance
- When an abstract class is inherited, however, the subclass is not required to supply the definition of the abstract method until and unless the subclass actually uses it.

## Class vs Structure
Classes - keyword class is used, stored in heap memory, supports data abstraction
Structure - struct keyword, stored in stack memory, does not achieve data abstraction


## Limitations of Inheritance
Yes, with more powers comes more complications. Inheritance is a very powerful feature in OOPs, but it has some limitations too. Inheritance needs more time to process, as it needs to navigate through multiple classes for its implementation. Also, the classes involved in Inheritance - the base class and the child class, are very tightly coupled together. So if one needs to make some changes, they might need to do nested changes in both classes. Inheritance might be complex for implementation, as well. So if not correctly implemented, this might lead to unexpected errors or incorrect outputs.

## Access Specifiers
Access specifiers are special types of keywords that are used to specify or control the accessibility of entities like classes, methods, and so on. Private, Public, and Protected are examples of access specifiers or access modifiers.
- Default : When no access modifier is specified for a class, method, or data member – The data members, classes, or methods that are not declared using any access modifiers i.e. having default access modifiers are accessible only within the same package.
- Private : The private access modifier is specified using the keyword private. The methods or data members declared as private are accessible only within the class in which they are declared.
- Protected : The protected access modifier is specified using the keyword protected. The methods or data members declared as protected are accessible within the same package or subclasses in different packages.
- Public : The public access modifier is specified using the keyword public. Classes, methods, or data members that are declared as public are accessible from everywhere in the program. There is no restriction on the scope of public data members.

## Exception
An exception can be considered as a special event, which is raised during the execution of a program at runtime, that brings the execution to a halt. The reason for the exception is mainly due to a position in the program, where the user wants to do something for which the program is not specified, like undesirable input.

## Exception Handling
Exceptions are the major reason for software failure. The exceptions can be handled in the program beforehand and prevent the execution from stopping. This is known as exception handling. So exception handling is the mechanism for identifying the undesirable states that the program can reach and specifying the desirable outcomes of such states. Try-catch is the most common method used for handling exceptions in the program.

## Garbage Collection
Object-oriented programming revolves around entities like objects. Each object consumes memory and there can be multiple objects of a class. So if these objects and their memories are not handled properly, then it might lead to certain memory-related errors and the system might fail. Garbage collection refers to this mechanism of handling the memory in the program. Through garbage collection, the unwanted memory is freed up by removing the objects that are no longer needed.

## SOLID Principles
- Single Responsibility : Every Java class must perform a single functionality
- Open Closed Principle : The module should be open for extension but closed for modification.
- Liskov's Substitution : Derived classes must be completely substitutable for their base classes. In other words, if class A is a subtype of class B, then we should be able to replace B with A without interrupting the behavior of the program.
- Interface Segregation : The principle states that the larger interfaces split into smaller ones. Because the implementation classes use only the methods that are required. We should not force the client to use the methods that they do not want to use. Single responsibility for interfaces.
- Dependency Inversion : The principle states that we must use abstraction (abstract classes and interfaces) instead of concrete implementations. High-level modules should not depend on the low-level module but both should depend on the abstraction. Because the abstraction does not depend on detail but the detail depends on abstraction. It decouples the software.

## GRASP - General Responsibility Assignment Software Problems
- Creator - B should create A if
    - B contains or aggregates instances of A
    - B closely uses A
    - B has the inputs to construct A
- Controller - Overall system/root object (or use case based)
- Information Expert - Assign responsibility to that class which has adequate information to complete the task
- Pure Fabrication - Create a class that does not map to a domain object, and let it achieve this new responsibility in a cohesive way. To ensure low coupling and high cohesion
- High Cohesion - The principle of High cohesion encourages to focus classes around one responsibility, and to have all its components oriented towards achieving this responsibility. This is the principle of “do one thing and do it well”.
- Low Coupling - Coupling happens between two parts of the code when one depends on the other. Coupling introduces complexity, if only because the code can then no longer be understood isolation.
- Polymorphism
- Protected Variation - The principle of Protected variations is related to the one of Low coupling, because it helps reducing the impacts of the changes of the code of one part A on another part B. The code of part B is protected against the variations of the code of part A, hence the name of the pattern.
- Indirection - The Indirection pattern is another way to reduce coupling by creating an intermediary class (or any kind of component) between two classes A and B.