---
layout: page
title: About
permalink: /about/
comments: true
---

<style>
  /* Container for the timeline, set to scroll horizontally */
  .timeline {
    display: flex; /* Align items in a row */
    flex-wrap: nowrap; 
    overflow-x: auto; /* Enable horizontal scrolling */
    margin: 0 auto; /* Center align the timeline */
    padding: 20px 0; 
    white-space: nowrap; 
    max-width: 100%; 
  }

  /* Style for scrollbar thumb */
  .timeline::-webkit-scrollbar-thumb {
    background: #FF9F55; 
    border-radius: 10px; 
  }

  /* Container for each timeline item */
  .container {
    flex: 0 0 auto; 
    width: 200px;
    margin: 10px; 
    background-color: white; 
    border-radius: 10px; 
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
    text-align: center; 
    cursor: pointer;
    transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out; 
  }

  /* Header style within each container */
  .container h2 {
    color: #FF9F55; 
    padding-top: 10px; 
    font-size: 1.2em; 
  }

  /* Image style within each container */
  .container img {
    width: 80%; 
    height: auto; 
    border-radius: 0 0 10px 10px; 
  }

  /* Hover effect for timeline items */
  .container:hover {
    transform: scale(1.05); /* Slightly enlarge item on hover */
    box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.2); /* Darker shadow on hover */
  }

  /* Style for modal background */
  .modal {
    display: none; 
    position: fixed; 
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%; 
    height: 100%; 
    overflow: auto; 
    background-color: rgba(0, 0, 0, 0.8); 
  }

  /* Style for modal content */
  .modal-content {
    margin: 15% auto; 
    padding: 20px; 
    background-color: white; 
    border-radius: 10px; 
    width: 60%;
    text-align: center; 
  }

  /* Image style within modal */
  .modal img {
    width: 80%;
    height: auto; 
    margin-bottom: 15px;
    border-radius: 10px; 
  }

  /* Bullet points style within modal */
  .modal ul {
    list-style-type: disc; 
    text-align: left; 
    margin: 0 auto; 
    padding-left: 20px; 
  }

  /* Paragraph text style within modal */
  .modal p {
    font-size: 1em; 
    color: #333; 
  }

  /* Style for close button in modal */
  .close {
    color: #aaa; 
    float: right; 
    font-size: 28px; 
    font-weight: bold; 
  }

  /* Hover and focus style for close button */
  .close:hover,
  .close:focus {
    color: black; 
    text-decoration: none; 
    cursor: pointer; 
  }
</style>

As an Extrovert I am...

- an aspiring senior at Del Norte High School 
- desire to major in Data Science 
- Experience as a leader in entrepreneurship, CS projects 
- A pretty friendly guy, am a people person, love hanging out with people in free time
- Been playing soccer for 14 years


<img src="/CSAstudent_T1/images/csacollage.png" alt="My Interests" height="500" width="400">

<div class="timeline">
  <!-- Timeline item for 2024 -->
  <div class="container" onclick="openModal('modal2024')">
    <h2>2024</h2>
    <img src="/CSAstudent_T1/images/EY.png" alt="EY Internship">
  </div>
  
  <!-- Timeline item for 2023 -->
  <div class="container" onclick="openModal('modal2023')">
    <h2>2023</h2>
    <img src="/CSAstudent_T1/images/weatherApp.png" alt="Weather application">
  </div>

  <!-- Timeline item for 2022 -->
  <div class="container" onclick="openModal('modal2022')">
    <h2>2022</h2>
    <img src="/CSAstudent_T1/images/saferoads.png" alt="Entrepreneurship Project">
  </div>
  
  <!-- Timeline item for 2021 -->
  <div class="container" onclick="openModal('modal2021')">
    <h2>2021</h2>
    <img src="/CSAstudent_T1/images/soccerShots.png" alt="Soccer Shots Volunteerd">
  </div>
</div>

<!-- Modal for 2024 -->
<div id="modal2024" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('modal2024')">&times;</span>
    <h2>2024 - EY Internship</h2>
    <img src="/CSAstudent_T1/images/EY.png" alt="EY Internship">
    <ul>
      <li>Completed an internship at EY.</li>
      <li>Gained insights into consulting and data science.</li>
      <li>OTHER ACTIVITIES IN 2024 SUMMER</li>
        <li>Completed AP Calculus BC</li>
        <li>Participated in Inspirit AI program</li>
        <li>Worked on College Apps!</li>
    </ul>
  </div>
</div>

<!-- Modal for 2023 -->
<div id="modal2023" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('modal2023')">&times;</span>
    <h2>2023 - Weather Application</h2>
    <img src="/CSAstudent_T1/images/weatherApp.png" alt="Weather application">
    <ul>
      <li>Developed a weather application.</li>
      <li>Integrated live weather data APIs.</li>
        <li>OTHER CS PROJECTS</li>
        <li>Stock Prediction ML</li>
        <li>Fully functioning Forum (Collabora)</li>
        <li>Titanic Survival ML</li>
        <li>Flask backend development</li>
        <li>Binary Clock</li>
    </ul>
  </div>
</div>

<!-- Modal for 2022 -->
<div id="modal2022" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('modal2022')">&times;</span>
    <h2>2022 - Entrepreneurship Project</h2>
    <img src="/CSAstudent_T1/images/saferoads.png" alt="Entrepreneurship Project">
    <ul>
      <li>Led a project on road safety.</li>
      <li>Focused on tech innovations.</li>
      <li>Placed 4th in NuFund Pitch Competition amongst Angel Investors</li>
      <li>OTHER SUMMER ACTIVITIES</li>
        <li>AP Calc BC Semester 1</li>
        <li>AP Macroeconomics</li>
        <li>Miramar Entrepreneurship Course</li>
    </ul>
  </div>
</div>

<!-- Modal for 2021 -->
<div id="modal2021" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('modal2021')">&times;</span>
    <h2>2021 - Soccer Team</h2>
    <img src="/CSAstudent_T1/images/soccerShots.png" alt="Soccer Shots">
    <ul>
      <li>Learned to coach children under 7</li>
      <li>Learned the operational aspect of Soccer Shots </li>
      <li>Developed teamwork and leadership skills</li>
    </ul>
  </div>
</div>

<!-- Trivia Section -->
<div id="trivia-section" style="text-align: center; padding: 30px 0;">
  <h2>Test Your Knowledge: Drishya Trivia!</h2>
  <p>How well do you know me? Answer these questions to find out!</p>

  <!-- Question 1 -->
  <div class="trivia-question">
    <h3>1. How long have I been playing soccer?</h3>
    <button onclick="checkAnswer(1, 'correct')">14 years</button>
    <button onclick="checkAnswer(1, 'wrong')">10 years</button>
    <button onclick="checkAnswer(1, 'wrong')">5 years</button>
    <p id="answer1"></p>
  </div>

  <!-- Question 2 -->
  <div class="trivia-question">
    <h3>2. What was my entrepreneurship project in 2022 focused on?</h3>
    <button onclick="checkAnswer(2, 'correct')">Road safety</button>
    <button onclick="checkAnswer(2, 'wrong')">Environmental conservation</button>
    <button onclick="checkAnswer(2, 'wrong')">Food delivery</button>
    <p id="answer2"></p>
  </div>

  <!-- Question 3 -->
  <div class="trivia-question">
    <h3>3. Where did I complete an Internship at over the Summer 2024?</h3>
    <button onclick="checkAnswer(3, 'wrong')">SoccerShots</button>
    <button onclick="checkAnswer(3, 'correct')">Ernst & Young</button>
    <button onclick="checkAnswer(3, 'wrong')">Baskin Robbins</button>
    <p id="answer3"></p>
  </div>

  <div style="margin-top: 20px;">
    <p id="final-message"></p>
  </div>
</div>

<script>
  let correctAnswers = 0;

  function checkAnswer(question, result) {
    let answerText = document.getElementById('answer' + question);
    if (result === 'correct') {
      answerText.innerHTML = "Correct!";
      answerText.style.color = "green";
      correctAnswers++;
    } else {
      answerText.innerHTML = "Oops! Try again.";
      answerText.style.color = "red";
    }
    checkCompletion();
  }

  function checkCompletion() {
    if (correctAnswers === 3) {
      document.getElementById('final-message').innerHTML = "You're a Drishya expert!";
    }
  }

  // Function to open a modal
  function openModal(modalId) {
    document.getElementById(modalId).style.display = "block";
  }

  // Function to close a modal
  function closeModal(modalId) {
    document.getElementById(modalId).style.display = "none";
  }
</script>
