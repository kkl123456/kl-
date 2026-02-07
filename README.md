<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <title>我的第一个计算器</title>
  <style>
    body {
      font-family: Arial;
      background: #f2f2f2;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .calculator {
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.2);
    }
    input {
      width: 100%;
      height: 40px;
      font-size: 20px;
      margin-bottom: 10px;
      text-align: right;
    }
    button {
      width: 60px;
      height: 40px;
      margin: 5px;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <div class="calculator">
    <input id="result" disabled>
    <br>
    <button onclick="press('1')">1</button>
    <button onclick="press('2')">2</button>
    <button onclick="press('3')">3</button>
    <button onclick="press('+')">+</button>
    <br>
    <button onclick="press('4')">4</button>
    <button onclick="press('5')">5</button>
    <button onclick="press('6')">6</button>
    <button onclick="press('-')">-</button>
    <br>
    <button onclick="press('7')">7</button>
    <button onclick="press('8')">8</button>
    <button onclick="press('9')">9</button>
    <button onclick="press('*')">*</button>
    <br>
    <button onclick="clearAll()">C</button>
    <button onclick="press('0')">0</button>
    <button onclick="calculate()">=</button>
    <button onclick="press('/')">/</button>
  </div>

  <script>
    function press(value) {
      document.getElementById('result').value += value;
    }
    function clearAll() {
      document.getElementById('result').value = '';
    }
    function calculate() {
      document.getElementById('result').value =
        eval(document.getElementById('result').value);
    }
  </script>
</body>
</html>
起点编程
