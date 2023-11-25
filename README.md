# Simple-Calculator
This is a Simple Calculator
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Simple Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 100px;
    }
    .calculator {
      display: inline-block;
      border: 1px solid #ccc;
      padding: 20px;
      border-radius: 5px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    .calculator input[type="text"] {
      width: 100%;
      margin-bottom: 10px;
      padding: 10px;
      font-size: 18px;
      border-radius: 3px;
      border: 1px solid #ccc;
    }
    .calculator button {
      width: 45px;
      height: 45px;
      margin: 5px;
      font-size: 18px;
      border-radius: 50%;
      border: none;
      cursor: pointer;
      background-color: #f0f0f0;
    }
    .calculator button:hover {
      background-color: #e0e0e0;
    }
  </style>
</head>
<body>

<div class="calculator">
  <input type="text" id="display" disabled>
  <br>
  <button onclick="appendToDisplay('7')">7</button>
  <button onclick="appendToDisplay('8')">8</button>
  <button onclick="appendToDisplay('9')">9</button>
  <button onclick="appendToDisplay('+')">+</button>
  <br>
  <button onclick="appendToDisplay('4')">4</button>
  <button onclick="appendToDisplay('5')">5</button>
  <button onclick="appendToDisplay('6')">6</button>
  <button onclick="appendToDisplay('-')">-</button>
  <br>
  <button onclick="appendToDisplay('1')">1</button>
  <button onclick="appendToDisplay('2')">2</button>
  <button onclick="appendToDisplay('3')">3</button>
  <button onclick="appendToDisplay('*')">*</button>
  <br>
  <button onclick="clearDisplay()">C</button>
  <button onclick="appendToDisplay('0')">0</button>
  <button onclick="calculateResult()">=</button>
  <button onclick="appendToDisplay('/')">/</button>
</div>

<script>
  function appendToDisplay(value) {
    document.getElementById('display').value += value;
  }

  function clearDisplay() {
    document.getElementById('display').value = '';
  }

  function calculateResult() {
    const displayValue = document.getElementById('display').value;
    let result;
    try {
      result = eval(displayValue);
    } catch (error) {
      result = 'Error';
    }
    document.getElementById('display').value = result;
  }
</script>

</body>
</html>
