# Understanding `Array.prototype.at()` Method in JavaScript

The `Array.prototype.at()` method is a newer addition to JavaScript, introduced in ECMAScript 2022. It provides a way to access elements in an array using positive and negative indices. This method allows for more flexible and expressive array element access compared to traditional indexing.

## Introduction to `Array.prototype.at()`

The `at()` method takes an integer value and returns the element at that position in the array. The key feature of `at()` is its support for negative integers, which count back from the end of the array. This is particularly useful when you want to access elements from the end of the array without calculating the exact index.

### Syntax

```javascript
array.at(index)
index - An integer representing the position in the array. Can be positive or negative.
'''
### Code Examples

### Example Implementaion

var arr = [10, 20, 30, 40, 50];

console.log(arr); // [10, 20, 30, 40, 50]

console.log(arr.at(2));  // 30
console.log(arr.at(-2)); // 40
console.log(arr.at(6));  // undefined



###Explanation
arr.at(2): This accesses the element at index 2 (third element) of the array, which is 30.

arr.at(-2): This accesses the element at the second-to-last position, which is 40.

arr.at(6): The index 6 is out of bounds for the array, so it returns undefined.


###Difference Between at() and Traditional Indexing
####Using at()
Positive Index: arr.at(index) behaves like traditional indexing for positive indices.
Negative Index: arr.at(-index) allows accessing elements from the end of the array.
\n
####Using Traditional Indexing
Positive Index: arr[index] accesses the element at the specified index. If the index is out of bounds, it returns undefined.
Negative Index: Negative indices are not supported. Attempting to access with a negative index results in undefined

console.log(arr); // [10, 20, 30, 40, 50]
console.log(arr.at(-2)); // 40
console.log(arr[-2]);   // undefined

arr.at(-2): Correctly accesses the second-to-last element (40).
arr[-2]: In JavaScript, this does not access elements from the end of the array and instead returns undefined because negative indices are not valid in traditional indexing.
