## Java OO Tutorial
### What is an Object?
- Objects are Methods(behavior) and Fields(state)
- data encapsulation is hiding internal state and requiring all interaction to be performed through an object's methods
- Bundling code into individual objects is good for 
   - Modularity, objects written and maintained independently
   - Information-hiding, only interacting with an objects methods
   - Code reuse, object already exists you can remove and plug in a diff object to replace
   - Pluggability and debugging ease, if a bolt breaks you replace it not the entire machice
### What is a Class?
- Class is a blueprint from which objects are created
- Fields represent object's state and the methods define its interaction

## Java Classes
- class declarations include...
    - modifiers
    - class name with the initial letter cappitalized
    - name of class's parent(superclass) after keyword extends
    - comma-separated list of interfaces implemented after keyword implements
    - class body surrounded by braces{}
- public modifier, the field is accessible from all classes
- private modifier, only within its own class
- all variables must have a type
- first (or only) work in a method name should be a verb
- Method declarations hve six components
    - Modifiers such s public, private
    - return type for value returned by method or void
    - method name
    - parameter list in parentheses
    - exception list
    - method body
- methods within a class can have the same name if they have different parameter lists
- parameters refer to the list of variables in a method declaration
- arguments are the actual values that are passes in when method is invoked
- invoke a methose the arguments used must match the declaration parameters in type and order

## Binary, Decimal and Hexadecimal Numbers
- every digit in a decimal number has a position and the decimal point helps to know which position is which
- you don't have to use base 10 to count
- Binary uses 2
- Hexadecimal uses 16