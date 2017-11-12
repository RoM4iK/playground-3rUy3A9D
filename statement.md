# Recursion

## Use cases

### Reduce function with traditional for loop

```javascript runnable
function reduce(arr) {
    let result = arr[0];
    for (let i = 1; i < arr.length; i++) {
        result = result + arr[i];
    }
    return result;
}

console.log(`Array: [1,2,3]; Expected: 6; Actual: ${reduce([1,2,3])}`);
console.log(`Array: [1,0,1]; Expected: 2; Actual: ${reduce([1,0,1])}`);
```

### Pow function with recursion

Deatiled example: 
```javascript runnable
function pow(base, exponent) {
    if (exponent > 0) {
        return pow(base * base,
    }
    else {
        
    }
}
```
