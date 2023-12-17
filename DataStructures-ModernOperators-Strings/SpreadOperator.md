# Spread Operator

The spread operator is a useful feature in JavaScript that allows an iterable (such as an array or string) to be expanded into individual elements. It is denoted by three dots (...) followed by the iterable is used in the following ways:

## 1. Array manipulation

### Copying arrays : Easily creates copies of arrays without mutating the original array.

```js
const originalArray = [1, 2, 3];
const copyArray = [...originalArray];
```

### Concatenating arrays : Easily concatenates two arrays without mutating the original arrays.

```js
const array1 = [1, 2, 3];
const array2 = [4, 5, 6];
const concatArray = [...array1, ...array2];
```

### Adding elements to arrays : Easily adds elements to an array without mutating the original array.

```js
const originalArray = [1, 2, 3];
const newArray = [...originalArray, 4, 5, 6];
```

## 2. Function Arguments

### Passing arguments: Enables passing arrays as individual arguments to functions.

```js
const numbers = [1, 2, 3, 4, 5];
const maxNumber = Math.max(...numbers);
```

## 3. Object manipulation(ES2018+)

### Copying objects : Easily creates copies of objects without mutating the original object.

```js
const originalObject = { a: 1, b: 2, c: 3 };
const copyObject = { ...originalObject };
```

### Merging objects : Easily merges two objects without mutating the original objects.

```js
const object1 = { a: 1, b: 2, c: 3 };
const object2 = { d: 4, e: 5, f: 6 };
const mergedObject = { ...object1, ...object2 };
```

## Rest Parameters (Function Parameters)

### collecting remaining parameters: Gathers remaining arguments into an array.

```js
function sum(...numbers) {
  return numbers.reduce((acc, cur) => acc + cur, 0);
}
```

## Note

### The spread operator only performs a shallow copy, not a deep copy. This means that nested arrays and objects will still be referenced in the new array.

### The spread operator is a versatile tool that simplifies array and object manipulation in JavaScript. It is a useful feature that is worth learning and using in your code.
