# Lecture 2 notes Oct 19 2023

## Incremental Development 

How to approach problem solving
* List the steps in order to solve a problem (don't think about syntax
* Step-by-step process
  * State hypothesis
  * Verify the hypothesis
  *  Make changes
* We express ourselves through code (like an author with a book)
  * Make sure your book can be understood!

## Git

* git remote -v checks for remotes (places to pull/push to) set up locally

## Practice JS, structural approach


// Write a function that adds the two highest numbers in an array

// PROBLEM SOLVING:
// 1. INPUTS -> Array (of numbers)
// 2. OUTPUTS -> A single Number (sum)
// 3. PROCESSING -> (break down our steps)
    // * Placeholder variables for 2 highest numbers    
    // * Sort from high to low?
    // * Add our two highest numbers together
  
    // [1, 2, 5, 10, 3, 1, 2]
    // [2, 1, 5, 10, 3, 1, 2]
    // (functions can be passed around as a variable! thank you JS!)
```javascript    
const compareNumbers = function(num1, num2) {
    /**
     * You should return -1, 0, +1
     */
    return num2 - num1; // 1
};

/**
 * Adds highest two numbers in array.
 * 
 * @param {Array<number>} arrayOfNums An array of numbers.
 * @return {number} The sum of the highest two numbers in the array.
 */
function sumTwoHighestNumsInArray(arrayOfNums) {
    let sum = 0;

    // * Placeholder variables for 2 highest numbers
    let highestNum1;
    let highestNum2;

    // * Sort from high to low?
    // @link https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort
    const sortedNums = arrayOfNums.sort(compareNumbers);
    // console.log('sortedNums', sortedNums);

    // * Assign highest nums to vars.
    highestNum1 = sortedNums[0];
    highestNum2 = sortedNums[1];
    // console.log('highestNum1', highestNum1);
    // console.log('highestNum2', highestNum2);

    // * Add our two highest numbers together
    sum = highestNum1 + highestNum2;

    return sum;
}

const arr = [1, 2, 5, 10, 3, 1, 2];
const result = sumTwoHighestNumsInArray(arr); // 15

console.log('result (should be 15):', result);
```