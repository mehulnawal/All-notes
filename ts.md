# TypeScript Notes

**Topics:**

TS File CConfiguration
open using ts --init in terminal 
- "noEmitOnError" : true   // Don't compile if there's an error
- "target": "ES6" 
- "module" : "es6:
- "strict": true,   // Enable all strict type checks

---
**Index:**
1. TS Define and Benefits
2. TS Data Types
3. Tuples
4. Enums
5. Interface - Basic, Extends Interface, Optional Interface
6. Type
7. Access Modifiers - Public, Private, Protected, Readonly
8. Parameter Properties
9.  Getters and Setters
10. Static
11. Callback
12. Rest and Spread
13. Generics
14. Type Assertions
15. Utility Types (`Partial<T>`, `Readonly<T>`, `Pick<T>`, etc.)
16. Type Guards

---

## 1. What is TypeScript?

TypeScript is a typed superset of JavaScript that compiles to plain JavaScript. It adds optional static types, interfaces, classes, access modifiers, and advanced tooling for better developer experience.

**Benefits of TypeScript:**

* Early error detection via static type checking
* Improved IDE support (autocompletion, IntelliSense)
* Better code organization with interfaces and types
* Easier refactoring

---

## 2. Basic Types:

```ts
let isDone: boolean = false;
let age: number = 25;
let username: string = "Mehul";
let numbers: number[] = [1, 2, 3];
let user: [string, number] = ["Mehul", 21]; // Tuple
```

---

## 3. Tuples

A tuple is a fixed-length array with specific types in specific positions.

```ts
let person: [string, number] = ["Mehul", 21];
```

**🧠 Use Case:**
Use a tuple when you want a group of related values of different types with a fixed structure — like name and age.

---

## 4. Enums

An enum is a set of named constants (labels for values) used to make your code more readable.

```ts
enum OrderStatus {
  Pending = "PENDING",
  Shipped = "SHIPPED",
}

function trackOrder(status: OrderStatus) {
  switch (status) {
    case OrderStatus.Pending:
      console.log("Your order is being processed.");
      break;
    case OrderStatus.Shipped:
      console.log("Your order is on the way!");
      break;
  }
}

// Call the function with different enum values
trackOrder(OrderStatus.Pending);    // Output: Your order is being processed.
trackOrder(OrderStatus.Delivered);  // Output: Order delivered. Enjoy!
```

---

## 5. Interface

### 5.1 Basic Interface

```ts
interface User {
    name: string;
    age?: number; // Optional property
}

function add(obj: User = { name: "name", age: 12 }) {
    console.log(obj.name, obj.age);
}

add({ name: "mehul", age: 20 });
```

### 5.2 Interface Extension

```ts
interface Admin extends User {
    admin: boolean;
}

function addAdmin(obj: Admin) {
    console.log(obj.name, obj.age, obj.admin);
}

addAdmin({ name: "mehul", age: 20, admin: true });
```

✅ If two interfaces have the same name, they will be merged automatically.

---

## 6. Type

### 6.1 Union Type

```ts
type Value = string | number | null;
let a: Value = "mehul";
a = 12;
```

### 6.2 Intersection Type

```ts
type A = {
    name: string;
};

type Admin = A & {
    admin: boolean;
};

function showAdmin(obj: Admin) {
    console.log(obj.name, obj.admin);
}

showAdmin({ name: "mehul", admin: true });
```

### Interface vs Type

1. **Declaration Merging**

   * `interface`: ✅ Supports merging
   * `type`: ❌ Does not support merging

2. **Extension**

   * `interface`: Uses `extends`
   * `type`: Uses intersections (`&`)

3. **Use Cases**

   * `interface`: For object structure
   * `type`: For primitives, unions, complex types

---

## 7. Access Modifiers

### 7.1 `public` (default)

Accessible everywhere.

```ts
class Person {
    public name: string;
    constructor(name: string) {
        this.name = name;
    }
    public greet() {
        console.log(`Hello, ${this.name}`);
    }
}
```

### 7.2 `private`

Accessible only within the same class.

```ts
class Person {
    private ssn: string;
    constructor(ssn: string) {
        this.ssn = ssn;
    }
}
```

### 7.3 `protected`

Accessible in class and its subclasses.

```ts
class Person {
    protected age: number;
    constructor(age: number) {
        this.age = age;
    }
}
```

### Readonly

```ts
class Bottle {
    constructor(public readonly companyName: string) { }
}

let b1 = new Bottle("Cello");
// b1.companyName = "Milton"; ❌ Error
```

---

## 8. Parameter Properties

```ts
class Bottle {
    constructor(
        public readonly companyName: string,
        public age: number,
        public gender?: string
    ) { }
}
```

---

## 9. Getters & Setters

```ts
class Person {
    constructor(private _name: string, private _age: number) { }

    get personName(): string {
        return this._name;
    }

    set personName(newName: string) {
        this._name = newName;
    }
}

let p1 = new Person("Mehul", 21);
console.log(p1.personName); // Mehul
p1.personName = "Nawal";
console.log(p1.personName); // Nawal
```

---

## 10. Static

```ts
class MehulJs {
    static version = 1.0;
    static getOwnerName() {
        return "Mehul";
    }
}

console.log(MehulJs.version);
console.log(MehulJs.getOwnerName());
```

---

## 11. Callback

```ts
function greet(name: string, cb: (msg: string) => void) {
    console.log(name);
    cb("Hello");
}

greet("Mehul", (msg) => console.log(msg));
```

### Optional & Default Parameters

```ts
function display(name: string, age: number, gender?: string) {
    console.log(name, gender);
}

display("Mehul", 21);

function show(name: string, age: number, gender: string = "Unknown") {
    console.log(name, gender);
}
```

---

## 12. Rest & Spread

```ts
function logValues(a: number, ...rest: number[]) {
    console.log(rest);
}

logValues(1, 2, 3, 4);

const arr1 = [1, 2];
const arr2 = [3, 4];
const merged = [...arr1, ...arr2];
console.log(merged);
```

---

## 13. Generics

### 13.1 Generic Function

```ts
function identity<T>(arg: T) {
    console.log(typeof arg);
}

identity("Mehul");
identity(42);
```

### 13.2 Generic Interface

```ts
interface Wrapper<T> {
    name: string;
    key: T;
}

function useWrapper(data: Wrapper<string | number>) {
    console.log(data.name, data.key);
}
```

### 13.3 Generic Class

```ts
class Container<T> {
    constructor(public label: string, public value: T) { }
}

let c1 = new Container("Item1", 123);
let c2 = new Container("Item2", "abc");
```

---

## 14. Type Assertions

```ts
let a: any = 12.34;
let b = Math.floor(a as number);
console.log(b);

let c: any = "hello";
console.log((<string>c).toUpperCase());
```

---

## 15. Utility Types

* `Partial<T>`
* `Readonly<T>`
* `Pick<T>`

(Examples can be added later)

---

## 16. Type Guards

### 16.1 Using `typeof`

```ts
function printValue(val: string | number) {
    if (typeof val === "string") {
        console.log("Uppercase:", val.toUpperCase());
    } else {
        console.log("Squared:", val * val);
    }
}
```

### 16.2 Using `instanceof`

```ts
class Car {
    drive() {
        console.log("Driving");
    }
}
class Bike {
    ride() {
        console.log("Riding");
    }
}

function useVehicle(v: Car | Bike) {
    if (v instanceof Car) {
        v.drive();
    } else {
        v.ride();
    }
}
```

### 16.3 Using `in` Operator

```ts
type Dog = { bark: () => void };
type Cat = { meow: () => void };

function makeSound(animal: Dog | Cat) {
    if ("bark" in animal) {
        animal.bark();
    } else {
        animal.meow();
    }
}
```

---

## ✅ Additional Topics to Cover

* Namespaces / Modules (organize large projects)
* Utility Types (`Partial<T>`, `Readonly<T>`, `Pick<T>`, etc.)
* `never` & `unknown` types
