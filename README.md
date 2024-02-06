# JavaScript-Q10
Write a JavaScript program that demonstrates the use of the 'try-catch-finally' statement to catch and handle an error, and then execute some cleanup code in the 'finally' block.

function divide_Numbers(x, y) {
  try {
    if (typeof x !== 'number' || typeof y !== 'number') {
      throw new TypeError('Invalid arguments. Both arguments should be numbers.');
    }

    if (y === 0) {
      throw new Error('Invalid divisor. Cannot divide by zero.');
    }
    const result = x / y;
    console.log('Result:', result);
  } catch (error) {
    console.log('Error:', error.message);
  } finally {
    console.log('Cleanup code executed.');
  }
}

// Example:
divide_Numbers(10, 2);  //  Valid division
divide_Numbers(10, 0); // Division by zero
divide_Numbers(10, '2'); // Invalid divisor

**Sample Output:**

"Result:"
5
"Cleanup code executed."
"Error:"
"Invalid divisor. Cannot divide by zero."
"Cleanup code executed."
"Error:"
"Invalid arguments. Both arguments should be numbers."
"Cleanup code executed."
