# JavaScript Basics

Is README mein hum JavaScript ke basics ko detail mein samjhenge. Har concept ko Hinglish mein explain kiya gaya hai taaki samajhna aasan ho. Chalo shuru karte hain!

---

## 1. Console Log (Print Statement)

JavaScript mein `console.log()` ka use console window pe output print karne ke liye hota hai. Yeh debugging ke liye bhi useful hai.

```javascript
console.log('Namaste Duniya'); // Output: Namaste Duniya
```

*Explanation:*  
- `console.log('Namaste Duniya');` - Yeh line console pe "Namaste Duniya" print karegi.

---

## 2. Variables - Named Memory Locations

JavaScript mein variables data ko store karne ke liye use kiye jate hain. JavaScript **Dynamically Typed** hai, iska matlab data type ko explicitly define karne ki zarurat nahi hai.

```javascript
let Name = "Ashutosh Panda";  // String
let Roll_num = 2210990191;     // Number 
let Married = false;           // Boolean
let num;                       // Undefined 
let num2 = null;               // Null

console.log(Name + " " + Roll_num + " " + Married + " " + num + " " + num2);
```

*Explanation:*  
- `let Name = "Ashutosh Panda";` - Yeh ek String variable hai jo naam store karta hai.  
- `let Roll_num = 2210990191;` - Yeh ek Number variable hai jo roll number store karta hai.  
- `let Married = false;` - Yeh ek Boolean variable hai jo married status store karta hai.  
- `let num;` - Yeh Undefined variable hai, iski value abhi assign nahi hui hai.  
- `let num2 = null;` - Yeh Null variable hai, iska matlab isko explicitly null value assign kiya gaya hai.

---

## 3. `var` aur `let` ke beech ka farak

### 3.1 `var` Keyword

`var` function-scoped hota hai. Agar `var` block ke andar declare kiya gaya ho, toh bhi us block ke bahar accessible rahega.

```javascript
for (var i = 0; i < 10; i++) {}
console.log(i); // Output: 10 (block ke bahar bhi accessible hai)
```

*Explanation:*  
- `var` ke saath declare kiya variable poore function ya global scope mein accessible hota hai, even if it is declared inside a block like a loop.

### 3.2 `let` Keyword

`let` block-scoped hota hai. Agar `let` block ke andar declare kiya gaya hai, toh us block ke bahar accessible nahi hoga.

```javascript
for (let j = 0; j < 10; j++) {}
// console.log(j); // Ye ReferenceError dega: j is not defined
```

*Explanation:*  
- `let` ke saath declare kiya variable sirf usi block ke andar accessible hota hai jahan pe use kiya gaya hai.

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

*Explanation:*  
- `var` ke saath variable ko dobara declare kar sakte hain bina error ke. Variable ki value ko change karna bhi allowed hai.

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

*Explanation:*  
- `let` ke saath variable ko dobara declare karna error dega, lekin variable ki value ko change kar sakte hain.

---

## 5. Primitive Data Types

JavaScript mein kuch basic data types hain jo har variable ko represent karte hain.

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

*Explanation:*  
- **String**: Textual data ko represent karta hai.  
- **Number**: Numerical data ko represent karta hai.  
- **Boolean**: True ya false values ko represent karta hai.  
- **Undefined**: Jab variable ko initialize nahi kiya jata tab value `undefined` hoti hai.  
- **Null**: Explicitly variable ko `null` value assign karne ka concept hai.

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

*Explanation:*  
- **Dynamic Typing**: Variables ka type runtime ke dauran change ho sakta hai.

---

## 7. Reference Types

JavaScript mein kuch reference types hote hain jo complex data structures ko represent karte hain:

### 7.1 Objects

Objects multiple variables ko ek unit mein combine karte hain. 

```javascript
let person = {
    firstName: "Ashutosh",
    age: 12,
    sex: "Male",
    martialStatus: false
};
console.log(person);
```

*Explanation:*  
- **Objects**: Key-value pairs ka collection hote hain. Key (property name) aur Value (property value) ke form mein data store hota hai.

### 7.2 Arrays

Arrays ordered list of items ko store karte hain.

```javascript
let arr1 = ["Ashutosh", 18, false, null];
console.log(arr1);
arr1[1] = 20; // 18 ko 20 se change kiya
arr1[0] = "Ashutosh Panda"; // "Ashutosh" ko "Ashutosh Panda" se change kiya
console.log(arr1);
```

*Explanation:*  
- **Arrays**: Indexed collection hota hai jisme items 0-based index se access kiye jate hain. Array ke elements ko modify kiya ja sakta hai.

### 7.3 Functions

Functions reusable blocks of code hote hain jo specific tasks perform karte hain.

```javascript
function greet(name) {
    return `Hello, ${name}!`;
}
console.log(greet("Ashutosh")); // Output: Hello, Ashutosh!
```

*Explanation:*  
- **Functions**: Function ek block of code hota hai jo ek naam ke saath define kiya jata hai aur function call karke execute kiya jata hai.

---

## 8. Operators in JavaScript

JavaScript mein operators alag-alag types ke operations perform karte hain:

### 8.1 Arithmetic Operators

```javascript
console.log(4 + 8); // Addition: 12
console.log(8 - 4); // Subtraction: 4
console.log(4 * 8); // Multiplication: 32
console.log(8 / 4); // Division: 2
console.log(4 ** 2); // Exponentiation: 16
console.log(4 % 8); // Modulus: 4
```

*Explanation:*  
- **Arithmetic Operators**: Basic mathematical operations perform karte hain.

Sure, continuing from where we left off:

```markdown
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

// Solve this for better understanding of Pre/Post Increment/Decrement
let j = 5;
let k = 10;

let ans1 = (++j) * (--k);  // Pre Increment (6) * Pre Decrement (9) = 54
let ans2 = (j++) * (--k);  // Post Increment (6) * Pre Decrement (8) = 48
let ans3 = (j++) * (k--);  // Post Increment (7) * Post Decrement (8) = 56
let ans4 = (++j) * (k--);  // Pre Increment (8) * Post Decrement (7) = 56

console.log(ans1); // Output: 54
console.log(ans2); // Output: 48
console.log(ans3); // Output: 56
console.log(ans4); // Output: 56

// Additional Assignment Operators
let nums = 0;
console.log(nums += 3); // Addition assignment: 3
console.log(nums -= 1); // Subtraction assignment: 2
console.log(nums *= 2); // Multiplication assignment: 4
console.log(nums /= 2); // Division assignment: 2
console.log(nums %= 2); // Modulus assignment: 0
```

*Explanation:*  
- **Assignment Operators**: Variables ko new values assign karne ke liye use kiye jate hain. Increment aur Decrement operators variables ki values ko modify karte hain.

### 8.3 Comparison Operators

```javascript
console.log(5 === 3);  // Strict Equality: false
console.log(5 !== 3);  // Inequality: true
console.log(5 > 3);    // Greater Than: true
console.log(5 < 3);    // Less Than: false
console.log(5 >= 3);   // Greater Than or Equal To: true
console.log(5 <= 3);   // Less Than or Equal To: false

// Equality Operator
// Strict Equality --> === 
// Loose Equality --> == 
// Difference between Strict and Loose Equality
let nums2 = 12;
let str2 = "12";
console.log(nums2 == str2); // Loose Equality: true (values match)
console.log(nums2 === str2); // Strict Equality: false (data types different)
```

*Explanation:*  
- **Comparison Operators**: Values ko compare karne ke liye use kiye jate hain. Strict Equality (`===`) aur Loose Equality (`==`) ke beech ka difference hai.

### 8.4 Ternary Operator

```javascript
let age = 12;
age >= 18 ? console.log("You can drive") : console.log("You cannot drive");
```

*Explanation:*  
- **Ternary Operator**: Ek compact way to perform conditional checks. Syntax: `condition ? valueIfTrue : valueIfFalse`.

### 8.5 Logical Operators

```javascript
let a1 = true;
let b1 = false;

if (a1 && b1) {
  console.log("Both a1 and b1 are true.");
} 
if (a1 || b1) {
    console.log("At least one of a1 or b1 is true.");
} 
if (!a1) {
    console.log("a1 is false.");
}
```

*Explanation:*  
- **Logical Operators**: Logical operations perform karte hain.
  - **AND (`&&`)**: Dono operands true honi chahiye tab true return karta hai.
  - **OR (`||`)**: Agar ek operand bhi true ho to true return karta hai.
  - **NOT (`!`)**: Operand ka truthiness invert karta hai.

### 8.6 Non-Booleans

*Explanation:*  
- **Falsey Values**: `false`, `undefined`, `null`, `0`, `''`, `NaN` (Not a Number).  
- **Truthy Values**: Falsey values ke alawa sabhi values truthy hoti hain.

```javascript
console.log(false || "lawda"); // Output: lawda (first truthy value)
```

*Explanation:*  
- **Non-Booleans**: JavaScript mein kuch values falsey hoti hain aur kuch truthy. OR (`||`) operator pehle truthy value ko return karta hai.

---

