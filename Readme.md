# Javascript Problem Solving

## ✔️DOM - Document Object Model 

Que. Create a H2 heading element with text - “Hello JavaScript”.Append “from MIT College students” to this text using JS.

HTML

```html
<html>
  <head>
    <title>Document Object Model</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h2>Hello Javascript!</h2>
    <script src="script.js"></script>
  </body>
</html>
```

Javascript

```javascript
let h2 = document.querySelector("h2");
h2.innerText = h2.innerText + " from MIT college student";
```

Que. Create 3 divs with common class name - “box”. Access them &add some unique text to each of them.

HTML

```html
<html>
  <head>
    <title>Document Object Model</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h2>Hello Javascript!</h2>
    <div class="box">first div</div>
    <div class="box">second div</div>
    <div class="box">third div</div>
    <script src="script.js"></script>
  </body>
</html>
```

CSS

```css
.box {
  width: 100px;
  height: 100px;
  border: 1px solid black;
  margin: 5px;
  text-align: center;
  background-color: aquamarine;
}
```

Javascript

```javascript
let divs = document.querySelectorAll(".box");

let idx = 1;

for (let div of divs) {
  div.innerText = `new unique value ${idx}`;
  idx++;
}
```

Que. Create a new button element. Give it a text “click me”, background color of red & text color of white.
Insert the button as the first element inside the body tag

HTML

```html
<html>
  <head>
    <title>Document Object Model</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <script src="script.js"></script>
  </body>
</html>
```

Javascript

```javascript
let newBtn = document.createElement("button");
newBtn.innerText = "Click me!";
newBtn.style.color = "white";
newBtn.style.backgroundColor = "red";

document.querySelector("body").prepend(newBtn);
```

Que. Create a p tag in html, give it a class & some styling.
Now create a new class in CSS and try to append this class to the p element.
Solve this problem using classList.
Did you notice, how you overwrite the class name when you add a new one?

HTML

```html
<html>
  <head>
    <title>Document Object Model</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <p class="content">I'm a paragraph.</p>
    <script src="script.js"></script>
  </body>
</html>
```

CSS

```css
.content {
  color: red;
}

.newClass {
  background-color: green;
}
```

Javascript

```javascript
let para = document.querySelector("p");

para.classList.add("newClass");
```

## ✔️Events in Javascript

Que. Create a toggle button that changes the screen to dark-mode when clicked & light-mode when clicked again.

HTML

```html
<html>
  <head>
    <title>Events</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <button id="mode">Change Mode</button>
    <p>Welcome to my website!</p>
    <script src="script.js"></script>
  </body>
</html>
```

CSS

```css
.dark {
  background-color: black;
  color: white;
}

.light {
  background-color: white;
  color: black;
}
```

Javascript

```javascript
let modeBtn = document.querySelector("#mode");
let body = document.querySelector("body");
let currMode = "light";

modeBtn.addEventListener("click", () => {
  if (currMode === "light") {
    currMode = "dark";
    body.classList.add("dark");
    body.classList.remove("light");
  } else {
    currMode = "light";
    body.classList.add("light");
    body.classList.remove("dark");
  }
  console.log(currMode);
});
```
