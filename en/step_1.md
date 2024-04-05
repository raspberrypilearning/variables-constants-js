A variable in programming is a named area of memory that holds a value. The value can be changed when the program runs.
For example, `var age = 30;` `age` is the variable holding the value `30`

You can create variables using various keywords such as `var` and `let` Each of these keywords has slightly different behaviors and use cases.

`let` is a more modern way to assign variables and can be used globally(throughout the program) or within a specific block of code.

--- code ---
---
language: js
filename: script.js
line_numbers: true
---

  // Using let to declare a variable
  let myLet = "Hello, World!";

  // Reassigning the variable
  myLet = "JavaScript is awesome!";

  // Variables declared with let are for use within the block
  if (true) {
      let blockVar = "I am a block-scoped variable.";
      console.log(blockVar);
  }

  console.log(myLet); // Outputs: JavaScript is awesome!
  console.log(blockVar); // ReferenceError: blockVar is not defined (outside the block)
    
--- /code ---

`var` is an older way of assigning variables because it could not be used within a specific block of code.

--- code ---
---
language: js
filename: script.js
line_numbers: true
---

  // Using var to declare a variable
  var myVar = "Hello, World!";

  // Reassigning the variable
  myVar = "JavaScript is awesome!";

  // Variables declared with var are function-scoped
  function exampleFunction() {
      var localVar = "I am a local variable.";
      console.log(localVar);
  }

  console.log(myVar); // Outputs: JavaScript is awesome!
  console.log(localVar); // ReferenceError: localVar is not defined (outside the function)
    
--- /code ---

A constant is like a variable; it is a named data value that can't change; once set, its value stays the same.
Therefore, you cannot reassign the value of a constant once you have declared it.

For example, `const PI = 3.3.14159265359;`;
`PI` cannot be assigned another value throughout the program.

--- code ---
---
language: js
filename: script.js
line_numbers: true
---

  // Using const to declare a constant
  const myConst = "Hello, World!";

  // Trying to reassign a constant (will show an error)
  // myConst = "JavaScript is awesome!"; // TypeError: Assignment to a constant variable.

  // Variables declared with const are for use within that block
  if (true) {
      const blockConst = "I am a block-scoped constant.";
      console.log(blockConst);
  }

  console.log(myConst); // Outputs: Hello, World!
  console.log(blockConst); // ReferenceError: blockConst is not defined (outside the block)
    
--- /code ---


