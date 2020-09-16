## Primitives vs Objects
- Java Type System, primitives and reference types. Every primitive type corresponds to a reference type
- Primitive type variables
  - boolean- 1 bit
  - byte- 8 bits
  - short, char - 16 bits
  - int, float - 32 bits
  - long, double - 64 bits
- not always what it seeems, arrays of the primitive types long and double consume more memoty than their wrapper classes Long and Double
- primitive types are much faster and require much less memory. 
- objects in Java are slower and have a bigger memory impact

## Exceptions in Java
- An exception is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions
- exception handler chosen will "catch the exception"
- checked exemption- one that application should anticipate and recover from
- error, external to the application
- runtime exception, internal bugs, logic errors
- Errors and runtime excetions are known for unchecked exceptions.

## Using Scanner 
- Objects of type Scanner break down formatted imput into tokens and translate individual tokens to their data type.