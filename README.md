# code-alpha-web-development-task2
## BACKGROUND GENERATOR
## background.html

<!DOCTYPE html>
<html>
<head>
  <title>Background Generator</title>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <h1>Background Generator</h1>
  <div class="container">
    <div class="color-picker">
      <label for="color1">Color 1:</label>
      <input type="color" id="color1">
    </div>
    <div class="color-picker">
      <label for="color2">Color 2:</label>
      <input type="color" id="color2">
    </div>
    <button id="gradientBtn">Generate Gradient</button>
  </div>
  <script src="script.js"></script>
</body>
</html>

###style.css

body {
  font-family: Arial, sans-serif;
  background: linear-gradient(to right, #ff0000, #00ff00);
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 0;
}

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 20px;
}

.color-picker {
  margin-bottom: 10px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  background-color: #ffffff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

h1 {
  color: #ffffff;
}


###script.js

const color1 = document.getElementById("color1");
const color2 = document.getElementById("color2");
const gradientBtn = document.getElementById("gradientBtn");
const body = document.querySelector("body");

gradientBtn.addEventListener("click", generateGradient);

function generateGradient() {
  body.style.background = `linear-gradient(to right, ${color1.value}, ${color2.value})`;
}
