---
layout: post
title: CB documentation
comments: True
permalink: /CBstudying
---

<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive AP Computer Science A Study Plan</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 2rem; background-color: #f5f5f5; }
    h1, h2, h3 { color: #333; }
    .unit {
      background: white;
      padding: 1rem;
      margin-bottom: 1rem;
      border-radius: 8px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }
    button {
      margin-top: 10px;
      padding: 0.5rem 1rem;
      font-size: 1rem;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #0056b3;
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
      background-color: rgba(0, 0, 0, 0.5);
    }
    .modal-content {
      background-color: #fff;
      margin: 10% auto;
      padding: 20px;
      border-radius: 8px;
      width: 80%;
    }
    .close {
      float: right;
      font-size: 24px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>📚 Interactive AP Computer Science A Study Plan</h1>
  <!-- <p>Plan: 10 weeks | 1 unit per week | 1-2 hours per day</p> -->

  <div id="units-container"></div>

  <div id="modal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal()">&times;</span>
      <div id="modal-body"></div>
    </div>
  </div>

  <!-- === FRQ TYPES SECTION === -->
<h1>📝 Mastering the 4 Types of AP CSA FRQs</h1>
<div id="frqs-container"></div>

<script>
  const frqs = [
    {
      title: 'Methods and Control Structures',
      skills: [
        'Writing methods using loops and conditionals',
        'Using parameters and return values',
        'Understanding control flow'
      ],
      challenges: [
        'Forgetting return statements',
        'Loop logic errors',
        'Not handling edge cases'
      ],
      tip: 'Practice writing small utility methods like checking if a number is prime or summing an array.'
    },
    {
      title: 'Class Design',
      skills: [
        'Creating instance variables and constructors',
        'Writing accessors and mutators',
        'Implementing object behavior with methods'
      ],
      challenges: [
        'Mixing up local and instance variables',
        'Improper use of “this” keyword',
        'Forgetting visibility modifiers'
      ],
      tip: 'Design simple classes like Book or Student and write methods that manipulate their state.'
    },
    {
      title: 'Array / ArrayList',
      skills: [
        'Traversing and modifying arrays and ArrayLists',
        'Using built-in methods for ArrayList',
        'Avoiding off-by-one errors'
      ],
      challenges: [
        'Mutating a list while looping through it',
        'Accessing invalid indices',
        'Mixing up array vs. list methods'
      ],
      tip: 'Practice removing elements, reversing lists, or finding specific values in arrays.'
    },
    {
      title: '2D Arrays',
      skills: [
        'Navigating 2D arrays using nested loops',
        'Reading and writing to rows and columns',
        'Summing or transforming data in grids'
      ],
      challenges: [
        'Confusing row vs. column indexes',
        'Hardcoding sizes instead of using .length',
        'Loop nesting mistakes'
      ],
      tip: 'Start with visual problems like summing rows or diagonals in a grid.'
    }
  ];

  const frqsContainer = document.getElementById('frqs-container');

  frqs.forEach((frq, index) => {
    const div = document.createElement('div');
    div.className = 'unit';
    div.innerHTML = `
      <h2>${frq.title}</h2>
      <button onclick="openFrqModal(${index})">Explore FRQ</button>
    `;
    frqsContainer.appendChild(div);
  });

  function openFrqModal(index) {
    const modal = document.getElementById('modal');
    const body = document.getElementById('modal-body');
    const frq = frqs[index];
    body.innerHTML = `
      <h3>${frq.title}</h3>
      <p><strong>What it tests:</strong></p>
      <ul>${frq.skills.map(skill => `<li>${skill}</li>`).join('')}</ul>
      <p><strong>Common challenges:</strong></p>
      <ul>${frq.challenges.map(ch => `<li>${ch}</li>`).join('')}</ul>
      <p><strong>Study tip:</strong> ${frq.tip}</p>
    `;
    modal.style.display = 'block';
  }
</script>
