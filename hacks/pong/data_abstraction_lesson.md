---
layout: opencs
title: Pong Game Lesson
permalink: /pong-lessons/abstraction
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

---

### Lessons: 💻 Data Abstraction

📌 What is **Data Abstraction**?
Data abstraction is a concept in programming that focuses on hiding the full implementation of something with a simpler interface, making this thing reusable and easier to use.
Examples:
- Classes
- Abstract classes 
- Abstract methods
- Functions
- Much more


We will be explaining data abstraction using pong
### 🧩 Explanation of different types of data abstraction with pong
**Functions**
```
function declareWinner(winner){
  winnerMsg.textContent = `${winner} Wins!`;
  running = false;
}
``` 
Take, for example, this function. Inside the curly braces ("{}") there is the implementation of the function.
Put simply, this function prints out who won the game on screen. Then, it ends the game by setting the "running" boolean to false.
The part where data abstraction starts is actually function definition. Instead of having to write the code inside the function every time you want to end the game, a function is declared with a parameter called "winner".
Now, when you want to declare a winner you can simply write:
```
declareWinner(player1);
```
> Note: "player1" can be replaced with whoever you want to win.

This is an example of data abstraction due to the fact that the code inside of the function is hidden and instead interfaced with a simple function call.
