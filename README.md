# CSD121 Developer Journal

Always use clear and meaningful names, comments, and JavaDoc.

Always test the program and use the debugger to fix errors.

Always remember to declare the type of variables, otherwise it will get an error.

Use break to end loops, you can use if statements in order to quit when the condittional has been executed.

readln won't read integers, remember to parse them before hand.

Use try/catch to handle errors without the programm crashing.

In order to use theWholeFile to write a file, first convert the ArrayList into a List<String>.

When wanting to write a file with StandardOpenOption.WRITE, also use StandardOpenOption.CREATE. If not, it won't work.

Be sure to use variables in scope, if not, it will appear as it is not declared.

Mutator methods change the state of the object.

Accessor methods refer to instance variables but do not change them.

An object is an instance of its class.

Constants use ALL_CAPS, variables and methods start with lowercase, and types (like classes) start with uppercase.

new Type() creates an object; "Type" accesses class members, while "var" accesses instance members.

A "function" associetad with a class or instance is a method, if it's not associetad with anything, it is just a function.

Class methods belong to the class itself, while instance methods act on a specific object.

Constants are fixed values defined by classes.

Enumerations: Used to list a small set of fixed choices a value can have.

Records: Used to group several related pieces of information together.

Separate logic from input/output. The core logic class shouldn’t handle user input or printing, keep that in the UI shell.

Keep core classes pure.

Each class should do one job

Enums prevent invalid data.

Making members private prevents unwanted changes from other classes.

Always give clear error messages to make sure the user knows what was wrong and how to fix it.

Software testing is running software or software components in specific ways to verify that it works as expected. We should test early and often!

Writing automated tests helps ensure program correctness.

Each test should clearly state: Expected output, actual output, and make a visual distinction between 'passed' and 'failed' states.

Write tests that verify that valid inputs produce valid outputs, but also, think about how your code could break or go wrong. Write tests that attempt to trigger those circumstances, and verify that your code handles them appropriately.

Test each instance method just like testing class methods. Should test constructors too!
