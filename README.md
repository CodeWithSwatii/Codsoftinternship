# Codsoftinternship
<!DOCTYPE html>
<html>
<head>
  <title>Simple Calculator</title>
  <h1>CALCULATOR</h1>
  <style>
    body{
        background-color: bisque;
    }
    h1{
        text-align: center;
    }
    .calculator {
      width: 300px;
      margin: 0 auto;
      border: 2px solid #138626;
      border-radius: 5px;
      background-color: #d9dfe1;
    }

    .calculator input[type="text"] {
      width: 100%;
      height: 40px;
      font-size: 40px;
      text-align: right;
      padding: 5px;
      border: none;
      outline: none;
    }

    .calculator .row {
      display: flex;
    }

    .calculator .row input[type="button"] {
      width: 25%;
      height: 60px;
      font-size: 24px;
      border: 1px solid #683c03;
      background-color: #d38383;
      cursor: pointer;
    }

    .calculator .row input[type="button"]:hover {
      background-color: #8fcf5d;
    }
  </style>
</head>
<body>
  <div class="calculator">
    <input type="text" id="display" disabled>
    <div class="row">
      <input type="button" value="7" onclick="addToDisplay('7')">
      <input type="button" value="8" onclick="addToDisplay('8')">
      <input type="button" value="9" onclick="addToDisplay('9')">
      <input type="button" value="/" onclick="addToDisplay('/')">
    </div>
    <div class="row">
      <input type="button" value="4" onclick="addToDisplay('4')">
      <input type="button" value="5" onclick="addToDisplay('5')">
      <input type="button" value="6" onclick="addToDisplay('6')">
      <input type="button" value="*" onclick="addToDisplay('*')">
    </div>
    <div class="row">
      <input type="button" value="1" onclick="addToDisplay('1')">
      <input type="button" value="2" onclick="addToDisplay('2')">
      <input type="button" value="3" onclick="addToDisplay('3')">
      <input type="button" value="-" onclick="addToDisplay('-')">
    </div>
    <div class="row">
      <input type="button" value="C" onclick="clearDisplay()">
      <input type="button" value="0" onclick="addToDisplay('0')">
      <input type="button" value="=" onclick="calculate()">
      <input type="button" value="+" onclick="addToDisplay('+')">
    </div>
  </div>

  <script>
    function addToDisplay(value) {
      document.getElementById("display").value += value;
    }

    function clearDisplay() {
      document.getElementById("display").value = '';
    }

    function calculate() {
      try {
        document.getElementById("display").value = eval(document.getElementById("display").value);
      } catch (err) {
        document.getElementById("display").value = 'Error';
      }
    }
  </script>
</body>
</html>
