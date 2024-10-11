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
            color: #4CAF50;
            margin: 15px 0;
            padding: 10px;
            background-color: #e0f7e0;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        h2:hover {
            background-color: #c8e6c9;
        }
        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.8);
            padding-top: 60px;
        }
        .modal-content {
            background-color: #ffffff;
            margin: 5% auto;
            padding: 20px;
            border: none;
            width: 80%;
            max-width: 800px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            position: relative;
        }
        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
        }
        .close:hover,
        .close:focus {
            color: #000;
            text-decoration: none;
            cursor: pointer;
        }
        .modal-header {
            text-align: center;
            font-size: 1.8em;
            margin-bottom: 15px;
            font-weight: bold;
        }
        .modal-body {
            font-size: 1.1em;
            line-height: 1.6;
        }
        .api-section {
            background-color: #f0f0f0;
            padding: 15px;
            margin-top: 20px;
            border-radius: 10px;
        }
        .api-section h3 {
            margin-top: 0;
        }
        .bullet-point-section {
            margin-bottom: 20px;
        }
        .bullet-point-section ul {
            list-style-type: disc;
            margin-left: 20px;
        }
    </style>
</head>
<body>
    <h1>AP Computer Science A Units Overview</h1>

    <!-- Unit 1 -->
    <h2 onclick="openModal('unit1Modal')">Unit 1: Primitive Types</h2>
    <div id="unit1Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit1Modal')">&times;</span>
            <div class="modal-header">Unit 1: Primitive Types</div>
            <div class="modal-body">
                <div class="bullet-point-section">
                    <h3>Main Concepts:</h3>
                    <ul>
                        <li>Store simple data such as deadlines, progress tracking, and GPA.</li>
                        <li>Use int for deadlines, double for GPA, and boolean for task statuses.</li>
                        <li>Apply condition checks with primitive types for progress tracking.</li>
                        <li>Use boolean logic to ensure application completion is tracked properly.</li>
                    </ul>
                </div>
                <div class="api-section">
                    <h3>API Implications:</h3>
                    <ul>
                        <li>Validate primitive types like GPA and deadlines in API endpoints.</li>
                        <li>Send boolean values for task statuses via API for updates.</li>
                        <li>API responses return primitive types for app completion or missing details.</li>
                        <li><a href="https://nighthawkcoders.github.io/portfolio_2025/csa/unit1/primitives">Data Type Def</a></li>                    </ul>
                </div>
            </div>
        </div>
    </div>

    <!-- Unit 2 -->
    <h2 onclick="openModal('unit2Modal')">Unit 2: Using Objects</h2>
    <div id="unit2Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit2Modal')">&times;</span>
            <div class="modal-header">Unit 2: Using Objects</div>
            <div class="modal-body">
                <div class="bullet-point-section">
                    <h3>Main Concepts:</h3>
                    <ul>
                        <li>Create objects to represent real-world data (Colleges, Applications, Students).</li>
                        <li>Encapsulate data to ensure privacy and control access to attributes like GPA.</li>
                        <li>Use methods in objects to manipulate data, like updating application status.</li>
                        <li>Write reusable, scalable code using objects and classes.</li>
                    </ul>
                </div>
                <div class="api-section">
                    <h3>API Implications:</h3>
                    <ul>
                        <li>Represent students and applications as objects when interacting with the API.</li>
                        <li>Serialize/deserialize objects when sending/receiving data from API.</li>
                        <li>Use class methods for data manipulation via API calls.</li>
                        <li><a href="https://nighthawkcoders.github.io/portfolio_2025/csa/unit2/period3/part4/">Constructor Usage</a></li>                    
                        <li><a href="https://www.digitalocean.com/community/tutorials/constructor-in-java">Constructor Resource I used</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <!-- Unit 3 -->
    <h2 onclick="openModal('unit3Modal')">Unit 3: Boolean Expressions and if Statements</h2>
    <div id="unit3Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit3Modal')">&times;</span>
            <div class="modal-header">Unit 3: Boolean Expressions and if Statements</div>
            <div class="modal-body">
                <div class="bullet-point-section">
                    <h3>Main Concepts:</h3>
                    <ul>
                        <li>Use if statements to check if a student has completed all requirements.</li>
                        <li>Apply boolean logic to dynamically determine eligibility for college matches.</li>
                        <li>Set triggers for feedback on essays or application steps using boolean flags.</li>
                        <li>Enhance decision-making in application workflows with conditionals.</li>
                    </ul>
                </div>
                <div class="api-section">
                    <h3>API Implications:</h3>
                    <ul>
                        <li>API endpoints return booleans for key operations like "application complete".</li>
                        <li>Use backend boolean logic to filter data for API responses (e.g., eligible colleges).</li>
                        <li>Send if-statement results to frontend to display status (e.g., essay submission status).</li>
                        <li><a href="https://nighthawkcoders.github.io/portfolio_2025/csa/unit3-p1/unit3-4">If Else and Elif in java</a></li>

                    </ul>
                </div>
            </div>
        </div>
    </div>

    <!-- Unit 4 -->
    <h2 onclick="openModal('unit4Modal')">Unit 4: Iteration</h2>
    <div id="unit4Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit4Modal')">&times;</span>
            <div class="modal-header">Unit 4: Iteration</div>
            <div class="modal-body">
                <div class="bullet-point-section">
                    <h3>Main Concepts:</h3>
                    <ul>
                        <li>Use loops to iterate through student applications and track completion rates.</li>
                        <li>Apply for loops to process a list of colleges or application requirements.</li>
                        <li>Use while loops for continuous processes like dashboard updates until application submission.</li>
                        <li>Streamline progress checks using break and continue statements.</li>
                    </ul>
                </div>
                <div class="api-section">
                    <h3>API Implications:</h3>
                    <ul>
                        <li>Backend iteration processes student and college data efficiently to generate match results.</li>
                        <li>For loops process lists of applications, returning only necessary data for the frontend.</li>
                        <li>Return paginated or chunked data in APIs to optimize iteration over large datasets.</li>
                        <li><a href="https://nighthawkcoders.github.io/portfolio_2025/csa/unit4-p1/unit4-2">While And For Loops in Java (forms of iteration)</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <!-- Unit 5 -->
    <h2 onclick="openModal('unit5Modal')">Unit 5: Writing Classes</h2>
    <div id="unit5Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit5Modal')">&times;</span>
            <div class="modal-header">Unit 5: Writing Classes</div>
            <div class="modal-body">
                <div class="bullet-point-section">
                    <h3>Main Concepts:</h3>
                    <ul>
                        <li>Create classes to represent complex entities like students or colleges.</li>
                        <li>Ensure encapsulation and proper constructor use when initializing objects.</li>
                        <li>Write methods to manipulate the object’s state (e.g., updating college preference or application progress).</li>
                        <li>Focus on Object-Oriented Programming principles like inheritance and polymorphism.</li>
                        
                    </ul>
                </div>
                <div class="api-section">
                    <h3>API Implications:</h3>
                    <ul>
                        <li>Ensure class methods are exposed via API calls for CRUD operations.</li>
                        <li>Apply Object-Oriented Programming principles to handle API data models (students, applications, colleges).</li>
                        <li>Use inheritance to extend features across multiple data models in API design.</li>
                        <li><a href="https://nighthawkcoders.github.io/portfolio_2025/csa/unit5/5.1/">Class Developing (used for CRUD)</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <!-- Unit 6 -->
    <h2 onclick="openModal('unit6Modal')">Unit 6: Arrays</h2>
    <div id="unit6Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit6Modal')">&times;</span>
            <div class="modal-header">Unit 6: Arrays</div>
            <div class="modal-body">
                <div class="bullet-point-section">
                    <h3>Main Concepts:</h3>
                    <ul>
                        <li>Store collections of data such as a student's multiple test scores.</li>
                        <li>Use arrays to organize large sets of data for easy access and manipulation.</li>
                        <li>Learn how to traverse arrays using loops to perform operations like calculating average scores.</li>
                        <li>Understand how to manipulate arrays (e.g., adding, removing, updating elements).</li>
                    </ul>
                </div>
                <div class="api-section">
                    <h3>API Implications:</h3>
                    <ul>
                        <li>Use arrays to represent lists of student data in API responses.</li>
                        <li>Send and receive arrays from the backend to display information like available colleges or student scores.</li>
                        <li>Implement efficient algorithms on arrays to process large sets of data via API endpoints.</li>
                        <li><a href="https://nighthawkcoders.github.io/portfolio_2025/csa/unit6_p3/6.2/">Array Traversing in java and how to access specific elemtns in index</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <!-- Unit 7 -->
    <h2 onclick="openModal('unit7Modal')">Unit 7: ArrayLists</h2>
    <div id="unit7Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit7Modal')">&times;</span>
            <div class="modal-header">Unit 7: ArrayLists</div>
            <div class="modal-body">
                <div class="bullet-point-section">
                    <h3>Main Concepts:</h3>
                    <ul>
                        <li>Work with dynamic arrays that can change size (ArrayLists).</li>
                        <li>Use ArrayLists to manage flexible data collections like lists of colleges that update frequently.</li>
                        <li>Understand the key differences between arrays and ArrayLists, such as resizing and additional methods.</li>
                        <li>Apply methods like `add()`, `remove()`, and `get()` to manipulate data in ArrayLists.</li>
                    </ul>
                </div>
                <div class="api-section">
                    <h3>API Implications:</h3>
                    <ul>
                        <li>Use ArrayLists in API design to represent dynamic data structures for applications and student information.</li>
                        <li>Ensure that APIs support list-like data operations for adding, removing, or fetching data dynamically.</li>
                        <li>Efficiently handle dynamic collections in backend systems to send ArrayList data to the frontend.</li>
                        <li><a href="https://nighthawkcoders.github.io/portfolio_2025/csa/unit7-p3/unit7-1">Making use of arraylists for dynamic data storage</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <!-- Unit 8 -->
    <h2 onclick="openModal('unit8Modal')">Unit 8: 2D Arrays</h2>
    <div id="unit8Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit8Modal')">&times;</span>
            <div class="modal-header">Unit 8: 2D Arrays</div>
            <div class="modal-body">
                <div class="bullet-point-section">
                    <h3>Main Concepts:</h3>
                    <ul>
                        <li>Work with two-dimensional arrays to store grid-like data (e.g., test scores for multiple subjects).</li>
                        <li>Understand how to traverse and manipulate 2D arrays with nested loops.</li>
                        <li>Store data like student grades across different subjects in a 2D array format.</li>
                        <li>Apply 2D arrays to solve problems that require matrix-like data structures.</li>
                    </ul>
                </div>
                <div class="api-section">
                    <h3>API Implications:</h3>
                    <ul>
                        <li>Use 2D arrays in APIs to manage data that requires both row and column storage (e.g., school timetable).</li>
                        <li>Implement backend algorithms to process 2D arrays efficiently and return relevant information.</li>
                        <li>Serialize 2D arrays to send complex data structures between the backend and frontend.</li>
                        <li><a href="https://nighthawkcoders.github.io/portfolio_2025/csa/unit8yay/8.1/">Static Data Storage in Java</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <!-- Unit 9 -->
    <h2 onclick="openModal('unit9Modal')">Unit 9: Inheritance</h2>
    <div id="unit9Modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('unit9Modal')">&times;</span>
            <div class="modal-header">Unit 9: Inheritance</div>
            <div class="modal-body">
                <div class="bullet-point-section">
                    <h3>Main Concepts:</h3>
                    <ul>
                        <li>Apply inheritance to reuse code and build upon existing classes (e.g., Student class and HonorsStudent subclass).</li>
                        <li>Understand how to use `extends` to create a child class that inherits the properties and methods of a parent class.</li>
                        <li>Override parent methods in child classes to create specific behaviors for subclasses.</li>
                        <li>Apply polymorphism to allow objects of different types to be treated as instances of a parent class.</li>
                    </ul>
                </div>
                <div class="api-section">
                    <h3>API Implications:</h3>
                    <ul>
                        <li>Use inheritance in API design to allow for flexible, reusable code when dealing with multiple user types (e.g., admin, student).</li>
                        <li>Extend API models for various object types while keeping shared properties and methods in the parent class.</li>
                        <li>Ensure API supports polymorphism to handle objects that belong to different but related classes efficiently.</li>
                        <li><a href="https://nighthawkcoders.github.io/portfolio_2025/inheritance/hierarchies">How subclasses inherent trait from parent classes in java</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <script>
        function openModal(modalId) {
            document.getElementById(modalId).style.display = "block";
        }

        function closeModal(modalId) {
            document.getElementById(modalId).style.display = "none";
        }

        // Close modal if clicked outside of modal content
        window.onclick = function(event) {
            var modals = document.getElementsByClassName("modal");
            for (var i = 0; i < modals.length; i++) {
                if (event.target == modals[i]) {
                    modals[i].style.display = "none";
                }
            }
        }
    </script>
</body>
</html>


## PEER REVIEW FOR SRINIVAS

| Assignment             | Weightage | Grade  | Comments                                                                                                                                                 |
|------------------------|-----------|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| College Board Coverage | 20        | 17/20  | Strong alignment with College Board standards. To improve, consider incorporating more explicit references to specific AP topics for a deeper connection. |
| Java Examples          | 30        | 26/30  | Solid examples of Java implementation. Adding more diverse and complex examples could further enhance the variety and challenge of the lesson.            |
| Popcorn Hack Usage     | 10        | 7/10   | Creative use of the Popcorn Hack. With some adjustments, it could be more seamlessly integrated into the flow of the lesson.                              |
| Homework               | 10        | 9/10   | Reinforces key concepts effectively. Adding a few more challenging questions would push students to think more critically.                                |
| Grading Plan           | 10        | 9/10   | Clear grading criteria are outlined. Adding more detail, such as including partial credit for creativity, would strengthen the assessment framework.       |
| Original and Creative  | 10        | 8/10   | The lesson incorporates some unique and creative ideas. For a fresh approach, try experimenting with elements that haven't been used in previous lessons. |
| **Total**              | 90        | 81/90  | **Overall, this is a strong lesson. With some added complexity and innovative elements, it could reach an even higher level of engagement and depth.**     |


## PERSONAL ASSESSMENT
<table style="width: 100%; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="border: 1px solid #ddd; padding: 8px;">Assignment</th>
      <th style="border: 1px solid #ddd; padding: 8px;">Points</th>
      <th style="border: 1px solid #ddd; padding: 8px;">Grade</th>
      <th style="border: 1px solid #ddd; padding: 8px;">Evidence</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">Pull Request (Integration)</td>
      <td style="border: 1px solid #ddd; padding: 8px;">2</td>
      <td style="border: 1px solid #ddd; padding: 8px;">1.7</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <img width="1172" alt="image" src="https://github.com/user-attachments/assets/83921a12-3e5c-43ce-86f2-193af7135a3a">
      </td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">Relevancy Checklist (Peer)</td>
      <td style="border: 1px solid #ddd; padding: 8px;">2</td>
      <td style="border: 1px solid #ddd; padding: 8px;">1.8</td>
      <td style="border: 1px solid #ddd; padding: 8px;">created this issue and peer reviewed Srinivas</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">Lesson (Group)</td>
      <td style="border: 1px solid #ddd; padding: 8px;">1</td>
      <td style="border: 1px solid #ddd; padding: 8px;">0.91</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <img width="1207" alt="image" src="https://github.com/user-attachments/assets/4029dc59-ec54-4382-84ee-6c0197903518">
      </td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">Homework, Popcorn Hacks</td>
      <td style="border: 1px solid #ddd; padding: 8px;">1 x 8</td>
      <td style="border: 1px solid #ddd; padding: 8px;">7.3</td>
      <td style="border: 1px solid #ddd; padding: 8px;">Refer to Google Sheet Grading</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">Individual Contribution</td>
      <td style="border: 1px solid #ddd; padding: 8px;">1</td>
      <td style="border: 1px solid #ddd; padding: 8px;">0.92</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <a href="https://nighthawkcoders.github.io/portfolio_2025/csa/unit7-p3/home">Contribution 1</a>, 
        <a href="https://nighthawkcoders.github.io/portfolio_2025/csa/unit7-p3/unit7-1">Contribution 2</a>, 
        <a href="https://nighthawkcoders.github.io/portfolio_2025/csa/unit7-p3/unit7-6">Contribution 3</a>
      </td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;">Personal Notebooks / Blogs</td>
      <td style="border: 1px solid #ddd; padding: 8px;">1</td>
      <td style="border: 1px solid #ddd; padding: 8px;">0.91</td>
      <td style="border: 1px solid #ddd; padding: 8px;">
        <a href="https://github.com/DrishyaMody/CSAstudent_T1/tree/main/_notebooks">Personal Notebooks</a>
      </td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 8px;"><strong>Total</strong></td>
      <td style="border: 1px solid #ddd; padding: 8px;"><strong>15</strong></td>
      <td style="border: 1px solid #ddd; padding: 8px;"><strong>13.54</strong></td>
      <td style="border: 1px solid #ddd; padding: 8px;"></td>
    </tr>
  </tbody>
</table>




| Skill                    | Points | Grade | Evidence |
|--------------------------|--------|-------|----------|
| Work Habits (Analytics)   | 1      |   0.92    | <img width="806" alt="image" src="https://github.com/user-attachments/assets/a2c42afc-8854-4b7e-b99c-a9c4b29e3c95">|
| Team Planning (Issue)     | 1      |    0.9   |  [Planning Issue](https://github.com/DrishyaMody/TeamTeachP3/issues/1) |
| Presentation Memories     | 1      |  1     |    - Was a fun experience for all of us collaborating on a repo since CSP, MERGE ERRORS!!!!! we developed a true hate for them, practicing our presentation together in office hours    |
| Grading and Feedback      | 1      |  0.9     |     - Have not received a grade for this aspect of the team Teach yet but we belive we graded fairly across all people but there is always room for improvement     |
| Beyond Perfunctory        | 1      |   0.91    |    We developed a solid lesson but brought a fun interactive aspect to it as well with the jeopardy game that will remain a memorable way to recollect and implement Arraylists in code in the future      |
| **Total**                 | **5**  |  4.63    |    0.926      |
