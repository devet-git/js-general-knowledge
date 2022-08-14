# 1. Copy array
```js
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];

// TODO: Copy array
let copyArr1 = [...arr1];
let copyArr2 = arr2.slice()
```

# 2. Combine array
```js
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];
let arr3 = [7, 8, 9];

// TODO: Combine array
let way1 = arr1.concat(arr2, arr3)
let way2 = [].concat(arr1, arr2, arr3);
let way3 = [...arr1, ...arr2, ...arr3]
```
