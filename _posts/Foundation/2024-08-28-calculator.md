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
            background-color: black; /* Black background */
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

        /* Vanta.js styling */
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
    <!-- Vanta.js background animation -->
    <div id="animation"></div>

    <div class="calculator-container">
        <!-- Output -->
        <div class="calculator-output" id="output">0</div>
        
        <!-- Number and operation buttons -->
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

        <div class="calculator-clear">A/C</div>
        <div class="calculator-number">0</div>
        <div class="calculator-number">.</div>
        <div class="calculator-equals">=</div>
    </div>

    <!-- JavaScript (JS) implementation of the calculator -->
    <script>
        // initialize important variables to manage calculations
        var firstNumber = null;
        var operator = null;
        var nextReady = true;
        // Build objects containing key elements
        const output = document.getElementById("output");
        const numbers = document.querySelectorAll(".calculator-number");
        const operations = document.querySelectorAll(".calculator-operation");
        const clear = document.querySelectorAll(".calculator-clear");
        const equals = document.querySelectorAll(".calculator-equals");

        // Number buttons listener
        numbers.forEach(button => {
            button.addEventListener("click", function() {
                number(button.textContent);
            });
        });

        // Number action
        function number(value) { // function to input numbers into the calculator
            if (value != ".") {
                if (nextReady == true) { // nextReady is used to tell the computer when the user is going to input a completely new number
                    output.innerHTML = value;
                    if (value != "0") { // if statement to ensure that there are no multiple leading zeroes
                        nextReady = false;
                    }
                } else {
                    output.innerHTML = output.innerHTML + value; // concatenation is used to add the numbers to the end of the input
                }
            } else { // special case for adding a decimal; can't have two decimals
                if (output.innerHTML.indexOf(".") == -1) {
                    output.innerHTML = output.innerHTML + value;
                    nextReady = false;
                }
            }
        }

        // Operation buttons listener
        operations.forEach(button => {
            button.addEventListener("click", function() {
                operation(button.textContent);
            });
        });

        // Operator action
        function operation(choice) { // function to input operations into the calculator
            if (firstNumber == null) { // once the operation is chosen, the displayed number is stored into the variable firstNumber
                firstNumber = parseFloat(output.innerHTML);
                nextReady = true;
                operator = choice;
                return; // exits function
            }
            // occurs if there is already a number stored in the calculator
            firstNumber = calculate(firstNumber, parseFloat(output.innerHTML)); 
            operator = choice;
            output.innerHTML = firstNumber.toString();
            nextReady = true;
        }

        // Calculator
        function calculate(first, second) { // function to calculate the result of the equation
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
                default: 
                    break;
            }
            return result;
        }

        // Equals button listener
        equals.forEach(button => {
            button.addEventListener("click", function() {
                equal();
            });
        });

        // Equal action
        function equal() { // function used when the equals button is clicked; calculates equation and displays it
            firstNumber = calculate(firstNumber, parseFloat(output.innerHTML));
            output.innerHTML = firstNumber.toString();
            nextReady = true;
        }

        // Clear button listener
        clear.forEach(button => {
            button.addEventListener("click", function() {
                clearCalc();
            });
        });

        // A/C action
        function clearCalc() { // clears calculator
            firstNumber = null;
            output.innerHTML = "0";
            nextReady = true;
        }
    </script>

    <!-- Vanta.js animations -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r121/three.min.js"></script>
    <script src="https://cdn.jsdelivr.net/gh/tengbao/vanta@latest/dist/vanta.halo.min.js"></script>
    <script>
        VANTA.HALO({
            el: "#animation",
            mouseControls: true,
            touchControls: true,
            gyroControls: false,
            backgroundColor: 0x0, // Black background
            amplitudeFactor: 1.0,
            size: 1.0,
            baseColor: 0xff007f, // Example color customization
            backgroundAlpha: 0.9,
        });
    </script>
</body>
</html>
