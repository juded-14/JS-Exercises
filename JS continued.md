# Spread Operators

The spread operator is a versatile and powerful feature in JavaScript that allows you to expand iterable elements. This can be used with arrays, objects, and function arguments.

## Spread Operator with Arrays

### Concatenating Arrays
You can use the spread operator to combine two or more arrays.
```javascript
const array1 = [1, 2, 3];
const array2 = [4, 5, 6];
const combinedArray = [...array1, ...array2];

console.log(combinedArray); // Outputs [1, 2, 3, 4, 5, 6]
```

### Cloning Arrays
You can create a shallow copy of an array by using the spread operator. This is useful when you want to create a new array that does not affect the original one.
```javascript
const originalArray = [1, 2, 3];
const clonedArray = [...originalArray];

clonedArray.push(4);
console.log(originalArray); // Outputs [1, 2, 3]
console.log(clonedArray);   // Outputs [1, 2, 3, 4]
```

### Inserting Elements
You can use the spread operator to insert elements of an array into a new array.
```javascript
const firstPart = [1, 2];
const lastPart = [4, 5];
const middle = 3;
const combined = [...firstPart, middle, ...lastPart];

console.log(combined); // Outputs [1, 2, 3, 4, 5]
```

### Splitting Strings into Arrays
The spread operator can be used to split a string into an array of characters.
```javascript
const str = "hello";
const chars = [...str];

console.log(chars); // Outputs ['h', 'e', 'l', 'l', 'o']
```

## Spread Operator with Objects

### Cloning Objects
Similar to arrays, the spread operator can be used to create a shallow copy of an object.
```javascript
const originalObject = { a: 1, b: 2 };
const clonedObject = { ...originalObject };

clonedObject.c = 3;
console.log(originalObject); // Outputs { a: 1, b: 2 }
console.log(clonedObject);   // Outputs { a: 1, b: 2, c: 3 }
```

### Merging Objects
You can merge multiple objects into one.
```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };
const mergedObject = { ...obj1, ...obj2 };

console.log(mergedObject); // Outputs { a: 1, b: 3, c: 4 }
```

### Adding or Overriding Properties
You can add new properties or override existing properties in an object.
```javascript
const obj = { a: 1, b: 2 };
const newObj = { ...obj, b: 3, c: 4 };

console.log(newObj); // Outputs { a: 1, b: 3, c: 4 }
```

## Spread Operator in Function Calls
The spread operator can also be used to pass elements of an array as arguments to a function.
```javascript
const numbers = [1, 2, 3];
function add(a, b, c) {
  return a + b + c;
}
console.log(add(...numbers)); // Outputs 6
```

# Destructuring

Destructuring is a convenient way of extracting multiple values from data stored in arrays and objects.

## Array Destructuring

### Basic Destructuring
You can assign the elements of an array to individual variables.
```javascript
const colors = ["red", "green", "blue"];
const [color1, color2, color3] = colors;

console.log(color1); // Outputs "red"
console.log(color2); // Outputs "green"
console.log(color3); // Outputs "blue"
```

### Skipping Elements
You can also skip elements that you don't need.
```javascript
const numbers = [1, 2, 3, 4, 5];
const [first, , , fourth] = numbers;

console.log(first);  // Outputs 1
console.log(fourth); // Outputs 4
```

### Rest Pattern
You can use the rest pattern to collect the remaining elements into an array.
```javascript
const numbers = [1, 2, 3, 4, 5];
const [first, second, ...rest] = numbers;

console.log(rest); // Outputs [3, 4, 5]
```

### Default Values
You can assign default values to variables if the array element is `undefined`.
```javascript
const [a = 1, b = 2] = [3];

console.log(a); // Outputs 3
console.log(b); // Outputs 2
```

## Object Destructuring

### Basic Destructuring
You can assign the properties of an object to individual variables.
```javascript
const person = { name: "Alice", age: 30 };
const { name, age } = person;

console.log(name); // Outputs "Alice"
console.log(age);  // Outputs 30
```

### Default Values
You can provide default values if the property doesn’t exist.
```javascript
const { city = "New York", country } = { country: "USA" };

console.log(city);    // Outputs "New York"
console.log(country); // Outputs "USA"
```

### Renaming
You can also rename variables while destructuring.
```javascript
const { name: firstName, age: userAge } = { name: "Bob", age: 28 };

console.log(firstName); // Outputs "Bob"
console.log(userAge);   // Outputs 28
```

### Nested Object Destructuring
You can destructure nested objects.
```javascript
const student = {
  name: "Alice",
  scores: {
    maths: 90,
    science: 85,
  },
};

const {
  name,
  scores: { maths, science },
} = student;

console.log(name, maths, science); // Outputs "Alice 90 85"
```

### Combining with Rest Pattern
You can combine object destructuring with the rest pattern.
```javascript
const { a, b, ...remaining } = { a: 1, b: 2, c: 3, d: 4 };

console.log(a);         // Outputs 1
console.log(b);         // Outputs 2
console.log(remaining); // Outputs { c: 3, d: 4 }
```

