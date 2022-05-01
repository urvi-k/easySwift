# Assertions And Preconditions

- This both are used to checks data at runtime.
- This is used to assure an essential condition is setisfied before executing any further code.
- If the condition is not setisfied the App will be terminated.
- Assertions is used for debug environment and it is not affect on production.
- Preconditions affect production or debug environments.

## Debugging with Assertions
- Pass condition in Assert functions and message.
- If condition will be false, the message will be display in console and the App will be terminated.

*Example:*
```
let age = -3
assert(age >= 0, "Age can't be less then 0")
```
#
- Can use assertionFailure() if condition is already checked.

*Example:*
```
if age > 10 {
  print("Age is above 10")
} else {
  print("Age is below 10")
}

Output:
// Age is below 10
```

# Difference Among Assert, Precondition and FatalError
- AssertionFailure will only affect debug environment.
- PreconditionFailure affect production or debug environments.
- FatalError dose not check any condition and will always create a crash.
