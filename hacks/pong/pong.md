---
layout: opencs
title: Pong Game
permalink: /pong/
---

Controls:
W/S to move and D to shoot (Left Player)
Arrow Up/Down to move and Arrow Left to shoot (Right Player)
Bullets freeze enemy paddles for 5 seconds

<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
.sidebar {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background-color: #111;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 60px;
}
.sidebar a {
  padding: 8px 8px 8px 32px;
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  display: block;
  transition: 0.3s;
}
.sidebar a:hover {
  color: #f1f1f1;
}
.sidebar .closebtn {
  position: absolute;
  top: 0;
  right: 25px;
  font-size: 36px;
  margin-left: 50px;
}
.openbtn {
  font-size: 20px;
  cursor: pointer;
  background-color: #111;
  color: white;
  padding: 10px 15px;
  border: none;
}
.openbtn:hover {
  background-color: #444;
}
#main {
  transition: margin-left .5s;
  padding: 16px;
}
/* On smaller screens, where height is less than 450px, change the style of the sidenav (less padding and a smaller font size) */
@media screen and (max-height: 450px) {
  .sidebar {padding-top: 15px;}
  .sidebar a {font-size: 18px;}
}
</style>
</head>
<body>

<div id="LessonSidebar" class="sidebar">
<div>
<br/>
<h2><b>CS Concept Lesson</b></h2>
<br/>
<h3> Easy Concept: Mathematical Expressions </h3>
<br/>
</div>
<br/>

<b>What Is a Mathematical Expression in Code?</b><br/>
In programming, a mathematical expression is a block of code used to return a mathematical value.
Example:
<br/>
let result = 5 + 3 * 2;
This calculates 5 + (3 × 2) and stores the answer in in the variable "result".
<br/><br/>

<b>Key Operators in JavaScript</b><br/>
<ul>
	<li>Addition: +</li>
	<li>Subtraction: -</li>
	<li>Multiplication: *</li>
	<li>Division: /</li>
	<li>Modulus: %</li>
	<li>Exponent: **</li>
</ul>
<br/>

<b>Variables in Expressions</b><br/>
You can use variables to store values and build expressions:<br/>
let x = 10;<br/>
let y = 3;<br/>
let total = x + y * 2; // total = 10 + (3 × 2) = 16<br/>
<br/>


<b>Order of Operations</b><br/>
Just like in math, JavaScript follows PEMDAS:<br/>
<ol>
	<li>Parentheses</li>
	<li>Exponents</li>
	<li>Multiplication/Division</li>
	<li>Addition/Subtraction</li>
</ol>
<br/>


<h4>Challenge Questions:</h4><br/>

<!-- 🎉 Answer Console with Confetti -->
<h3>🎯 Challenge: What is the out put when you type let 10 * 20 + 5?</h3>
<p>Type your answer below and hit "Check Answer"</p>

<div id="answer-console">
  <input type="text" id="user-answer" placeholder="Your answer..." />
  <button onclick="checkAnswer()">Check Answer</button>
  <p id="feedback"></p>
  <canvas id="confetti-canvas"></canvas>
</div>

<style>
  #answer-console {
    margin-top: 20px;
    padding: 10px;
    background: #222;
    color: #fff;
    font-family: monospace;
    border-radius: 8px;
    position: relative;
  }
  #user-answer {
    width: 60%;
    padding: 8px;
    font-size: 1em;
    background: #333;
    color: #fff;
    border: 1px solid #555;
    border-radius: 4px;
  }
  button {
    padding: 8px 12px;
    margin-left: 10px;
    background: #0f0;
    color: #000;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  #feedback {
    margin-top: 10px;
    font-weight: bold;
  }
  #confetti-canvas {
    position: absolute;
    top: 0;
    left: 0;
    pointer-events: none;
    width: 100%;
    height: 100%;
  }
</style>

<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
<script>
  function checkAnswer() {
    const input = document.getElementById("user-answer").value.trim();
    const feedback = document.getElementById("feedback");
    const correctAnswer = "205";

    if (input === correctAnswer) {
      feedback.textContent = "✅ Correct! You nailed it!";
      feedback.style.color = "#0f0";
      confetti({
        particleCount: 200,
        spread: 95,
        origin: { y: 0.6 }
      });
    } else {
      feedback.textContent = "❌ Try again!";
      feedback.style.color = "#f00";
    }
  }
</script>

<h3>🧪 Experiment: Calculate the Area of a Rectangle</h3>
<p>Type a JavaScript expression that calculates the area using <code>width</code> and <code>height</code>.</p>

<pre><code>let width = 5;
let height = 10;
</code></pre>

<div id="experiment-console">
  <input type="text" id="experiment-input" placeholder="Type your expression..." />
  <button onclick="runExperiment()">Run</button>
  <p id="experiment-feedback"></p>
  <canvas id="experiment-confetti"></canvas>
</div>

<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
<script>
  function runExperiment() {
    const input = document.getElementById("experiment-input").value.trim();
    const feedback = document.getElementById("experiment-feedback");

    try {
      let width = 5;
      let height = 10;
      let result = eval(input);

      if (result === width * height) {
        feedback.textContent = `✅ Correct! Area is ${result}.`;
        feedback.style.color = "#0f0";
        confetti({
          particleCount: 150,
          spread: 70,
          origin: { y: 0.6 }
        });
      } else {
        feedback.textContent = `❌ Hmm... That gives ${result}. Try again!`;
        feedback.style.color = "#f00";
      }
    } catch (err) {
      feedback.textContent = `⚠️ Error: ${err.message}`;
      feedback.style.color = "#ff0";
    }
  }
</script>

<style>
  #experiment-console {
    margin-top: 20px;
    padding: 10px;
    background: #222;
    color: #fff;
    font-family: monospace;
    border-radius: 8px;
    position: relative;
  }
  #experiment-input {
    width: 60%;
    padding: 8px;
    font-size: 1em;
    background: #333;
    color: #fff;
    border: 1px solid #555;
    border-radius: 4px;
  }
  button {
    padding: 8px 12px;
    margin-left: 10px;
    background: #0f0;
    color: #000;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  #experiment-feedback {
    margin-top: 10px;
    font-weight: bold;
  }
  #experiment-confetti {
    position: absolute;
    top: 0;
    left: 0;
    pointer-events: none;
    width: 100%;
    height: 100%;
  }
</style>

<br/><br/>

<h4>Interactive JavaScript Console</h4><br/>

Type a command below and click *Run* to see the result.<br/>

<div id="console-container">
<input type="text" id="console-input" placeholder="Type JavaScript here..." />
<button onclick="runCommand()">Run</button>
<pre id="console-output"></pre>
</div>

<button type="button" onclick="closeNav()" style="padding: 15px 30px; cursor:pointer;">
Close Lesson
</button>
</div>

<div id="main">
  <button class="openbtn" onclick="window.location.href='{{site.baseurl}}/pong-lessons/math';" style="margin-left: 100px">☰ Open Math Expressions Lesson</button>  
</div>

<div id="main">
  <button class="openbtn" onclick="window.location.href='{{site.baseurl}}/pong-lessons/abstraction';" style="margin-left: 100px">☰ Open Data Abstraction Lesson</button>  
</div>

<script>
var sidebarOpen = false;

function triggerNav() {
	if (!sidebarOpen)
	{
		document.getElementById("LessonSidebar").style.width = "700px";
		sidebarOpen = true;
	}
	else
	{
		document.getElementById("LessonSidebar").style.width = "0";
		sidebarOpen = false;
	}
}

function closeNav() {
  document.getElementById("LessonSidebar").style.width = "0";
}
</script>

<script>
  function runCommand() {
    const input = document.getElementById("console-input").value;
    const output = document.getElementById("console-output");
    try {
      const result = eval(input);
      output.textContent = `> ${input}\n${result}`;
    } catch (err) {
      output.textContent = `> ${input}\nError: ${err.message}`;
    }
  }
</script>


<script src="{{site.baseurl}}/hacks/pong/pong.js"></script>
   
</body>
</html> 