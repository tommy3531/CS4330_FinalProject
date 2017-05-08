# Comparing C++ to Swift 3

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
- **Why was Swift created?** When apple decided to create Swift they wanted to provide a language for programmers that was fast and more effecient.  Swift was not created for one specific purpose. Apple wanted a language that developers could use to write fast and effeicent IOS apps using Xcode. According to Apple, Swift code must be
        - _Safe:_ Swift Objects can never be nil and trying to make them nil will throw a complie error.  For cases where nil is appropriate programmers can use optionals which is represented by using a ?.  By using optionals they force the programmer to safetly deal with nil values so the complier can safetly handle it.     
        - _Fast:_ Swift allows and encourages the use of constants much more.  By using optionals ensures that certains pointers can never be nil, so the complier can omit nil checks.  Also, objects in Swift can call one another which is one reason why Swift is faster then Objective-C
        - _Expressive:_ Swift classes are defined in a single file, programmers do not need to use the import statement for classes.  Also there is no more alloc and init when the programmers creates an object from a class.
- **What problems is Swift trying to address?** Apple set out to create a language that was easy to use compared to Objective-C where programmers had to manage memory and didnt have features like interred typing.  Swift addresses these issues and many more.
    - _Memory Allocation:_ One of Swifts biggest advantage is that it does Automatic garbage collection, which means that Swift will automatically take care of allocating and deallocating memory. This makes it easier for the programmer becasue they do not have to deal with memory management.
    - _Inferred Typing:_ Programmers do not have to spend time definning what types of variables they are using
    - _Less Error Prone:_ Because optionals are built-in and if used correctly can produce less errors.
    - Interpreted languages such as Ruby and Pythong let the programmer develop software more quickly because they can handle tasks in the background that they would have to handle on their own Swift appears to change this.  
- **Is Swift a reaction to a previous language or a replacement for another language?** Before Swift, IOS developers used Objective-C which is a laugage Apple spent years refining.  Objective-C is built on top the LLVM language complier.  Swift was created to fix or make life easier on the programmer with features like Automatic Reference Counting
- **Why was C++ created?** Developed by Bjarne Stroustrup at Bell Labs in 1979 as an extension of the C language. He wanted an efficient and flexible language similar to C, but also provides high-level features for program organization.
- **What problems was C++ to address?** Its main mission was to improve the C language. Stroustrup liked C for its general-purpose, and that it was fast and widely used, but he hated the low-levelness to it. C++ (which signifies the increment operator “++” in C) was created to make an efficient low-level language while providing users the option to have high-level convenience.
- **Is C++ a reaction to a previous language or a replacement for another language?** C++ was initially called “C with Classes” but eventually changed to C++ to indicate the increment operator in C, showing that it is C but better. On top of using C as the foundation, Stroustrup also liked and used Simula for its features that were very helpful for large software development. He combined C’s efficiency and Simula’s easy organization to make one ultra powerful and efficient language
---

# Unique features
- **Unique features of Swift:** 
    - _Playgrounds:_ When a playground is created in Swift the programmer can write code in the playground and see results instantly.  This makes learning and exploring the Swift language very enjoyable becasue the programmer is given instant feedback. 
    - _Immutability:_ In Objective-C this is a mess in swift it takes very little effort with     var and let
        ```
        var dateString = formatter.stringFromData(date)
        let dateString = formatter.stringFromDate(date)
        ```
    - _Open Source:_ The source code for Swift is Open Source meaning anyone can analyze the source and even make suggestions.  
    - Optionals - These come built-in and are complier driven so that crashes are not at all possible if used correctly. 
- **Does C++ have any particularly unique features?** Templatized Coding. In templatized coding, you write one function that is valid for any data type that has operators defined
    ```
    template<object>
        //insert necessary stuff to define function and set stuff up
        object sum = 0;
        for each object in container
            sum += object;
            return sum;
    ```
    - Other than that, C++ has influenced so many languages that there aren’t that many unique features to it
---
# Name spaces
 - **How are name spaces implemented in Swift?**
    - To access items in one namespace from another a programmer must first import the module             using the import declaration.   The import delcaration consists of the import           keyword followed by the module name.  
        ```
        import moduleName
        ```
 - **How are name spaces used in Swift?**
    - A namespace acts as a border/boundary, another namespace can not access               another namespace  without mentioning it first.  Name spaces provides a virtual         partition seperating the names in one namespace from names in another.  By              creating this seperation two items can be declared with the same name                   as long as they are in different namespaces.  In Swift namespaces are used as a         boundary when a import declaration is used within a .swift file.  For example,          if I was using Alamofire to make rest calls to an API, I would import the               module, which gives the current file access to Alamofire.  

        ```
        import Alamofire
        ```
        
        The import declaration can be used to make a sepecific classe or method                 available to the current namespace. 
        
        ```
        import UIKit.NSData
        ```
- **How are name spaces implemented in C++?** Typically, you declare a namespace in a header     file. If your function implementations are in a separate file, then qualify the function     names.
- **How are names spaces used in C++?** Namespaces are used to organize code into logical groups and to prevent name collisions that can occur especially when your code base includes multiple libraries. Code: The following example shows  namespace declaration and three ways that code outside the namsespace can access their members.
    ```
    namespace DoSomething   
    {           
	    class Manager        
	    {       
	    public:           
		    void DoSomethingElse() {}       
	    };       
		    void Func(Manager) {}  
    }
    ```

---
### Type
Within a given program a program needs to use types to store different information inside variables.  Variables are nothing but reserved memory locations to store values.  A programmer may store information of various data types likes string, character, integer, floating point and boolean.  Based on the data type of a variable the operating system allocates memory and decides what can be stored in the reserved memory. Swift has the following Types
- **What types does Swift support?**
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
- **Are both reference and values type supported in Swift?**
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
- **What Types does C++ Support**
    | Type	   |Typical Bit Width	|Typical Range|
    |----------|:------------------:|---------------------:| 
    |char	   |1byte               |	-128 to 127 or 0 to 255|
    |unsigned char| 1byte           |	0 to 255|
    |signed char|	1byte|	-128 to 127|
    |int|	4bytes|	-2147483648 to 2147483647|
    |unsigned int|	4bytes|	0 to 4294967295|
    |signed int	|4bytes|	-2147483648 to 2147483647|
    |short int	|2bytes	|-32768 to 32767|
    |unsigned short int|	2bytes|	0 to 65,535|
    |signed short int|	2bytes|	-32768 to 32767|
    |long int	|8bytes|	-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807|
    |signed long int|	8bytes	|-9,223,372,036,854,775,808 to             9,223,372,036,854,775,807|
    |unsigned long int|	8bytes|	0 to 18,446,744,073,709,551,615|
    |float	|4bytes|	+/- 3.4e +/- 38 (~7 digits)|
    |double	|8bytes|	+/- 1.7e +/- 308 (~15 digits)|
    |long double|	8bytes|	+/- 1.7e +/- 308 (~15 digits)|
    |wchar_t	|2 or 4 bytes|	1 wide character|

- **Are both reference and value types supported in C++** Yes, both reference and value types are supported by C++. C++ allows you to override the assignment operator to do anything your heart desires, however the default (and most common) choice is to copy the value.
- **Can new value types be created in C++?** Yes. User-defined types are allowed. Just like you could have a 65 as a short int or it could be represented as an A as a char.

---
### Classes 
A class is a blueprint and is used to create objects, classes can have           properties to store values and methods to add behavior.  

 - **Defining a class in Swift:** The class keyword indicates that you are defining a class of a particular type.  The            implementation of the class is wrapped in a pair of curly braces.  Inside the curly braces, the        programmer can define properites.  Properites within a class can either be var or let, var     keyword to     define a variable and the let var is used to define a constant property.
    
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
 - **Creating a new Instances of a class in Swift:** Instantiating an instance of a class is very similar to invoking a     function.  To create an      instance, the name of the class is followed by a pair of parentheses and the     return value is      assigned to a constant or variable
    ```
    var newClass : NewClass!
    newClass = newClass()
    ```
 - **De-initializing in Swift:** De-initializing (deinit), is only avaiable for classes and not structures they give the programmer the ability to run some code before objects are destoryed.          Programmers can define a deinitializer by using deinit.
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
- **Defining a class in C++** Classes are defined using either keyword class or keyword struct, with the following syntax
    ```
	class class_name {   
		access_specifier_1:     member1;   
		access_specifier_2:     member2;   
		... 
	} object_names;
    ```
- **Constructing/Initializing in C++** 
```
// Creates an object of type Pet in dynamic memory, pet points to it.
Pet* pet = new Pet ();
```
```
// Creates a pet object called pet2 in automatic storage
Pet pet2
```
- **Destructing/de-initializing in C++** This is what is called a virtual destructor. To build an object the constructor must be of the same type as the object and because of this a constructor cannot be a virtual function. But the same thing does not apply to destructors. A destructor can be defined as virtual or even pure virtual. You would use a virtual destructor if you ever expect a derived class to be destroyed through a pointer to the base class. This will ensure that the destructor of the most derived classes will get called
```
A* b = new B;
Delete b;
```
---
### Instance references
 - **Instance References in Swift:** In Swift Classes, Structures and Enumeration are accessed through instance         methods. Instance methods help the programmer to access and modify instance properites by having these         capabilities the programmer can change functionality related to the needs of the instance.  
    ```
    // Class Instance
    class Person() {
        // Property
        var firstName: String
        int() {}
    }
    
    let matt = Person()
    matt.firstName = "Matt"

    // Enum Instance
    extension Person {
        init(fn: String) {
            self = .firstName(fn)
        }
    }
    nicole = Person(fn: "Nicole")
    print(nicole)
    
    // Struct Instance
    struct Person {
        var firstName: String
    }
    
    var tom = Person(firstName: "Tom")
    
    ```
- **Instance reference names in data type (class) in C++** A class declaration can contain static object of self type, it can also have pointer to self type, but it cannot have a non-static object of self type.
    ```
    // A class can have a static member of self type
    #include<iostream>

    using namespace std;
    
    class Test {
    	static Test self;// works fine
        /* other stuff in class*/
    
    };
    
        int main()
        {
            Test t;
            getchar();
            return 0;
        }
    }
    ```

---
### Properties

- **Getter and Setters in Swift:** Computed properties do not store a value, instead getters and setters are     provided to retrieve and set properties.
    ```
    class Person {
        var_firstName = "Tom"

        var getFirstName: String {
            get {
                return _firstName
            }
            set(newValue) {
                _firstName = newValue
            }
        }
    }
    var person = Person()
    // Tom
    person.getFirstName 
    
    // Set the FirstName to Nicole
    person.getFirstName = "Nicole"
    
    // Get the firstName "Nicole"
    person.getFirstName
    ```

- **Backing Variables in Swift:** In addition to properties, you can use instance variables as a backing store     for the values stored in a property. Swift unifies these concepts into a single property declaration. A Swift property does not have a corresponding instance variable, and the backing store for a property is not accessed directly. This approach avoids confusion about how the value is accessed in different contexts and simplifies the property’s declaration into a single, definitive statement. All information about the property—including its name, type, and memory management characteristics—is defined in a single location as part of the type’s definition

- **Store properties in Swift:** Declared using var or let and given an initial value
    
- **Computed properties in Swift**: Are also declared with var but instead of an initial value you assign a         function to calculate the value.  You must delcare the type for a computed property

- **Lazy Store Properties in Swift**: Lazy properties are always declared using the var keyword. You can         declare     a stored property lazy if you want to defer their initialization.  The value     of an     lazy property won’t be calculated until the first time it is accessed.     For example, say you     had a stored property performs a network call to get its     initial value. Instead of having this     happen when the object is initialized,     you can have it happen when the property is first         accessed by declaring the      property as lazy.

    ```
    lazy var shippingCosts = downloadShippingData()
    ```
    
- **Property callbacks in Swift** A programmer can also attach a function to a stored property and have it called          whenever the value of that property is about to change. These are called         property observers.
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
- **Getters and setters in C++** Unfortunately, C++ does not natively support properties. Properties in C++ involve writing out each function for each setter and getter.
- **Backing Variables in C++** Since getters and setters have to be made manually backing variables must be made manually too. 
---
### Interface / Protocols 

- **What does the Swift Support:**
    _Protocol:_ A protocol is a list of prerequisities to inherit a title, meaning a class will have to         conform to a given protoclo before it could be considered a class object.  
    ```
    class somethingViewController: UIViewController {
    
        func tableView(tableView: UITableView, didSelectRowAtIndexPath indexPath: NSIndexPath) {
            // Target the selectedRows within the TableView
        }
    }
    ```
- **What abilities do Protocols have in Swift:** Protocols are great     becasue they help the developer make sure they have everything they need.  Protocols are used     with UITableView and if the developer wanted to add items to the TableView cells they must          adopt the protocols in the class definition
    ```
    protocol SomeProtocol {
    
    }
    ```
- **How are Protocols used swift:**
    _Structure and name the protocol:_
    ```
    protocol Fighter {
    
    }
    ```
    _Add property requirments:_
    ``` 
    protocol Fighter {
        var name: String
        var fightName: String
    }
    ```
    
    _Add definite method requirements:_
    ```
    protocol Fighter {
        var name: String
        var fightName: String
        
        // Methods
        func punch()
        func kick()
        fucn grapple()
    ```
- **What does C++ support?** Often the term Interface is used in C++ to describe an abstract class like, that describes a service that can be provided by a range of different, otherwise unrelated classes.
- **What abilities do interfaces have in C++** C++ possess the ability to directly express designs that include this separation of concerns through purely abstract classes, but additionally affords you the ability to connect components and algorithms (using templates) without the need to impose an interface declaration upon the components
- **How are intefaces used in C++?** By creating an abstract class which only contains pure virtual functions
---
### Inheritance / extensions
- **Inheritance in Swift:** It allows a class to be defined that has a certain set of methods and properities     and other classes can be     dervived from the same class.
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
    
- **Extensions in Swift:** Add new functionality to an exisiting class, structure, enumeration, or protocol.      Extensions in Swift        give the programer the ability to add computed instance properties and computed type properties, define       instance methods and type methods, provide new initializers, define subscripts, define and use new nested     types, makes an exisiting type conform to a protocol.  
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
### Reflection 

- **What is a reflection in Swift?** Reflections are a set of functions that allow a program to inspect and      modify its own structure or even hoe it works at runtime.  Although reflection are slow they give    the programmer the ability to write highly dynamic code that minimizes interface and still           achieves functionalitiies. In Swift reflections are based around a struct called Mirror. The         programmer creates a mirorr for a particular object and the mirror will then let the programmer     query it.
- **What reflection abilities are supported in Swift** 
    - _children:_ 
    - _customMirror:_ 
    - _description:_
    - _displayStyle:_
    - subjectType:_
    - superclassMirror:_
- **How is a reflection used in Swift?** 
    ```
    let aStructMirror = Mirror(reflection: yourStructName)
    print(aStructMirror)
    // prints : Mirror for yourStruct
    ```
- **What relfection abilites are supported in C++** Not supported in C++
- **How are reflections used** It is not since reflections are not supported
 

---
### Memory management 
 - **How does Swift handle memory:** Swift uses a system of memory management called Automatic     Referenece Counting (ARC).  ARC keeps track of how many references there are to an object in the code.  When the programmer creates a new reference to a object the reference count is increased for that object.  When the reference count for that object reaches zero the memory for that object is released, this is something the ARC handles automatically
 - **How does C++ handle memory** NOTHING GIVEN
---
### Comparisons of references and values
- **How are values compared in Swift? (comparing two strings)** In Swift you can use the == operator to compare to strings variables or constants
    ```
    var helloWord = "Hello, World!"
    var helloSwift = "Hello, Swift!"
    
    if helloWord == helloSwift {
        print("The strings are equal")
    } else {
        print("The string are not equal")
    }
    
    // Prints
    The strings are not equal
    ```
    
    ```
    // Compare Values Return true or false
    Equal to (a == b)
    Not equal to (a != b)
    Greater than (a > b)
    Less than (a < b)
    Greater than or equal to (a >= b)
    Less than or equal to (a <= b)
    
    1 == 1   // true because 1 is equal to 1
    2 != 1   // true because 2 is not equal to 1
    2 > 1    // true because 2 is greater than 1
    1 < 2    // true because 1 is less than 2
    1 >= 1   // true because 1 is greater than or equal to 1
    2 <= 1   // false because 2 is not less than or equal to 1
    
    Logical NOT (!a)
    Logical AND (a && b)
    Logical OR (a || b)
    
    ```
- **How are values compared in C++? (comparing two strings)** NOTHING GIVEN
---
### Null/nil references
- **Which does Swift use? (null,nil)?** Any time you need a variable that can be null the programmer can use the "?" operator to identify a variable whose value is optional.  A variable declared as an optional can be set to nil to represent an absence value.

- **Does Swift have features for handling null/nil references?** Swift supports handling null and nil references by using optionals.
    ```
    var age: Int? = 2
    age = nil
    ```
    If an optional is not given an initial value it is automatically set to nil and the programmer can always check forthe presence of a value by comparing the optional to nil
    ```
    if (age != nil) {
        // Do something with age
    }
    ```
- **Which does C++ use? (null,nil)?** NOTHING GIVEN
- **Does C++ have features for handling null/nil references?** NOTHING GIVEN
---
### Errors and execption handling
- **Error handling in Swift:** In swift error handling is the process of responding to and recovering from error condition within a program.  In swift programmers can throw and catach errors at runtime
    - _Throwing Errors:_ Throwing an error lets the programmer indicate that something unexpected         happened and can not contiue to execute.
        ```
        func canThrowErrors() throws -> String
        ```
    - _Catching Errors:_ Catching an error lets the programmer indicate that something unexpected happend, by catching the error the programmer gives the program the ability to handle the error
        ```
        do {
            try expression
                statements
        } catch pattern 1 {
            statements
        } catch pattern 2 where condition {
            statements
        }
        ```
- **Error handling in C++:** NOTHING GIVEN
---
### Closures
 - **Closures in Swift:** Are self contained chunks of code that can be passed around they can capture and store references to any constant or variable in which they are defined
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
 - **Closures in C++:**
---
### Implementation of listeners and event handlers
- **Event Handlers (action handlers) in Swift:** Is called when a user taps a certain button on the interface. 
    ```
    @IBAction func btnPressed(_ sender: Any) {
        let alert = UIAlertController(
        title: "Howdy!", message: "You tapped me!", preferredStyle: .Alert)
        alert.addAction(
            UIAlertAction(title: "OK", style: .Cancel))
        self.present(alert, animated: true)
    }
    ```
- **Event Handlers (action handlers) in C++:** NOTHING GIVEN
---
### Singleton
- **How is a Singleton implemented in Swift?** The programmer will create a class inside the curly brackets of the class they will create a static constant named sharedAPIAccess which contains an instance of the class.  By using static constant only one instance will ever exist within in the program
    ```
    class APIAccess {
        
    }

    // Only one instance will ever exist
    static let sharedAPIAccess = APIAccess() 
    ```
- **Can it be made thread-safe in Swift** The programmer must ensure that the singleton is only instantiated once not matter the caller thread, t and be 
- **lazily instantiated in Swift?** The lazy initializer for a global variable is run the first time that global variable is accessed and is lanuched as dispatch_once to make sure that the initializer is atomic.  This enables a neat way to use 
    ```
    class APIAccess {
        
    }
    // This will be lazy loaded when first called and is thread safe
    let sharedAPIAccess = APIAccess() 
    ```
- **How is a Singleton implemented in C++?** NOTHING GIVEN
- **Can it be made thread-safe in C++** NOTHING GIVEN
- **lazily instantiated in Swift?** NOTHING GIVEN
---
### Procdural Programming
- **Does Swift support procedural programming?** There are two kinds of procedures in Swift atomic which describes how an external program can be executed and compound procedures which consist of a sequence of Swift script statements.  
    - _Declare a procedure:_ A procedure declaration defines the names of a procedure and its input and output paramenters.  Inputs are specified ot the right of the function name and outputs are specified to the left. Below a procedure called myproc is declared and it has two inputs and two ouputs
    ```
    (type3 out1, type4 out2) myproc (type1 in1, type2 in2)
    ```
    -  _Atomic Procedures:_ Specifies how to invoke an external executable program, and how logical data types are mapped to command line arguments.  Below procedure specifies that myproc invokes an executable called myapp, passing the values of i, s and the filename of bf as command line arguments
    ```
    app (binaryfile bf) myproc (int i, string s="foo") {
        myapp i s @filename(bf);
    }
    ```
    - _Compound Procedures:_ 
    ```
    (type2 b) foo_bar (type1 a) {
        type3 c;
        c = foo(a);    // c holds the result of foo
        b = bar(c);    // c is an input to bar
    }
    ```
- **Does C++ support procedural programming?** NOTHING GIVEN
---
### Functional Programming
- Does the language support functional programming?
 - **Functional Programming in Swift:** Is a declarative programming style that treats computation as the evalution of mathematical functions it is based on the mathematical concept called Category Theory.  Functional programming can make the programmers code more concise and expressive and can be better explained by understanding the following concepts.
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
 - **Functional Programming in C++:** NOTHING GIVEN
---
### Multithreading
- **Multithreading in Swift:** Swift uses Grand Centeral Dispatch which is paramount for creating responsive apps with smooth animations and transitions.  Multithreading allows the processor to create concurrent threads in which it can switch between so multiple tasks can be executed at the same time. For example if the programmers does not want the User Inferface to freeze up when the user is saving something they would use a background process so two things can be executed at the same time on that thread.  Grand Center dispatch provides a way to interface with threads via queues.  
    - _Queues:_ Queues are managed through DispatchQueue, the programmer can either execute tasks in order which is considered a serial queue or along side each other which is a concurrent queue.
    - Multithreading is great for returning data back from a rest call and displaying it in the UI.   bBy using multithreading the main queue can show the UI and dowloading the data will be handled by the Global queue so it can run in the background.  This techique is what I used to download JSON from a Rest call and displayed the parsed JSON in a table view cell.  
- - **Multithreading in C++:** NOTHING GIVEN