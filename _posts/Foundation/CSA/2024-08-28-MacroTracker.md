---
layout: post
title: Macronutrients tracker
# courses: {'csa': {'week': 1}}
# type: ccc
comments: True
permalink: /macroTracker
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Macro Tracker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }
        h1 {
            color: #333;
        }
        .tracker-wrapper {
            display: flex;
            gap: 20px;
        }
        .tracker-container {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
            display: flex;
            flex-direction: column;
        }
        input[type="number"], input[type="date"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-sizing: border-box;
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
        }
        button:hover {
            background-color: #0056b3;
        }
        .results {
            margin-top: 20px;
            text-align: left;
        }
        .results p {
            margin: 5px 0;
            font-size: 16px;
            color: #555;
        }
        .reset-button {
            background-color: #dc3545;
            margin-top: 10px;
        }
        .reset-button:hover {
            background-color: #c82333;
        }
    </style>
</head>
<body>

    <h1>Macro Tracker</h1>
    <div class="tracker-wrapper">
        <div class="tracker-container">
            <input type="number" id="calories" placeholder="Enter calories">
            <input type="number" id="protein" placeholder="Enter protein (grams)">
            <input type="number" id="carbs" placeholder="Enter carbs (grams)">
            <button onclick="addMacros()">Add Macros</button>
            <button class="reset-button" onclick="resetMacros()">Reset for Next Day</button>
            <div class="results" id="results"></div>
        </div>

        <div class="tracker-container">
            <input type="date" id="datePicker">
            <button onclick="viewMacros()">View Macros for Selected Date</button>
            <div class="results" id="viewResults"></div>
        </div>
    </div>

    <script>
        function getTodayDateKey() {
            const today = new Date();
            return today.toISOString().split('T')[0];
        }

        function getStoredMacros(dateKey) {
            return JSON.parse(localStorage.getItem(dateKey)) || {
                calories: 0,
                protein: 0,
                carbs: 0
            };
        }

        function saveMacros(dateKey, macros) {
            localStorage.setItem(dateKey, JSON.stringify(macros));
        }

        function updateResults() {
            const todayKey = getTodayDateKey();
            const { calories, protein, carbs } = getStoredMacros(todayKey);
            document.getElementById('results').innerHTML = `
                <p><strong>Total Calories:</strong> ${calories} kcal</p>
                <p><strong>Total Protein:</strong> ${protein} g</p>
                <p><strong>Total Carbs:</strong> ${carbs} g</p>
            `;
        }

        function addMacros() {
            const inputCalories = parseInt(document.getElementById('calories').value) || 0;
            const inputProtein = parseInt(document.getElementById('protein').value) || 0;
            const inputCarbs = parseInt(document.getElementById('carbs').value) || 0;

            const todayKey = getTodayDateKey();
            const storedMacros = getStoredMacros(todayKey);

            const newMacros = {
                calories: storedMacros.calories + inputCalories,
                protein: storedMacros.protein + inputProtein,
                carbs: storedMacros.carbs + inputCarbs
            };

            saveMacros(todayKey, newMacros);

            updateResults();

            document.getElementById('calories').value = '';
            document.getElementById('protein').value = '';
            document.getElementById('carbs').value = '';
        }

        function resetMacros() {
            const todayKey = getTodayDateKey();
            localStorage.removeItem(todayKey);
            updateResults();
        }

        function viewMacros() {
            const dateKey = document.getElementById('datePicker').value;
            if (!dateKey) {
                document.getElementById('viewResults').innerHTML = `<p style="color: red;">Please select a date.</p>`;
                return;
            }

            const { calories, protein, carbs } = getStoredMacros(dateKey);
            document.getElementById('viewResults').innerHTML = `
                <p><strong>Date:</strong> ${dateKey}</p>
                <p><strong>Total Calories:</strong> ${calories} kcal</p>
                <p><strong>Total Protein:</strong> ${protein} g</p>
                <p><strong>Total Carbs:</strong> ${carbs} g</p>
            `;
        }

        updateResults();
    </script>

</body>
</html>
