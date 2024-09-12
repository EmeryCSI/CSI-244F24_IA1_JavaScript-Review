# Renton Technical College CSI-244

<br />

![RTC Logo](logo.jpg)

This tutorial is part of CSI-244 at Renton Technical College.

## Independent Activity I - JavaScript Fundamentals Review

### Part 1 - Setup

1. Clone this repository to your local machine using either the terminal or GitHub Desktop.
   - If using the terminal, use the following command:
     ```
     git clone [repository-url]
     ```
   - If using GitHub Desktop, click on "File" > "Clone Repository" and select the repository.

2. Navigate to the cloned repository directory in your terminal:
   ```
   cd [repository-name]
   ```

3. Before you can complete this assignment, you MUST have Node.js installed on your computer.

4. We will start this assignment as a group in class. Refer to the lecture videos for reference.

5. If you do not have Node.js installed, come to office hours or make an appointment with myself or a TA to get this set up.

6. Verify your Node.js installation by running:
   ```
   node --version
   ```

7. Create a new JavaScript file named `app.js` in the root of your local repository:
   ```
   new-item app.js  # For Windows
   # OR
   touch app.js  # For Mac/Linux
   ```

8. Open `app.js` in your preferred code editor.

9. As you complete each part of this assignment, be sure to save your work in `app.js` before committing and pushing your changes.

### Part 2 - Basic JavaScript Concepts

In this section, we'll cover the fundamental building blocks of JavaScript programming.

1. Variables and Data Types:
   ```javascript
   // Variables can be declared using let, const, or var
   let name = "John Doe";  // String data type, can be reassigned
   const age = 30;  // Number data type, cannot be reassigned
   var isStudent = true;  // Boolean data type, older way of declaring variables
   
   // Template literals allow for easy string interpolation
   console.log(`Name: ${name}, Age: ${age}, Is Student: ${isStudent}`);
   ```
   Note: It's generally recommended to use `let` and `const` over `var` in modern JavaScript.

2. Functions:
   In JavaScript, there are several ways to create functions. Let's explore each:

   a. Function Declaration:
   ```javascript
   function greet(name) {
     return `Hello, ${name}!`;
   }
   console.log(greet("Alice"));
   ```
   This is the most traditional way to define a function. Function declarations are hoisted, meaning they can be called before they are defined in the code.

   b. Function Expression:
   ```javascript
   const greet = function(name) {
     return `Hello, ${name}!`;
   };
   console.log(greet("Bob"));
   ```
   This assigns an anonymous function to a variable. Function expressions are not hoisted, so they can only be called after they are defined.

   c. Arrow Function:
   ```javascript
   const greet = (name) => {
     return `Hello, ${name}!`;
   };
   console.log(greet("Charlie"));
   ```
   Arrow functions provide a more concise syntax. They also handle `this` keyword differently than traditional functions.

   d. Concise Arrow Function:
   ```javascript
   const greet = name => `Hello, ${name}!`;
   console.log(greet("David"));
   ```
   For simple functions that just return a value, you can make them even more concise by removing the curly braces and `return` keyword.

3. Arrays and Objects:
   ```javascript
   // Arrays are ordered lists
   let fruits = ["apple", "banana", "orange"];
   
   // Objects are collections of key-value pairs
   let person = {
     name: "Bob",
     age: 25,
     city: "Seattle"
   };
   
   console.log(fruits);
   console.log(person);
   ```
   Arrays and objects are fundamental data structures in JavaScript for organizing and storing data.

### Part 2 - Practice Exercises

Complete the following exercises in `app.js`:

1. Create a function called `calculateArea` that takes the length and width of a rectangle as parameters and returns its area.

2. Create an object representing a movie with properties for title, director, and releaseYear. Add a method to the object that returns a string with the movie's details.

3. Convert the following function to an arrow function:
   ```javascript
   function multiply(a, b) {
     return a * b;
   }
   ```

After completing these exercises, commit your changes:

```
git add .
git commit -m "Completed Part 2"
git push
```

### Part 3 - Loops in JavaScript

In this section, we'll explore different types of loops in JavaScript. Loops are essential for iterating over data structures and performing repetitive tasks efficiently.


1. For Loop:
   The most traditional type of loop in JavaScript.

   ```javascript
   console.log("For Loop:");
   for (let i = 0; i < 5; i++) {
     console.log(i);
   }
   ```

2. While Loop:
   Executes a block of code as long as a specified condition is true.

   ```javascript
   console.log("While Loop:");
   let count = 0;
   while (count < 5) {
     console.log(count);
     count++;
   }
   ```

3. Do...While Loop:
   Similar to the while loop, but it always executes the code block at least once before checking the condition.

   ```javascript
   console.log("Do...While Loop:");
   let x = 0;
   do {
     console.log(x);
     x++;
   } while (x < 5);
   ```

4. For...Of Loop:
   Used to iterate over iterable objects (arrays, strings, etc.).

   ```javascript
   console.log("For...Of Loop:");
   const fruits = ["apple", "banana", "cherry"];
   for (const fruit of fruits) {
     console.log(fruit);
   }
   ```

5. For...In Loop:
   Used to iterate over the enumerable properties of an object.

   ```javascript
   console.log("For...In Loop:");
   const person = { name: "John", age: 30, city: "New York" };
   for (const key in person) {
     console.log(key + ": " + person[key]);
   }
   ```

6. forEach Method:
   A method on arrays to execute a provided function once for each array element.

   ```javascript
   console.log("forEach Method:");
   const numbers = [1, 2, 3, 4, 5];
   numbers.forEach(function(number) {
     console.log(number);
   });
   ```

### Part 3 - Practice Exercises

Complete the following exercises in `app.js`:

1. Use a `for` loop to print the numbers from 1 to 10.

2. Create an array of 5 fruits. Use a `foreach` loop to print each fruit to the console.

3. Create an array of numbers. Use a `for...of` loop to calculate and print the sum of all numbers in the array.

4. Create an object representing a car with properties like make, model, and year. Use a `for...in` loop to print all the properties and their values.

After completing these exercises, commit your changes:

```
git add app.js
git commit -m "Completed Part 3 exercises on Loops"
git push
```

### Part 4 - Destructuring, Spread, and Rest Operators

This section introduces powerful JavaScript features that allow for more elegant and efficient code: destructuring, spread, and rest operators.

1. Object Destructuring:
   Object destructuring allows you to extract multiple properties from an object and assign them to variables in a single statement.

   ```javascript
   // Basic object destructuring
   const person = { firstName: "John", lastName: "Doe", age: 30 };
   const { firstName, lastName } = person;
   console.log(firstName, lastName); // Output: John Doe

   // Assigning to different variable names
   const { firstName: fName, lastName: lName } = person;
   console.log(fName, lName); // Output: John Doe

   // Setting default values
   const { age, occupation = "Unknown" } = person;
   console.log(age, occupation); // Output: 30 Unknown
   ```

2. Array Destructuring:
   Array destructuring allows you to extract multiple elements from an array and assign them to variables in a single statement.

   ```javascript
   // Basic array destructuring
   const colors = ["red", "green", "blue"];
   const [firstColor, secondColor] = colors;
   console.log(firstColor, secondColor); // Output: red green

   // Skipping elements
   const [, , thirdColor] = colors;
   console.log(thirdColor); // Output: blue

   // Swapping variables
   let a = 1, b = 2;
   [a, b] = [b, a];
   console.log(a, b); // Output: 2 1
   ```

3. Spread Operator:
   The spread operator (...) allows an iterable (like an array or string) to be expanded in places where zero or more arguments or elements are expected.

   ```javascript
   // Combining arrays
   const arr1 = [1, 2, 3];
   const arr2 = [4, 5, 6];
   const combinedArray = [...arr1, ...arr2];
   console.log(combinedArray); // Output: [1, 2, 3, 4, 5, 6]

   // Copying arrays
   const originalArray = [1, 2, 3];
   const copiedArray = [...originalArray];
   
   // Spreading into function arguments
   function sum(x, y, z) {
     return x + y + z;
   }
   const numbers = [1, 2, 3];
   console.log(sum(...numbers)); // Output: 6

   // Spreading object properties
   const basicInfo = { firstName: "John", lastName: "Doe" };
   const detailedInfo = { ...basicInfo, age: 30, occupation: "Developer" };
   console.log(detailedInfo);
   // Output: { firstName: "John", lastName: "Doe", age: 30, occupation: "Developer" }
   ```

4. Rest Operator:
   The rest operator (...) allows you to represent an indefinite number of arguments as an array. It's used in function parameters or in destructuring assignments.

   ```javascript
   // Rest in function parameters
   function sum(...numbers) {
     return numbers.reduce((total, num) => total + num, 0);
   }
   console.log(sum(1, 2, 3, 4)); // Output: 10

   // Rest in array destructuring
   const [first, second, ...rest] = [1, 2, 3, 4, 5];
   console.log(first, second, rest); // Output: 1 2 [3, 4, 5]

   // Rest in object destructuring
   const { a, b, ...others } = { a: 1, b: 2, c: 3, d: 4 };
   console.log(a, b, others); // Output: 1 2 { c: 3, d: 4 }
   ```

### Part 4 - Practice Exercises

Complete the following exercises in `app.js`:

1. Given the object `{ name: "Alice", age: 25, city: "New York", country: "USA" }`, use object destructuring to extract the `name` and `age` properties. Then, use rest to collect the remaining properties into a new object called `location`.

2. Create an array of numbers `[1, 2, 3, 4, 5]`. Use array destructuring to assign the first two numbers to variables `a` and `b`, and the rest of the numbers to a variable `remaining`.

3. Write a function `printPersonInfo` that takes an object with properties `name`, `age`, and `occupation`. Use object destructuring in the function parameter to extract these properties, and provide a default value of "Unknown" for `occupation`.


After completing these exercises, commit your changes:

```
git add .
git commit -m "Completed Part 4"
git push
```

### Part 5 - Callbacks in JavaScript

Callbacks are a fundamental concept in JavaScript, especially for handling asynchronous operations. A callback is a function that is passed as an argument to another function and is executed after the first function has completed.

1. Basic Callback Example:
   ```javascript
   function greet(name, callback) {
     console.log('Hello ' + name);
     callback();
   }

   function callMe() {
     console.log('I am callback function');
   }

   greet('John', callMe);
   ```
   In this example, `callMe` is passed as a callback to the `greet` function.

2. Callbacks with Arguments:
   ```javascript
   function calculateSquare(number, callback) {
     const result = number * number;
     callback(result);
   }

   function displayResult(result) {
     console.log('The square is: ' + result);
   }

   calculateSquare(5, displayResult);
   ```
   Here, the callback `displayResult` receives the result as an argument.

3. Anonymous Function as Callback:
   ```javascript
   setTimeout(function() {
     console.log('This message is shown after 3 seconds');
   }, 3000);
   ```
   An anonymous function is used as a callback for `setTimeout`.

4. Error Handling in Callbacks:
   ```javascript
   function divideNumbers(a, b, callback) {
     if (b === 0) {
       callback(new Error('Cannot divide by zero'), null);
     } else {
       callback(null, a / b);
     }
   }

   divideNumbers(10, 2, function(error, result) {
     if (error) {
       console.error('Error:', error.message);
     } else {
       console.log('Result:', result);
     }
   });
   ```
   This pattern is common in Node.js for handling errors in asynchronous operations.

5. Callback Hell:
   ```javascript
   asyncOperation1(function(result1) {
     asyncOperation2(result1, function(result2) {
       asyncOperation3(result2, function(result3) {
         // This nesting can go on...
       });
     });
   });
   ```
   This demonstrates the potential for deeply nested callbacks, often referred to as "callback hell". This is one of the reasons why Promises and async/await were introduced in later versions of JavaScript.

### Part 5 - Practice Exercises

Complete the following exercises in `app.js`:

1. Write a function `fetchUserData` that takes a userId and a callback function as parameters. The function should simulate fetching user data from a server (use `setTimeout` to simulate delay) and then call the callback with an object containing user information.

2. Call fetchUserData using a traditional Function Declaration as the callback.

3. Call fectchUserData using an arrow function as the callback.

After completing these exercises, commit your changes:

```
git add .
git commit -m "Completed"
git push
```
