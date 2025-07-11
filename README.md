<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Trái Tim Linh ❤️</title>
  <style>
    body {
      background: #111;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    canvas {
      background: #111;
    }
  </style>
</head>
<body>
  <canvas id="heartCanvas" width="600" height="600"></canvas>

  <script>
    const canvas = document.getElementById("heartCanvas");
    const ctx = canvas.getContext("2d");

    ctx.translate(300, 300);
    ctx.beginPath();
    for (let t = 0; t <= Math.PI * 2; t += 0.01) {
      let x = 16 * Math.pow(Math.sin(t), 3);
      let y = 13 * Math.cos(t) - 5 * Math.cos(2 * t)
              - 2 * Math.cos(3 * t) - Math.cos(4 * t);
      ctx.lineTo(x * 15, -y * 15);
    }
    ctx.closePath();
    ctx.fillStyle = "red";
    ctx.fill();

    ctx.fillStyle = "white";
    ctx.font = "bold 40px Arial";
    ctx.textAlign = "center";
    ctx.fillText("Linh", 0, 10);
  </script>
</body>
</html>
