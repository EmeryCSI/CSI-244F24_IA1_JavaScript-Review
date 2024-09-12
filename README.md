# Renton Technical College CSI-244

<br />

![RTC Logo](Images/logo.jpg)

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
   touch app.js  # For Mac/Linus
   ```

8. Open `app.js` in your preferred code editor.

9. As you complete each part of this assignment, be sure to save your work in `app.js` before committing and pushing your changes.

Now, let's proceed with the JavaScript fundamentals review.

### Part 2 - Basic JavaScript Concepts

1. Variables and Data Types:
   ```javascript
   // Add this to app.js
   let name = "John Doe";
   const age = 30;
   var isStudent = true;
   
   console.log(`Name: ${name}, Age: ${age}, Is Student: ${isStudent}`);
   ```

2. Functions:
   ```javascript
   // Add this to app.js
   function greet(name) {
     return `Hello, ${name}!`;
   }
   
   console.log(greet("Alice"));
   ```

3. Arrays and Objects:
   ```javascript
   // Add this to app.js
   let fruits = ["apple", "banana", "orange"];
   let person = {
     name: "Bob",
     age: 25,
     city: "Seattle"
   };
   
   console.log(fruits);
   console.log(person);
   ```

4. Run your code using Node.js:
   ```
   node app.js
   ```

### Part 2 - Practice Exercises

Complete the following exercises in `app.js`:

1. Create a function that takes two numbers as parameters and returns their sum.
2. Create an array of numbers and use the `map` function to create a new array with each number squared.
3. Create an object representing a car with properties for make, model, and year. Add a method to the object that returns a string with the car's details.

### Part 3 - Advanced JavaScript Concepts

1. Arrow Functions:
   ```javascript
   // Add this to app.js
   const multiply = (a, b) => a * b;
   console.log(multiply(4, 5));
   ```

2. Object Destructuring:
   ```javascript
   // Add this to app.js
   const person = { name: "Alice", age: 30, city: "New York" };
   const { name, age, city } = person;
   console.log(`${name} is ${age} years old and lives in ${city}`);
   ```

3. Array Destructuring:
   ```javascript
   // Add this to app.js
   const colors = ["red", "green", "blue"];
   const [firstColor, secondColor, thirdColor] = colors;
   console.log(`First color: ${firstColor}, Second color: ${secondColor}, Third color: ${thirdColor}`);
   ```

4. Spread Operator:
   ```javascript
   // Add this to app.js
   const newFruits = [...fruits, "grape"];
   console.log(newFruits);
   ```

### Part 3 - Practice Exercises

1. Rewrite the sum function from Part 2 using an arrow function.
2. Create an object with at least 5 properties and use object destructuring to extract 3 of them in a single line.
3. Create an array with at least 5 elements and use array destructuring to assign the first, third, and fifth elements to variables.
4. Use the spread operator to merge two arrays into a new array.

### Part 4 - Advanced Destructuring and Default Values

1. Nested Object Destructuring:
   ```javascript
   // Add this to app.js
   const user = {
     id: 1,
     name: "John Doe",
     address: {
       street: "123 Main St",
       city: "Anytown",
       country: "USA"
     }
   };
   
   const { name, address: { city, country } } = user;
   console.log(`${name} lives in ${city}, ${country}`);
   ```

2. Array Destructuring with Rest:
   ```javascript
   // Add this to app.js
   const numbers = [1, 2, 3, 4, 5];
   const [first, second, ...rest] = numbers;
   console.log(`First: ${first}, Second: ${second}, Rest: ${rest}`);
   ```

3. Default Values in Destructuring:
   ```javascript
   // Add this to app.js
   const settings = { theme: "dark" };
   const { theme, fontSize = 16 } = settings;
   console.log(`Theme: ${theme}, Font Size: ${fontSize}`);
   ```

4. Combining Array and Object Destructuring:
   ```javascript
   // Add this to app.js
   const people = [
     { name: "Alice", age: 30 },
     { name: "Bob", age: 25 }
   ];
   const [{ name: firstName }, { age: secondAge }] = people;
   console.log(`First person's name: ${firstName}, Second person's age: ${secondAge}`);
   ```

### Part 4 - Practice Exercises

1. Create a nested object representing a company with departments. Use nested destructuring to extract the name of a sub-department.
2. Write a function that takes an array as an argument and uses array destructuring with rest to separate the first two elements from the rest.
3. Create an object with some properties and use destructuring with default values to extract properties that may not exist in the object.
4. Given an array of objects representing students, use a combination of array and object destructuring to extract specific properties from the second student.

### Part 5 - Practical Applications of Destructuring

1. Function Parameter Destructuring:
   ```javascript
   // Add this to app.js
   function printUserInfo({ name, age, email = "N/A" }) {
     console.log(`Name: ${name}, Age: ${age}, Email: ${email}`);
   }
   
   const user1 = { name: "Alice", age: 30, email: "alice@example.com" };
   const user2 = { name: "Bob", age: 25 };
   
   printUserInfo(user1);
   printUserInfo(user2);
   ```

2. Destructuring in Loops:
   ```javascript
   // Add this to app.js
   const products = [
     { id: 1, name: "Laptop", price: 1000 },
     { id: 2, name: "Phone", price: 500 },
     { id: 3, name: "Tablet", price: 300 }
   ];
   
   for (const { name, price } of products) {
     console.log(`${name} costs $${price}`);
   }
   ```

3. Swapping Variables:
   ```javascript
   // Add this to app.js
   let a = 5, b = 10;
   [a, b] = [b, a];
   console.log(`a = ${a}, b = ${b}`);
   ```

4. Destructuring Return Values:
   ```javascript
   // Add this to app.js
   function getMinMax(numbers) {
     return [Math.min(...numbers), Math.max(...numbers)];
   }
   
   const [min, max] = getMinMax([3, 1, 4, 1, 5, 9, 2, 6]);
   console.log(`Min: ${min}, Max: ${max}`);
   ```

### Part 5 - Practice Exercises

1. Write a function that takes an object as a parameter and uses destructuring to extract and use multiple properties.
2. Create an array of objects and use destructuring in a `forEach` loop to log specific properties of each object.
3. Implement a function that returns an object with multiple properties, and use destructuring to extract these properties when calling the function.
4. Use array destructuring to easily swap the values of three variables without using a temporary variable.

### Submitting Your Work

After completing the practice exercises for each part:

1. Save your JavaScript files in your project directory.
2. Open your git bash terminal in the project directory.
3. Type `git add .` to stage your new files.
4. Type `git commit -m "Completed JavaScript Fundamentals Review"`.
5. Type `git push` to submit your work.

If you have any questions about this assignment, please reach out to your instructor or the TA for this course.

Feel free to message your instructor or the TA on Canvas if you need any clarification.
