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
console.log(false || "Hello"); // Output: Hello (first truthy value)
```

*Explanation:*  
- **Non-Booleans**: JavaScript mein kuch values falsey hoti hain aur kuch truthy. OR (`||`) operator pehle truthy value ko return karta hai.

---

## 8.7 Objects in JavaScript

Objects ka use multiple linked entities ko ek saath group karne ke liye kiya jata hai. Example ke liye, agar aapko ek shape `circle` ka radius, diameter, aur circumference ko ek entity ke roop mein represent karna hai, toh aap ek object use karenge.

```javascript
console.log("Hello jee !");

// Object definition with properties and method
let rectangle = {
    length: 12,
    breadth: 11,
    draw: function() {  // Method inside the object
        console.log("Draw a Rectangle");
    }
};

console.log(rectangle.length);  // Dot notation
console.log(rectangle['length']); // Bracket notation
console.log(rectangle.draw); // Method

// Creating an empty object
let obj1 = {};

// Factory Function for object creation
function createRectangle(length, breadth) {
    return {
        length,
        breadth,
        draw: function() {
            console.log("Draw a Rectangle");
        }
    };
}

let rectangleObj1 = createRectangle(12, 32);
console.log(rectangleObj1);

// Constructor Function for object creation
function Rectangle(length, breadth) {
    this.length = length;
    this.breadth = breadth;
    this.draw = function() {
        console.log('drawing');
    };
}

let rectangleObj2 = new Rectangle(56, 67);
console.log(rectangleObj2);

// Proving functions are objects
// More explanation can be found [here](https://drive.google.com/file/d/1mj7ioPn0uS68f72JQ1CSEmFMilNdx6Vb/view?usp=sharing)

// Dynamic Nature of Objects
let circle = {
    radius: 6, 
    diameter: 12
};

circle.color = "pink"; // Adding a property
console.log(circle);

delete circle.color;  // Removing a property
console.log(circle);
```

*Explanation:*  
- **Objects**: Multiple related properties ko ek single entity ke roop mein group karte hain.
- **Factory Function**: Reusable function for creating objects with similar properties and methods.
- **Constructor Function**: Special function for creating and initializing objects.

## 8.8 Primitives vs Reference Types

JavaScript mein values do types ki hoti hain: Primitives aur Reference Types.

### Primitives

```javascript
// Primitives
let a = 10;
let b = a;
console.log("\nBefore a's increment-->  a: " + a);
console.log("Before a's increment-->  b: " + b);
a++;
console.log("After a's increment-->  a: " + a);
console.log("After a's increment-->  b: " + b);
```

*Explanation:*  
- **Primitives**: Value ko directly copy kiya jata hai. Changes ek value pe effect nahi daalte dusri values pe.

### Reference Types

```javascript
// Reference Types
let a1 = { value: 10 };
let b1 = a1;
console.log("\nBefore value increment-->  a1: " + a1.value);
console.log("Before value increment-->  b1: " + b1.value);
a1.value++;
console.log("After value increment-->  a1: " + a1.value);
console.log("After value increment-->  b1: " + b1.value);
```

*Explanation:*  
- **Reference Types**: Object ka reference (address) copy kiya jata hai. Changes ek object pe sabhi references pe effect daalte hain.

### Functions with Primitives and Objects

```javascript
// Passing primitives to functions (Pass by Value)
let a2 = 10;
function increment(a) {
    a++;
}
increment(a2);
console.log("\n" + a2); // 10

// Passing objects to functions (Pass by Reference)
let a3 = { value: 10 };
function inc(a) {
    a.value++;
}
inc(a3);
console.log("\n" + a3.value); // 11
```

*Explanation:*  
- **Pass by Value**: Primitive values functions mein pass karte waqt copy create hoti hai.
- **Pass by Reference**: Objects functions mein pass karte waqt reference (address) pass hota hai, jisse changes reflect hote hain.

## 8.9 Iterating Over Objects

Objects ke properties ko iterate karne ke liye `for-in` aur `for-of` loops use kiye ja sakte hain.

### For-in Loop

```javascript
let square = {
    sides: 4,
    length: 12,
    color: "Yellow",
    property: "Sundar Square"
};

// Print all key-value pairs of the object
for (let key in square) {
    console.log(key, square[key]);
}
```

*Explanation:*  
- **For-in Loop**: Object ke sabhi properties ko iterate karta hai.

### For-of Loop

```javascript
// Printing keys using for-of loop
for (let key of Object.keys(square)) {
    console.log(key);
}

// Printing key-value pairs using for-of loop
for (let [key, value] of Object.entries(square)) {
    console.log(key, value);
}
```

*Explanation:*  
- **For-of Loop**: `Object.keys()` aur `Object.entries()` methods ke saath use kiya jata hai.

### Checking Property Existence

```javascript
if ("length" in square) {
    console.log("Present");
} else {
    console.log("Absent");
}
```

*Explanation:*  
- **Checking Property**: `in` operator se check kiya jata hai ki object mein specific property hai ya nahi.

## 8.10 Object Cloning

Objects ko clone karne ke liye 3 methods use kiye ja sakte hain:

### 1. Iteration

```javascript
let src = {
    name: "John",
    age: 30,
    city: "New York"
};

let dest = {};
for (let key in src) {
    dest[key] = src[key];
}
console.log(dest);
```

*Explanation:*  
- **Iteration**: Source object ke properties ko manually copy kiya jata hai destination object mein.

### 2. Object.assign

```javascript
let src1 = {
    name: "John",
    age: 30,
    city: "New York"
};

let dest1 = Object.assign({}, src1);
console.log(dest1);
```

*Explanation:*  
- **Object.assign()**: Source object ko destination object mein copy karta hai.

### 3. Spread Operator

```javascript
let src2 = {
    name: "John",
    age: 30,
    city: "New York"
};

let dest2 = { ...src2 };
console.log(dest2);
```

*Explanation:*  
- **Spread Operator**: Object ke properties ko ek naya object mein spread karta hai.

## 8.11 Garbage Collection

JavaScript mein garbage collection automatic hoti hai, jo unused variables aur objects ko deallocate karti hai. 

*Explanation:*  
- **Garbage Collection**: JavaScript automatic memory management provide karta hai. C ya C++ ke comparison mein, jahan manual memory allocation aur deallocation hoti hai, JavaScript mein garbage collector background mein kaam karta hai.

---

### 9\. Objects

JavaScript me objects key-value pairs ka collection hote hain. Ye different data types ko store karne aur manage karne ke liye useful hote hain.

#### 9.1. Creating Objects

**Object Literals**:

Objects ko define karne ka sabse common tareeka object literals ka use karke hota hai.

```javascript
let person = {
    name: "Ashutosh",
    age: 25,
    greet() {
        console.log("Hello, " + this.name);
    }
};
```

**Factory Functions**:

Factory functions objects banane ke liye use hote hain.

```javascript
function createPerson(name, age) {
    return {
        name,
        age,
        greet() {
            console.log("Hello, " + this.name);
        }
    };
}

let person1 = createPerson("Ashutosh", 25);
person1.greet(); // Output: Hello, Ashutosh
```

**Constructor Functions**:

Constructor functions bhi objects create karne ke liye use hote hain, aur ye `new` keyword ke sath call kiye jate hain.

```javascript
function Person(name, age) {
    this.name = name;
    this.age = age;
    this.greet = function() {
        console.log("Hello, " + this.name);
    };
}

let person2 = new Person("Ashutosh", 25);
person2.greet(); // Output: Hello, Ashutosh
```

#### 9.2. Accessing and Modifying Object Properties

**Accessing Properties**:

Object properties ko dot notation ya bracket notation se access kiya ja sakta hai.

```javascript
console.log(person.name); // Dot notation
console.log(person["age"]); // Bracket notation
```

**Modifying Properties**:

Properties ko modify bhi kiya ja sakta hai.

```javascript
person.age = 26; // Dot notation
person["name"] = "Panda"; // Bracket notation
```

**Adding New Properties**:

Nayi properties add kar sakte hain.

```javascript
person.email = "ashutosh@example.com"; // Add new property
```

**Deleting Properties**:

Properties ko delete bhi kiya ja sakta hai.

```javascript
delete person.email; // Delete a property
```

#### 9.3. Methods in Objects

**Object Methods**:

Objects ke andar methods define kar sakte hain jo unki properties ko operate karte hain.

```javascript
let person = {
    name: "Ashutosh",
    greet() {
        console.log("Hello, " + this.name);
    }
};

person.greet(); // Output: Hello, Ashutosh
```

**Getter and Setter Methods**:

Getter aur setter methods use karke properties ko read aur modify kar sakte hain.

```javascript
let person = {
    firstName: "Ashutosh",
    lastName: "Panda",
    get fullName() {
        return this.firstName + " " + this.lastName;
    },
    set fullName(name) {
        [this.firstName, this.lastName] = name.split(" ");
    }
};

console.log(person.fullName); // Access getter
person.fullName = "John Doe"; // Use setter
console.log(person.firstName); // Output: John
console.log(person.lastName); // Output: Doe
```

#### 9.4. Object Iteration

**For...in Loop**:

Objects ke properties ko iterate karne ke liye `for...in` loop use karte hain.

```javascript
for (let key in person) {
    console.log(key + ": " + person[key]);
}
```

**Object.keys()**:

Object ki keys ko array me convert karta hai.

```javascript
let keys = Object.keys(person);
console.log(keys); // Output: Array of property names
```

**Object.values()**:

Object ki values ko array me convert karta hai.

```javascript
let values = Object.values(person);
console.log(values); // Output: Array of property values
```

**Object.entries()**:

Object ke key-value pairs ko array of arrays me convert karta hai.

```javascript
let entries = Object.entries(person);
console.log(entries); // Output: Array of [key, value] pairs
```

#### 9.5. Prototypes and Inheritance

**Prototype Property**:

Prototype property se methods ko share kar sakte hain.

```javascript
function Person(name) {
    this.name = name;
}

Person.prototype.greet = function() {
    console.log("Hello, " + this.name);
};

let person1 = new Person("Ashutosh");
person1.greet(); // Output: Hello, Ashutosh
```

**Inheritance**:

Inheritance se ek class ki properties aur methods ko doosri class me extend kar sakte hain.

```javascript
function Employee(name, jobTitle) {
    Person.call(this, name); // Call parent constructor
    this.jobTitle = jobTitle;
}

Employee.prototype = Object.create(Person.prototype); // Inherit methods from Person
Employee.prototype.constructor = Employee;

let employee1 = new Employee("Ashutosh", "Developer");
console.log(employee1.name); // Output: Ashutosh
console.log(employee1.jobTitle); // Output: Developer
employee1.greet(); // Output: Hello, Ashutosh
```

### 10\. Advanced Array Methods

#### 10.1. `find()` Method

**Finding an Element**:

`find()` method se array me se ek element ko condition ke basis pe find kar sakte hain.

```javascript
let courses = [
    { id: 1, name: 'JavaScript' },
    { id: 2, name: 'Python' }
];

let course = courses.find(c => c.name === 'JavaScript');
console.log(course); // Output: { id: 1, name: 'JavaScript' }
```

#### 10.2. `filter()` Method

**Filtering an Array**:

`filter()` method se ek condition ke basis pe array ke elements ko filter kar sakte hain.

```javascript
let numbers = [-1, 2, 3, -4, 5];
let positiveNumbers = numbers.filter(n => n > 0);
console.log(positiveNumbers); // Output: [2, 3, 5]
```

#### 10.3. `map()` Method

**Mapping Elements**:

`map()` method se array ke elements ko kisi function ke basis pe map kar sakte hain.

```javascript
let numbers = [1, 2, 3];
let doubled = numbers.map(n => n * 2);
console.log(doubled); // Output: [2, 4, 6]
```

#### 10.4. `reduce()` Method

**Reducing an Array**:

`reduce()` method se array ke elements ko ek single value me reduce kar sakte hain.

```javascript
let numbers = [1, 2, 3, 4];
let sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0);
console.log(sum); // Output: 10
```

#### 10.5. `sort()` Method

**Sorting an Array**:

`sort()` method se array ko sort kar sakte hain. Numbers ko ascending ya descending order me sort karna.

```javascript
let numbers = [4, 2, 5, 1, 3];
numbers.sort((a, b) => a - b); // Ascending order
console.log(numbers); // Output: [1, 2, 3, 4, 5]
```

**Sorting Objects**:

Objects ko kisi property ke basis pe sort kar sakte hain.

```javascript
let people = [
    { name: 'Ashutosh', age: 25 },
    { name: 'Panda', age: 30 }
];

people.sort((a, b) => a.age - b.age);
console.log(people); // Output: Sorted by age
```

#### 10.6. `some()` and `every()` Methods

**`some()`**:

`some()` method se check kar sakte hain ki array me kisi element ne condition ko meet kiya hai ya nahi.

```javascript
let numbers = [1, 2, 3, 4];
let hasNegative = numbers.some(n => n < 0);
console.log(hasNegative); // Output: false
```

**`every()`**:

`every()` method se check kar sakte hain ki array ke sabhi elements ne condition ko meet kiya hai ya nahi.

```javascript
let numbers = [1, 2, 3, 4];
let allPositive = numbers.every(n => n > 0);
console.log(allPositive); // Output: true
```

### 11\. Additional Array Methods

#### 11.1. `findIndex()` Method

**Finding Index of an Element**:

`findIndex()` method se array me kisi element ka index find kar sakte hain.

```javascript
let numbers = [1, 2, 3, 4, 5];
let index = numbers.findIndex(n => n === 3);
console.log(index); // Output: 2
```

#### 11.2. `flat()` and `flatMap()` Methods

**Flattening Arrays**:

`flat()` method se nested arrays ko flatten kar sakte hain. Ye method nested arrays ko specified depth tak flatten karta hai.

```javascript
let nestedArray = [1, [2, [3, 4]]];
let flatArray = nestedArray.flat(2); // Flatten 2 levels deep
console.log(flatArray); // Output: [1, 2, 3, 4]
```

**Flattening with Mapping**:

`flatMap()` method ek array ko map karta hai aur uske baad result ko flatten bhi karta hai. Ye method ek hi step me map aur flatten dono operations perform karta hai.

```javascript
let arrays = [[1, 2, 3], [4, 5], [6]];
let flatMappedArray = arrays.flatMap(x => x.map(n => n * 2));
console.log(flatMappedArray); // Output: [2, 4, 6, 8, 10, 12]
```

### 12\. Additional Array Operations

#### 12.1. `splice()` Method

**Adding and Removing Elements**:

`splice()` method se array me elements ko add aur remove kar sakte hain. Ye method directly array ko modify karta hai.

```javascript
let numbers = [1, 2, 3, 4, 5];

// Adding elements
numbers.splice(2, 0, 6, 7); // Syntax: arr.splice(index, deleteCount, item1, item2, ...)
console.log(numbers); // Output: [1, 2, 6, 7, 3, 4, 5]

// Removing elements
numbers.splice(4, 2); // Syntax: arr.splice(index, deleteCount)
console.log(numbers); // Output: [1, 2, 6, 7, 5]
```

#### 12.2. `slice()` Method

**Extracting Subarrays**:

`slice()` method se array ka ek subarray extract kar sakte hain bina original array ko modify kiye.

```javascript
let numbers = [1, 2, 3, 4, 5];
let subArray = numbers.slice(1, 4); // Syntax: arr.slice(startIndex, endIndex)
console.log(subArray); // Output: [2, 3, 4]
```

**Full Slicing**:

Full slicing se array ka part extract kar sakte hain start index se lekar end tak.

```javascript
let numbers = [1, 2, 3, 4, 5];
let slicedArray = numbers.slice(2); // From index 2 to end
console.log(slicedArray); // Output: [3, 4, 5]
```

#### 12.3. `join()` Method

**Joining Array Elements into a String**:

`join()` method se array ke elements ko ek string me join kar sakte hain, separator specify karke.

```javascript
let numbers = [1, 2, 3, 4, 5];
let joinedString = numbers.join('-'); // Syntax: arr.join(separator)
console.log(joinedString); // Output: "1-2-3-4-5"
```

#### 12.4. `split()` Method

**Splitting a String into an Array**:

`split()` method se ek string ko array me split kar sakte hain, specified separator ke basis pe.

```javascript
let str = "Hello there how are you?";
let strArray = str.split(' '); // Syntax: str.split(separator)
console.log(strArray); // Output: ["Hello", "there", "how", "are", "you?"]
```

### 13\. String Manipulation

#### 13.1. String Methods

**Basic String Methods**:

JavaScript me strings ko manipulate karne ke liye kai methods available hain.

```javascript
let str = "   Ashutosh Panda   ";

console.log(str.length); // Length of the string
console.log(str.trim()); // Removes whitespace from both ends
console.log(str.toUpperCase()); // Converts to uppercase
console.log(str.toLowerCase()); // Converts to lowercase
console.log(str.includes("Panda")); // Checks if substring is present
console.log(str.startsWith("Ash")); // Checks if string starts with specified value
console.log(str.endsWith("Panda")); // Checks if string ends with specified value
console.log(str.slice(3, 10)); // Extracts a section of the string
console.log(str.replace("Panda", "Kumar")); // Replaces specified substring
```

**Template Literals**:

Multiline strings aur placeholders ke saath strings create karne ke liye backticks (`) ka use karte hain.

```javascript
let name = "Ashutosh";
console.log(`Hello ${name},
How are you?
Regards.`);
```

### 14\. Date and Time

JavaScript me date aur time handle karne ke liye `Date` object ka use hota hai.

#### 14.1. Creating a Date Object

**Current Date and Time**:

```javascript
let now = new Date();
console.log(now); // Current date and time
```

**Specific Date and Time**:

```javascript
let birthday = new Date(1998, 8, 22); // year, month (0-indexed), day
console.log(birthday);
```

**Formatting Date and Time**:

```javascript
console.log(now.toDateString()); // Date in readable format
console.log(now.toTimeString()); // Time in readable format
console.log(now.toISOString()); // ISO format
```

### 15\. Common Array Operations

#### 15.1. `some()` Method

**Checking if Any Element Matches Condition**:

```javascript
let numbers = [1, 2, 3, 4];
let hasNegative = numbers.some(n => n < 0);
console.log(hasNegative); // Output: false
```

#### 15.2. `every()` Method

**Checking if All Elements Match Condition**:

```javascript
let numbers = [1, 2, 3, 4];
let allPositive = numbers.every(n => n > 0);
console.log(allPositive); // Output: true
```

