# Ex.08 Design of a Standard Calculator
## Date:

## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        .container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .calculator {
            background-color: #333;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
            width: 300px;
        }

        input {
            width: calc(100% - 10px);
            height: 50px;
            padding: 10px;
            margin-bottom: 10px;
            border: none;
            border-radius: 5px;
            font-size: 24px;
            text-align: right;
            background-color: #444;
            color: #fff;
        }

        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
        }

        button {
            width: calc(100% - 10px);
            height: 50px;
            padding: 10px;
            border: none;
            border-radius: 5px;
            font-size: 20px;
            background-color: #777;
            color: #fff;
            cursor: pointer;
        }

        .equal {
            grid-column: span 2;
            background-color: #ff9500;
        }

        .header {
            text-align: center;
            margin-bottom: 20px;
            color: #fff;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="calculator">
            <div class="header">
                <h2>Calculator</h2>
                <p>MURALI KRISHNA.S (212223230129)</p>
            </div>
            <input type="text" id="output-screen" placeholder="0">
            <div class="buttons">
                <button onclick="clearScreen()">C</button>
                <button onclick="deleteLast()">DEL</button>
                <button onclick="appendToScreen('%')">%</button>
                <button onclick="appendToScreen('/')">/</button>
                <button onclick="appendToScreen('7')">7</button>
                <button onclick="appendToScreen('8')">8</button>
                <button onclick="appendToScreen('9')">9</button>
                <button onclick="appendToScreen('')"></button>
                <button onclick="appendToScreen('4')">4</button>
                <button onclick="appendToScreen('5')">5</button>
                <button onclick="appendToScreen('6')">6</button>
                <button onclick="appendToScreen('-')">-</button>
                <button onclick="appendToScreen('1')">1</button>
                <button onclick="appendToScreen('2')">2</button>
                <button onclick="appendToScreen('3')">3</button>
                <button onclick="appendToScreen('+')">+</button>
                <button onclick="appendToScreen('.')">.</button>
                <button onclick="appendToScreen('0')">0</button>
                <button onclick="calculate()" class="equal">=</button>
            </div>
        </div>
    </div>

    <script>
        let outputScreen = document.getElementById("output-screen");

        function appendToScreen(value) {
            outputScreen.value += value;
        }

        function calculate() {
            try {
                outputScreen.value = eval(outputScreen.value);
            } catch(err) {
                alert("Invalid expression");
            }
        }

        function clearScreen() {
            outputScreen.value = "";
        }

        function deleteLast() {
            outputScreen.value = outputScreen.value.slice(0, -1);
        }
    </script>
</body>
</html>
```

## OUTPUT:
![Screenshot 2024-05-10 140124](https://github.com/Murali-Krishna0/Calc/assets/149054535/e44c1fb6-cacb-4505-8de1-d3e865e36d86)
![Screenshot 2024-05-10 140134](https://github.com/Murali-Krishna0/Calc/assets/149054535/a5988411-da4d-4310-a349-83508e6915d1)


## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
