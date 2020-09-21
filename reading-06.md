## Java OO Tutorial
### Object
Bundling code into individual software objects provides a number of benefits, including:

1. Modularity: The source code for an object can be written and maintained independently of the source code for other objects. Once created, an object can be easily passed around inside the system.
1. Information-hiding: By interacting only with an object's methods, the details of its internal implementation remain hidden from the outside world.
1. Code re-use: If an object already exists (perhaps written by another software developer), you can use that object in your program. This allows specialists to implement/test/debug complex, task-specific objects, which you can then trust to run in your own code.
1. Pluggability and debugging ease: If a particular object turns out to be problematic, you can simply remove it from your application and plug in a different object as its replacement. This is analogous to fixing mechanical problems in the real world. If a bolt breaks, you replace it, not the entire machine.

You create an object from a class by using the new operator and a constructor. The new operator returns a reference to the object that was created. You can assign the reference to a variable or use it directly.

### Class
In the real world, you'll often find many individual objects all of the same kind. There may be thousands of other bicycles in existence, all of the same make and model. Each bicycle was built from the same set of blueprints and therefore contains the same components. In object-oriented terms, we say that your bicycle is an instance of the class of objects known as bicycles. A class is the blueprint from which individual objects are created.

A class declaration names the class and encloses the class body between braces. The class name can be preceded by modifiers. The class body contains fields, methods, and constructors for the class. A class uses fields to contain state information and uses methods to implement behavior. Constructors that initialize a new instance of a class use the name of the class and look like methods without a return type.

## Java Inheritance & Interfaces

### Interfaces

- Interfaces are contracts that spells out how their software interacts. Each group should be able to write their code without the knowledge of how the other groups code is written.
- Interface is a reference type similar to a class that can contain only constants, method signatures, default methods, static methods and nested types
- Interfaces cannot be instantiated
- A class tht implements an interfave must implement all the methods declared in the interface

### Inheritance
- When you want to crate a new class and there i already a clss that includes some of the code that you want you can derive your new class from the existing class. In doing this you can reuse the fields and methods of the existing class without having to write them yourself.
- A subclass inherits all the members from its superclass. Constructors are not memebers but can be invoked by the subclass.
- classes can have fields whereas interfaces cannot
- Except for the *Object* class a class has exactly one direct superclass. A class inherits fields and methods from all its superclasses whether direct or indirect. A subclass can override methods that it inherits or it can hide fields of methods that it inherits.
- The *Object* class is the top of the class hierarchy. All classes are descendants from this class and inherit methods from it. Useful methods inherited from Object include *toString()*, *equals()*, *clone()*, and *getClass()*
- You can prevent a class from being subclasses by using the *final* keyword in the class's declaration
- You can prevent a method from being overridden by subclasses by declaring it as a final method
- 

