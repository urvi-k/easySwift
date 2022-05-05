# ARC - Automatic Reference Counting
- Swift use ARC to track and manage your Apps memory usage.
- ARC Automatically frees up the space of the instances when it is no longer required. 
- While in some caces ARC needs some more information about the code to frees up the spaces of unUsed instances.
- Reference counting only applies to `Classes` as `Structures` and `Enumeration` are of value types.

## How ARC Works
- ARC allocate some chunck of memory to the instance of the classes when they are created, so the instances value can be stored in it.
- When instance is no longer in use ARC automatically frees up the space.
- If ARC were deallocate the instance that is still being used, than the instances properties can not be accessible, and if we try to use that instance the app could get crashed.
- ARC automatically tracks that if any instance, variable or constants of the class instance are still being used till than ARC will not deallocate that class instance.
- To make this possible create an instance with strong reference, so it will not allow the firm to deallocate it where it is being used.

## ARC in Action
- here is a Example of class `Person` where `name` variable has one initializer to assign value to it, and has deinitializer to deallocate the constant `name`.
```
class Person {
    let name: String
    init(name: String) {
        self.name = name
        print("\(name) is being initialized")
    }
    deinit {
        print("\(name) is being deinitialized")
    }
}
```
#
- Let's create three variables of type `Person` which will be used to create instance on type `Person`.
```
var reference1: Person?
var reference2: Person?
var reference3: Person?
```
- here, `reference1`, `reference2` and `reference3` are of Optional type, that means they are by default initialized with `nil`.
- You can now create a new `Person` instance and assign it to one of these three variables:
```
reference1 = Person(name: "John Appleseed")
// Prints "John Appleseed is being initialized"
```
- here, at the time of creating an instance initializer will be called so it will be print `"John Appleseed is being initialized"` which is in init block of `Person` class.
- As new `Person` instance has been assigned to `reference1` variable, so now there is strong reference from `reference1` to the `Person`.
- Untill at least one strong refrence will be remain, ARC makes sure that this `Person` is kept in memory and isn’t deallocated.

- If you assign the same `Person` instance to two more variables, two more strong references to that instance are established:
```
reference2 = reference1
reference3 = reference1
```

- Now let's break two of these strong references by assigning `nil` to `reference1` and `reference2`.
- This will not destroy `reference3` even if Original strong reference `reference1` has been broak.
```
reference1 = nil
reference2 = nil
```
- Now let's break strong reference of`reference3`. 
- here, the `Person` instance will be deallocated because there is no strong referance left to class `Person`.
```
reference3 = nil
// Prints "John Appleseed is being deinitialized"
```

## Strong Reference Cycles Between Class Instances
- In above section we have looked that ARC will not deallocate the `Person` until it is not being used anymore, And ARC is able to track the count of strong references of the perticuler instances.
- However it is possible to write the code where the count of strong references will never be 0. This can happen when two instance hold a strong references of each other, such that each instance keeps the other alive. This is known as a strong reference cycle.
- To resolve that we need to define one of the instance using `weak` and in some cases can use `unowned` based on syntax.

- Here’s an example of how a strong reference cycle can be created by accident. This example defines two classes called `Person` and `Apartment`, which model a block of apartments and its residents:
```
class Person {
    let name: String
    init(name: String) { self.name = name }
    var apartment: Apartment?
    deinit { print("\(name) is being deinitialized") }
}

class Apartment {
    let unit: String
    init(unit: String) { self.unit = unit }
    var tenant: Person?
    deinit { print("Apartment \(unit) is being deinitialized") }
}
```
- here, we have created `Person` class has variable `name` and `apartment` of type Optional `Apartment` which is initialized by nil by default as there can be case where a person has or has not live in any apartment.
- here, we have created `Apartment` class has variable `unit` and `tenant` of type Optional `Person` which is initialized by nil by default as there can be case where a apartment has or has not any person live in it.

- Both the class has deinitializer which prints the fact that an instance of that class is being deinitialized. It enabels us to see wather the class instanse has been deallocated as expected.

- Let's define two optional variable of type `Person` and `Apartments`, as it's opetional it will initializes with `nil` by default.
```
var john: Person?
var unit4A: Apartment?
```
- You can now create a specific `Person` instance and `Apartment` instance and assign these new instances to the `john` and `unit4A` variables:
```
john = Person(name: "John Appleseed")
unit4A = Apartment(unit: "4A")
```

