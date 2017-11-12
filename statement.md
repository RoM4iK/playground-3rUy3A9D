# Recursion

## Use case

### Traditional for loop

```javascript runnable
// Pow function
function pow(base, exponent) {
    let result = base;
    for (let i = 1; i < exponent; i++) {
        result = result * base;
    }
    return result;
}

console.log('Expected: 2**3 == 8; Actual: ', pow(2,3))
console.log('Expected: 7**2 == 49; Actual: ', pow(7,2))
```

# Advanced usage

If you want a more complex example (external libraries, viewers...), use the [Advanced Node.js template](https://tech.io/select-repo/442)
