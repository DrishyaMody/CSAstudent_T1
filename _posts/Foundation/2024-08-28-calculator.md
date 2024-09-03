---
layout: post
title: Calculator
# courses: {'csa': {'week': 1}}
# type: ccc
comments: True
permalink: /calculator
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Styled Calculator</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: black;
        }
        .calculator-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            grid-gap: 10px;
            background-color: #222;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
            max-width: 400px;
            width: 100%;
        }
        .calculator-output {
            grid-column: span 4;
            background-color: #333;
            color: white;
            font-size: 2rem;
            padding: 15px;
            border-radius: 10px;
            text-align: right;
            border: 2px solid #444;
        }
        .calculator-number, .calculator-operation, .calculator-clear, .calculator-equals {
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.5rem;
            padding: 20px;
            border-radius: 10px;
            background-color: #555;
            color: white;
            cursor: pointer;
            border: 2px solid #666;
            transition: background-color 0.3s, box-shadow 0.3s;
        }
        .calculator-number:hover, .calculator-operation:hover, .calculator-clear:hover, .calculator-equals:hover {
            background-color: #777;
            box-shadow: 0 0 10px rgba(255, 255, 255, 0.2);
        }
        .calculator-clear {
            background-color: orange;
            color: black;
            grid-column: span 2;
        }
        .calculator-equals {
            background-color: red;
            color: white;
            grid-column: span 2;
        }
        /* History display styling */
        .calculator-history {
            grid-column: span 4;
            background-color: #111;
            color: white;
            font-size: 1rem;
            padding: 10px;
            border-radius: 10px;
            text-align: left;
            border: 2px solid #444;
            max-height: 100px;
            overflow-y: auto;
            margin-top: 10px;
        }
        #animation {
            width: 100%;
            height: 100%;
            position: fixed;
            top: 0;
            left: 0;
            z-index: -1;
        }
    </style>
</head>
<body>
    <div id="animation"></div>
    <div class="calculator-container">
        <div class="calculator-output" id="output">0</div>
        <div class="calculator-number">1</div>
        <div class="calculator-number">2</div>
        <div class="calculator-number">3</div>
        <div class="calculator-operation">+</div>
        <div class="calculator-number">4</div>
        <div class="calculator-number">5</div>
        <div class="calculator-number">6</div>
        <div class="calculator-operation">-</div>
        <div class="calculator-number">7</div>
        <div class="calculator-number">8</div>
        <div class="calculator-number">9</div>
        <div class="calculator-operation">*</div>
        <!-- Operators you added: ^, /, % -->
        <div class="calculator-operation">^</div> <!-- Exponentiation -->
        <div class="calculator-operation">/</div> <!-- Division -->
        <div class="calculator-operation">%</div> <!-- Modulus -->
        <div class="calculator-clear">A/C</div>
        <div class="calculator-number">0</div>
        <div class="calculator-number">.</div>
        <div class="calculator-equals">=</div>
        <!-- History display area -->
        <div class="calculator-history" id="history"></div>
    </div>
    <script>
        var firstNumber = null;
        var operator = null;
        var nextReady = true;
        const output = document.getElementById("output");
        const history = document.getElementById("history");
        const numbers = document.querySelectorAll(".calculator-number");
        const operations = document.querySelectorAll(".calculator-operation");
        const clear = document.querySelectorAll(".calculator-clear");
        const equals = document.querySelectorAll(".calculator-equals");
        numbers.forEach(button => {
            button.addEventListener("click", function() {
                number(button.textContent);
            });
        });
        function number(value) {
            if (value != ".") {
                if (nextReady == true) {
                    output.innerHTML = value;
                    if (value != "0") {
                        nextReady = false;
                    }
                } else {
                    output.innerHTML = output.innerHTML + value;
                }
            } else {
                if (output.innerHTML.indexOf(".") == -1) {
                    output.innerHTML = output.innerHTML + value;
                    nextReady = false;
                }
            }
        }
        operations.forEach(button => {
            button.addEventListener("click", function() {
                operation(button.textContent);
            });
        });
        function operation(choice) {
            if (firstNumber == null) {
                firstNumber = parseFloat(output.innerHTML);
                nextReady = true;
                operator = choice;
                return;
            }
            firstNumber = calculate(firstNumber, parseFloat(output.innerHTML));
            operator = choice;
            output.innerHTML = firstNumber.toString();
            nextReady = true;
        }
        function calculate(first, second) {
            let result = 0;
            switch (operator) {
                case "+":
                    result = first + second;
                    break;
                case "-":
                    result = first - second;
                    break;
                case "*":
                    result = first * second;
                    break;
                case "/":
                    result = first / second;
                    break;
                case "^": // Exponentiation operation
                    result = Math.pow(first, second);
                    break;
                case "%": // Modulus operation
                    result = first % second;
                    break;
                default:
                    break;
            }
            // Add operation to history
            updateHistory(`${first} ${operator} ${second} = ${result}`);
            return result;
        }
        equals.forEach(button => {
            button.addEventListener("click", function() {
                equal();
            });
        });
        function equal() {
            firstNumber = calculate(firstNumber, parseFloat(output.innerHTML));
            output.innerHTML = firstNumber.toString();
            nextReady = true;
        }
        clear.forEach(button => {
            button.addEventListener("click", function() {
                clearCalc();
            });
        });
        function clearCalc() {
            firstNumber = null;
            output.innerHTML = "0";
            nextReady = true;
        }
        // Function to update the history display
        function updateHistory(entry) {
            const newHistoryItem = document.createElement("div");
            newHistoryItem.textContent = entry;
            history.appendChild(newHistoryItem);
            // Scroll history to the bottom
            history.scrollTop = history.scrollHeight;
        }
    </script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r121/three.min.js"></script>
    <script src="https://cdn.jsdelivr.net/gh/tengbao/vanta@latest/dist/vanta.halo.min.js"></script>
    <script>
        VANTA.HALO({
            el: "#animation",
            mouseControls: true,
            touchControls: true,
            gyroControls: false,
            backgroundColor: 0x0,
            amplitudeFactor: 1.0,
            size: 1.0,
            baseColor: 0xff007f,
            backgroundAlpha: 0.9,
        });
    </script>
</body>
</html>
