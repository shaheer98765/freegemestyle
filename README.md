# freegemestyle
freegemestyle_site/
├── index.html         ← Homepage
├── play.html          ← Pagina di gioco
├── style.css          ← Stile del sito
└── game/
    └── main.js        ← Script del gioco
    <!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>FreeGemeStyle</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="container">
    <h1>Benvenuto su FreeGemeStyle</h1>
    <p>Unisciti alla battaglia più stilosa del web!</p>
    <a href="play.html" class="play-button">Gioca Ora</a>
  </div>
</body>
</html>
<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gioca – FreeGemeStyle</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="container">
    <h1>Modalità di Gioco</h1>
    <canvas id="gameCanvas"></canvas>
    <script src="game/main.js"></script>
  </div>
</body>
</html>
body {
  margin: 0;
  font-family: 'Arial', sans-serif;
  background: #111;
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

.container {
  text-align: center;
}

.play-button {
  padding: 12px 24px;
  background: #00ff99;
  color: #000;
  font-weight: bold;
  border: none;
  border-radius: 6px;
  text-decoration: none;
  transition: 0.3s;
}

.play-button:hover {
  background: #00cc77;
}
const canvas = document.getElementById("gameCanvas");
const ctx = canvas.getContext("2d");

canvas.width = 600;
canvas.height = 400;

ctx.fillStyle = "#00ff99";
ctx.font = "30px Arial";
ctx.fillText("FreeGemeStyle - Work in Progress", 50, 200);
