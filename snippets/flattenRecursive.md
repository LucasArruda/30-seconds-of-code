### flattenRecursive

Flattens an array, recursive, even if there are any depths of array inside it.

Use `Array.reduce()` to get all elements inside the array and `concat()` to flatten them. 
If an element happens to be an array, calls the function again, so we always end up with a flatten array,
no matter the array depth.

```js
const flattenRecursive = arr => arr.reduce((a, v) => a.concat( Array.isArray(v) ? flattenRecursive(v) : v ), []);
// flattenRecursive([1,[2],[[[3, 4],5],6]]) -> [1,2,3,4,5,6]
```
