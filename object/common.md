


## Browser all object properties (Duyệt qua tất cả các thuộc tính của đối tượng)
```js
let obj = {
   1: "One",
   2: "true",
   3: "three",
   4: "Four"
}

// TODO: browser all object properties
for (const key in obj) {
   if (obj.hasOwnProperty(key)) {
      console.log(key);
   }
}
```

## Convert object to Json and vice versa
```js
let obj = {
   1: "One",
   2: "true",
   3: "three",
   4: "Four"
}
let json = JSON.stringify(obj)
let toObj = JSON.parse(toJson)
```
