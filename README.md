### Basic Calculator Web App
A simple web-based calculator built using HTML, CSS and JavaScript.

## The Process
Below are code snippets to help you build your own online calculator.
## HTML (The Foundation):
<body>
    <div class="calculator">
        <input type="text" id="display" readonly>
        <div class="buttons">
            <button onclick=""clearDisplay"()">C</button>
            <button onclick=""appendToDisplay"*('7')">7</button>
            <button onclick=""appendToDisplay"('8')">8</button>
            <button onclick=""appendToDisplay"('9')">9</button>
            <button onclick=""appendToDisplay"('+')">+</button>
            <button onclick=""appendToDisplay"('4')">4</button>
            <button onclick=""appendToDisplay"('5')">5</button>
            <button onclick=""appendToDisplay"('6')">6</button>
            <button onclick=""appendToDisplay"('-')">-</button>
            <button onclick=""appendToDisplay"('1')">1</button>
            <button onclick=""appendToDisplay"('2')">2</button>
            <button onclick=""appendToDisplay"('3')">3</button>
            <button onclick=""appendToDisplay"('*')">*</button>
            <button onclick=""appendToDisplay"('0')">0</button>
            <button onclick=""appendToDisplay"('.')">.</button>
            <button onclick="calculate()">=</button>
            <button onclick="appendToDisplay('/')">/</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
* "appendToDisplay" meaning to add to an existing element. When a number value is selected it fills the empty space within
the calculator for you to prcoeed with the next portion of the equation/calculation. 

Note: Delete the "" surrounding 'appendToDisplay' within your own application for proper functionality.

## CSS (The Style):
.calculator {
    width: 250px;
    margin: 100px auto;
    border: 1px solid #ccc;
    border-radius: 5px;
    padding: 10px;
    background-color: #f9f9f9;
}

.buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);**
    grid-gap: 5px;
}

button {
    padding: 10px;
    font-size: 18px;
    border: none;
    background-color: #ddd;
    cursor: pointer;
}

button:hover {
    background-color: #ccc;
}

** Sets the way in which the buttons will be displayed on the calculator.

## JavaScript (The Functionality):
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

Linked is a download to my calculator. 
