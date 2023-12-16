## Key Points to Remember for Object Destructuring in JavaScript

Object destructuring is a powerful feature that allows you to extract properties from objects into separate variables. It's a great way to make your code more concise and readable, especially when dealing with large or nested objects.

Here are some key points to keep in mind when using object destructuring:

1. **Square Braces Denote Destructuring:** Object destructuring is initiated and concluded using curly braces `{}`.

2. **Variable Names Correspond to Property Names:** Specify the names of the variables you want to extract, aligning them with the names of the corresponding object properties.

```js
const restaurant = {
  name: "Classico Italiano",
  location: "Via Angelo Tavanti 23, Firenze, Italy",
  categories: ["Italian", "Pizzeria", "Vegetarian", "Organic"],
  starterMenu: ["Focaccia", "Bruschetta", "Garlic Bread", "Caprese Salad"],
  mainMenu: ["Pizza", "Pasta", "Risotto"],

  openingHours: {
    thu: {
      open: 12,
      close: 22,
    },
    fri: {
      open: 11,
      close: 23,
    },
    sat: {
      open: 0, // Open 24 hours
      close: 24,
    },
  },

  order: function (starterIndex, mainIndex) {
    return [this.starterMenu[starterIndex], this.mainMenu[mainIndex]];
  },
};

// need to use the same name as the property
const { name, openingHours, categories } = restaurant;
console.log(name, openingHours, categories); /// Classico Italiano {thu: {…}, fri: {…}, sat: {…}} (4) ["Italian", "Pizzeria", "Vegetarian", "Organic"]
```

3. **Destructuring Single Properties:** You can extract a single property by placing its name inside square brackets `[]` within the curly braces `{}`.

4. **Spread Operator (`...`) for Nested Objects:** Use the spread operator (`...`) to extract the entire contents of an object into a single variable.

5. **Matching Properties with Index Positions:** For object properties with numeric indices, you can use the index position instead of the property name.

6. **Rest Operator (`...`) for Extra Properties:** Use the rest operator (`...`) to capture additional properties that don't have corresponding variables.

7. **Combining Destructuring with Spread Operator:** Destructuring can be combined with the spread operator to extract specific properties or reorder them.

Remember, object destructuring is a valuable tool for simplifying your JavaScript code and accessing data from objects more effectively.

### different name

```js
const {
  name: restaurantName,
  openingHours: hours,
  categories: tags,
} = restaurant;
console.log(restaurantName, hours, tags); // Classico Italiano {thu: {…}, fri: {…}, sat: {…}} (4) ["Italian", "Pizzeria", "Vegetarian", "Organic"]
```

The provided JavaScript snippet demonstrates the concept of object destructuring with a renaming syntax. This is a feature in ES6 that allows you to unpack values from objects or arrays into distinct variables.

In the given code, an object named `restaurant` is being destructured into three new variables: `restaurantName`, `hours`, and `tags`. The syntax `{name: restaurantName}` means "extract the property `name` from the object and assign it to a new variable called `restaurantName`". The same is done for `openingHours` and `categories`, which are assigned to `hours` and `tags` respectively.

### default value

specify a default value for a variable that does not have a corresponding property in the object.

```js
const { menu = [], starterMenu: starters = [] } = restaurant;
console.log(menu, starters); // [] (4) ["Focaccia", "Bruschetta", "Garlic Bread", "Caprese Salad"]
```

### mutating variables

```js
let a = 111;
let b = 999;
const obj = { a: 23, b: 7, c: 14 };

// By adding the parentheses around the entire assignment, we inform the JavaScript interpreter that we are not defining a block of code but rather assigning a value.
({ a, b } = obj);
console.log(a, b); // 23 7
```

### nested objects

```js
const {
  fri: { open: o, close: c },
} = openingHours;
console.log(o, c); // 11 23
```

### object as a function parameter

```js
const add = function ({ a, b }) {
  return a + b;
};

console.log(add({ a: 2, b: 3 })); // 5
```

### default values for function parameters

```js
const add = function ({ a, b, c = 1 }) {
  return a + b + c;
};

console.log(add({ a: 2, b: 3 })); // 6
```
