---
layout: opencs
title: Pong Game Lesson
permalink: /pong-lessons/math
---


### Pong Game Lessons Java Script


### Roles

| Role            | Name                 |
|:---------------:|:--------------------:|
| 🧭 Scrum Master | **Devin Bir**        | 
| 📋 Assistant Scrum/Enginner | **Jonah Larsson**   |
| 🧪 Tester | **Malachi Mendoza**         |
| 🧪 Tester | **Aarush Bandi**         |
| 🏁 Tester/Finisher    | **Santiago Alverado**         | 
| 💻 Engineer/Finisher   | **Sri Rohit Varma Datla**         | 

### **Lessons On JavaScript**

### Lessons: 💻 Mathmatical Expresions

📌 What Is a Mathematical Expression in Code?
In programming, a mathematical expression is a line of code that calculates a value using numbers, variables, and operators.
Example:
let result = 5 + 3 * 2;


This calculates 5 + (3 × 2) and stores the result in result.

🧩 Key Operators in JavaScript

| Operator         | Symbol | Example     | Result | JS Code to Get Result       |
|------------------|--------|-------------|--------|-----------------------------|
| Addition         | `+`    | `2 + 3`     | `5`    | `console.log(2 + 3);`       |
| Subtraction      | `-`    | `5 - 2`     | `3`    | `console.log(5 - 2);`       |
| Multiplication   | `*`    | `4 * 3`     | `12`   | `console.log(4 * 3);`       |
| Division         | `/`    | `10 / 2`    | `5`    | `console.log(10 / 2);`      |
| Remainder        | `%` | `7 % 3`     | `1`    | `console.log(7 % 3);`       |
| Exponentiation   | `**`   | `2 ** 3`    | `8`    | `console.log(2 ** 3);`      |

You can also use inequality operators in conditional statements (>, <, ==, <=, =>)



🧠 Variables in Expressions
You can use variables to store values and build expressions:
let x = 10;
let y = 3;
let total = x + y * 2; // total = 10 + (3 × 2) = 16


🔍 Order of Operations
Just like in math, JavaScript follows PEMDAS:
- Parentheses
- Exponents
- M/D Multiplication/Division (left to right)
- A/S Addition/Subtraction (left to right)
let result = (4 + 2) * 3; // = 6 × 3 = 18

## Examples of Mathematical Expressions in pong
Pong is a game that requires a lot of mathematical operations, here are some of the few:
Ball physics:
```
if(ballY - ballRadius < 0 || ballY + ballRadius > canvas.height) ballSpeedY *= -1;

if(ballX - ballRadius < 20 + paddleWidth && ballY > leftY && ballY < leftY + paddleHeight){
	ballSpeedX *= -1; ballX = 20 + paddleWidth + ballRadius;
	sndPaddle.play();
}
if(ballX + ballRadius > canvas.width - 20 - paddleWidth && ballY > rightY && ballY < rightY + paddleHeight){
	ballSpeedX *= -1; ballX = canvas.width - 20 - paddleWidth - ballRadius;
	sndPaddle.play();
}
```


``` 
ballY - ballRadius < 0
```
This line checks if the ball is at the top of the screen (0 is the top because javascript follows a y-down system)

```
ballSpeedX *= -1; ballX = 20 + paddleWidth + ballRadius;
```
If a check if the ball is on the border of the screen is true, then the ball's direction will be reversed along with the ball being clamped to the side of the screen.


## 🧪 Practice Challenges

### Challenge 1:

<!-- 🎉 Answer Console with Confetti -->
<h3>Challenge 1: What is the out put when you type let 10 * 20 + 5?</h3>
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

<h3>Challenge 2: Calculate the Area of a Rectangle</h3>
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

### 🖥️ Interactive JavaScript Console

Type a command below and click **Run** to see the result.

<div id="console-container">
  <input type="text" id="console-input" placeholder="Type JavaScript here..." />
  <button onclick="runCommand()">Run</button>
  <pre id="console-output"></pre>
</div>

<style>
  #console-container {
    margin-top: 20px;
    padding: 10px;
    background: #1e1e1e;
    color: #eee;
    font-family: monospace;
    border-radius: 8px;
  }
  #console-input {
    width: 70%;
    padding: 8px;
    font-size: 1em;
    background: #333;
    color: #fff;
    border: none;
    border-radius: 4px;
  }
  button {
    padding: 8px 12px;
    margin-left: 10px;
    background: #007acc;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  #console-output {
    margin-top: 10px;
    white-space: pre-wrap;
  }
</style>

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

---

<!-- <h3>🎮 Mini Pong Game</h3>
<canvas id="pongCanvas" width="600" height="400"></canvas>

<div id="pong-console">
  <input type="text" id="pong-input" placeholder="Type a command (e.g. bg blue)" />
  <button onclick="runPongCommand()">Run</button>
  <button onclick="restartPong()">Restart</button>
  <p id="pong-feedback"></p>
</div>

<style>
  #pongCanvas {
    border: 2px solid #000;
    background: #eee;
    display: block;
    margin-bottom: 10px;
  }
  #pong-console {
    font-family: monospace;
    background: #222;
    color: #fff;
    padding: 10px;
    border-radius: 8px;
  }
  #pong-input {
    width: 60%;
    padding: 8px;
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
</style>

<script>
  const canvas = document.getElementById("pongCanvas");
  const ctx = canvas.getContext("2d");
  const feedback = document.getElementById("pong-feedback");

  let ball, paddle1, paddle2, bgColor;
  let animationId;

  function initGame() {
    ball = { x: 300, y: 200, dx: 2, dy: 2, radius: 10, color: "red" };
    paddle1 = { x: 50, y: 180, width: 10, height: 80, color: "black" };
    paddle2 = { x: 540, y: 180, width: 10, height: 80, color: "black" };
    bgColor = "#eee";
  }

  function draw() {
    ctx.fillStyle = bgColor;
    ctx.fillRect(0, 0, canvas.width, canvas.height);

    ctx.fillStyle = paddle1.color;
    ctx.fillRect(paddle1.x, paddle1.y, paddle1.width, paddle1.height);

    ctx.fillStyle = paddle2.color;
    ctx.fillRect(paddle2.x, paddle2.y, paddle2.width, paddle2.height);

    ctx.beginPath();
    ctx.arc(ball.x, ball.y, ball.radius, 0, Math.PI * 2);
    ctx.fillStyle = ball.color;
    ctx.fill();
    ctx.closePath();

    ball.x += ball.dx;
    ball.y += ball.dy;

    if (ball.x + ball.radius > canvas.width || ball.x - ball.radius < 0) ball.dx *= -1;
    if (ball.y + ball.radius > canvas.height || ball.y - ball.radius < 0) ball.dy *= -1;

    animationId = requestAnimationFrame(draw);
  }

  function runPongCommand() {
    const input = document.getElementById("pong-input").value.trim().toLowerCase();
    const parts = input.split(" ");
    const cmd = parts[0];
    const val = parts.slice(1).join(" ");

    if (cmd === "bg") {
      bgColor = val;
      feedback.textContent = `✅ Background changed to ${val}`;
    } else if (cmd === "ball") {
      ball.color = val;
      feedback.textContent = `✅ Ball color changed to ${val}`;
    } else if (cmd === "paddle1") {
      paddle1.color = val;
      feedback.textContent = `✅ Paddle 1 color changed to ${val}`;
    } else if (cmd === "paddle2") {
      paddle2.color = val;
      feedback.textContent = `✅ Paddle 2 color changed to ${val}`;
    } else if (cmd === "speed") {
      const speed = parseFloat(val);
      if (!isNaN(speed)) {
        ball.dx = speed;
        ball.dy = speed;
        feedback.textContent = `✅ Ball speed set to ${speed}`;
      } else {
        feedback.textContent = `❌ Invalid speed`;
      }
    } else if (cmd === "size") {
      const size = parseInt(val);
      if (!isNaN(size)) {
        paddle1.height = size;
        paddle2.height = size;
        feedback.textContent = `✅ Paddle height set to ${size}`;
      } else {
        feedback.textContent = `❌ Invalid size`;
      }
    } else {
      feedback.textContent = `❌ Unknown command`;
    }
  }

  function restartPong() {
    cancelAnimationFrame(animationId);
    initGame();
    draw();
    feedback.textContent = "🔁 Game restarted!";
  }

  initGame();
  draw();
</script> -->