# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨

### My answers start here.
## index.html 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript DOM Practice</title>
  <link rel="stylesheet" href="styles.css">
  <script src="script.js" defer></script>
</head>
<body>
  <header>
    <h1 id="mainHeading">Regomoditswe Dibobo</h1>
  </header>

  <section>
    <p id="infoText">This is a paragraph that will be changed with JavaScript.</p>
    <button onclick="changeText()">Change Text</button>
  </section>

  <section>
    <button onclick="changeStyle()">Change Style</button>
  </section>

  <section>
    <button onclick="addElement()">Add Element</button>
    <button onclick="removeElement()">Remove Element</button>
    <div id="container"></div>
  </section>

  <footer>
    <p>&copy; 2025 Regomoditswe Dibobo</p>
  </footer>
</body>
</html>

## script.js
function changeText() {
  document.getElementById("infoText").textContent = "🎉 The text has been changed dynamically!";
}

function changeStyle() {
  document.getElementById("mainHeading").style.color = "purple";
  document.getElementById("mainHeading").style.fontSize = "3rem";
  document.body.style.backgroundColor = "#f0f8ff";
}

function addElement() {
  const newPara = document.createElement("p");
  newPara.textContent = "✨ A new paragraph has been added!";
  newPara.id = "newPara";
  document.getElementById("container").appendChild(newPara);
}

function removeElement() {
  const existingPara = document.getElementById("newPara");
  if (existingPara) {
    existingPara.remove();
  }
}
## styles.css

body {
  font-family: Arial, sans-serif;
  padding: 20px;
  transition: all 0.3s ease-in-out;
}

button {
  margin: 10px;
  padding: 10px 15px;
  font-weight: bold;
  cursor: pointer;
}

