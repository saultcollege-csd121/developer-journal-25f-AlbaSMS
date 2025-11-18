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
