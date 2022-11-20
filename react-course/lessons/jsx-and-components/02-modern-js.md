---
marp: true
theme: gaia
_class: 
  - lead

---

![bg left:40% 80%](../../assets//dll-logo.png)

# Learn React

Modern JavaScript Crash Course

With Daryl

---

## Arrow Functions
Condensed alternative to regular function expressions.
Limited. Can't be used in all situations
Omits `function` and (in some cases) `return` keywords

```js
// Regular func
function sum(a, b) {
    return a + b;
}
// Arrow funcs
const sum = (a, b) => a + b;
const sum = (a, b) => (a + b);
const sum = (a, b) => {
    return a + b
};
```

---

## Destructuring assignment
### Arrays
Original array is not modified

```js
// Example 1
let arr = ["Eren", "Yeager"];
let [firstName, lastName] = arr;
console.log(firstName, lastName);
console.log(arr);

// Example 2
let [firstName, lastName] = "Eren Yeager".split(' ');
console.log(firstName, lastName);

```

---

Works with any iterable

```js
let [a, b, c] = "abc"; // ["a", "b", "c"]
let [one, two, three] = new Set([1, 2, 3]);
```

Use any “assignables” on the left side.

```js
let user = {};
[user.name, user.surname] = "John Smith".split(' ');
console.log(user);
```

---

Create a new array from the "rest" (extra values)

```js
let [a, b, ...others] = ['a', 'b', 'c', 'd', 'e'];
console.log(others);
```

Ignore values

```js
let [a, , c] = ['a', 'b', 'c', 'd', 'e'];
console.log(a, c);
```

Default values

```js
let [firstName, lastName = "Yeager"] = "Eren".split(' ');
console.log(firstName, lastName);
```

---

### Objects

```js
let person = {
    name: "Eren Yeager",
    height: 183,
    weight: 82,
    gender: "Male",
}

let {name, height, weight, gender} = person;
```
Variables are named using keys and assigned correponding values.
However, Variables can be renamed

```js
let {name, height: h, weight: w, gender} = person;
console.log(name, h, w);
```

---

Order does not matter. Properties can be ignored

```js
let {name, weight, height} = person;
```

Missing properties can be assigned defaults

```js
let {name, height, weight, gender, residence = "Wall Rose"} = person;
```

"Rest" applies

```js
let {name, ...rest} = person;
console.log(name, rest);
```

---

## Template Strings
AKA Template Literals 
Uses backticks

```js
const a = 10;
const b = 5;

console.log(`Sum of a and b is ${a + b}`);

```

---

## Debugging using `console`

You can do more than `console.log()`

For example

```js
console.table(['apples', 'bananas', 'cherries', 'dates']);
console.table({
  firstName: 'Daryl',
  lastName: 'Lukas',
  occupation: 'Developer'
});
```

Learn more [here](https://dev.to/daryllukas/you-can-do-more-than-just-console-log-598a)
