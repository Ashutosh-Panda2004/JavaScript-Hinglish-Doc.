Here's the complete `README.md` with code and Hinglish explanations in one code block:

# JavaScript Basics

Is README mein hum JavaScript ke basic concepts ko samjhenge, saath mein thode Hinglish (Hindi + English) comments bhi diye hain. Chalo shuru karte hain!

---

## 1. Console Log (Print Statement)

Neeche wali line console window pe output print karne ke liye use hoti hai:

```javascript
console.log('Namaste Duniya'); // Output: Namaste Duniya
```

---

## 2. Variables - Named Memory Locations

JavaScript mein variables ka use data store karne ke liye hota hai.  
JavaScript **Dynamically Typed** hai → Iska matlab data type ko explicitly specify karne ki zarurat nahi hai.

```javascript
let Name = "Ashutosh Panda";  // String
let Roll_num = 2210990191;     // Number 
let Married = false;           // Boolean
let num;                       // Undefined 
let num2 = null;               // Null

console.log(Name + " " + Roll_num + " " + Married + " " + num + " " + num2);
```

*Explanation:*  
- `let Name = "Ashutosh Panda";` - Ye ek String variable hai.  
- `let Roll_num = 2210990191;` - Ye ek Number variable hai.  
- `let Married = false;` - Ye ek Boolean variable hai.  
- `let num;` - Ye Undefined variable hai, abhi value assign nahi hui hai.  
- `let num2 = null;` - Ye Null variable hai, iska matlab variable ko explicitly null value assign kiya gaya hai.

---

## 3. `var` aur `let` ke beech ka farak

### 3.1 `var` Keyword

`var` **function-scoped** hota hai. Agar `var` block ke andar declare kiya gaya ho, toh bhi us block ke bahar accessible rahega.

```javascript
for (var i = 0; i < 10; i++) {}
console.log(i); // Output: 10 (block ke bahar bhi accessible hai)
```

### 3.2 `let` Keyword

`let` **block-scoped** hota hai. Agar `let` block ke andar declare kiya gaya hai, toh us block ke bahar accessible nahi hoga.

```javascript
for (let j = 0; j < 10; j++) {}
// console.log(j); // Ye ReferenceError dega: j is not defined
```

---

## 4. `var` aur `let` ki Redeclaration aur Redefinition

### 4.1 `var` Keyword

- **Redeclaration**: `var` ke saath ek hi variable ko dobara declare kar sakte hain.

```javascript
var a = 12;
var a = 32; // Ye valid hai
```

- **Redefinition**: `var` ke saath ek variable ki value ko change kar sakte hain.

```javascript
var b = 12;
b = 32; // Ye valid hai
```

### 4.2 `let` Keyword

- **Redeclaration**: `let` ke saath ek variable ko dobara declare nahi kar sakte.

```javascript
let c = 12;
// let c = 32; // Ye Error dega: Identifier 'c' has already been declared
```

- **Redefinition**: `let` ke saath ek variable ki value ko change kar sakte hain.

```javascript
let d = 12;
d = 32; // Ye valid hai
```

---

## 5. Primitive Data Types

JavaScript mein kuch basic data types hote hain:

```javascript
// String
let str1 = "Hi, how are you?";
console.log(str1); // Output: Hi, how are you?

// Number
let num1 = 123;
console.log(num1); // Output: 123

// Boolean
let bool1 = false;
console.log(bool1); // Output: false

// Undefined
let e;
console.log(e); // Output: undefined

// Null
let f = null;
console.log(f); // Output: null
```

---

## 6. Dynamic Typing

JavaScript mein ek variable alag-alag types ki values ko hold kar sakta hai.

```javascript
// Initially, 'data' is of type string
let data = "Hello, World!";
console.log(data); // Output: Hello, World!

// Now 'data' is reassigned to a number
data = 42;
console.log(data); // Output: 42

// Now 'data' is reassigned to a boolean
data = true;
console.log(data); // Output: true

// Now 'data' is reassigned to an object
data = { name: "John Doe", age: 30 };
console.log(data); // Output: { name: "John Doe", age: 30 }

// Now 'data' is reassigned to an array
data = [1, 2, 3, 4, 5];
console.log(data); // Output: [1, 2, 3, 4, 5]

// Finally, 'data' is reassigned to a function
data = function() { return "I am a function"; };
console.log(data()); // Output: I am a function
```

---

## 7. Reference Types

JavaScript mein kuch reference types hote hain:

1. **Objects**: Multiple variables ko ek object mein group kiya jata hai.

```javascript
let person = {
    firstName: "Ashutosh",
    age: 12,
    sex: "Male",
    martialStatus: false
};
console.log(person);
```

2. **Arrays**: List of items ko array ke form mein store kiya jata hai.

```javascript
let arr1 = ["Ashutosh", 18, false, null];
console.log(arr1);
arr1[1] = 20; // 18 ko 20 se change kiya
arr1[0] = "Ashutosh Panda"; // "Ashutosh" ko "Ashutosh Panda" se change kiya
console.log(arr1);
```

3. **Functions**: Functions bhi ek reference type hain.

---

## 8. Operators in JavaScript

JavaScript mein kuch operators hote hain jo various operations perform karte hain:

### 8.1 Arithmetic Operators

```javascript
console.log(4 + 8); // Addition: 12
console.log(8 - 4); // Subtraction: 4
console.log(4 * 8); // Multiplication: 32
console.log(8 / 4); // Division: 2
console.log(4 ** 2); // Exponentiation: 16
console.log(4 % 8); // Modulus: 4
```

### 8.2 Assignment Operators

```javascript
// Pre Increment, Pre Decrement
let num3 = 12;
console.log(++num3);   // Pre Increment: 13

let num4 = 32;
console.log(--num4);   // Pre Decrement: 31

// Post Increment, Post Decrement
let num5 = 12;
console.log(num5++);   // Post Increment: 12
console.log(num5);     // Updated value: 13

let num6 = 32;
console.log(num6--);   // Post Decrement: 32
console.log(num6);     // Updated value: 31

// Additional Assignment Operators
let nums = 0;
console.log(nums += 3);  // Addition Assignment: 3
console.log(nums -= 1);  // Subtraction Assignment: 2
console.log(nums *= 2);  // Multiplication Assignment: 4
console.log(nums /= 2);  // Division Assignment: 2
console.log(nums %= 2);  // Modulus Assignment: 0
```

### 8.3 Comparison Operators

```javascript
console.log(5 === 3); // Strict Equality: false
console.log(5 !== 3); // Inequality: true
console.log(5 > 3);  // Greater than: true
console.log(5 < 3);  // Less than: false
console.log(5 >= 3); // Greater than or equal to: true
console.log(5 <= 3); // Less than or equal to: false

let nums2 = 12;
let str2 = "12";
console.log(nums2 == str2); // Loose Equality: true (value same, type different)
console.log(nums2 === str2); // Strict Equality: false (value and type both different)
```

### 8.4 Ternary Operator

```javascript
let age = 12;
age >= 18 ? console.log("You can drive") : console.log("You cannot drive");
```

### 8.5 Logical Operators

JavaScript mein primary logical operators hain:

- **AND (&&)**: Dono operands true hain tabhi true return karta hai.
- **OR (||)**: Agar kisi bhi operand ka value true hai, tabhi true return karta hai.
- **NOT (!)**: Operand ke truthiness ko invert karta hai.

```javascript
let a1 = true;
let b1 = false;

if (a1 && b1) {
  console.log("Both a1 and b1 are true.");
}
if (a1 || b1) {
  console.log("At least one of a1 or b1 is true.");
}
if
