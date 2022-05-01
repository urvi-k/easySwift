# Tuples
- With the use of tupple multiple values can be used as a Single compound value.
- Tupple can be made by similler or different types.

*Example:*
`let httpError = (404, "Not found")`

## Decompose Tupple:
*Example:*
```
var (errorCode, message) = httpError
print(errorCode)    // 404
print(message)      // Not found
```
## Individually Access Tupple Values:
*Example:*
```
print(httpError.0)      // 404
print(httpError.1)      // Not found
```

*Example:*
```
print(httpError.errorCode)      // 404
print(httpError.message)        // Not found
```
