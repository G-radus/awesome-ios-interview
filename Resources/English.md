- [UIKit](#UIKit)
	- [How could you setup Live Rendering?](#How-could-you-setup-Live-Rendering?)
	- [What are different ways that you can specify the layout of elements in a UIView?](#What-are-different-ways-that-you-can-specify-the-layout-of-elements-in-a-UIView?)
	- [Formula of Autolayout](#Formula-of-Autolayout)
	- [Size Classes](#Size-Classes)
	- [Intrinsic Content Size](#Intrinsic-Content-Size)
	- [What’s the difference between the frame and the bounds?](#What’s-the-difference-between-the-frame-and-the-bounds?)
- [TESTING](#TESTING)
	- [What is the benefit writing tests in iOS apps?](#What-is-the-benefit-writing-tests-in-iOS-apps?)
	- [Please explain “Arrange-Act-Assert”](#Please-explain-“Arrange-Act-Assert”)
	- [What is the Test Driven Development?](#What-is-the-Test-Driven-Development-of-three-simple-rules?)
- [TASKS](#TASKS)
	- [Explain why a compile time error occurs. How can you fix it?](#Explain-why-a-compile-time-error-occurs.-How-can-you-fix-it?)
	- [Consider the code](#Consider-the-following-code:)
	- [Determine the value of “x” in the Swift code](#Determine-the-value-of-“x”-in-the-Swift-code-below)
- [SDK](#sdk)
	- [Application States](#Application-States)
	- [Can you explain what happens when you call autorelease on an object?](#Can-you-explain-what-happens-when-you-call-autorelease-on-an-object?)
	- [What are iBeacons?](#What-are-iBeacons?)
	- [What kind of JSONSerialization have ReadingOptions?](#What-kind-of-JSONSerialization-have-ReadingOptions?)
- [PATTERNS](#PATTERNS)
	- [Adapter Pattern](#What-is-Adapter-Pattern?)
	- [What Are B-Trees?](#What-Are-B-Trees?)
	- [What is Memento Pattern?](#What-is-Memento-Pattern?)
	- [MVC](#MVC)
	- [Responder Chain](#What-is-Responder-Chain?)
	- [MVVM](#MVVM)
	- [Observer Pattern](#What-is-Observer-Pattern?)
	- [Singleton Pattern](#What-is-Singleton-Pattern?)
	- [Decorator Pattern](#What-is-Decorator-Design-Pattern?)
	- [Facade Pattern](#What-is-Facade-Design-Pattern?)
- [OOP](#OOP)
	- [Inheritance](#Inheritance)
	- [Polymorphism](#Polymorphism)
	- [Encapsulation](#Encapsulation)
	- [What is the abstract class?](#What-is-the-abstract-class?)
- [Language](#language)
	- [Fileprivate and private access level](#What-is-the-difference-fileprivate-and-private-access-level?)
	- [What is final class?](#What-is-final-class?)
	- [Structs vs Classes](#Structs-vs-Classes)
	- [Swift Standard Library Protocol](#Swift-Standard-Library-Protocol)
	- [What is Downcasting?](#What-is-Downcasting?)
	- [“Strong” and “Weak” references?](#What-are-“strong”-and-“weak”-references?)
	- [Explain weak and unowned self?](#Explain-[weak-self]-and-[unowned-self]?)
	- [Lazy in Swift](#Lazy-in-Swift)
	- [Difference between raw and associated values in Swift](#Difference-between-raw-and-associated-values-in-Swift)
	- [Differences between Swift and Objective-C?](#Can-you-briefly-describe-differences-between-Swift-and-Objective-C?)
	- [Non-Escaping and Escaping Closures?](#What-is-the-difference-Non-Escaping-and-Escaping-Closures?)
	- [Method Swizzling in Swift](#Please-explain-Method-Swizzling-in-Swift)
	- [Errors handling in Swift?](#How-should-one-handle-errors-in-Swift?)
	- [Difference strong, weak, readonly and copy?](#What-is-the-difference-strong,-weak,-readonly-and-copy?)
	- [Benefits of Guard?](#What-are-benefits-of-Guard?)
	- [Raw values and associated values in Swift enumerations](#In-Swift-enumerations,-what’s-the-difference-between-raw-values-and-associated-values?)
	- [Swift Transforming Array functions](#Swift-Transforming-Array-functions)
	- [Dynamic in Objective-C?](#What-is-dynamic-in-Objective-C?)
	- [NSError object?](#What-is-made-up-of-NSError-object?)
	- [Extensions](#extensions)
	- [KVO](#kvo)
	- [KVC](#kvc)
	- [By calling performSelector:withObject:afterDelay: - is the object retained?](#By-calling-performSelector:withObject:afterDelay:-is-the-object-retained?)
	- [What is defer?](#What-is-defer?)
	- [Selectors](#selectors)
	- [Any and AnyObject](#What-is-the-difference-Any-and-AnyObject?)
- [GENERAL](#GENERAL)
	- [HTTP request types](#HTTP-request-types)
	- [REST](#rest)
	- [Deep and shallow copy](#Deep-and-shallow-copy)
- [DATA](#DATA)
	- [How does NSManagedObjectContext work?](#How-does-NSManagedObjectContext-work?)
	- [NSFetchedResultsController](#NSFetchedResultsController)
	- [NSPersistentContainer](#NSPersistentContainer)
	- [Managed object context and the functionality that it provides](#Managed-object-context-and-the-functionality-that-it-provides)
	- [What is NSFetchRequest?](#What-is-NSFetchRequest?)
- [CONCURRENCY](#CONCURRENCY)
	- [Different ways of achieving concurrency in OS X and iOS](#Different-ways-of-achieving-concurrency-in-Mac-OS-and-iOS)
	- [What is DispatchGroup?](#What-is-DispatchGroup?)
	- [Synchronized](#Synchronized)
	- [What is the difference between Synchronous & Asynchronous task?](#What-is-the-difference-between-Synchronous-&-Asynchronous-task?)


# UIKit
### How could you setup Live Rendering?
The attribute `@IBDesignable` lets Interface Builder perform live updates on a particular view

## What are different ways that you can specify the layout of elements in a UIView?
Here are a few common ways to specify the layout of elements in a UIView:

Using `Interface Builder`, you can add a `XIB file` to your project, layout elements within it, and then load the XIB in your application code (either automatically, based on naming conventions, or manually). Also, using InterfaceBuilder you can create a storyboard for your application.
You can your own code to use NSLayoutConstraints to have elements in a view arranged by Auto Layout.
You can create CGRects describing the exact coordinates for each element and pass them to UIView’s  
```objectivec  
  - (id)initWithFrame:(CGRect)frame method.
```
## Formula of Autolayout
Attribute 1 = Multiplier * Attribute 2 + Constant

## Size Classes
A size class is a new technology used by iOS to allow you to custom your app for a given device class, based on its orientation and screen size.
There are presently four size classes:  
- Horizontal Regular   
- Horizontal Compact  
- Vertical Regular  
- Vertical Compact  

## Intrinsic Content Size
The Intrinsic Content Size is one of the most powerful features you gain when you opt-in to using Auto Layout to describe your interfaces. When a view has an intrinsic content size, it is promising Auto Layout that it will have a predefined size that the engine can use to calculate and lay out its views

## What’s the difference between the frame and the bounds? 
`The bounds` of an UIView is the rectangle, expressed as a location (x,y) and size (width,height) relative to its own coordinate system (0,0)   
`The frame` of an UIView is the rectangle, expressed as a location (x,y) and size (width,height) relative to the superview it is contained within.  

# TESTING
### What is the benefit writing tests in iOS apps?
Tests gives us a clear perspective on the API design, by getting into the mindset of being a client of the API before it exists.
Good tests serve as great documentation of expected behavior.
It gives us confidence to constantly refactor our code because we know that if we break anything our tests fail.
If tests are hard to write its usually a sign architecture could be improved. Following RGR ( Red — Green — Refactor ) helps you make improvements early on.

## Please explain “Arrange-Act-Assert”
AAA is a pattern for arranging and formatting code in Unit Tests. If we were to write XCTests each of our tests would group these functional sections, separated by blank lines:
Arrange all necessary preconditions and inputs.
Act on the object or method under test.
Assert that the expected results have occurred.


## What is the Test Driven Development of three simple rules?
You are not allowed to write any production code unless it is to make a failing unit test pass.
You are not allowed to write any more of a unit test than is sufficient to fail; and compilation failures are failures.
You are not allowed to write any more production code than is sufficient to pass the one failing unit test.


# TASKS
### Explain why a compile time error occurs. How can you fix it?
Task:
The following code snippet results in a compile time error:
```objectivec  
struct IntStack {
  var items = [Int]()
  func add(x: Int) {
    items.append(x) // Compile time error here
  }
}
``` 

Solution:
Structures are value types. By default, the properties of a value type cannot be modified from within its instance methods.
However, you can optionally allow such modification to occur by declaring the instance methods as ‘mutating’:
```objectivec  
struct IntStack {
  var items = [Int]()
  mutating func add(x: Int) {
    items.append(x) // All good!
  }
}
``` 

## Consider the following code:
Task:
```objectivec  
var defaults = UserDefaults.standard()
var userPref = defaults.stringForKey("userPref")!
printString(userPref)
 
func printString(string: String) {
    print(string)
}
``` 


Solution:
The second line uses the stringForKey method of UserDefaults, which returns an optional, to account for the key not being found, or for the corresponding value not being convertible to a string.

During its execution, if the key is found and the corresponding value is a string, the above code works correctly. But if the key doesn’t exist, or the corresponding value is not a string, the app crashes with the following error:

fatal error: unexpectedly found nil while unwrapping an Optional value
The reason is that the forced unwrapping operator ! is attempting to force unwrap a value from a nil optional. The forced unwrapping operator should be used only when an optional is known to contain a non-nil value.

The solution consists of making sure that the optional is not nil before force-unwrapping it:
```objectivec  

let userPref = defaults.stringForKey("userPref")
if userPref != nil {
    printString(userPref!)
}
``` 
## Determine the value of “x” in the Swift code below
Task: 
```swift  
var a1 = [1, 2, 3, 4, 5]
var a2 = a1
a2.append(6)
var x = a1.count
```

Solution:
In Swift, arrays are implemented as structs, making them value types rather than reference types (i.e., classes). When a value type is assigned to a variable as an argument to a function or method, a copy is created and assigned or passed. As a result, the value of “x” or the count of array “a1” remains equal to 5 while the count of array “a2” is equal to 6, appending the integer “6” onto a copy of the array “a1.” The arrays appear in the box below.
```swift
a1 = [1, 2, 3, 4, 5]  
a2 = [1, 2, 3, 4, 5, 6]  
``` 

# SDK
### Application States
The iOS application states are as follows:

Not running state: The app has not been launched or was running but was terminated by the system.  

Inactive state: The app is running in the foreground but is currently not receiving events. (It may be executing other code though.) An app usually stays in this state only briefly as it transitions to a different state. The only time it stays inactive for any period of time is when the user locks the screen or the system prompts the user to respond to some event (such as an incoming phone call or SMS message).  

Active state: The app is running in the foreground and is receiving events. This is the normal mode for foreground apps.  

Background state: The app is in the background and executing code. Most apps enter this state briefly on their way to being suspended. However, an app that requests extra execution time may remain in this state for a period of time. In addition, an app being launched directly into the background enters this state instead of the inactive state.  

Suspended state: While suspended, an app remains in memory but does not execute any code. When a low-memory condition occurs, the system may purge suspended apps without notice to make more space for the foreground app.

## Can you explain what happens when you call autorelease on an object?
When you send an object a autorelease message, its retain count is decremented by 1 at some stage in the future. The object is added to an autorelease pool on the current thread. The main thread loop creates an autorelease pool at the beginning of the function, and release it at the end. This establishes a pool for the lifetime of the task. However, this also means that any autoreleased objects created during the lifetime of the task are not disposed of until the task completes. This may lead to the taskʼs memory footprint increasing unnecessarily. You can also consider creating pools with a narrower scope or use NSOperationQueue with itʼs own autorelease pool. (Also important – You only release or autorelease objects you own.)

## What are iBeacons?
iBeacon.com defines iBeacon as Apple’s technology standard which allows Mobile Apps to listen for signals from beacons in the physical world and react accordingly. iBeacon technology allows Mobile Apps to understand their position on a micro-local scale, and deliver hyper-contextual content to users based on location. The underlying communication technology is Bluetooth Low Energy.

## What kind of JSONSerialization have ReadingOptions?
- MutableContainers specifies that arrays and dictionaries are created as variables objects, not constants    
- MutableLeaves specifies that leaf strings in the JSON object graph are created as instances of variable String   
- AllowFragments specifies that the parser should allow top-level objects that are not an instance of Array or Dictionary   

# PATTERNS
### What is Adapter Pattern? 
An Adapter allows classes with incompatible interfaces to work together. It wraps itself around an object and exposes a standard interface to interact with that object.

## What Are B-Trees? 
B-trees are search trees that provide an ordered key-value store with excellent performance characteristics. In principle, each node maintains a sorted array of its own elements, and another array for its children

## What is Memento Pattern? 
In Memento Pattern saves your stuff somewhere. Later on, this externalized state can be restored without violating encapsulation; that is, private data remains private. One of Apple’s specialized implementations of the Memento pattern is Archiving.

## MVC
`Model` —   responsible for the domain data or a data access layer which manipulates the data, think of ‘Person’ or ‘PersonDataProvider’ classes.
`Views`  —  responsible for the presentation layer (GUI), for iOS environment think of everything starting with ‘UI’ prefix.
`Controller/Presenter/ViewModel` —  mediator between the Model and the View, in general responsible for altering the Model by reacting to the user’s actions performed on the View and updating the View with changes from the Model.

## What is Responder Chain? 
A ResponderChain is a hierarchy of objects that have the opportunity to respond to events received.

## MVVM 
UIKit independent representation of your View and its state. The View Model invokes changes in the Model and updates itself with the updated Model, and since we have a binding between the View and the View Model, the first is updated accordingly.
Your `View Model` will actually take in your model, and it can format the information that’s going to be displayed on your view.

## What is Observer Pattern?
In the Observer pattern, one object notifies other objects of any state changes.

## What is Singleton Pattern?
The Singleton design pattern ensures that only one instance exists for a given class and that there’s a global access point to that instance. It usually uses lazy loading to create the single instance when it’s needed the first time.

## What is Decorator Design Pattern?
The Decorator pattern dynamically adds behaviors and responsibilities to an object without modifying its code. It’s an alternative to subclassing where you modify a class’s behavior by wrapping it with another object.

## What is Facade Design Pattern? 
The Facade design pattern provides a single interface to a complex subsystem. Instead of exposing the user to a set of classes and their APIs, you only expose one simple unified API.

# OOP
### Inheritance
It allows a class to be defined that has a certain set of characteristics (such as methods and instance variables) and then other classes to be created which are derived from that class. The derived class inherits all of the features of the parent class and typically then adds some features of its own.

## Polymorphism
The word polymorphism means having many forms. Typically, polymorphism occurs when there is a hierarchy of classes and they are related by inheritance.

Objective-C polymorphism means that a call to a member function will cause a different function to be executed depending on the type of object that invokes the function.

Consider the example, we have a class Shape that provides the basic interface for all the shapes. Square and Rectangle are derived from the base class Shape.

## Encapsulation
Encapsulation is an Object-Oriented Programming concept that binds together the data and functions that manipulate the data and that keeps both safe from outside interference and misuse. Data encapsulation led to the important OOP concept of data hiding.

Data encapsulation is a mechanism of bundling the data and the functions that use them, and data abstraction is a mechanism of exposing only the interfaces and hiding the implementation details from the user.

## What is the abstract class?
An abstract class is a class that contains at least one abstract method, which is a method without any actual code in it, just the name and the parameters, and that has been marked as "abstract".

The purpose of this is to provide a kind of template to inherit from and to force the inheriting class to implement the abstract methods.

An abstract class thus is something between a regular class and a pure interface. Also interfaces are a special case of abstract classes where ALL methods are abstract

# LANGUAGE
### What is the difference fileprivate and private access level?
`Fileprivate` is accessible within the current file, private is accessible within the current declaration.

## What is final class?
By adding the keyword final in front of the method name, we prevent the method from being overridden

## Structs vs Classes
1. Inheritance.

Structures can't inherit in swift. If you want 

class Vehicle {
}

class Car : Vehicle {
}

Go for an class.

2. Pass By

Swift structures pass by value and class instances pass by reference.

3. Thread Safety

Structs are thread-safe

## Swift Standard Library Protocol
There are a few different protocol. Equatable protocol, that governs how we can distinguish between two instances of the same type. That means we can analyze. If we have a specific value is in our array. The comparable protocol, to compare two instances of the same type and sequence protocol: prefix(while:) and drop(while:) [SE-0045].
Swift 4 introduces a new Codable protocol that lets us serialize and deserialize custom data types without writing any special code.

## What is Downcasting?
When we’re casting an object to another type in Objective-C, it’s pretty simple since there’s only one way to do it. In Swift, though, there are two ways to cast — one that’s safe and one that’s not .
as used for upcasting and type casting to bridged type
as? used for safe casting, return nil if failed
as! used to force casting, crash if failed. should only be used when we know the downcast will succeed.

## What are “strong” and “weak” references?
By default, any variable that points to another object does so with what is referred to as a “strong” reference. A retain cycle occurs when two or more objects have reciprocal strong references (i.e., strong references to each other). Any such objects will never be destroyed by ARC (iOS’ Automatic Reference Counting). Even if every other object in the application releases ownership of these objects, these objects (and, in turn, any objects that reference them) will continue to exist by virtue of those mutual strong references. This therefore results in a memory leak.

Reciprocal strong references between objects should therefore be avoided to the extent possible. However, when they are necessary, a way to avoid this type of memory leak is to employ weak references. Declaring one of the two references as weak will break the retain cycle and thereby avoid the memory leak.

To decide which of the two references should be weak, think of the objects in the retain cycle as being in a parent-child relationship. In this relationship, the parent should maintain a strong reference (i.e., ownership of) its child, but the child should not maintain maintain a strong reference (i.e., ownership of) its parent.

For example, if you have Employer and Employee objects, which reference one another, you would most likely want to maintain a strong reference from the Employer to the Employee object, but have a weak reference from the Employee to thr Employer.

## Explain [weak self] and [unowned self]?
unowned does the same as weak with one exception: The variable will not become nil and therefore the variable must not be an optional.
But when you try to access the variable after its instance has been deallocated. That means, you should only use unowned when you are sure, that this variable will never be accessed after the corresponding instance has been deallocated.
However, if you don’t want the variable to be weak AND you are sure that it can’t be accessed after the corresponding instance has been deallocated, you can use unowned.
By declaring it [weak self] you get to handle the case that it might be nil inside the closure at some point and therefore the variable must be an optional. A case for using [weak self] in an asynchronous network request, is in a view controller where that request is used to populate the view.

## Lazy in Swift
An initial value of the lazy stored properties is calculated only when the property is called for the first time. There are situations when the lazy properties come very handy to developers.

## Difference between raw and associated values in Swift
This question tests the developer’s understanding of enumeration in Swift. Enumeration provides a type-safe method of working with a group of related values. Raw values are compile time-set values directly assigned to every case within an enumeration, as in the example detailed below:
enum Alphabet: Int {
case A = 1
case B
case C
}

In the above example code, case “A” was explicitly assigned a raw value integer of 1, while cases “B” and “C” were implicitly assigned raw value integers of 2 and 3, respectively. Associated values allow you to store values of other types alongside case values, as demonstrated below:
enum Alphabet: Int {
case A(Int)
case B
case C(String)
}


## Can you briefly describe differences between Swift and Objective-C?
When Swift was first launched in 2014, it was aptly described as “Objective-C without the C.” By dropping the legacy conventions that come with a language built on C, Swift is faster, safer, easier to read, easier to maintain, and designed specifically for the modern world of consumer-facing apps. One of the most immediately visible differences is the fact that Objective-C lacks formal support for namespaces, which forces Objective-C code to use two- or three-letter prefixes to differentiate itself. Instead of simple names like “String,” “Dictionary,” and “Array,” Objective-C must use oddities like “NSString,” “NSDictionary,” and “NSArray.”
Another major advantage is that Swift avoids exposing pointers and other “unsafe” accessors when referring to object instances. That said, Objective-C has been around since 1983, and there is a mountain of Objective-C code and resources available to the iOS developer. The best iOS developers tend to be pretty well versed in both, with an understanding that Swift is the future of iOS development.

## What is the difference Non-Escaping and Escaping Closures?
The lifecycle of a non-escaping closure is simple:
Pass a closure into a function
The function runs the closure (or not)
The function returns
Escaping closure means, inside the function, you can still run the closure (or not); the extra bit of the closure is stored some place that will outlive the function. There are several ways to have a closure escape its containing function:
Asynchronous execution: If you execute the closure asynchronously on a dispatch queue, the queue will hold onto the closure for you. You have no idea when the closure will be executed and there’s no guarantee it will complete before the function returns.
Storage: Storing the closure to a global variable, property, or any other bit of storage that lives on past the function call means the closure has also escaped.

## Please explain Method Swizzling in Swift
Method Swizzling is a well known practice in Objective-C and in other languages that support dynamic method dispatching.
Through swizzling, the implementation of a method can be replaced with a different one at runtime, by changing the mapping between a specific #selector(method) and the function that contains its implementation.
To use method swizzling with your Swift classes there are two requirements that you must comply with:
The class containing the methods to be swizzled must extend NSObject
The methods you want to swizzle must have the dynamic attribute

## How should one handle errors in Swift?
The method for handling errors in Swift differ a bit from Objective-C. In Swift, it's possible to declare that a function throws an error. It is, therefore, the caller's responsibility to handle the error or propagate it. This is similar to how Java handles the situation.

You simply declare that a function can throw an error by appending the throws keyword to the function name. Any function that calls such a method must call it from a try block.

func canThrowErrors() throws -> String
 
//How to call a method that throws an error
try canThrowErrors()
 
//Or specify it as an optional
let maybe = try? canThrowErrors()

## What is the difference strong, weak, readonly and copy?
- `Strong` means that the reference count will be increased and the reference to it will be maintained through the life of the object
- `Weak` means that we are pointing to an object but not increasing its reference count. It’s often used when creating a parent child relationship. The parent has a strong reference to the child but the child only has a weak reference to the parent.
- `Readonly`, we can set the property initially but then it can’t be changed.
- `Copy` means that we’re copying the value of the object when it’s created. Also prevents its value from changing.

## What are benefits of Guard?
There are two big benefits to guard. One is avoiding the pyramid of doom, as others have mentioned — lots of annoying if let statements nested inside each other moving further and further to the right. The other benefit is provide an early exit out of the function using break or using return.


## When applied to strings, what’s the complexity of the countElements function and why?
Comments: The String struct doesn’t provide a count or length property or method to count the number of characters it contains. Instead a global countElements<T>() function is available.


Solution: Swift strings support extended grapheme clusters. Each character stored in a string is a sequence of one or more unicode scalars that, when combined, produce a single human readable character. Since different characters can require different amounts of memory, and considering that an extreme grapheme cluster must be accessed sequentially in order to determine which character it represents, it’s not possible to know the number of characters contained in a string upfront, without traversing the entire string. For that reason, the complexity of the countElements function is O(n).

## In Swift enumerations, what’s the difference between raw values and associated values?
Raw values are used to associate constant (literal) values to enum cases. The value type is part of the enum type, and each enum case must specify a unique raw value (duplicate values are not allowed).

The following example shows an enum with raw values of type Int:

enum IntEnum : Int {
    case ONE = 1
    case TWO = 2
    case THREE = 3
}
An enum value can be converted to its raw value by using the rawValue property:

var enumVar: IntEnum = IntEnum.TWO
var rawValue: Int = enumVar.rawValue
A raw value can be converted to an enum instance by using a dedicated initializer:

var enumVar: IntEnum? = IntEnum(rawValue: 1)
Associated values are used to associate arbitrary data to a specific enum case. Each enum case can have zero or more associated values, declared as a tuple in the case definition:

enum AssociatedEnum {
    case EMPTY
    case WITH_INT(value: Int)
    case WITH_TUPLE(value: Int, text: String, data: [Float])
}
Whereas the type(s) associated to a case are part of the enum declaration, the associated value(s) are instance specific, meaning that an enum case can have different associated values for different enum instances.

## Swift Transforming Array functions  
→ map and flatMap— how to transform element. 
→ filter— should an element be included?  
→ reduce— how to fold an element into an aggregate value  
→ sort and lexicographicCompare—in what order should two elements come?  
→ indexOf and contains—does this element match?  
→ minElement and maxElement—which is the min/max of two elements?  
→ elementsEqual and startsWith—are two elements equivalent?  
→ split—is this element a separator?  

## What is dynamic in Objective-C?
`@dynamic` used to delegate the responsibility of implementing the accessors.
Dynamic for properties means that it setters and getters will be created manually and/or at runtime.

## What is made up of NSError object?
There are three parts of NSError object a domain, an error code, and a user info dictionary. The domain is a string that identifies what categories of errors this error is coming from.


## Extensions
Extensions add new functionality to an existing class, structure, enumeration, or protocol type. This includes the ability to extend types for which you do not have access to the original source code. Extensions are similar to categories in Objective-C

Extensions in Swift can:  
- Add computed instance properties and computed type properties  
- Define instance methods and type methods  
- Provide new initializers  
- Define subscripts  
- Define and use new nested types  
- Make an existing type conform to a protocol  

## KVO
KVO stands for `Key-Value Observing` and allows a controller or class to observe changes to a property value. In KVO, an object can ask to be notified of any changes to a specific property; either its own or that of another object.

## KVC 
KVC adds stands for `Key-Value Coding`. It’s a mechanism by which an object’s properties can be accessed using string’s at runtime rather than having to statically know the property names at development time.

## By calling performSelector:withObject:afterDelay: is the object retained?
Yes, the object is retained. It creates a timer that calls a selector on the current threads run loop. It may not be 100% precise time-wise as it attempts to dequeue the message from
the run loop and perform the selector

## What is defer?
`defer` keyword which provides a block of code that will be executed in the case when execution is leaving the current scope.


## Selectors
In Objective-C, selector has two meanings. It can be used to refer simply to the name of a method when it’s used in a source-code message to an object. It also, though, refers to the unique identifier that replaces the name when the source code is compiled. Compiled selectors are of type SEL. All methods with the same name have the same selector. You can use a selector to invoke a method on an object—this provides the basis for the implementation of the target-action design pattern in Cocoa

[friend performSelector:@selector(gossipAbout:) withObject:aNeighbor]
is equivalent to
 [friend gossipAbout:aNeighbor]

## What is the difference Any and AnyObject?
According to Apple’s Swift documentation:
Any can represent an instance of any type at all, including function types and optional types.
AnyObject can represent an instance of any class type.


# GENERAL
### HTTP request types
An HTTP request is a class consisting of HTTP style requests, request lines, request methods, request URL, header fields, and body content. The most common methods that are used by a client in an HTTP request are as follows:

1) GET:- Used when the client is requesting a resource on the Web server.

2) HEAD:- Used when the client is requesting some information about a resource but not requesting the resource itself.

3) POST:- Used when the client is sending information or data to the server—for example, filling out an online form (i.e. Sends a large amount of complex data to the Web Server).

4) PUT:- Used when the client is sending a replacement document or uploading a new document to the Web server under the request URL.
## REST 
An architectural style called REST (Representational State Transfer) advocates that web applications should use HTTP as it was originally envisioned. Lookups should use GET requests. PUT, POST, and DELETE requests should be used for *mutation, creation, and deletion respectively *.

REST proponents tend to favor URLs, such as

server.com/catalog/thing/1723
but the REST architecture does not require these “pretty URLs”. A GET request with a parameter

server.com/catalog?thing=1723
is every bit as RESTful.

GET requests should never be used for updating information. For example, a GET request for adding an item to a cart

server.com/addToCart?cart=314159&thing=1723

would not be appropriate. GET requests should be idempotent. That is, issuing a request twice should be no different from issuing it once. That’s what makes the requests cacheable. An “add to cart” request is not idempotent—issuing it twice adds two copies of the item to the cart. A POST request is clearly appropriate in this context. Thus, even a RESTful web application needs its share of POST requests.

## Deep and shallow copy
There are two kinds of object copying: shallow copies and deep copies. The normal copy is a shallow copy that produces a new collection that shares ownership of the objects with the original. Deep copies create new objects from the originals and add those to the new collection.

# DATA
### How does NSManagedObjectContext work?
`Managed object context` exists for three reasons: life-cycle management, notifications, and concurrency. It allows the developer to fetch an object from a persistent store and make the necessary modifications before deciding whether to discard or commit these changes back to the persistent store. The managed object context tracks these changes and allows the developer to undo and redo changes.

## NSFetchedResultsController
`NSFetchedResultsController` is a controller, but it’s not a view controller. It has no user interface. Its purpose is to make developers’ lives easier by abstracting away much of the code needed to synchronize a table view with a data source backed by Core Data.
Set up an NSFetchedResultsController correctly, and your table will mimic its data source without you have to write more than a few lines of code.

## NSPersistentContainer
The persistent container creates and returns a container, having loaded the store for the application to it. This property is optional since there are legitimate error conditions that could cause the creation of the store to fail.

## Managed object context and the functionality that it provides
A managed object context (represented by an instance of NSManagedObjectContext) is basically a temporary “scratch pad” in an application for a (presumably) related collection of objects. These objects collectively represent an internally consistent view of one or more persistent stores. A single managed object instance exists in one and only one context, but multiple copies of an object can exist in different contexts.

You can think of a managed object context as an intelligent scratch pad. When you fetch objects from a persistent store, you bring temporary copies onto the scratch pad where they form an object graph (or a collection of object graphs). You can then modify those objects however you like. Unless you actually save those changes, though, the persistent store remains unchanged.

Key functionality provided by a managed object context includes:

Life-cycle management. The context provides validation, inverse relationship handling, and undo/redo. Through a context you can retrieve or “fetch” objects from a persistent store, make changes to those objects, and then either discard the changes or commit them back to the persistent store. The context is responsible for watching for changes in its objects and maintains an undo manager so you can have finer-grained control over undo and redo. You can insert new objects and delete ones you have fetched, and commit these modifications to the persistent store.
Notifications. A context posts notifications at various points which can optionally be monitored elsewhere in your application.
Concurrency. Core Data uses thread (or serialized queue) confinement to protect managed objects and managed object contexts. In OS X v10.7 and later and iOS v5.0 and later, when you create a context you can specify the concurrency pattern with which you will use it using initWithConcurrencyType:

## What is NSFetchRequest?
`NSFetchRequest` is the class responsible for fetching from Core Data. Fetch requests are both powerful and flexible. You can use fetch requests to fetch a set of objects meeting the provided criteria, individual values and more.

# CONCURRENCY
### Different ways of achieving concurrency in OS X and iOS
There are basically three ways of achieving concurrency in iOS:  
1. threads  
2. GCD 
3. NSOperationQueue  

The disadvantage of threads is that they relegate the burden of creating a scalable solution to the developer. You have to decide how many threads to create and adjust that number dynamically as conditions change. Also, the application assumes most of the costs associated with creating and maintaining the threads it uses.

OS X and iOS therefore prefer to take an asynchronous design approach to solving the concurrency problem rather than relying on threads.

One of the technologies for starting tasks asynchronously is Grand Central Dispatch (GCD) that relegates thread management down to the system level. All the developer has to do is define the tasks to be executed and add them to the appropriate dispatch queue. GCD takes care of creating the needed threads and scheduling tasks to run on those threads.

All dispatch queues are first-in, first-out (FIFO) data structures, so tasks are always started in the same order that they are added.

An operation queue is the Cocoa equivalent of a concurrent dispatch queue and is implemented by the NSOperationQueue class. Unlike dispatch queues, operation queues are not limited to executing tasks in FIFO order and support the creation of complex execution-order graphs for your tasks.

## What is DispatchGroup?
`DispatchGroup` allows for aggregate synchronization of work. We can use them to submit multiple different work items and track when they all complete, even though they might run on different queues. This behavior can be helpful when progress can’t be made until all of the specified tasks are complete. 

## Synchronized
The `@synchronized` directive is a convenient way to create mutex locks on the fly in Objective-C code.

`Synchronized` guarantees that only one thread can be executing that code in the block at any given time.

Syntax:
```objectivec  
 @synchronized(key) 
 { 
  // thread-safe code 
 }
 ```

Example:
```objectivec  
 -(void)AppendExisting:(NSString*)val
{
  @synchronized (oldValue) {
      [oldValue stringByAppendingFormat:@"-%@",val];
  }
}
```
Now the above code is perfectly thread safe..Now Multiple threads can change the value.


## What is the difference between Synchronous & Asynchronous task?
`Synchronous`: waits until the task has completed
`Asynchronous`: completes a task in background and can notify you when complete