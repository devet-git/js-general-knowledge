## Copy array (Sao chép mảng)
```js
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];

// TODO: Copy array
let way1 = [...arr1];
let way2 = arr2.slice()
```

***

## Combine array (Nối mảng)
```js
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];
let arr3 = [7, 8, 9];

// TODO: Combine array
let way1 = arr1.concat(arr2, arr3)
let way2 = [].concat(arr1, arr2, arr3);
let way3 = [...arr1, ...arr2, ...arr3]
```

***

## Filter array (Lọc mảng)
See an example *_"Make a filtered list of all the people who are older than 18"_* bellow:

```js 
/**
 * 
 * @param {object[]} arr 
 */
const ageFilter = (arr) => arr.filter((e) => e.age > 18)

const peoples = [
   { name: "people1", age: 22 },
   { name: "people2", age: 5 },
   { name: "people3", age: 17 },
]

console.log(ageFilter(peoples)); 
// output: [{ name: "people1", age: 22 }]
```

