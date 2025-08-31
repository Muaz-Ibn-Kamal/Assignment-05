# Assignment – JavaScript DOM & Events

## Q1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

- **getElementById** → Selects a single element by its unique `id`. It always returns one element or `null`.
- **getElementsByClassName** → Selects multiple elements that have the same class. It returns an HTMLCollection (like an array, but not exactly).
- **querySelector** → Selects the **first element** that matches a CSS selector (id, class, tag, attribute etc.).
- **querySelectorAll** → Selects **all elements** that match a CSS selector. It returns a NodeList which you can loop through.

👉 In short:  
- `getElementById("id")` → one element only  
- `getElementsByClassName("class")` → many elements by class  
- `querySelector(".class or #id")` → first match  
- `querySelectorAll(".class")` → all matches  

---

## Q2. How do you create and insert a new element into the DOM?

Steps:
1. Create the element using `document.createElement("tag")`.  
   Example: `let div = document.createElement("div");`
2. Add content or attributes → `div.innerText = "Hello";` or `div.classList.add("box");`
3. Insert it into the DOM using methods like:
   - `appendChild()` → adds inside at the end  
   - `prepend()` → adds inside at the beginning  
   - `insertBefore()` → adds before a specific element  

Example:
```js
let p = document.createElement("p");
p.innerText = "This is a new paragraph.";
document.body.appendChild(p);
