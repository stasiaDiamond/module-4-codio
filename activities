// *** --- comments prefaced by an asterisk (*) are my own, not part of curriculum --- ***


// ------- TASK 01: First Array in Memory pt 1-------

// Instructions
// - Given the following 6 empty functions, add the right return statement to each of them to complete the activity
// Please do not change any of the function names

//This is your starting array
const arr = [10, 10, 16, 12];

function returnFirst(arr) {
  // return the first item from the array
  return arr[0];
}

function returnLast(arr) {
  // return the last item of the array
  // * is this assuming we know what it is from the list above? 
  // * or does it want the length?
  // * .length hasn't been established yet.
  // * probably should reorder this and the next functions bc the next answer establishes array.length 
  // * progression flow isn't optimal and comment isn't explicit in what it wants
  // * it is not this: return arr[3];
  return arr[arr.length - 1];
  // * must always subtract by 1 bc Arrays are 0 index. 
  // * [0, 1, 2, 3] <--- 4 items in the array, but 4th is at index 3, so 4 -1 to access arr[3]
}

function getArrayLength(arr) {
  // return the length of the array
  return arr.length;
}

function incrementByOne(arr) {
  // arr is an array of integers(numbers), Increment all items in the array by
  // * typo in the instruction's comment above. Look to function's name for a clue. 
  // * Is typo omitted to make this difficult or was it an honest mistake?
  // * if mistake, please fix
  for (let i = 0; i < arr.length; i++) {
    // return the array
    arr[i]++;
    // arr[i] = arr[i] + 1;
  }
  return arr;
}

function addItemToArray(arr, item) {
  // add the parameter item to the end of the array arr
  arr.push(item);
  // return the array
  return arr;
}

function addItemToFront(arr, item) {
  // add the parameter item to the front of the array arr
  arr.unshift(item);
  // return the array
  return arr;
  // hint: use the array method .unshift
}

//uncomment these lines to check results in browser console
console.log("returnFirst result:" + returnFirst(arr))
console.log("returnLast result:" + returnLast(arr))
console.log("getArrayLength result:" + getArrayLength(arr))
console.log("incrementByOne result:" + incrementByOne(arr))
console.log("addItemToArray result:" + addItemToArray(arr, 10))
console.log("addItemToFront result:" + addItemToFront(arr, 10))

//////////////////////////////////
//don't change this line
if (typeof module !== 'undefined') {
  module.exports = {
    returnFirst,
    returnLast,
    getArrayLength,
    incrementByOne,
    addItemToArray,
    addItemToFront,
  };
}


// ------- TASK 02: First Array in Memory pt 2 -------

//Instructions 
//Given an array of strings, words, return a string that has all the words concatenated together
// - spaces are needed in between words
//
//ex. ['how', 'are', 'you'] -> 'how are you'
const words = ["living", "the", "dream"];

function wordsToSentence(words) {
  //your code here
  // * a clue in the name of function. We need a sentence variable. An empty string
  let sentence = "";
  // * loop over the array
  for (let i = 0; i < words.length; i++) {
    // * for each index in the array ADD each word plus a space AND SET sentence variable EQUAL TO that word and space
    // * made possible by +=
    sentence += words[i] + " ";
  }
  // * must return if we want to use sentence variable elsewhere
  return sentence.trim();
}

//console log results
console.log('results', wordsToSentence(['hey', 'there']));

//don't change this line
module.exports = { wordsToSentence };





// ------- TASK 03: Passing Arguments to Functions -------
/*
Instructions
Compare Objects 
- Define a function, `compareCities`, that accepts two objects as arguments.

compareCities({ name: 'Dresden' }, { name: 'Dresden' }) // -> true
compareCities({ name: 'Raleigh' }, { name: 'Raleigh', income_pc: 1200000 }) // -> false
*/

function compareCities(c1, c2) {
  // * first create variables to house the Arrays of Keys for city 1 and city 2
  // * then use JS built-in Method: Object.keys() 
  // * Object.keys() will return an Array whose items are Strings
  // * we'll compare the returned two Strings to see if identical
  // * see above for what they want compareCities()'s arguments called
  const c1Keys = Object.keys(c1);
  const c2Keys = Object.keys(c2);

  // * commonly used practice: check if Arrays are equal in length first to save effort 
  // * if they're not equal in length, it's false right off the bat
  // * therefore no need to check the rest of the statements
  if (c1Keys.length !== c2Keys.length) {
    // * always return if you want to use outside of scope
    return false;
  }

  // * loop over each KEY in the first Object
  // * for each KEY in c1Keys, give me an Array of Keys as Strings
  // * iterate over each Key (** in **) each Object
  for (let key in c1Keys) {
    // * now use the arguments passed into the function 
    // * we need to use Array Indexing to check their Keys: c1[key]
    // * check if they are not exactly equal
    if (c1[key] !== c2[key]) {
      // * always return if you want to use data elsewhere
      return false;
    }
  }
  // * if any of the above if's aren't false, return true
  return true;
}

//uncomment next lines to console log results
console.log(compareCities({}, {}))
console.log(compareCities({ name: 'San Jose' }, { name: 'San Jose' }))
console.log(compareCities({ name: 'San Jose' }, { otherkey: 'San Jose' }))

//don't change this line
module.exports = compareCities;

// ------ Challenges Encountered -------
// * read the instructions incorrectly, oops! 
// * i am comparing only the Keys to each other
// * i should have compared the key/value pairs
// * in that case, the "for...of" in the Solution File is appropriate





// ------- TASK 04: Functions with Arguments -------

/*
Instructions
- Create a calculator function
- By using a switch statement, ask for each case to find out what's the operator being passed to the function, then set the result of that operation by using value1 and value2

function c(value1,operator,value2){
}
*/
//your code

function calculator(value1, operator, value2) {
  // * switch statement is followed by an expression in parenthesis
  // * the expression value is what each case will check against
  // * if the case value matches the expression value, only that case block runs
  // * must break after each case in order to exit the case block
  // * include a default at the end as a catch-all for what to do if none of the cases match
  switch (operator) {
    case "+":
      return value1 + value2;
      break;
    case "-":
      return value1 - value2;
      break;
    case "*":
      return value1 * value2;
      break;
    case "/":
      return value1 / value2;
      break;
    default:
      console.log(`Sorry, operator not supported`);
  }
}

//uncomment next lines one by one, then check the console for results
console.log(calculator(1, "+", 1));
console.log(calculator(3, "-", 2));
console.log(calculator(3, "*", 2));
console.log(calculator(30, "/", 2));
console.log(calculator(5, "/", 0));

//don't change this line.

module.exports = calculator;

// ------ Challenges Encountered -------
// * none





// ------- TASK 05: Loop on an Array -------

//Array flattenr activity
// Define a function arrayFlattener with a 2 dimensional array as parameter:
// example of 2 dimensional array: [1,[2,3],4,5]

//Return a new 1 dimensional array like, [1,2,3,4]

function arrayFlattener(arr) {
  // * create a variable to house the new Array we're gonna make
  let flattenedArray = [];

  // * for loop to iterate thru the Array that is the argument: arr
  for (let i = 0; i < arr.length; i++) {
    // * check if the element [i] found when looping is an Array
    // * using built-in JS Method: Array.isArray()
    if (Array.isArray(arr[i])) {
      // * now we need to take the Array we have and add to it
      // * every time we loop thru arr, there's a possibility that it will return an Array
      // * so we'll need to recursively call arrayFlattener() on itself
      // * using built-in JSMethod: .concat() we add the newly made Array to what was there before
      // * .concat() takes the arrayFlattener Array and the new Array and smushes them together
      // * .concat() makes a new Array out of the 2 smushed ones
      flattenedArray = flattenedArray.concat(arrayFlattener(arr[i]));
      // * if the element at arr[i] is not an Array, we simply .push() to the flattenedArray variable's Array
    } else {
      flattenedArray.push(arr[i]);
    }
  }
  // * always return if you wanna use data elsewhere
  return flattenedArray;
}

//uncomment next line one by one, then check the console for results
console.log(arrayFlattener([1, [2, 3], 4, 5]))

//don't change this line
module.exports = { arrayFlattener };

// ------ Challenges Encountered -------
// * assignment suggests using "instanceof" on Task 03. 
// * seems like introducing complexity and confusion seeking an answer that's unwarranted in the given context
// * perhaps introducing constructor types and instances was unnecessary here?
// * we have not been taught object construction, instances, prototypes or any of that stuff yet
// * "instanceof" isn't the best way to solve the problem given what info the class knows at this time.
// * why say it'll help here and give us a link to "instanceof" instead of Array.isArray()?
// * they say: 

// " Hints:
// A useful way to check if a specific element is a String, Array, Boolean, etc… is using the instanceof operator. See an example of it’s use at the following link: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/instanceof "



// --------- Given Solutions below for my reference:

// --------- TASK-01 ----------
// // Instructions
// // - Given the following 6 empty functions, add the right return statement to each of them to complete the activity
// // Please do not change any of the function names

// //This is your starting array
// const arr = [10, 10, 16, 12];

// function returnFirst(arr) {
//   // return the first item from the array
//   return arr[0];
// }

// function returnLast(arr) {
//   // return the last item of the array
//   return arr[arr.length - 1];
// }

// function getArrayLength(arr) {
//   // return the length of the
//   return arr.length;
// }

// function incrementByOne(arr) {
//   // arr is an array of integers(numbers), Increment all items in the array by
//   for (let i = 0; i < arr.length; i++) {
//     arr[i] = arr[i] + 1;
//   }
//   // return the array
//   return arr;
// }

// function addItemToArray(arr, item) {
//   // add the parameter item to the end of the array arr
//   arr.push(item);
//   // return the array
//   return arr;
// }

// function addItemToFront(arr, item) {
//   // add the parameter item to the front of the array arr
//   arr.unshift(item);
//   // return the array
//   return arr;
//   // hint: use the array method .unshift
// }

// //uncomment these lines to check results in browser console
// // console.log("returnFirst result:" + returnFirst(arr))
// // console.log("returnLast result:" + returnLast(arr))
// // console.log("getArrayLength result:" + getArrayLength(arr))
// // console.log("incrementByOne result:" + incrementByOne(arr))
// // console.log("addItemToArray result:" + addItemToArray(arr, 10))
// // console.log("addItemToFront result:" + addItemToFront(arr, 10))

// //////////////////////////////////
// //don't change this line
// if (typeof module !== 'undefined') {
//   module.exports = {
//     returnFirst,
//     returnLast,
//     getArrayLength,
//     incrementByOne,
//     addItemToArray,
//     addItemToFront,
//   };
// }

// --------- TASK-02 ----------
//Instructions - activity -2
//Given an array of strings, words, return a string that has all the words concatenated together
// - spaces are needed in between words
//
//ex. ['how', 'are', 'you'] -> 'how are you'

// function wordsToSentence(words) {
//   //your code here
//   var sentence = '';

//   for (let i = 0; i < words.length; i++) {
//     sentence += words[i] + ' ';
//   }

//   return sentence.trim();
// }

// //console log results
// console.log('results', wordsToSentence(['hey', 'there']));

// //don't change this line
//   module.exports =  {wordsToSentence};



// --------- TASK-03 ----------

/*
Instructions
Compare Objects
- Define a function, `compareCities`, that accepts two objects as arguments.

compareCities({ name: 'Dresden' }, { name: 'Dresden' }) // -> true
compareCities({ name: 'Raleigh' }, { name: 'Raleigh', income_pc: 1200000 }) // -> false
*/
// function compareCities(object1, object2) {
//   const keys1 = Object.keys(object1);
//   const keys2 = Object.keys(object2);

//   if (keys1.length !== keys2.length) {
//     return false;
//   }

//   for (let key of keys1) {
//     if (object1[key] !== object2[key]) {
//       return false;
//     }
//   }

//   return true;
// }

// //uncomment next lines to console log results
// console.log(compareCities({}, {}));
// console.log(compareCities({ name: "San Jose" }, { name: "San Jose" }));
// console.log(compareCities({ name: "San Jose" }, { otherkey: "San Jose" }));

// //don't change this line 
// module.exports = compareCities;




// --------- TASK-04 ----------
// /*
// Instructions
// - Create a calculator function
// - By using a switch statement, ask for each case to find out what's the operator being passed to the function, then set the result of that operation by using value1 and value2

// function c(value1,operator,value2){

// }
// */
// //your code

// function calculator(value1, operator, value2) {
//   switch (operator) {
//     case "+":
//       return value1 + value2;
//       break;
//     case "-":
//       return value1 - value2;
//       break;
//     case "*":
//       return value1 * value2;
//       break;
//     case "/":
//       return value1 / value2;
//       break;
//     default:
//       console.log(`Sorry, operator not supported`);
//   }
// }

// //uncomment next lines one by one, then check the console for results
// console.log(calculator(1, "+", 1));
// console.log(calculator(3, "-", 2));
// console.log(calculator(3, "*", 2));
// console.log(calculator(30, "/", 2));
// console.log(calculator(5, "/", 0));

// //don't change this line.

// module.exports = calculator;





// --------- TASK-05 ----------
// //Array flattener activity
// // Define a function arrayFlattener with a 2d array as parameter:
// // [1,[2,3],4,5]

// //Return a new 1 dimensional array like, [1,2,3,4]

// //your code
// function arrayFlattener(arr) {
//   var newArr = [];

//   for (var i = 0; i < arr.length; i++) {
//     newArr = newArr.concat(arr[i]);
//   }

//   return newArr;
// }

// //uncomment next line one by one, then check the console for results
// console.log(arrayFlattener([1, [2, 3], 4, 5]));

// //don't change this line

//   module.exports =  {arrayFlattener};
