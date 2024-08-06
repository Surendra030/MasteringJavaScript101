# Understanding `Array.prototype.concat()` Method in JavaScript

The `Array.prototype.concat()` method in JavaScript is used to merge two or more arrays into a single new array. It creates a new array by combining the elements of the arrays provided as arguments. Importantly, this method does not alter the original arrays but instead returns a new array.

## Introduction to `Array.prototype.concat()`

The `concat()` method can be used to combine arrays or add elements to an existing array. It performs a shallow copy of the arrays being combined. When dealing with primitive values (like numbers, strings, or booleans), `concat()` creates a new array with copies of those values. Changes to the new array do not affect the original arrays.

### Syntax

```javascript
array.concat([value1[, value2[, ...]]])
'''

value1, value2, ... - Arrays and/or values to concatenate with the original array. These values are added to the end of the new array.

###Example Implementation with Primitive Values
let arr1 = ['a', 'b', 'c'];
let arr2 = ['d', 'e', 'f'];

let res = arr1.concat(arr2);

console.log('Original Arrays:');
console.log('Arr1:', arr1); // ['a', 'b', 'c']
console.log('Arr2:', arr2); // ['d', 'e', 'f']
console.log('Concatenated Array:', res); // ['a', 'b', 'c', 'd', 'e', 'f']

res[0] = 'p'; // Modify the new array

console.log('\nArrays After Modification:');
console.log('Arr1:', arr1); // ['a', 'b', 'c']
console.log('Arr2:', arr2); // ['d', 'e', 'f']
console.log('Concatenated Array:', res); // ['p', 'b', 'c', 'd', 'e', 'f']


E###xplanation
arr1.concat(arr2) creates a new array res that combines the elements of arr1 and arr2.
Modifying res[0] does not affect arr1 or arr2 because res holds copies of the primitive values from arr1 and arr2, not references to the original values.

###Key Points
Arrays with Primitive Values: When you concatenate arrays that contain only primitive values (like numbers, strings, or booleans), the concatenation creates a new array with copies of those values. Since primitives are copied by value (not by reference), changes to elements in the new array do not affect the original arrays.
Arrays with Objects: When concatenating arrays containing objects, the new array will hold references to the same objects. Changes to these objects in the new array will affect the original arrays because the objects are shared between them.
