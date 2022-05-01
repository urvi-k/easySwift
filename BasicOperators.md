# Basic Operators

## Terminology
### A) Unary:
1) on Single target  --> *Example:* `-4`
2) Unary prefix  --> *Example:* `!a`
3) Unary postfix  --> *Example:* `a!`

### B) Binary:
1) infix  --> *Example:* `a + b`

### B) Ternary:
1) on Three targets  --> *Example:* `a ? b : c`

#
# Assignment Operator
- sign (=)
- *Example:* `a = b`

# Arithmetic Operators
### 1) Addition (+):
- Used to do Addition of two values.
 *Example:* 
```
var val1 = 10
var val2 = 20
var val3 = val1 + val2
print(val3)

Output:
// 30
```
### 2) Subtraction (-):
- Used to do Subtraction of two values.
 *Example:* 
```
var val1 = 20
var val2 = 10
var val3 = val1 - val2
print(val3)

Output:
// 10
```
### 3) Multiplication (*):
- Used to do Multiplication of two values.
 *Example:* 
```
var val1 = 20
var val2 = 10
var val3 = val1 * val2
print(val3)

Output:
// 200
```
### 4) Division (*):
- Used to do Division of two values.
 *Example:* 
```
var val1 = 20
var val2 = 10
var val3 = val1 / val2
print(val3)

Output:
// 2
```
# Reminder Operator
- Sign (%)
 *Example:* 
```
10 % 2 = 0 (Reminder)
5 % 3  = 2 (Reminder)
```
# Compound Assignment Operators
- Used to combine assignment Operator with another Operations.
- Sign (%)
 *Example:* 
 - Addition, assignment Operator (+=).
```
var a
a += 2 can be write as a = a + 2
```

# Comparision Operators
- Each Comparision Operators returns bool.
1) Equal `(a == b)`
2) Not Equal `(a != b)`
3) Greater than `(a > b)`
4) Less than `(a < b)`
5) Greater than or equal `(a >= b)`
6) Less than or equal `(a <= b)`

*Example:*
```
let name = "Hello world"
if name == "Hello world" {
  print("Yes name is Hello world")
}

Output:
// Yes name is Hello world
```

- Comparision using Tupples:
```
1) (1, "zebra") < (2, "apple")     // true
2) (3, "apple") < (3, "bird")      // true
3) (4, "dog") == (4, "dog")        // true
```
- Comparision is determines by tupples 1st element. If it's true it is not check tupples 2nd element.

# Ternary Operator
- It is a short form of if condition.
*Example:*
```
if a == b {
  print(a)
} else {
  print(b)
}
can be write as,

a == b ? print(a) : print(b)
```

# Range Operators
### 1) Closed Range Operator: (a...b)
- Include value from a to b.
*Example:*
```
var a = 1
var b = 5
for value in a...b {
  print(value)
}

Output:
// 1
// 2
// 3
// 4
// 5
```
### 2) Half-Open Range Operator: (a..<b)
*Example:*
```
var a = 1
var b = 5
for value in a..<b {
  print(value)
}

Output:
// 1
// 2
// 3
// 4
```

### 3) One side Range Operator: (a..<b)
*Example:*
```
var name = ["heals", "velly", "wowe"]
for value in name[1...] {
  print(value)
}

Output:
// velly
// wowe

for value in name[...1] {
  print(value)
}

Output:
// heals
// velly
```

# Logical Operators
### 1) NOT (!a)
*Example:*
```
let isAllow = true
if !isAllow {
  print("Allow")
} else {
  print("Not Allow")
}

Output:
// Not Allow
```
### 2) AND (&&)
*Example:*
```
let a = true, b = true
if a && b {
  print("Allow")
} else {
  print("Not Allow")
}

Output:
// Allow
```

### 3) OR (||)
*Example:*
```
let a = true, b = false
if a || b {
  print("Allow")
} else {
  print("Not Allow")
}

Output:
// Allow
```
