---
layout: post
title: Team Teach Understanding
courses: {'csa': {'week': 7}}
comments: True
type: ccc
permalink: /understanding
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AP CSA Blog</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
            background-color: #f4f4f4;
        }
        h1 {
            text-align: center;
            margin-bottom: 30px;
        }
        h2 {
            cursor: pointer;
            color: #4CAF50; /* Green color */
            margin: 15px 0;
            padding: 10px;
            background-color: #e0f7e0; /* Light green background */
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        h2:hover {
            background-color: #c8e6c9; /* Darker light green on hover */
        }
        /* Modal styles */
        .modal {
            display: none; /* Hidden by default */
            position: fixed; /* Stay in place */
            z-index: 1; /* Sit on top */
            left: 0;
            top: 0;
            width: 100%; /* Full width */
            height: 100%; /* Full height */
            overflow: auto; /* Enable scroll if needed */
            background-color: rgba(0,0,0,0.5); /* Black w/ opacity */
            padding-top: 60px; /* Location of the box */
        }
        .modal-content {
            background-color: #fefefe;
            margin: 5% auto; /* 15% from the top and centered */
            padding: 20px;
            border: 1px solid #888;
            width: 80%; /* Could be more or less, depending on screen size */
            border-radius: 10px;
        }
        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
        }
        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>AP Computer Science A Units Overview</h1>

    <h2 onclick="openModal('unit1Modal')">Unit 1: Primitive Types</h2>
    <div id="unit1Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit1Modal')">&times;</span>
            <ul>
                <li>Introduction to data types: int, double, char, boolean.</li>
                <li>Understanding variable declaration and initialization.</li>
                <li>Exploring type conversion and casting.</li>
            </ul>
        </div>
    </div>

    <h2 onclick="openModal('unit2Modal')">Unit 2: Using Objects</h2>
    <div id="unit2Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit2Modal')">&times;</span>
            <ul>
                <li>Creating and using objects from classes.</li>
                <li>Understanding method calls and parameters.</li>
                <li>Exploring return types and method overloading.</li>
            </ul>
        </div>
    </div>

    <h2 onclick="openModal('unit3Modal')">Unit 3: Boolean Expressions and if Statements</h2>
    <div id="unit3Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit3Modal')">&times;</span>
            <ul>
                <li>Creating boolean expressions with logical operators.</li>
                <li>Using if-else statements for decision-making.</li>
                <li>Nesting if statements for complex conditions.</li>
            </ul>
        </div>
    </div>

    <h2 onclick="openModal('unit4Modal')">Unit 4: Iteration</h2>
    <div id="unit4Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit4Modal')">&times;</span>
            <ul>
                <li>Understanding for, while, and do-while loops.</li>
                <li>Using loops to iterate over arrays and collections.</li>
                <li>Identifying and preventing infinite loops.</li>
            </ul>
        </div>
    </div>

    <h2 onclick="openModal('unit5Modal')">Unit 5: Writing Classes</h2>
    <div id="unit5Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit5Modal')">&times;</span>
            <ul>
                <li>Creating custom classes and defining attributes.</li>
                <li>Understanding constructors and methods.</li>
                <li>Using encapsulation and access modifiers.</li>
            </ul>
        </div>
    </div>

    <h2 onclick="openModal('unit6Modal')">Unit 6: Arrays</h2>
    <div id="unit6Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit6Modal')">&times;</span>
            <ul>
                <li>Declaring, initializing, and accessing array elements.</li>
                <li>Understanding array length and common array operations.</li>
                <li>Exploring multidimensional arrays.</li>
            </ul>
        </div>
    </div>

    <h2 onclick="openModal('unit7Modal')">Unit 7: ArrayList</h2>
    <div id="unit7Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit7Modal')">&times;</span>
            <ul>
                <li>Using ArrayList for dynamic data storage.</li>
                <li>Understanding common methods like add, remove, and get.</li>
                <li>Exploring the advantages of ArrayLists over arrays.</li>
            </ul>
        </div>
    </div>

    <h2 onclick="openModal('unit8Modal')">Unit 8: String</h2>
    <div id="unit8Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit8Modal')">&times;</span>
            <ul>
                <li>Understanding String immutability and common operations.</li>
                <li>Exploring methods like substring, indexOf, and charAt.</li>
                <li>Using StringBuilder for mutable strings.</li>
            </ul>
        </div>
    </div>

    <h2 onclick="openModal('unit9Modal')">Unit 9: 2D Arrays</h2>
    <div id="unit9Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit9Modal')">&times;</span>
            <ul>
                <li>Understanding 2D arrays and their representation.</li>
                <li>Iterating through 2D arrays using nested loops.</li>
                <li>Common use cases for 2D arrays in programming.</li>
            </ul>
        </div>
    </div>

    <script>
        function openModal(modalId) {
            document.getElementById(modalId).style.display = "block";
        }

        function closeModal(modalId) {
            document.getElementById(modalId).style.display = "none";
        }

        // Close the modal if the user clicks anywhere outside of it
        window.onclick = function(event) {
            const modals = document.getElementsByClassName("modal");
            for (let i = 0; i < modals.length; i++) {
                if (event.target == modals[i]) {
                    modals[i].style.display = "none";
                }
            }
        }
    </script>
</body>
</html>
