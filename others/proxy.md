# Proxy object
For instance, when you just push number to array:
```js
let numbers = [];

numbers = new Proxy(numbers, {
	set(target, prop, value) {
		if (typeof value === "number") {
			target[prop] = value;
			return true;
		} else {
			return false;
		}
	}
})
numbers.push(12, 12, 9)
console.log(numbers);
```

To protect properties in object:
```js
let users = {
	name: "devet",
	_pw: "12345",
	addr: "Cao Thang"
}

users = new Proxy(users, {

	get(target, prop) {
		if (prop.startsWith('_')) {
			throw new Error("Access denied");
		}
		let value = target[prop]
		return (typeof value === 'function') ? value.bind(target) : value;

		// return target[prop]
	},
	set(target, prop, value) {
		if (prop.startsWith("_")) throw new Error("Access denied");
		target[prop] = value;
		return true;
	},
	deleteProperty(target, prop) {
		if (prop.startsWith('_')) throw new Error("Access denied");
		delete target[prop]
		return true
	},

	ownKeys(target) {
		return Object.keys(target).filter(key => !key.startsWith("_"));
	}
})
delete users._pw; //! error
console.log(users.name); // devet
```

