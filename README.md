# Building a Basic Calculator Web Application

This README provides a step-by-step guide on how to build a simple web-based calculator using HTML, CSS, and JavaScript.

## Table of Contents
- [Introduction](#introduction)
- [Step-by-Step Guide](#step-by-step-guide)
  - [1. Set Up the Project Structure](#1-set-up-the-project-structure)
  - [2. Create the HTML Structure](#2-create-the-html-structure)
  - [3. Style the Calculator](#3-style-the-calculator)
  - [4. Add JavaScript Functionality](#4-add-javascript-functionality)
- [Demo](#demo)
- [Conclusion](#conclusion)

## Introduction

Building a basic calculator web application is a great way to practice front-end development skills. This project will involve creating the user interface using HTML and CSS, and implementing the calculator's functionality using JavaScript.

## Step-by-Step Guide

### 1. Set Up the Project Structure

Create a new directory for your project and set up the following files:
- `index.html`: HTML file for the calculator's user interface.
- `styles.css`: CSS file for styling the calculator.
- `script.js`: JavaScript file for implementing the calculator's functionality.

### 2. Create the HTML Structure

In the `index.html` file, create the basic structure for the calculator:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Basic Calculator</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Calculator display -->
    <input type="text" id="display" readonly>

    <!-- Calculator buttons -->
    <div class="buttons">
        <!-- Add buttons for numbers and operators -->
    </div>

    <script src="script.js"></script>
</body>
</html>
```

### 3. Style the Calculator
In the .css file, add styles to make the calculatoe more visually appealing. 

### 4. Add JavaScript Functionality
Within the .js file, implement logic and code that allows the calculator to work, below is an example of what I did.
```
'use strict';

function appendToDisplay(value) {
    document.getElementById('display').value += value;
}

function clearDisplay() {
    document.getElementById('display').value = '';
}

function calculate() {
    let expression = document.getElementById('display').value;
    try {
        let result = eval(expression);
        document.getElementById('display').value = result;
    } catch (error) {
        document.getElementById('display').value = 'Error';
    }
}
```

### Demo
Once the steps have been completed, you should have a fully functional basic calculator web application. Linked below is a download to mine. 
