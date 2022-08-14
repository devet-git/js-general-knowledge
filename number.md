## Declare number (Khai báo số)
```js
let oldSyntax = 123456789;
let newSyntax = 123_456_789;
console.log(newSyntax); //output: 123456789
```

***

## Swap number (Hoán vị)
```js
let x = 1, y = 2;
[x, y] = [y, x]
console.log(x, y); //output: 2,1
```

***

<details open>
  <summary>UTILITIES</summary>
  
  ## Generate random number (Tạo số ngấu nhiên)
  ```js
  /**
    * 
    * @param {number} min
    * @param {number} max
    * @returns {number} [A random number from min to max]
    */
   random(min, max) {
      return Math.floor(Math.random() * (max - min + 1)) + min;
   }
  ```
  ***


</details>