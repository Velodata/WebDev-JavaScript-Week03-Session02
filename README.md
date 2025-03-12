# WebDev-JavaScript-Week03-Session02
In this lesson we'll be learning about conditional statements and do-while-for-loops.  Happy coding dear students!


# JavaScript Control Structures

## Conditional Statements

### 1. The `if` Statement
The `if` statement allows you to execute a block of code only if a specified condition is `true`.

#### Syntax:
```javascript
if (condition) {
    // Code to execute if the condition is true
}
```

#### Example:
```javascript
let age = 18;

if (age >= 18) {
    console.log("You are eligible to vote.");
}
```

---

### 2. The `else` Statement
The `else` statement executes a block of code when the `if` condition is `false`.

#### Syntax:
```javascript
if (condition) {
    // Code if condition is true
} else {
    // Code if condition is false
}
```

#### Example:
```javascript
let temperature = 30;

if (temperature > 25) {
    console.log("It's a hot day.");
} else {
    console.log("It's a cool day.");
}
```

---

### 3. The `else if` Statement
The `else if` statement allows checking multiple conditions.

#### Syntax:
```javascript
if (condition1) {
    // Code if condition1 is true
} else if (condition2) {
    // Code if condition2 is true
} else {
    // Code if all conditions are false
}
```

#### Example:
```javascript
let score = 85;

if (score >= 90) {
    console.log("Grade: A");
} else if (score >= 80) {
    console.log("Grade: B");
} else if (score >= 70) {
    console.log("Grade: C");
} else {
    console.log("Grade: F");
}
```

---

### 4. The `switch` Statement
The `switch` statement is used to execute different blocks of code based on different conditions.

#### Syntax:
```javascript
switch (expression) {
    case value1:
        // Code to execute if expression === value1
        break;
    case value2:
        // Code to execute if expression === value2
        break;
    default:
        // Code to execute if no cases match
}
```

#### Example:
```javascript
let day = "Monday";

switch (day) {
    case "Monday":
        console.log("Start of the workweek!");
        break;
    case "Friday":
        console.log("Weekend is near!");
        break;
    default:
        console.log("It's a regular day.");
}
```

---

## Loops

### 5. The `while` Loop
The `while` loop executes a block of code as long as a specified condition is `true`.

#### Syntax:
```javascript
while (condition) {
    // Code to execute
}
```

#### Example:
```javascript
let count = 1;

while (count <= 5) {
    console.log("Count is: " + count);
    count++;
}
```

---

### 6. The `do...while` Loop
The `do...while` loop executes a block of code once before checking the condition, ensuring it runs at least once.

#### Syntax:
```javascript
do {
    // Code to execute
} while (condition);
```

#### Example:
```javascript
let num = 1;

do {
    console.log("Number: " + num);
    num++;
} while (num <= 5);
```

---

### 7. The `for` Loop
The `for` loop is used to run a block of code a specific number of times.

#### Syntax:
```javascript
for (initialization; condition; increment) {
    // Code to execute
}
```

#### Example:
```javascript
for (let i = 1; i <= 5; i++) {
    console.log("Iteration: " + i);
}
```

---

### Summary
- Use `if` to execute code based on a condition.
- Use `else` to specify code for when an `if` condition is false.
- Use `else if` to check multiple conditions.
- Use `switch` to handle multiple possible values for a variable.
- Use `while` when you want to repeat code as long as a condition is true.
- Use `do...while` when you want to ensure the loop runs at least once.
- Use `for` to run a loop for a fixed number of iterations.

Happy coding! 🚀
