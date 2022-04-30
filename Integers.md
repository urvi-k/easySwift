# Integers

- Integers are whole numbers with no fractional component.

*Example:*
42 and -23

### A) Signed Integer:  
- Include Positive, zero and Nagetive numbers.


### A) Unsigned Integer:  
- Include Positive and zero numbers.

#
- Swift provides signed and unsigned Integers in 8,16,32 and 64 forms.

### Types:
*Example:*
```
Unsigned:
8-bit = UInt8
32-bit = UInt32

Signed:
8-bit = Int8
32-bit = Int32
64-bit = Int64
```

### Integer Bounds:
- Can access Int tyoes min and max values with it's properties.
*Example:*
```
let minValue = UInt8.min       // 0
let maxValue = UInt8.max       // 255
```

## Int
- Swift provide addition type `int` which has the same size as your current plateforms native word size.
- Don't need to pick a spacific Int size like (Int8, int32, etc..)
*Example:*
```
32-bit platform,      Int size = Int32
64-bit platform,      Int size = Int64
```

## UInt
- Also automatically takes size as its platform.
```
Note: Use Int to avoid type casting in the most cases unless its really required to use UInt.
```
