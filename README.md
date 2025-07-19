# freegemestyle
<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>FreeGemeStyle</title>
  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background: #111;
      color: #fff;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      flex-direction: column;
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
      transition: background 0.3s;
      margin-top: 20px;
      display: inline-block;
      cursor: pointer;
    }
    .play-button:hover {
      background: #00cc77;
    }
    #gameCanvas {
      background: #222;
      border: 2px solid #00ff99;
      border-radius: 8px;
      margin-top: 30px;
      display: none; /* nascosto di default */
    }
  </style>
</head>
<body>

  <h1>Benvenuto su FreeGemeStyle</h1>
  <p>Unisciti alla battaglia più stilosa del web!</p>
  <button class="play-button" id="playBtn">Gioca Ora</button>

  <canvas id="gameCanvas" width="600" height="400"></canvas>

  <script>
    const playBtn = document.getElementById('playBtn');
    const canvas = document.getElementById('gameCanvas');
    const ctx = canvas.getContext('2d');

    playBtn.addEventListener('click', () => {
      // Nascondi il bottone e i testi
      playBtn.style.display = 'none';
      document.querySelector('h1').style.display = 'none';
      document.querySelector('p').style.display = 'none';

      // Mostra il canvas
      canvas.style.display = 'block';

      // Disegna testo nel canvas
      ctx.fillStyle = "#00ff99";
      ctx.font = "30px Arial";
      ctx.textAlign = "center";
      ctx.fillText("FreeGemeStyle - Lavori in corso", canvas.width / 2, canvas.height / 2);
    });
  </script>

</body>
</html>
