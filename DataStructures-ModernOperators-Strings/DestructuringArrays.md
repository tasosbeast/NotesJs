## Remembering Array Destructuring

To effectively utilize array destructuring in your JavaScript code, memorize these key points:

1. **Square Brackets Denote Destructuring:** Array destructuring is initiated and concluded using square brackets `[]`.

```js
const arr = [1, 2, 3, 4, 5, 6, 7, 8];
const [x, y, z] = arr;
```

2. **Variable Names Correspond to Array Elements:** Specify the names of the variables you want to extract, aligning them with the positions of the corresponding array elements.

3. **Trailing Commas Bypass Extra Elements:** Employ trailing commas to skip or ignore remaining elements in an uneven array, enhancing code readability.

```js
const [first, , second] = restaurant.categories;
```

4. **Destructuring Embraces Nested Structures:** Array destructuring extends to nested arrays and objects, enabling efficient extraction of data from intricate data structures.

### Switching Variables

Destructuring arrays is a great way to switch the values of two variables without the need for a temporary variable.

```js
[first, second] = [second, first];
```

### Nested destructuring

Destructuring arrays can be nested to extract data from nested arrays.

```js
const nested = [2, 4, [5, 6]];
const [i, , j] = nested;
console.log(i, j); // 2 [5, 6]

const [i, , [j, k]] = nested;
console.log(i, j, k); // 2 5 6
```
