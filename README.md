# Sorted-Union

FreeCodeCamp
    JavaScript Algorithms and Data Structures
    Intermediate Algorithm Scripting

Sorted Union

Write a function that takes two or more arrays and returns a new array of unique values in the order of the original provided arrays.

In other words, all values present from all arrays should be included in their original order, but with no duplicates in the final array.

The unique numbers should be sorted by their original order, but the final array should not be sorted in numerical order.

Check the assertion tests for examples.


--- Here's the Code ---

function uniteUnique(arg) {
  const argsLength = arguments.length
  const output = []

  for (let i = 0; i < argsLength; i++){
    arguments[i].forEach(elt => {
      if(output.indexOf(elt) < 0){
        output.push(elt)
      }
    })
  }
  return output;
}

uniteUnique([1, 3, 2], [5, 2, 1, 4], [2, 1]);
