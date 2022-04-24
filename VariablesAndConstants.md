# Variables and Constants

**Constants**
- Constants used `let` keyword to be declare.
- Constants value can't be changed after it is initialized.

*Example:*
`let cricket = "Indian Team"`


**Variables**
- Variables used `var` keyword to be declare.
- Variables value can be changed after it is initialized.

*Example:*
```
var cricket = "Indian Team"
cricket = "African Team"
print("cricket-team : \(cricket)")

Output:
// cricket-team : African Team
```

- Multiple constants and variable can be initialized on single line.

*Example:* `let name = "Urvashi", country = "India"`

## Type Annotation
- Use type name to allocate the type to variable or constant at the time of declarartion.

 *Example:*
```
let cricket: String = "Indian Team"
var cricket: String = "African Team"
```

- Can define multiple variable or constant on the same line with the same type.

 *Example:* 
```
let red, green, black = "Colors"
var white, yellow, purple = "Colors"
print("red-color: \(red), green-color: \(green), black-color: \(black)")
print("white-color: \(white), yellow-color: \(yellow), purple-color: \(purple)")

Output:
// red-color: Colors, green-color: Colors, black-color: Colors, 
// white-color: Colors, yellow-color: Colors, purple-color: Colors, 
```

## Naming Variables and Constants
- It can be named using any alphabet, character Or unicode.
 *Example:* 
```
var π = "pi" 
var 😀 = "smile"
```

- Can use white-space, Mathematical Symboles, arrows, private use unicode scalar values, line box-drawing characters.
- Can't begin with Numbers.
*Example:* 
```
var cricket1 = "Indian Team" ✅
var 1cricket = "Indian Team" ❌
```

- Variables and Constants name with reserved keyword needs to be declared using backtickes(`) arround the name. 
*Example:* 
```
 var `extension` = "Hello World!" 
```
