<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Click the Box Game</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Click the Box!</h1>
    <p>Score: <span id="score">0</span></p>
    <div id="gameArea">
        <div id="box"></div>
    </div>
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    text-align: center;
}

#gameArea {
    position: relative;
    width: 300px;
    height: 300px;
    border: 2px solid black;
    margin: auto;
    background-color: lightgray;
}

#box {
    width: 50px;
    height: 50px;
    background-color: red;
    position: absolute;
    cursor: pointer;
}
let score = 0;
const box = document.getElementById("box");
const scoreDisplay = document.getElementById("score");
const gameArea = document.getElementById("gameArea");

function moveBox() {
    const maxX = gameArea.clientWidth - box.clientWidth;
    const maxY = gameArea.clientHeight - box.clientHeight;
    const randomX = Math.floor(Math.random() * maxX);
    const randomY = Math.floor(Math.random() * maxY);
    
    box.style.left = `${randomX}px`;
    box.style.top = `${randomY}px`;
}

box.addEventListener("click", () => {
    score++;
    scoreDisplay.textContent = score;
    moveBox();
});

// Verplaats het vakje elke seconde automatisch
setInterval(moveBox, 1000);

moveBox();
git init
git add .
git commit -m "Eerste versie van Click the Box Game"
git branch -M main
git remote add origin https://github.com/jouwgebruikersnaam/Click-The-Box-Game.git
git push -u origin main
