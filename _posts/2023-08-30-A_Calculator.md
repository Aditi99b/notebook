---
toc: true
comments: false
layout: post
title: Calculator
description: A calculator  
type: hacks
courses: { compsci: {week: 2} }
---


<!--
Hack 0: Right justify result
Hack 1: Test conditions on small, big, and decimal numbers, report on findings. Fix issues.
Hack 2: Add the common math operation that is missing from calculator
Hack 3: Implement 1 number operation (ie SQRT)
-->


<!--
HTML implementation of the calculator.
-->


{% include nav_home.html %}


<!--
    Style and Action are aligned with HRML class definitions
    style.css contains majority of style definition (number, operation, clear, and equals)
    - The div calculator-container sets 4 elements to a row
    Background is credited to Vanta JS and is implemented at bottom of this page
-->
<style>
  .calculator-output {
    /* the calculator output will be on the top of the calculator, taking up the grid of 4 blocks 
    */

    /* there are 4 columns 
    */
    grid-column: span 4;
    grid-row: span 1;
 
 /* black border, centered */
    border-radius: 10px;
    padding: 0.25em;
    font-size: 20px;
    border: 5px solid black;
 
    display: flex;
    align-items: center;
  }
</style>


<!-- a container for calculator history -->
<div class="calculation-history">
    <h2>Calculation History</h2>
    <ul id="history-list"></ul>
</div>

<!-- container for animation -->
<div id="animation">
  <div class="calculator-container">
      <!--result-->
      <div class="calculator-output" id="output">0</div>
      <!--row 1-->
      <div class="calculator-number">1</div>
      <div class="calculator-number">2</div>
      <div class="calculator-number">3</div>
      <div class="calculator-operation">+</div>
      <!--row 2-->
      <div class="calculator-number">4</div>
      <div class="calculator-number">5</div>
      <div class="calculator-number">6</div>
      <div class="calculator-operation">-</div>
      <!--row 3-->
      <div class="calculator-number">7</div>
      <div class="calculator-number">8</div>
      <div class="calculator-number">9</div>
      <div class="calculator-operation">*</div>
      <!--row 4-->
      <div class="calculator-clear">A/C</div>
      <div class="calculator-number">0</div>
      <div class="calculator-number">.</div>
      <div class="calculator-equals">=</div>
</div>


  </div>
</div>


<!-- JavaScript (JS) implementation of the calculator. -->
<script>
  // Initialize an array to store calculation history
var calculationHistory = [];
// initialize important variables to manage calculations
var firstNumber = null;
var operator = null;
var nextReady = true;
// Initialize an array to store calculation history

// build objects containing key elements
const output = document.getElementById("output");
const numbers = document.querySelectorAll(".calculator-number");
const operations = document.querySelectorAll(".calculator-operation");
const clear = document.querySelectorAll(".calculator-clear");
const equals = document.querySelectorAll(".calculator-equals");


// Number buttons listener
numbers.forEach(button => {
  button.addEventListener("click", function() {
    number(button.textContent);
  });
});


// Number action
function number (value) { // function to input numbers into the calculator: makes sure its not a decimal 
    if (value != ".") {
        if (nextReady == true) { // nextReady tells the computer that the user will input a new number 
            output.innerHTML = value;
            if (value != "0") { // if statement to ensure that there are no multiple leading zeroes
                nextReady = false; // the user is not inputting a new number 
            }
        } else {
            output.innerHTML = output.innerHTML + value; 
        }
    } else { // special case for adding a decimal; can't have two decimals
        if (output.innerHTML.indexOf(".") == -1) {
            output.innerHTML = output.innerHTML + value;
            nextReady = false;
        }
    }
}


// Operation buttons listener
operations.forEach(button => {
  button.addEventListener("click", function() { //when the user clicks on a button, the specific function will be used 
    operation(button.textContent); //when the user clicks on a button, it starts the operation function 
  });
});


// Operator action
function operation (choice) { // function to input operations into the calculator
    if (firstNumber == null) { // once the operation is chosen, the displayed number is stored into the variable firstNumber
        firstNumber = parseInt(output.innerHTML);
        nextReady = true;
        operator = choice;
        return; // exits function
    }
    // occurs if there is already a number stored in the calculator
    firstNumber = calculate(firstNumber, parseFloat(output.innerHTML));
    operator = choice;
    output.innerHTML = firstNumber.toString();
    nextReady = true;
}


// Calculator
function calculate (first, second) { // function to calculate the result of the equation, first is number 1, second is number 2
    let result = 0; //stores the result of the calculation 
    switch (operator) {
        case "+":
            result = first + second; //addition 
            break;
        case "-":
            result = first - second; //subtraction 
            break;
        case "*":
            result = first * second; //mulitplication 
            break;
        case "/":
            result = first / second; //divison 
            break;
        default:
            break;
    }
    return result; //returns the calculated result 
}


// Equals button listener
equals.forEach(button => {
  button.addEventListener("click", function() {
    equal();
  });
});


// Equal action
function equal () {
    if (firstNumber !== null) {
        const result = calculate(firstNumber, parseFloat(output.innerHTML));
        calculationHistory.push(`${firstNumber} ${operator} ${output.innerHTML} = ${result}`);
        updateHistory(); // Call this function to update the history list
        firstNumber = result;
        output.innerHTML = result.toString();
        nextReady = true;
    }
}


// Clear button listener
clear.forEach(button => {
  button.addEventListener("click", function() {
    clearCalc();
  });
});


// A/C action
function clearCalc () { // clears calculator
    firstNumber = null;
    output.innerHTML = "0";
    nextReady = true;
}


function updateHistory() {
    const historyList = document.getElementById("history-list");
    historyList.innerHTML = "";
    calculationHistory.forEach((calculation, index) => {
        const listItem = document.createElement("li");
        listItem.textContent = `Calculation ${index + 1}: ${calculation}`;
        historyList.appendChild(listItem);
    });
}


</script>


<!--
Vanta animations just for fun, load JS onto the page
-->
<script src="/teacher/assets/js/three.r119.min.js"></script>
<script src="/teacher/assets/js/vanta.halo.min.js"></script>
<script src="/teacher/assets/js/vanta.birds.min.js"></script>
<script src="/teacher/assets/js/vanta.net.min.js"></script>
<script src="/teacher/assets/js/vanta.rings.min.js"></script>


<script>
// setup vanta scripts as functions
var vantaInstances = {
  halo: VANTA.HALO,
  birds: VANTA.BIRDS,
  net: VANTA.NET,
  rings: VANTA.RINGS
};


// obtain a random vanta function
var vantaInstance = vantaInstances[Object.keys(vantaInstances)[Math.floor(Math.random() * Object.keys(vantaInstances).length)]];


// run the animation
vantaInstance({
  el: "#animation",
  mouseControls: true,
  touchControls: true,
  gyroControls: false
});
</script>