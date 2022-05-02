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
