# Recursion

> An act of a function calling itself. Recursion is used to solve problems that contain smaller sub-problems. A recursive function can receive two inputs: a base case (ends recursion) or a recursive case (continues recursion). (MDN)

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

### Deep map function without recursion

```javascript runnable
function deepMapAtoB(arr) {
    return arr.map(value => {
        if (Array.isArray(value)) {
            return value.map(nestedValue => {
                return nestedValue === 'a' ? 'b' : nestedValue;
            });
        }
        return value === 'a' ? 'b' : value;
    });
}

console.log(`Given: ["a",["a"],"c"]; Result: ${JSON.stringify(deepMapAtoB(["a",["a"],"c"]))}`);
```

### Deep map function with recursion

```javascript runnable
function deepMapAtoB(arr) {
    return arr.map(value => {
        if (Array.isArray(value)) {
            return deepMapAtoB(value);
        }
        return value === 'a' ? 'b' : value;
    });
}

console.log(`Given: ["a",["a"],"c"]; Result: ${JSON.stringify(deepMapAtoB(["a",["a"],"c"]))}`);
```

## Translated resources

https://learn.javascript.ru/recursion
https://karmazzin.gitbooks.io/eloquentjavascript_ru/content/chapters/chapter3.html 
