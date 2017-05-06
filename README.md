# Comparing C++ to Swift 3
(https://iswift.org/cookbook/declare-a-closure)
(https://code.tutsplus.com/tutorials/swift-from-scratch-an-introduction-to-classes-and-structures--cms-23197)

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)
<h1> Team Members</h1>
<h4> Tom Marler </h4>
<h4>Matt Barmann</h4>
<h4> Nicolle Lenzmeier</h4># Comparing C++ to Swift 3

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
### Types (https://cocoacasts.com/value-types-and-reference-types-in-swift/)
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

        - Enums

        - Tuples


9. Type Erasure
    - Explain:
10. Type Methods (http://stackoverflow.com/questions/24087936/how-do-i-make-class-methods-properties-in-swift)
    - Explain

---
### Classes (http://rshankar.com/difference-between-struct-and-class-in-swift/)
A class is a blueprint and is used to create objects, classes can have           properties to store values and methods to add behavior.  In swift 3 classes      can have 2 types of properties stored and computed.  

---
### Instance references
Explain Instance References: 

---
### Properties (http://www.aidanf.net/learn-swift/classes)
- Store properties 
    - Declared using var or let and given an initial value
- Computed properties
    - Are also declared with var but instead of an initial value you assign a         function to calculate the value.  You must delcare the type for a                computed property
- Lazy Store Properties
    - Lazy properties are always declared using the var keyword. You can declare     a stored property lazy if you want to defer their initialization.  The value     of an lazy property won’t be calculated until the first time it is accessed.     For example, say you had a stored property performs a network call to get its     initial value. Instead of having this happen when the object is initialized,     you can have it happen when the property is first accessed by declaring the      property as lazy.
    ```
    lazy var shippingCosts = downloadShippingData()
    ```
    
- Property callbacks
    - We can also attach a function to a stored property and have it called          whenever the value of that property is about to change. These are called         property observers.
    There are 2 observers that you can define: willSet gets called before the        variable changes, and didSet gets called after the variable has changed.
    ```
    class ObservedCirlce {
        var radius:Double = 1.0 {
            willSet{
                print(”Radius is changing from \(radius) to \(newValue).”)
            }
        }
        var area:Double {
            return(3.14 * radius * radius)
        }
   }
    var oc = ObservedCirlce()
    oc.radius = 2.5 // prints "Radius is changing from 1.0 to 2.5."
    oc.area // 19.625
    ```


---
### Interface / Protoclo (https://medium.com/ios-os-x-development/introduction-to-protocols-in-swift-3-73f9a9be6b15)
Explain Protocols: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
### Inheritance / extensions
Explain Inheritance:
Explain extensions:


```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
### Reflection
Explain Reflection:
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
### Memory management
Explore Memory management: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
### Comparisons of references and values
Explain references and values: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
### NUll/nil references
Explain NULL references: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
### Errors and execption handling
Explain Errors: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
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
---
### Implementation of listeners and event handlers
Explain listeners:
Explain event handlers:
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
### Singleton
Explain singleton:
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
### Procdural Programming
Explain Procedural Programming: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
### Functional Programming
Explain functional Programming:
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
### Multithreading
Explain Multithreading: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
