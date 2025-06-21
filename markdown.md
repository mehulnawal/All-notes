# Markdown Language Notes

📑 Markdown Notes Index
What is Markdown?
Headings
Emphasis (Bold, Italic, Strikethrough)
Lists (Ordered and Unordered)
Checkboxes (To-Do Lists)
Code (Inline and Code Blocks)
Links
Images
Blockquote
Horizontal Rule
Tables
Escape Special Characters
Line Breaks
Table of Contents (Manual Linking)
Markdown in VS Code - Preview
Use Cases
Bonus Tip (HTML in Markdown)


## 📘 What is Markdown?

Markdown is a lightweight markup language that allows you to write formatted text using plain text syntax. It’s widely used for documentation, notes, READMEs, blogs, and more.

---

## 🔹 Headings

Use `#` for headings. The number of `#` symbols determines the heading level.

```md
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
```

---

## 🔹 Emphasis

```md
*italic* or _italic_          → italic
**bold** or __bold__          → bold
~~strikethrough~~             → ~~strikethrough~~
```

---

## 🔹 Lists

### Unordered List

```md
- Item 1
- Item 2
  - Subitem 2a
  - Subitem 2b
```

### Ordered List

```md
1. First
2. Second
   1. Sub-numbered
```

---

## 🔹 Checkboxes (To-Do List)

```md
- [x] Completed task
- [ ] Incomplete task
```

---

## 🔹 Code

### Inline Code

```md
Use the `let` keyword.
```

### Code Block

<pre>
```js
function greet(name) {
  return `Hello, ${name}`;
}
```
</pre>

You can also specify the language: `js`, `ts`, `html`, `css`, `bash`, etc.

---

## 🔹 Links

```md
[Google](https://www.google.com)
```

---

## 🔹 Images

```md
![Alt Text](image-url.jpg)
```

---

## 🔹 Blockquote

```md
> This is a blockquote.
```

---

## 🔹 Horizontal Rule

```md
---
```

---

## 🔹 Tables

```md
| Name  | Age |
| ----- | --- |
| Mehul | 21  |
| Riya  | 19  |
```

---

## 🔹 Escape Special Characters

Use `\` before a special character.

```md
\*not italic\*
```

---

## 🔹 Line Breaks

Use **two spaces** at the end of a line or `<br>` tag.

---

## 🔹 Table of Contents (Manually)

```md
## Table of Contents
- [Introduction](#what-is-markdown)
- [Headings](#headings)
- [Emphasis](#emphasis)
```

---

## 🔹 Markdown in VS Code

* `.md` file extension
* Preview with `Ctrl + Shift + V`
* Recommended extensions:

  * Markdown All in One
  * Paste Image
  * Markdown Preview Enhanced

---

## ✅ Use Cases

* Writing clean developer notes
* GitHub README files
* Blog formatting
* Documentation for projects and APIs

---

## 🔚 Bonus Tip

You can combine HTML and Markdown for advanced formatting when needed.

```md
<p style="color: red;">This is red text</p>
```

---
