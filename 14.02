<!DOCTYPE html>
<html lang="bg">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>❤️ За Теб ❤️</title>

<style>
body {
    margin: 0;
    overflow: hidden;
    background: linear-gradient(135deg, #ff9a9e, #fad0c4);
    font-family: 'Arial', sans-serif;
    text-align: center;
}

h1 {
    margin-top: 50px;
    color: white;
    font-size: 28px;
}

#heartBtn {
    font-size: 60px;
    border: none;
    background: none;
    cursor: pointer;
    animation: pulse 1.5s infinite;
}

@keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.2); }
    100% { transform: scale(1); }
}

.teddy {
    position: absolute;
    font-size: 60px;
}

.heart {
    position: absolute;
    font-size: 24px;
    animation: fall 3s linear forwards;
}

@keyframes fall {
    0% { transform: translateY(0); }
    100% { transform: translateY(80vh); opacity: 0; }
}

#message {
    position: absolute;
    bottom: 20%;
    width: 100%;
    font-size: 40px;
    font-weight: bold;
    color: red;
    opacity: 0;
    transition: opacity 2s;
}
</style>
</head>

<body>

<h1>Натисни сърцето ❤️</h1>
<button id="heartBtn">❤️</button>

<div id="message">Обичам те</div>

<audio id="music" loop>
  <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
</audio>

<script>
const btn = document.getElementById("heartBtn");
const music = document.getElementById("music");
const message = document.getElementById("message");

btn.addEventListener("click", () => {
    btn.style.display = "none";
    music.play();

    // Създаваме мечета
    const teddy1 = document.createElement("div");
    teddy1.innerHTML = "🧸";
    teddy1.classList.add("teddy");
    teddy1.style.left = "20%";
    teddy1.style.top = "40%";
    document.body.appendChild(teddy1);

    const teddy2 = document.createElement("div");
    teddy2.innerHTML = "🧸";
    teddy2.classList.add("teddy");
    teddy2.style.right = "20%";
    teddy2.style.top = "40%";
    document.body.appendChild(teddy2);

    // Замерване със сърца
    let count = 0;
    const interval = setInterval(() => {
        createHeart();
        count++;
        if (count > 25) {
            clearInterval(interval);
            setTimeout(() => {
                message.style.opacity = "1";
            }, 2000);
        }
    }, 200);
});

function createHeart() {
    const heart = document.createElement("div");
    heart.innerHTML = "❤️";
    heart.classList.add("heart");
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.top = "30vh";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 3000);
}
</script>

</body>
</html>
