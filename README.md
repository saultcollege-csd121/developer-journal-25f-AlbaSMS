# CSD121 Developer Journal

Always use clear and *meaningful names, comments, and JavaDoc.*

Always *test* the program and use the debugger to fix errors.

Always remember to *declare* the type of variables, otherwise it will get an error.

Use break to end loops, you can use if statements in order to quit when the condittional has been executed.

readln won't read integers, remember to parse them before hand.

Use **try/catch** to handle errors without the programm crashing.

In order to use theWholeFile to write a file, first convert the ArrayList into a List<String>.

When wanting to write a file with StandardOpenOption.WRITE, also use StandardOpenOption.CREATE. If not, it won't work.

Be sure to use *variables in scope*, if not, it will appear as it is not declared.

**Mutator methods** change the state of the object.

**Accessor methods** refer to instance variables but do not change them.

An **object** is an instance of its class.

**Constants** use ALL_CAPS, **variables** and **methods** start with lowercase, and types (like **classes**) start with uppercase.

**new** Type() creates an object; "Type" accesses class members, while "**var**" accesses instance members.

A "**function**" associetad with a class or instance is a method, if it's not associetad with anything, it is just a function.

**Class methods** belong to the class itself, while instance methods act on a specific object.

*Constants* are fixed values defined by classes.

**Enumerations**: Used to list a small set of fixed choices a value can have.

**Records**: Used to group several related pieces of information together.

Separate logic from input/output. The core logic class shouldn’t handle user input or printing, keep that in the UI shell.

**Keep core classes pure.**

Each class should do one job.

**Enums** prevent invalid data.

Making members private prevents unwanted changes from other classes.

Always give clear error messages to make sure the user knows what was wrong and how to fix it.

Software testing is running software or software components in specific ways to verify that it works as expected. We should test early and often!

Writing **automated tests** helps ensure program correctness.

Each test should clearly state: *Expected output, actual output, and make a visual distinction between 'passed' and 'failed' states.*

Write tests that verify that valid inputs produce valid outputs, but also, think about how your code could break or go wrong. Write tests that attempt to trigger those circumstances, and verify that your code handles them appropriately.

Test each instance method just like testing class methods. Should *test constructors too*.


**November 11th (Lecture 5)**

Create software components that: are **cohesive**, are **loosely coupled with other components**, and have a **single responsibility**.

Place repeated implementations of the same task into **reusable functions**. 

**Cohesion** is the degree to which the parts of one component are related to each other.

**Coupling** is the degree to which different components depend on each other. How much do different components need to 'know' about each other to function?

**Polymorphism** is the enabling of uniform interaction for different types.

**Subtype polymorphism** occurs when subtype values are allowed to be treated as values of a supertype. This is what is usually meant by 'polymorphism' with respect to OOP.

**Generalization**: It can be useful to analyze the ‘things’ being modelled (types / data structures) in a program for common state or behaviour. Reduces code repetition (DRY). Can make programs more maintainable. Sharing common details in a broader abstraction. An encapsulation of common implementation details in a shared superclass. Superclasses are abstractions of all their subclasses.

Using the ‘**extends**’ keyword, we can make ‘subclasses’ of the superclass. Subclasses ‘inherit’ all non-private members of their superclasses, so only the members specific to the subclasses need to be defined in the subclasses.

**Superclass**: A class that defines members that are common among several subclasses.

**Subclass**: A class that defines members that are common among several subclasses.

**Inherit**: A class that inherits another class’s members has all the latter’s variables and methods.

**Inheritance/class hierarchy**: A set of classes that are all connected as superclasses or subclasses of each other.

**Abstraction**: Focusing essential detail; ignoring irrelevant complexity.

**Encapsulation**: Exposing an abstraction; hiding implementation detail. Public members usually constitute the abstraction.

Java classes may have *ONLY ONE* superclass. Specified using the extends keyword. If not specified, then Object is the superclass.

The **protected visibility** modifier can be used to make members accessible from inside subclass code.

A **protected member** will be accessible even in subclasses multiple steps down an inheritance hierarchy.

Constructors in an inheritance hierarchy are called in sequence from the base superclass down to the subclass being instantiated.

The **super** keyword can be used to call a constructor of the superclass. Must be the FIRST statement in a constructor.

If the superclass of a class has a default constructor, *the call to super is automatic.*

**Overriding**: In a subclass, providing a specialized implementation of a superclass method. An  override method must have the SAME SIGNATURE as the method being overridden.

**Overloading**: In one class, providing multiple signatures for one method name. An overload method must have a DIFFERENT SIGNATURE than all other same-named methods in the class.

**Dynamic method** dispatch allows for subtype polymorphism (allowing subtype values to be treated as supertype instances)

**Subtype Polymorphism** complements generalization in that it allows the programmer to: Use more the more general (simpler, more abstract) interface of a superclass, while still getting the specialized behaviour of subclasses at run-time

An abstract class is intended to be extended by subclasses and cannot be directly instantiated. *Abstract classes may define abstract methods.*

**Software component** should be: ***Open for extension***, and ***closed for modification.***

**Liskov substitution principle**: Any subtype should be usable in place of a supertype without changing the behaviour of the program. *Violations of this principle increase coupling.*


**November 20th (Lecture 6)**

**Classes** define both behaviour (methods) AND state (variables).

**Superclasses** classes may define both behaviour AND state.

**Subclasses** inherit the behaviour AND state of their superclasses.

An **interface** can be used to define the common behaviour that all these different alert classes must share.

A class that implements an interface **MUST** *implement all methods defined by the interface.*

**Single Responsibility** Each interface should have a single, clear purpose

**Interface Segregation** All classes that implement an interface should need all interface methods

**Dependency Inversion** Depend on broader abstractions (interfaces) rather than specific types

Adhering to the **Interface segregation principle** *increases coherence and loosens coupling.*

If **NOT ALL** implementers need **ALL the methods** of the interface, *break the interface into smaller interfaces.*

**High-level components** should not depend on low-level components. Instead, both should depend on abstractions.

**Abstractions** should not depend on details. Instead, details should depend on abstractions.

Adhering to the **Dependency inversion principle** loosens coupling.

**Dependency Injection** refers to the practice of injecting rather than directly instantiating dependencies into software components.

**The Strategy Design Pattern:** Create a class for each approach (strategy) that implements a common interface through which the component interacts.

**The Observer Design Pattern:** A class representing the subject keeps a list of observers (via an interface); when the change occurs, the subject notifies all observers via the interface method.


**November 25th**

Every **JavaFX** app starts with a class that:

1. Extends the JavaFX **Application** class

2. Overrides the **start** method

The main method calls Application.launch(). Once JavaFX platform is ready, your class’s start method is called with a Stage object as an argument.

The **Stage:** Represents the root window of an app. Usually has window decorations. Operating system determines appearance of decorations. The Stage usually contains a Scene.

The **Scene** Class: Consists of a scene graph. A tree of Node objects, each node has 1 parent (except the root node). Each node may have 0 or more children.

An **event handler** class may be used to provide behaviour in response to specific events.

**EventHandler** is an interface that defines a single method: *handle.* The handle method is passed an Event object that represents information about the specific event that occurred. *Event is the most abstract of a hierarchy of Event classes.*


**November 27th**

**Controls:** UI element that can be manipulated by the user. Another class hierarchy. Extend the javafx.scene.controls.Control class.


**December 2nd (Lecture 7)**

A **functional interface** is ANY interface with only one abstract (non-default) method.

The optional **@FunctionalInterface** annotation can be used to enable compile-time warnings if an interface is not in fact functional.

Functional interfaces can be implemented *without writing a full class.* As version 8, Java supports **lambda expressions** as a concise way to implement a functional interface.

The arrow separates the parameter list from the function body. If the body of the function is just a single return statement, you only need the returned expression to the right of the arrow. If the body of the function is just a *single return statement*, you only need the returned expression to the right of the arrow. If the function has only a *single parameter*, you don't even need the parentheses around the parameter list.

Anywhere a functional interface is expected, *a lambda expression may be used instead.*

The **:: operator** before a method name turns this into a function REFERENCE.

A **function reference** may be used anywhere that a *function interface is expected.*

a function reference may be used anywhere that a function interface is expected.

An **anonymous inner** class is a one-time, unnamed implementation of an interface that is usually immediately instantiated.

The syntax where a code block comes immediately after a 'new' expression creates an anonymous class that *extends/implements the type that was just 'newed'.*

Lambda expressions and function references are *automatically converted to their equivalent anonymous inner class.*

Java's **Stream interface** provides a number operations that can be performed on Collection objects. Access a collection's stream using the **stream()** method

Many operations in the stream interface return a Stream. These operations can thus be **chained**, *one after the next.*

Many operations in the stream interface do **NOT** return a Stream. These operations can **NOT be chained** and are thus typically the *final method call in a stream operation*
