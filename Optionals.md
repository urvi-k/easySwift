# Optionals
- Optionals can be used for the variables or constants which can either contains value or nil.

*Example:*
- Convert String to Int.
```
var value1 = "123" 
var value2 = Int(value1) 
```
- In this case `value`2 will return `123` but what if,
```
var value1 = "hello" 
var value2 = Int(value1) 
```
- here, `value2` returns nil as `"hello"` can't be convert to Int type.
- In that case `value2` should br Optional(`Int?`) type. It can be unwrape using(`!`). to get actual value.

*Example:*
```
var value2: Int? = 123
print(value2!) // 123
```

# Nil
- nil represents empty. That means there is no value at all.

*Example:*
```
var value2: Int? = nil
value2 = 10
```

# Optional Binding:
- Optional Binding is used to find out whether an Optional contains a value, if so, to make that value available as a tempotaty constant or variable.
- Optional Binding can be done with `if let` or `Guard`.

### if let:
*Example:*
```
if let val = value2 {
  print(val)     // 10
}
```
- If `value2` has value it will assigned to the `val` else it will skip the `if` block.
- **Note:** Constant in `if let` only usefull within it's block.


### Guard:
*Example:*
```
guard let val = value1 else { return }
```
- constant in `guard` can be used for its following statements.
