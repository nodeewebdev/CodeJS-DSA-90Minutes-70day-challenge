# 🧠 JavaScript Array & String Methods: 20 Practice Challenges

## 1. Reverse a String
**Problem**: Write a function that reverses a given string.
**Approach**: Use `split('')` to convert the string into an array, `reverse()` to reverse the array, and `join('')` to combine it back into a string.

```javascript
function reverseString(str) {
  return str.split('').reverse().join('');
}
```

## 2. Count Words in a String
**Problem**: Write a function that counts the number of words in a given string.
**Approach**: Use `split(' ')` to divide the string into an array of words and then return the `length` of the array.

```javascript
function countWords(str) {
  return str.split(' ').length;
}
```

## 3. Find the Largest Number in an Array
**Problem**: Write a function that returns the largest number from a given array.
**Approach**: Use `Math.max(...arr)` to find the maximum value.

```javascript
function findLargest(arr) {
  return Math.max(...arr);
}
```

## 4. Remove Duplicates from an Array
**Problem**: Write a function that removes duplicate values from an array.
**Approach**: Convert the array to a `Set` and then back to an array using the spread operator (`...`).

```javascript
function removeDuplicates(arr) {
  return [...new Set(arr)];
}
```

## 5. Count Occurrences of a Value in an Array
**Problem**: Write a function that counts how many times a specific value appears in an array.
**Approach**: Use `filter()` to create a new array with matching values and return its `length`.

```javascript
function countOccurrences(arr, val) {
  return arr.filter(item => item === val).length;
}
```

## 6. Merge Two Arrays
**Problem**: Write a function that merges two arrays into one.
**Approach**: Use the spread operator (`...`) to combine both arrays.

```javascript
function mergeArrays(arr1, arr2) {
  return [...arr1, ...arr2];
}
```

## 7. Convert a String to Title Case
**Problem**: Write a function that converts a string to title case (capitalizing the first letter of each word).
**Approach**: Use `split(' ')` to divide the string into words, `map()` to capitalize each word, and `join(' ')` to combine them back.

```javascript
function toTitleCase(str) {
  return str.split(' ').map(word => word.charAt(0).toUpperCase() + word.slice(1)).join(' ');
}
```

## 8. Check if a String is a Palindrome
**Problem**: Write a function that checks if a given string is a palindrome.
**Approach**: Compare the string with its reverse using `split('')`, `reverse()`, and `join('')`.

```javascript
function isPalindrome(str) {
  const reversed = str.split('').reverse().join('');
  return str === reversed;
}
```

## 9. Convert a String to an Array of Words
**Problem**: Write a function that converts a string into an array of words.
**Approach**: Use `split(' ')` to divide the string into words.

```javascript
function stringToArray(str) {
  return str.split(' ');
}
```

## 10. Find the Index of a Value in an Array
**Problem**: Write a function that returns the index of a specific value in an array.
**Approach**: Use `indexOf()` to find the index.

```javascript
function findIndex(arr, val) {
  return arr.indexOf(val);
}
```

## 11. Replace All Spaces in a String with '%20'
**Problem**: Write a function that replaces all spaces in a string with `'%20'`.
**Approach**: Use `replace()` with a regular expression (`/\s/g`) to replace all spaces.

```javascript
function replaceSpaces(str) {
  return str.replace(/\s/g, '%20');
}
```

## 12. Get the First N Characters of a String
**Problem**: Write a function that returns the first N characters of a string.
**Approach**: Use `slice(0, n)` to extract the first N characters.

```javascript
function firstNChars(str, n) {
  return str.slice(0, n);
}
```

## 13. Join an Array of Strings into a Single String
**Problem**: Write a function that joins an array of strings into a single string.
**Approach**: Use `join('')` to concatenate the array elements.

```javascript
function joinStrings(arr) {
  return arr.join('');
}
```

## 14. Convert a String to Lowercase
**Problem**: Write a function that converts a string to lowercase.
**Approach**: Use `toLowerCase()` to convert the string.

```javascript
function toLowerCase(str) {
  return str.toLowerCase();
}
```

## 15. Convert a String to Uppercase
**Problem**: Write a function that converts a string to uppercase.
**Approach**: Use `toUpperCase()` to convert the string.

```javascript
function toUpperCase(str) {
  return str.toUpperCase();
}
```

## 16. Remove the First Character from a String
**Problem**: Write a function that removes the first character from a string.
**Approach**: Use `slice(1)` to get the string starting from the second character.

```javascript
function removeFirstChar(str) {
  return str.slice(1);
}
```

## 17. Remove the Last Character from a String
**Problem**: Write a function that removes the last character from a string.
**Approach**: Use `slice(0, -1)` to get the string up to the last character.

```javascript
function removeLastChar(str) {
  return str.slice(0, -1);
}
```

## 18. Sort an Array of Strings Alphabetically
**Problem**: Write a function that sorts an array of strings alphabetically.
**Approach**: Use `sort()` to sort the array in place.

```javascript
function sortStrings(arr) {
  return arr.sort();
}
```

## 19. Find the Length of a String
**Problem**: Write a function that returns the length of a string.
**Approach**: Use the `length` property to get the length.

```javascript
function stringLength(str) {
  return str.length;
}
```

## 20. Check if a String Contains a Substring
**Problem**: Write a function that checks if a string contains a specific substring.
**Approach**: Use `includes()` to check for the substring.

```javascript
function containsSubstring(str, substr) {
  return str.includes(substr);
}
```