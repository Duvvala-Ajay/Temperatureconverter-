

1. Create an HTML file (index.html):

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <div class="container">
    <h1>Temperature Converter</h1>
    <input type="number" id="inputTemp" placeholder="Enter temperature in Celsius" />
    <button onclick="convertToCelsius()">Celsius to Fahrenheit</button>
    <button onclick="convertToFahrenheit()">Fahrenheit to Celsius</button>
    <p id="result"></p>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

```css
body {
  font-family: Arial, sans-serif;
  text-align: center;
  background-color: #f2f2f2;
}

.container {
  margin: 20% auto;
  padding: 20px;
  background-color: white;
  border-radius: 5px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
}

h1 {
  color: #333;
}

input {
  width: 100%;
  padding: 10px;
  margin: 10px 0;
  border: 1px solid #ccc;
  border-radius: 3px;
}

button {
  background-color: #4CAF50;
  color: white;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}

#result {
  font-weight: bold;
  font-size: 18px;
  margin-top: 20px;
}
``

```javascript
function convertToCelsius() {
  const inputTemp = parseFloat(document.getElementById('inputTemp').value);
  const result = (inputTemp * 9/5) + 32;
  document.getElementById('result').innerText = `${inputTemp}°C is ${result}°F`;
}

function convertToFahrenheit() {
  const inputTemp = parseFloat(document.getElementById('inputTemp').value);
  const result = (inputTemp - 32) * 5/9;
  document.getElementById('result').innerText = `${inputTemp}°F is ${result}°C`;
}
```

