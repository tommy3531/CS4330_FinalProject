# Comparing C++ to Swift 3

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

Swift 3 is a new Open Source language that was created by Apple in 2002.

  - Language Purpose
  - Unique features
  - Name spaces
  - Types
  - Classes
  - Instance references
  - Properties
  - Interface / Protocl
  - Inheritance / extensions
  - Reflection
  - Memory management
  - Comparisons of references and values
  - NUll/nil references
  - Errors and execption handling
  - lambda expressions, closures or functions as types
  - Implementation of listeners and event handlers
  - Singleton
  - Procdural Programming
  - Functional Programming
  - Multithreading
  - 
  
---

# Language Purpose
Swift 3: Explain the language and why it was created
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```

---
# Unique features
Explain the unique features: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
# Name spaces
1. How are name spaces implemented?
    - To access items in one namespace from another we must first import the module             using the import declaration.   The import delcaration consists of the import           keyword followed by the module name.  
        ```
        import moduleName
        ```
2. How are name spaces used?
    - A namespace acts as a border/boundary and another namespace can not access               another namespace  without mentioning it first.  Name spaces provides a virtual         partition seperating the names in one namespace from names in another.  By              creating this seperation two items can be declared with the same name                   as long as they are in different namespaces.  In Swift namespaces are used as a         boundary when a import declaration is used within a .swift file.  For example,          if I was using Alamofire to make rest calls to an API, I would import the               module, which gives the current file access to Alamofire.  

        ```
        import Alamofire
        ```
        
        The import declaration can be used to make a sepecific classe or method                 available to the current namespace. 
        
        ```
        import UIKit.NSData
        ```

---
### Types
Within a given program a program needs to use types to store different information inside variables.  Variables are nothing but reserved memory locations to store values.  A programmer may store information of various data types likes string, character, integer, floating point and boolean.  Based on the data type of a variable the operating system allocates memory and decides what can be stored in the reserved memory. Swift has the following Types
1. Built-in Data Types
    - Int or UInt
        - This is used for whole numbers, you can use Int32, Int64 to define 32 
          bit signed integer.
    - Float
        - This is used to represent a 32-bit floating-point number and numbers with smaller decimals points. Example, 3.14159, 0.1, and -273.158
    - Double
        - This is used to represent a 64-bit floating-point number and used when floating-point values must be very large.  Example, 3.14159, 0.1, -273.158
    - Boolean
        - This represents a boolean value which is either true or false
    - String 
        - This is an ordered collection of characters, Example Hello,World
    - Character - This is a single-character string literal. Example, "C"
    - Optional
        - This represents a variable that can hold either a value or no value
2. Bound Values
    |Type     |Typical Bit Width|Typical Range|
   |----------|:--------------:|------------:|
   |Int8      | 1 byte         |-127 to 127  |
   |UInt8     | 1 byte         |0 to 255     |
   |Int32     | 4 btyes        |-2147483648 to 2147483647|              
   |UInt32    | 4 bytes        |0 to 4294967295 |
   |Int64     | 8 bytes        |-9223372036854775808 to 9223372036854775807|
   |UInt64    | 8 bytes        |0 to 18446744073709551615|
   |Float     | 4 bytes        |1.2E-38 to 3.4E+38 (~6 digits)|
   |Double    | 8 bytes        |2.3E-308 to 1.7E+308 (~15 digits)|
3. Type Aliases
    - Gives the programmer the ability to create a new name for an exisitng type
    ```sh
    typealias newName = type
    typealias Feet = Int
    var distance: Feet = 100
    print(distance)
    output: 100
    ```
4. Type Safety
    - Type-safe help ensures a variable that is declaraed as string can and will only expect a string value.  Swift performs type-checks at complie time and will flag any mismatches types as errors.
    ```
    var holdInt = 42
    holdInt = "This is forty-two"
    print(holdInt)
    output: Complie time error
    ```
5. Type Inference (https://www.raywenderlich.com/143885/swift-tutorial-part-2-types-operations)
    - Enables a comp
    ```
    ```
    
6. Collection Types (https://learn.co/lessons/swift-collection-types)
    - Explain:
    ```
    ```
7. Reference Types (https://medium.com/capital-one-developers/reference-and-value-types-in-swift-de792db330b2)
    - Classes and closures
    -  I believe the best way to understand reference types is by initializaing a class and passing the class object to a function.  The function that the class object is passed to returns a reference to the same existing class object instance. The instance of the class object is referecing the location in memory.
    ```
    class Person {
        var name: String
        init(name: String) {
            self.name = name
        }
    }
    var person = Person(name: "Michael Jackson")
    ```
8. Value Type (http://blog.stablekernel.com/when-to-use-value-types-and-reference-types-in-swift)
    - a value type contains data and a reference type contains the location in memory where data lives
        - Structs
            ```
            ```
        - Enums
            ```
            ```
        - Tuples
            ```
            ```

9. Type Erasure
    - Explain:
    ```
    ```
### Classes
    A class is a blueprint and is used to create objects, classes can     have properties to store values and methods to add behavior.  In swift 3 classes can have 2 types of properties stored and computed.  
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Instance references
Explain Instance References: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Properties (http://www.aidanf.net/learn-swift/classes)
    - Store properties 
        - Declared using var or let and given an initial value
    - Computed properties
        - Are also declared with var but instead of an initial value you assign a function to calculate the value.  You must delcare the type for a computed property
Explain Properties: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Interface / Protoclo
Explain Protocols: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Inheritance / extensions
Explain Inheritance:
Explain extensions:

```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Reflection
Explain Reflection:
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Memory management
Explore Memory management: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Comparisons of references and values
Explain references and values: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### NUll/nil references
Explain NULL references: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Errors and execption handling
Explain Errors: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### lambda expressions, closures or functions as types
Explain Lambda:
Explain closures: 
Explain functions are types: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Implementation of listeners and event handlers
Explain listeners:
Explain event handlers:
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Singleton
Explain singleton:
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Procdural Programming
Explain Procedural Programming: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Functional Programming
Explain functional Programming:
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
### Multithreading
Explain Multithreading: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
