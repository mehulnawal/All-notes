# 📘 SCSS Notes (with Advanced Topics)

## Index : 
# 📘 SCSS Notes (with Advanced Topics)

---

## 🧭 Index
- 1. What is SCSS?
- 2.📜 History
- 3. Difference Between SCSS and Sass
- 4. Installation of SCSS in VS Code
- 🛠️ Steps:
- 5. Why Use SCSS in 2025?
- 6. Operators
- 7. Variables
- 8. Nesting and `&`
- 9. Mixins
- 10. Parameters in Mixins
- 11. Partials
- 12. `@use` (Modern Import)
- 13. `@forward` (Module Re-export)
- 14. `@extend` (Inheritance)
- 15. Functions

---



## 1. What is SCSS?

**SCSS (Sassy CSS)** is a **CSS preprocessor syntax** that adds powerful features to CSS like variables, nesting, mixins, inheritance, etc. It is a more CSS-like syntax of Sass that supports all CSS syntax.

### 📜 History:

* SCSS was introduced in **Sass 3** as a more CSS-compatible syntax.
* It allows writing standard CSS while adding Sass features.

---

## 2. What is Sass?

**Sass (Syntactically Awesome Stylesheets)** is a preprocessor scripting language that is interpreted or compiled into CSS. It provides advanced functionality not available in vanilla CSS.

### 📜 History:

* Created by **Hampton Catlin** and developed by **Natalie Weizenbaum** in 2006.
* Originally used indented syntax (no `{}` or `;`)
* SCSS syntax was introduced later for CSS compatibility.

---

## 3. Difference Between SCSS and Sass

| Feature       | SCSS Syntax                 | Sass Syntax                  |
| ------------- | --------------------------- | ---------------------------- |
| Extension     | `.scss`                     | `.sass`                      |
| Syntax Style  | CSS-like with `{}` and `;`  | Indented with no `{}` or `;` |
| Compatibility | Fully compatible with CSS   | Not directly compatible      |
| Readability   | More readable for CSS users | Cleaner for minimalists      |

---

## 4. Installation of SCSS in VS Code

### 🛠️ Steps:

1. **Install Node.js** from [https://nodejs.org](https://nodejs.org)
2. Open terminal and install Sass:

   ```bash
   npm install -g sass
   ```
3. Create a `.scss` file in your project.
4. Compile SCSS to CSS:

   ```bash
   sass style.scss style.css
   ```
5. To watch for changes automatically:

   ```bash
   sass --watch style.scss:style.css
   ```

---

## 5. Why Use SCSS in 2025?

CSS now supports variables and nesting partially, but SCSS still has:

* Full nesting with `&`
* Advanced math operators
* Reusable mixins and functions
* Partials and modular file structure
* Inheritance with `@extend`
* `@use` and `@forward` for scoped imports and modules

---

## 6. Operators

```scss
.container {
  width: 100% / 2; // 50%
  margin: 10px + 5px; // 15px
}
```

---

## 7. Variables

```scss
$primary-color: #3498db;

.button {
  background-color: $primary-color;
}
```

---

## 8. Nesting and `&`

```scss
.card {
  padding: 10px;

  h2 {
    color: red;
  }

  &:hover {
    background-color: #f0f0f0;
  }
}
```

---

## 9. Mixins

```scss
@mixin flexCenter {
  display: flex;
  justify-content: center;
  align-items: center;
}

.header {
  @include flexCenter;
}
```

---

## 10. Parameters in Mixins

```scss
@mixin theme($color) {
  background-color: $color;
}

.button {
  @include theme(blue);
}
```

---

## 11. Partials

Split SCSS into reusable files:

* File: `_variables.scss`

```scss
$font-stack: Helvetica, sans-serif;
```

* File: `main.scss`

```scss
@use 'variables';

body {
  font-family: variables.$font-stack;
}
```

---
## 12. `@use` (Modern Import)

```scss
// _colors.scss
$primary: #007bff;
```

```scss
// main.scss
@use 'colors';

body {
  color: colors.$primary;
}
```

* Scoped access prevents variable conflicts.
* Replaces older `@import` method.

---

## 13. `@forward` (Module Re-export)

Used in combination with `@use` to create centralized modules.

```scss
// _index.scss
@forward 'colors';
@forward 'mixins';
```

```scss
// main.scss
@use 'index';
```

* Helps create reusable design systems or utility packs.

---

## 14. `@extend` (Inheritance)

```scss
%button-base {
  padding: 10px;
  border: none;
}

.btn-primary {
  @extend %button-base;
  background-color: blue;
}
```

* Use `%placeholder` selectors to avoid compiling unused styles.

---

## 15. Functions

```scss
@function double($value) {
  @return $value * 2;
}

.container {
  width: double(50px); // 100px
}
```

* Custom functions help make styles more dynamic.

---

> ✅ SCSS makes your CSS more powerful, maintainable, and modular — especially helpful for large-scale or component-based designs.

```