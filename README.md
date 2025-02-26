# JavaScript One-Liners Cheat Sheet 🚀

## **1. Nullish Coalescing (`??`)**

Returns right operand if left is `null` or `undefined`.

```javascript
let user = null ?? "Guest"; // "Guest"
let count = 0 ?? 10; // 0 (not nullish)
```

## **2. Optional Chaining (`?.`)**

Safely access nested properties.

```javascript
let obj = { user: { name: "Alice" } };
console.log(obj?.user?.name); // "Alice"
console.log(obj?.profile?.age); // undefined
```

## **3. Logical OR (`||`)**

Returns right operand if left is **falsy**.

```javascript
let name = "" || "Default"; // "Default"
let age = 0 || 18; // 18
```

## **4. Logical AND (`&&`)**

Returns right operand if left is **truthy**.

```javascript
let isLoggedIn = true && "Welcome!"; // "Welcome!"
let isAdmin = false && "Admin Panel"; // false
```

## **5. Ternary Operator (`? :`)**

Shortens `if-else`.

```javascript
let age = 20;
let status = age >= 18 ? "Adult" : "Minor"; // "Adult"
```

## **6. Destructuring Assignment**

Extract values into variables.

```javascript
const user = { name: "John", age: 30 };
const { name, age } = user;
console.log(name, age); // "John", 30
```

## **7. Spread Operator (`...`)**

Expands arrays or objects.

```javascript
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5]; // [1, 2, 3, 4, 5]
```

## **8. Rest Operator (`...`)**

Collects values into an array.

```javascript
function sum(...nums) {
  return nums.reduce((acc, num) => acc + num, 0);
}
console.log(sum(1, 2, 3, 4)); // 10
```

## **9. Arrow Functions (`=>`)**

Shortens function expressions.

```javascript
const add = (a, b) => a + b;
console.log(add(2, 3)); // 5
```

## **10. Exponentiation (`**`)\*\*

Replaces `Math.pow()`.

```javascript
console.log(2 ** 3); // 8
```

## **11. Numeric Separators (`_`)**

Improves large number readability.

```javascript
const billion = 1_000_000_000;
console.log(billion); // 1000000000
```

## **12. Default Parameters (`=`)**

Handles missing arguments.

```javascript
function greet(name = "Guest") {
  return `Hello, ${name}!`;
}
console.log(greet()); // "Hello, Guest!"
```

## **13. Short-Circuiting (`||=`, `&&=`, `??=`)**

Shorthand for assignments.

```javascript
let a = 0;
a ||= 10; // 10 (assigns if falsy)

let b = true;
b &&= "Updated"; // "Updated" (assigns if truthy)

let c = null;
c ??= "Fallback"; // "Fallback" (assigns if nullish)
```

## **14. Array Methods (One-Liners)**

### `map()` – Transform Elements

```javascript
const nums = [1, 2, 3];
const squares = nums.map((n) => n ** 2); // [1, 4, 9]
```

### `filter()` – Keep Certain Elements

```javascript
const evens = nums.filter((n) => n % 2 === 0); // [2]
```

### `reduce()` – Aggregate Values

```javascript
const sum = nums.reduce((acc, num) => acc + num, 0); // 6
```

## **15. Fetch API + Promise Chaining**

Simplifies async requests.

```javascript
fetch("https://api.example.com/data")
  .then((response) => response.json())
  .then((data) => console.log(data))
  .catch((error) => console.error(error));
```

## **16. Template Literals (Backticks ` `` `)**

Allows multiline strings & variable interpolation.

```javascript
let name = "Alice";
console.log(`Hello, ${name}!`);
```

## **17. Object Property Shorthand**

Concise object creation.

```javascript
const age = 30;
const user = { name, age }; // { name: "Alice", age: 30 }
```

## **18. Dynamic Object Keys (`[]`)**

Define object keys dynamically.

```javascript
const key = "score";
const obj = { [key]: 100 };
console.log(obj); // { score: 100 }
```

## **19. Object Method Shorthand**

Shortens function definitions inside objects.

```javascript
const user = {
  name: "John",
  greet() {
    return `Hello, ${this.name}!`;
  },
};
console.log(user.greet()); // "Hello, John!"
```

## **20. Async/Await**

Cleaner than `.then()`.

```javascript
async function fetchData() {
  try {
    let response = await fetch("https://api.example.com/data");
    let data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}
fetchData();
```

## **21. Set (`new Set()`)**

Removes duplicates from arrays.

```javascript
const nums = [1, 2, 2, 3, 4, 4, 5];
const uniqueNums = [...new Set(nums)];
console.log(uniqueNums); // [1, 2, 3, 4, 5]
```

---

🚀 **Use This Cheat Sheet for Quick Reference!**
