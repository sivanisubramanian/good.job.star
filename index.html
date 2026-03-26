<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Good Job!</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      width: 100%;
      height: 100vh;
      background: #ffffff;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }

    #app {
      width: 100%;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      overflow: hidden;
    }

    #star-screen, #congrats-screen {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      width: 100%;
      height: 100%;
      position: absolute;
      inset: 0;
    }

    #congrats-screen { display: none; }

    .star-wrap {
      cursor: pointer;
      transition: transform 0.15s ease;
      user-select: none;
    }
    .star-wrap:hover { transform: scale(1.08); }
    .star-wrap:active { transform: scale(0.95); }

    #good-job {
      font-family: sans-serif;
      font-size: 64px;
      font-weight: 500;
      color: #B8860B;
      letter-spacing: -1px;
      animation: popIn 0.4s cubic-bezier(0.34,1.56,0.64,1) both;
    }

    @keyframes popIn {
      from { transform: scale(0.4); opacity: 0; }
      to   { transform: scale(1);   opacity: 1; }
    }

    canvas#confetti-canvas {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
    }
  </style>
</head>
<body>
  <div id="app">
    <canvas id="confetti-canvas"></canvas>

    <div id="star-screen">
      <div class="star-wrap" id="star-btn">
        <svg width="220" height="220" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <polygon
            points="50,5 61,35 95,35 68,57 79,91 50,70 21,91 32,57 5,35 39,35"
            fill="#FFD700"
            stroke="#B8860B"
            stroke-width="1.5"
            stroke-linejoin="round"
          />
          <circle cx="40" cy="46" r="4" fill="#5a3e00"/>
          <circle cx="60" cy="46" r="4" fill="#5a3e00"/>
          <path d="M37 60 Q50 74 63 60" fill="none" stroke="#5a3e00" stroke-width="3" stroke-linecap="round"/>
          <ellipse cx="33" cy="62" rx="5" ry="3" fill="#FFB347" opacity="0.6"/>
          <ellipse cx="67" cy="62" rx="5" ry="3" fill="#FFB347" opacity="0.6"/>
        </svg>
      </div>
    </div>

    <div id="congrats-screen">
      <div id="good-job">Good Job!</div>
    </div>
  </div>

  <script>
    const starScreen = document.getElementById('star-screen');
    const congratsScreen = document.getElementById('congrats-screen');
    const starBtn = document.getElementById('star-btn');
    const canvas = document.getElementById('confetti-canvas');
    const ctx = canvas.getContext('2d');

    let particles = [];
    let animId = null;
    let returnTimer = null;

    function resizeCanvas() {
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
    }

    function randomBetween(a, b) { return a + Math.random() * (b - a); }

    const COLORS = ['#FFD700','#FF6B6B','#4ECDC4','#45B7D1','#96CEB4','#FFEAA7','#FF8E53','#A29BFE','#FD79A8','#55EFC4'];

    function spawnParticles() {
      particles = [];
      const w = canvas.width, h = canvas.height;
      for (let i = 0; i < 140; i++) {
        particles.push({
          x: randomBetween(w * 0.2, w * 0.8),
          y: randomBetween(-20, -5),
          vx: randomBetween(-3, 3),
          vy: randomBetween(2, 7),
          size: randomBetween(6, 14),
          color: COLORS[Math.floor(Math.random() * COLORS.length)],
          rotation: randomBetween(0, Math.PI * 2),
          rotSpeed: randomBetween(-0.15, 0.15),
          shape: Math.random() > 0.5 ? 'rect' : 'circle',
          gravity: randomBetween(0.08, 0.18),
          alpha: 1
        });
      }
    }

    function drawParticle(p) {
      ctx.save();
      ctx.globalAlpha = p.alpha;
      ctx.translate(p.x, p.y);
      ctx.rotate(p.rotation);
      ctx.fillStyle = p.color;
      if (p.shape === 'rect') {
        ctx.fillRect(-p.size / 2, -p.size / 4, p.size, p.size / 2);
      } else {
        ctx.beginPath();
        ctx.arc(0, 0, p.size / 2, 0, Math.PI * 2);
        ctx.fill();
      }
      ctx.restore();
    }

    function animate() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      particles.forEach(p => {
        p.x += p.vx;
        p.y += p.vy;
        p.vy += p.gravity;
        p.rotation += p.rotSpeed;
        if (p.y > canvas.height * 0.75) p.alpha -= 0.02;
        drawParticle(p);
      });
      particles = particles.filter(p => p.alpha > 0);
      if (particles.length > 0) {
        animId = requestAnimationFrame(animate);
      } else {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
      }
    }

    function showCongrats() {
      resizeCanvas();
      starScreen.style.display = 'none';
      congratsScreen.style.display = 'flex';

      spawnParticles();
      if (animId) cancelAnimationFrame(animId);
      animate();

      if (returnTimer) clearTimeout(returnTimer);
      returnTimer = setTimeout(() => {
        if (animId) { cancelAnimationFrame(animId); animId = null; }
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        congratsScreen.style.display = 'none';
        starScreen.style.display = 'flex';
      }, 5000);
    }

    starBtn.addEventListener('click', showCongrats);
    window.addEventListener('resize', resizeCanvas);
    resizeCanvas();
  </script>
</body>
</html>
