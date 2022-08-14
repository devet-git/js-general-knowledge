# When you copy and then make the array empty

```js
let arr1 = [1,2,3,4]
let arr2 = arr1 // => arr2 = [1,2,3]
arr1 = []; // => arr2 = [1,2,3] even thought arr1 = []
```

If you want to make "arr2" empty when "arr1" empty, use:
```js
let arr1 = [1,2,3,4]
let arr2 = arr1 //now arr2 =[1,2,3]
arr1.length = 0; // or: arr1.splice(0, arr1.length) 
// => arr1 = [] and arr2 = []
```

In another way for copy an array using **spread operator**:
```js
let arr1 = [1,2,3,4]
let arr2 = [...arr1] //now arr2 = [1,2,3]
arr1.length = 0; 
// or: 
arr1.splice(0, arr1.length)

// => despite arr1 is [], arr2 still is [1,2,3,4]
```

