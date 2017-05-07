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
- **Why was the language created?**
    - Swift was not created for one specific purpose, Apple wanted a language that developers could use to write IOS apps as well as system programming or scaling up to cloud services.  According to Apple, Swift code must be
        - _Safe:_
        - _Fast:_
        - _Expressive:_
- **What problems was the language trying to address?**
- 
- Is the language a reaction to a previous language or a replacement for another language?
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
 - **How are name spaces implemented?**
    - To access items in one namespace from another a programmer must first import the module             using the import declaration.   The import delcaration consists of the import           keyword followed by the module name.  
        ```
        import moduleName
        ```
 - **How are name spaces used?**
    - A namespace acts as a border/boundary, another namespace can not access               another namespace  without mentioning it first.  Name spaces provides a virtual         partition seperating the names in one namespace from names in another.  By              creating this seperation two items can be declared with the same name                   as long as they are in different namespaces.  In Swift namespaces are used as a         boundary when a import declaration is used within a .swift file.  For example,          if I was using Alamofire to make rest calls to an API, I would import the               module, which gives the current file access to Alamofire.  

        ```
        import Alamofire
        ```
        
        The import declaration can be used to make a sepecific classe or method                 available to the current namespace. 
        
        ```
        import UIKit.NSData
        ```

---
### Types in _Swift_


Within a given program a program needs to use types to store different information inside variables.  Variables are nothing but reserved memory locations to store values.  A programmer may store information of various data types likes string, character, integer, floating point and boolean.  Based on the data type of a variable the operating system allocates memory and decides what can be stored in the reserved memory. Swift has the following Types
- **What types does the language support?**
    - _Int or UInt:_ This is used for whole numbers, you can use Int32, Int64 to define 32 
          bit signed integer.
    - _Float:_ This is used to represent a 32-bit floating-point number and numbers with smaller decimals points. Example, 3.14159, 0.1, and -273.158
    - _Double:_ This is used to represent a 64-bit floating-point number and used when floating-point values must be very large.  Example, 3.14159, 0.1, -273.158
    - _Boolean:_ This represents a boolean value which is either true or false
    - _String:_ This is an ordered collection of characters, Example Hello,World
    - _Character:_ This is a single-character string literal. Example, "C"
    - _Optional:_ This represents a variable that can hold either a value or no value
    - _Bound Values_
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
    - _Type Aliases_:  Gives the programmer the ability to create a new name for an exisitng type
        ```sh
        typealias newName = type
        typealias Feet = Int
        var distance: Feet = 100
        print(distance)
        output: 100
        ```
    - _Type Safety_:  Type-safe help ensures a variable that is declaraed as string can and will only expect a     string value.  Swift performs type-checks at complie time and will flag any mismatches types as errors.
        ```
        var holdInt = 42
        holdInt = "This is forty-two"
        print(holdInt)
        output: Complie time error
        ```
    - _Type Inference:_ Swift will infer the type of a variable when the programmer assigns it an initial values, basically the programmer just needs to remember to give variabels an intial value or expliticly declare the variable type.

        ```
        // Type Expliticly
        // Initial Value no need to declare variable type
        var stringOne = "A string" 
        
        // Initialize variable without initial value swift cant infer the variable type
        var stringTwo : String   
        
        // Assign string value to variable
        stringTwo = "Another string"
        ```
    
    - _Collection Types:_ Swift provides three primary collection types know as arrays, sets, and dictionaries         for storing collections of values.
        - Arrays: Ordered Collection of values
        - Sets: Unordered collections of unique values
        - Dictionary - Unordered collections of key-value associations
            ```
            // Array
            let array: [Type] = []      // type annotation
            let array: Array<Type> = [] // long form annotation
            let array = [Type]()        // initializer
            
            // Set
            var letters = Set<Type>()
            
            // Dictionary
            let dictionary: [KeyType: ValueType] = [:]           // type annotation
            let dictionary: Dictionary<KeyType, ValueType> = [:] // long form annotation
            let dictionary = [KeyType: ValueType]()              // initializer
            ```
- **Are both reference and values type supported?**
    - _Reference Types:_  I believe the best way to understand reference types is by initializaing a class and passing the class object to a function.  The function that the class object is passed to returns a reference to the same existing class object instance. The instance of the class object is referecing the location in memory.
    
        ```
        class Person {
            var name: String
            init(name: String) {
                self.name = name
            }
        }
        var person = Person(name: "Michael Jackson")
        ```
    - _Value Type:_ Are alwyas copied when they are passed around, examples of values types in Swift are          structs, enum and tuples

---
### Classes (http://rshankar.com/difference-between-struct-and-class-in-swift/)
A class is a blueprint and is used to create objects, classes can have           properties to store values and methods to add behavior.  

 - **Defining a class:** The class keyword indicates that you are defining a class of a particular type.  The            implementation of the class is wrapped in a pair of curly braces.  Inside the curly braces, the        programmer can define properites.  Properites within a class can either be var or let, var     keyword to     define a variable and the let var is used to define a constant property.
    
    ```
    class NewClass {
        
        // Class property
        var _propertyName: String
        
        // initializer
        init(){}
        
        // initializer with paraemeters
        init(propertyName: String){
            self._propertyName = propertyName
    }
    ```
 - **Creating a new Instances of a class:** Instantiating an instance of a class is very similar to invoking a     function.  To create an      instance, the name of the class is followed by a pair of parentheses and the     return value is      assigned to a constant or variable
    ```
    var newClass : NewClass!
    newClass = newClass()
    ```
 - **De-initializing:** Are used if the programmer needs some code to run before objects are destoryed.          Programmers can define a deinitializer by using deinit.
    ```
    class NewClass {
        var _classProperty: String
    }
    deinit {
        print("BYE")
    }
    
    var newclass: NewClass!
    newclass = NewClass()
    mc = nil
    // bye is printed 
    // becasue the programmer has assigned nil to newclass which causes it to deallocate
    ```
---
### Instance references
 - **Instance References:** In Swift Classes, Structures and Enumeration are accessed through instance         methods. Instance methods help the programmer to access and modify instance properites by having these         capabilities the programmer can change functionality related to the needs of the instance.  
    ```
    func newFunction() {
            
    }
    ```

---
### Properties (http://www.aidanf.net/learn-swift/classes)
- Getters and Setters write your own or built in?
- Backing Variables
- **Store properties**

    - Declared using var or let and given an initial value
    
- **Computed properties**

    - Are also declared with var but instead of an initial value you assign a         function to calculate the value.  You must delcare the type for a                computed property
    
- **Lazy Store Properties**

    - Lazy properties are always declared using the var keyword. You can declare     a stored property lazy if you want to defer their initialization.  The value     of an lazy property won’t be calculated until the first time it is accessed.     For example, say you had a stored property performs a network call to get its     initial value. Instead of having this happen when the object is initialized,     you can have it happen when the property is first accessed by declaring the      property as lazy.

        ```
        lazy var shippingCosts = downloadShippingData()
        ```
    
- **Property callbacks**
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
-What does the language support?
- What abilities does it have?
- How is it used?
 - Protocols: 
    - A protocol is a list of prerequisities to inherit a title, meaning a class will have to         conform to a given protoclo before it could be considered a class object.  Protocols are great     becasue they help the developer make sure they have everything they need.  Protocols are used     with TableView and if the developer wanted to add items to the TableView cells they must          adopt the protocols in the class definition
        ```
        class somethingViewController: UIViewController {
    
            func tableView(tableView: UITableView, didSelectRowAtIndexPath indexPath: NSIndexPath) {
                // Target the selectedRows within the TableView
            }
        }
        ```
    
        ```
        protocol SomeProtocol {
    
        }
        ```
    - Steps to define a protocol
    1. Structure and name the protocol
        ```
        protocol Fighter {
    
        }
        ```
    2.  Add property requirments
        ``` protocol Fighter {
            var name: String
            var fightName: String
        }
    3. Add definite method requirements
        ```
        protocol Fighter {
        var name: String
        var fightName: String
        
        // Methods
        func punch()
        func kick()
        fucn grapple()
        ```
---
### Inheritance / extensions
 - Inheritance:
    It allows a class to be defined that has a certain set of methods and properities and other classes can be     dervived from the same class.
    ```
    class Person {
        var _socialSecurityNumber: Int
        
        init(ssn: Int)
        self._socialSecurityNumber = ssn
    }
    class Employee: Person{
        // Employee is the subclass and Person is the parent
        // Employee has inherited all the properities from the Parent class callled Person
    }
    ```
    
 - Extensions:  
    Add new functionality to an exisiting class, structure, enumeration, or protocol.  Extensions in Swift        give the programer the ability to add computed instance properties and computed type properties, define       instance methods and type methods, provide new initializers, define subscripts, define and use new nested     types, makes an exisiting type conform to a protocol.  
    ```
    extension SomeType {
            
    }
    ```
    ```
    extension SomeType: SomeProtocol, AnotherProtocol {
        // Extends the existing type and make it adpot the Protocols
    }
    ```
---
### Reflection (http://www.superarts.org/blog/2016/03/28/reflection-in-swift)
                (http://nshipster.com/mirrortype/)
- What reflection abilities are supported
- How is a reflection used?
    - Reflection:
        - Reflections are a set of functions that allow a program to inspect and modify its own structure or even hoe it works at runtime.  Although reflection are slow they give the programmer the ability to write highly dynamic code that minimizes interface and still achieves functionalitiies 

---
### Memory management (https://www.raywenderlich.com/134411/arc-memory-management-swift)
- How is it handled?
- How does it work?
- Garbage Collection?
- Automatic reference counting?
Explore Memory management: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
### Comparisons of references and values
- How are values compared? (comparing two strings)
Explain references and values: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
---
### NUll/nil references
- Which does the language use? (null,nil)?
- Does the language have features for handling null/nil references?
Explain NULL references: 
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
### Closures
 - **Closures:** Are self contained chunks of code that can be passed around they can capture and store references to any constant or variable in which they are defined
    - _Types of Closures_
        1. Global Functions - they have a name and cannot caputre any values
        2. Nested Functions - They have a name can can capture values from their enclosing functions
        3. Closure Expressions - They do not have a name and can capture values from their context
            ```
            // Capture Values
            // The name variable is in the global context s
            var number = 0

            var addOne = {
                number += 1
            }
            
            var printNumber = {
                print(number)
            }
            
            printNumber() // 0
            addOne() // number is 1
            printNumber() // 1
            addOne() // number is 2
            addOne() // number is 3
            addOne() // number is 4
            printNumber() // 4
            ```
---
### Implementation of listeners and event handlers
Explain listeners:
Explain event handlers:

---
### Singleton
- How is a singleton implemented?
- Can it be made thread-safe?
- Can the singleton instance be lazily instantiated?
 - **Singleton:** A singleton guarantees that only one instance of a class is instantiated. When you create a singleton the programmer is giving the project global access to the singleton object.  
    ```
    let sharedNetworkManager = NetowrkManager
    ```

---
### Procdural Programming
- Does the language support procedural programming?
Explain Procedural Programming: 

---
### Functional Programming
- Does the language support functional programming?
 - **Functional Programming:** Is a declarative programming style that treats computation as the evalution of mathematical functions it is based on the mathematical concept called Category Theory.  Functional programming can make the programmers code more concise and expressive and can be better explained by understanding the following concepts.
    - _First-Class functions_ - Functions can be returned from and passed as arugments to other functions, can be stored in variables they are just like any other type.
    - _Pure functions_ - Functions given the same input will always return the same output and do no modify other states within the program.  Example: Most math functions like sin, cos fibonacci and factorial are pure.
    - _Immutablity_ - Mutability is de-emphaized as it is more difficult to reason about data whose values can change.
    - _Strong Typing_ - A Strong type system increases the runtime saftety of the code because the guarantees of the language's type system are checked at complie time.
        ```
        // Arugment to a functiona call
        funcName({ (ParameterTypes) -> ReturnType in statements })
        
        // Function parameter
        array.sorted(by: { (item1: Int, item2: Int) -> Bool in 
        return item1 < item2 })
        
        // As a constant
        let closureName: ClosureType = {}
        ```
        ```
        // Higher Order Functions
        map(_:), filter(_:), reduce(_:_:)
        ```
---
### Multithreading
- Threads or thread-like abilities
- Hw is multitasking accomplished?
Explain Multithreading: 
```sh
$ This is used to write an example
$ cd dillinger
$ npm install -d
$ node app
```
