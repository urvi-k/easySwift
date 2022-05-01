## Type Saftey:
- You can provide type to variable or constants.

*Example:*
`let cricket: String = "Indian Team"`

- `cricket` variable is a `String` type so it can't hold another type of value like `Int`, `Float`. 

## Type Inference:
- If you don't provides the type of variable or constants, swift takes type automatically at compile time as per the data variable assigned.


*Example:*
`let cricket = "Indian Team"`
- Swift takes `String` type automatically here as per the value of `cricket`.

## Type Conversion:
- To convert type of any variable or constant it should have the specific type of initializer to convert the type into.


*Example:*
```
let ballCount: Int8 = 3
let batCount: Int16 = 16
let total = batCount + Int16(ballCount)
print("totalCount: \(total)")

Output:
// totalCount: 19
```
- here, Int16 has initializer to accept Int8, which implicitly cast Int8 into Int16.

## Type Aliases:
- Type Aliases used to give appropriate name to existing type.

*Example:*
`typealias AudioSample = UInt16`
- Now you can use `AudioSample` instead of `UInt16` everywhere you want.


*Example:*
`var maxValue = AudioSample.max`


