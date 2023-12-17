# Spread Operator in JavaScript

The spread operator (`...`) in JavaScript is a powerful feature used for:

## 1. Array Manipulation

- **Copying Arrays:** Easily creates copies of arrays without modifying the original.

  ```javascript
  const originalArray = [1, 2, 3];
  const copyArray = [...originalArray];
  ```

- **Concatenating Arrays:** Combines arrays without mutating them.

  ```javascript
  const array1 = [1, 2, 3];
  const array2 = [4, 5, 6];
  const concatenatedArray = [...array1, ...array2];
  ```

- **Adding Elements to Arrays:** Appends new elements while preserving the original array.
  ```javascript
  const originalArray = [1, 2, 3];
  const newArray = [...originalArray, 4, 5, 6];
  ```

## 2. Function Arguments

- **Passing Arguments:** Enables passing arrays as individual arguments to functions.
  ```javascript
  const numbers = [1, 2, 3, 4, 5];
  const maxNumber = Math.max(...numbers);
  ```

## 3. Object Manipulation (ES2018+)

- **Copying Objects:** Creates shallow copies of objects.

  ```javascript
  const originalObj = { a: 1, b: 2 };
  const copyObj = { ...originalObj };
  ```

- **Merging Objects:** Combines objects into a new one.
  ```javascript
  const obj1 = { a: 1, b: 2 };
  const obj2 = { c: 3, d: 4 };
  const mergedObj = { ...obj1, ...obj2 };
  ```

## 4. Rest Parameter (Function Parameter)

- **Collecting Remaining Parameters:** Gathers remaining arguments into an array.
  ```javascript
  function sum(...numbers) {
    return numbers.reduce((acc, val) => acc + val, 0);
  }
  ```

### Note:

- The spread operator only performs a shallow copy for objects, meaning it copies references to nested objects rather than creating distinct copies.

- The spread operator is a versatile tool that simplifies array and object manipulation in JavaScript.

- works on all iterables (arrays, strings, maps, sets, etc.)
- can be used on both arrays and objects
