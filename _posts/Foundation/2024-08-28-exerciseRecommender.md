---
layout: post
title: Excercise Recommender
# courses: {'csa': {'week': 1}}
# type: ccc
comments: True
permalink: /exerciseRecommender
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
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
        .container {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }
        select {
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
    </style>
</head>
<body>

    <div class="container">
        <select id="muscleGroup">
            <option value="" disabled selected>Select a muscle group</option>
            <option value="chest">Chest, Triceps & Shoulders</option>
            <option value="back">Back & Biceps</option>
            <option value="legs">Legs</option>
        </select>
        <button onclick="recommendExercise()">Recommend Exercises</button>
        <div class="results" id="exerciseResults"></div>
    </div>

    <script>
        function recommendExercise() {
            const muscleGroup = document.getElementById('muscleGroup').value;
            let exercises = '';

            if (muscleGroup === 'chest') {
                exercises = `
                    <p><strong>Chest, Triceps & Shoulders Exercises:</strong></p>
                    <ul>
                        <li>Bench Press</li>
                        <li>Push-Ups</li>
                        <li>Overhead Press</li>
                        <li>Tricep Dips</li>
                        <li>Lateral Raises</li>
                    </ul>
                `;
            } else if (muscleGroup === 'back') {
                exercises = `
                    <p><strong>Back & Biceps Exercises:</strong></p>
                    <ul>
                        <li>Pull-Ups</li>
                        <li>Barbell Rows</li>
                        <li>Deadlifts</li>
                        <li>Bicep Curls</li>
                        <li>Face Pulls</li>
                    </ul>
                `;
            } else if (muscleGroup === 'legs') {
                exercises = `
                    <p><strong>Legs Exercises:</strong></p>
                    <ul>
                        <li>Squats</li>
                        <li>Lunges</li>
                        <li>Leg Press</li>
                        <li>Leg Curls</li>
                        <li>Calf Raises</li>
                    </ul>
                `;
            } else {
                exercises = '<p>Please select a muscle group.</p>';
            }

            document.getElementById('exerciseResults').innerHTML = exercises;
        }
    </script>

</body>
</html>
