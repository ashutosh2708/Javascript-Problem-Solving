# Javascript Problem Solving

### DOM - Document Object Model

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
