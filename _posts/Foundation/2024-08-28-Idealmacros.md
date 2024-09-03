---
layout: post
title: Ideal Macros
# courses: {'csa': {'week': 1}}
# type: ccc
comments: True
permalink: /idealMacros
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Macro Nutrient Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f7f7f7;
        }
        .calculator-container {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            max-width: 300px;
            width: 100%;
            text-align: center;
        }
        h1 {
            font-size: 24px;
            color: #28a745;
            margin-bottom: 20px;
        }
        input {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 16px;
        }
        button {
            background-color: #007bff;
            color: white;
            padding: 10px;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            width: 100%;
        }
        button:hover {
            background-color: #0056b3;
        }
        p {
            font-size: 16px;
            color: #333;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="calculator-container">
        <h1>Macro Calculator</h1>
        <input type="number" id="weight" placeholder="Enter your weight in pounds">
        <button onclick="calculateMacros()">Calculate</button>

        <h2>Results</h2>
        <p id="calories"></p>
        <p id="protein"></p>
        <p id="carbs"></p>
    </div>

    <script>
        function calculateMacros() {
            const weight = document.getElementById('weight').value;

            // Assuming 15 calories per pound as a moderate activity level
            const calories = weight * 15;

            // Ideal protein goal: 30% of daily calories
            const protein = (calories * 0.30) / 4;

            // Ideal carbohydrate goal: 55% of daily calories
            const carbs = (calories * 0.55) / 4;

            // Display results
            document.getElementById('calories').innerText = `Your daily calorie goal: ${calories.toFixed(0)} calories`;
            document.getElementById('protein').innerText = `Daily protein goal: ${protein.toFixed(0)}g`;
            document.getElementById('carbs').innerText = `Daily carbohydrate goal: ${carbs.toFixed(0)}g`;
        }
    </script>
</body>
</html>
