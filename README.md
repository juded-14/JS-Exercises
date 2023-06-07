# JavaScript Exercises

## 1. Number Guessing Game

### Description:

This is a simple guessing game where a number between 1 and 100 is randomly
generated and the user has to guess it. The game gives feedback whether the
guessed number is too high, too low, or correct.

### Step-by-step guide:

1. Generate a random number and store it in a variable.
2. Ask the user to guess a number.
3. Compare the guessed number with the generated number.
4. If the guessed number is higher, inform the user that their guess is too
   high.
5. If the guessed number is lower, inform the user that their guess is too low.
6. If the guessed number is equal to the generated number, congratulate the
   user.
7. Repeat steps 2-6 until the user guesses the correct number.

### JavaScript features/functions used:

`Math.random`, `Math.floor`, `parseInt`, `if/else`, `alert`, `prompt`

## 2. Inventory System

### Description:

This is a basic inventory system for a store. The inventory is represented as an
array of objects, each with properties like "name", "price", and "quantity".
Functions allow for adding, removing, or updating items in the inventory, and
calculating the total value of the inventory.

### Step-by-step guide:

1. Create an empty array to store the inventory items.
2. Define a function to add items to the inventory. This function should create
   an object with the given name, price, and quantity, and push it to the array.
3. Define a function to remove items from the inventory. This function should
   filter the array to remove the item with the given name.
4. Define a function to update items in the inventory. This function should loop
   through the array and update the price and quantity of the item with the
   given name.
5. Define a function to calculate the total value of the inventory. This
   function should loop through the array, multiply the price and quantity of
   each item, and add up the results.

### JavaScript features/functions used:

`Array.push`, `Array.filter`, `for` loop, `if` statement, objects

## 3. Library System

### Description:

This is a basic library system where books are represented as objects. Each book
has properties like "title", "author", "isAvailable", and "patron". Functions
allow for checking out and returning books, and displaying the status of all
books.

### Step-by-step guide:

1. Create an empty array to store the books.
2. Define a function to add books to the library. This function should create an
   object with the given title and author, and push it to the array.
3. Define a function to check out books. This function should loop through the
   array and update the "isAvailable" and "patron" properties of the book with
   the given title.
4. Define a function to return books. This function should loop through the
   array and update the "isAvailable" and "patron" properties of the book with
   the given title.
5. Define a function to display the status of all books. This function should
   loop through the array and print the properties of each book.

### JavaScript features/functions used:

`Array.push`, `for` loop, `if` statement, objects, `console.log`

## 4. Temperature Converter

### Description:

This is a simple program that converts temperatures from Fahrenheit to Celsius
and vice versa. The user inputs a temperature and a unit to convert to, and the
program displays the converted temperature.

### Step-by-step guide:

1. Define a function to convert temperatures. This function should take a
   temperature and a unit as parameters, and return the converted temperature.
2. Ask the user to input a temperature.
3. Ask the user to input a unit to convert to.
4. Pass the inputted temperature and unit to the conversion function and store
   the result.
5. Display the result to the user.

### JavaScript features/functions used:

`parseFloat`, `isNaN`, `if/else`, `alert`, `prompt`

## JavaScript Features/Functions

```javascript
// An object in JavaScript
let item = {
  name: "Apple",
  price: 1.0,
  quantity: 10,
};

// Displaying an object property using alert
alert(item.name);

// Asking the user for input using prompt and storing it in a variable
let userGuess = prompt("Guess the price of the apple:");

// Converting the user's guess from a string to an integer using parseInt
let guessedPrice = parseInt(userGuess);

// Checking if the conversion was successful using isNaN
if (isNaN(guessedPrice)) {
  alert("That's not a valid number!");
} else {
  // Using if/else for control flow
  if (guessedPrice > item.price) {
    alert("Too high! Try again.");
  } else if (guessedPrice < item.price) {
    alert("Too low! Try again.");
  } else {
    alert("Congratulations! You guessed the price!");
  }
}

// An array in JavaScript
let array = [];

// Adding an item to the end of the array using Array.push
array.push(item);

// Filtering the array using Array.filter
let expensiveItems = array.filter((item) => item.price > 0.5);

// Printing the expensive items
console.log(expensiveItems);

// Generating a random number between 1-10 using Math.random and Math.floor
let randomNumber = Math.floor(Math.random() * 10) + 1;
console.log(randomNumber);

// Converting a string to a float using parseFloat
let floatPrice = parseFloat("1.25");
console.log(floatPrice);

// Using a for loop to iterate over the array
for (let i = 0; i < array.length; i++) {
  console.log(array[i]);
}
```
