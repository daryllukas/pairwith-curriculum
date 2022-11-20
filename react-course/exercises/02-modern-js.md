# Modern JavaScript Exercises
*TIP: Use `console.log()` to test your solutions*
## Arrow Functions
- Rewrite the following function using arrow syntax

```js
const toCelsius = function(fahrenheit) {
    return (5 / 9) * (fahrenheit - 32);
}
```

## Destructuring Assignment
- Given the oject below, write the destructuring assignment that reads:
  - `name` property into the variable `name`.
  - `years` property into the variable `age`.
  - `isAdmin` property into the variable `isAdmin` (`false`, if no such property)

  ```js
    let user = {
        name: "John",
        years: 30
    };
  ```

- Create a function `youngestStudent(students)` that returns the name of the youngest student
    - Use `Object.entries` and destructuring to iterate over key/value pairs
    - If `students` is empty, the function should return `null`.
    ```js
    let salaries = {
        "Mapalo": 21,
        "Madalitso": 25,
        "Blessings": 19
    };
    ```