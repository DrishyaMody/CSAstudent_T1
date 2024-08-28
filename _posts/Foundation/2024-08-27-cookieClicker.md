---
layout: post
title: Cookie Clicker
courses: {'csa': {'week': 1}}
type: ccc
comments: True
permalink: /cookies
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
        }
        img {
            cursor: pointer;
            width: 350px; /* cookie size */
        }
        .shop {
            margin-top: 20px; /* margin between score and shop titlem*/
        }
    </style>
</head>
<body>
    <img id="cookie" src="/CSAstudent_T1/images/cookie.png" alt="cookie"> 
    <!-- referral to my images file with the cookie image -->
    <p>Score: <span id="score">0</span></p> 
    <div class="shop">
        <h2>SHOP</h2>
        <p>Worker: 100 cookies</p> 
        <!-- // price of worker -->
        <button id="buyWorker">Buy Worker</button> 
        <!-- // button for worker purchase -->
        <p>Each worker adds 1 cookie per click</p> 
        <!-- // worker legend -->
    </div>
    <audio id="clickSound" src="/CSAstudent_T1/click.mp3"></audio> 
    <!-- //referring to mp3 file to create clicking noise when cookie is clicked -->
    <script>
        let score = 0; // defining score 
        let cookiesPerClick = 1; // per click one cookie gained in the beginning
        let workers = 0; // starting with no workers purchased
        document.getElementById('cookie').addEventListener('click', () => {
            score += cookiesPerClick; // getting cookie image & listener so when cookie is clicked will add cpc to current score
            document.getElementById('score').innerText = score; // updating score
            document.getElementById('clickSound').play(); //play sound after every click
        });
        document.getElementById('buyWorker').addEventListener('click', () => { // listener to provide worker 
            if (score >= 100) { // ensuring that player has at least 100 cookies
                score -= 100; // subtracts 100 from score after worker purchased
                workers++; //adds worker
                cookiesPerClick = 1 + workers; //updates cpc
                document.getElementById('score').innerText = score; // score update
            }
        });
    </script>
</body>
</html>
