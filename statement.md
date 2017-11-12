# Recursion

## Use cases

### Sum function with traditional for loop

```javascript runnable
function sum(arr) {
    let result = arr[0];
    for (let i = 1; i < arr.length; i++) {
        result = result + arr[i];
    }
    return result;
}

console.log(`Array: [1,2,3]; Expected: 6; Actual: ${sum([1,2,3])}`);
console.log(`Array: [1,0,1]; Expected: 2; Actual: ${sum([1,0,1])}`);
```

### Sum function with recursion

Deatiled example: 
```javascript runnable
function sum(arr, initial = 0) {
    if (arr.length === 0) {
        return initial;
    }
    return sum(arr.slice(1), initial + arr[0]);
}

console.log(`Array: [1,2,3]; Expected: 6; Actual: ${sum([1,2,3])}`);
console.log(`Array: [1,0,1]; Expected: 2; Actual: ${sum([1,0,1])}`);
```

Short example:
```javascript runnable
function sum(arr, initial = 0) {
    return arr.length === 0 ? initial : sum(arr.slice(1), initial + arr[0]);
}

console.log(`Array: [1,2,3]; Expected: 6; Actual: ${sum([1,2,3])}`);
console.log(`Array: [1,0,1]; Expected: 2; Actual: ${sum([1,0,1])}`);
```
