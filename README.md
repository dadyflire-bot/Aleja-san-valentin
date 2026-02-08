# Aleja-san-valentin
Para aleja❤️
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Aleja 💖 Daniel</title>

<style>
* { box-sizing: border-box; }

body {
  margin: 0;
  font-family: 'Arial', sans-serif;
  background: radial-gradient(circle at top, #3b0a45, #0d0d0d);
  color: white;
  text-align: center;
  overflow-x: hidden;
}

/* Secciones */
section {
  min-height: 100vh;
  display: none;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 25px;
}
section.active { display: flex; }

/* Botones */
button {
  margin-top: 25px;
  padding: 15px 30px;
  font-size: 18px;
  border: none;
  border-radius: 40px;
  background: linear-gradient(45deg, #ff4d6d, #ff85a1);
  color: white;
  cursor: pointer;
  box-shadow: 0 0 20px rgba(255,77,109,0.6);
  transition: transform 0.2s;
}
button:hover {
  transform: scale(1.05);
}

/* Texto */
h1, h2, h3 {
  text-shadow: 0 0 15px rgba(255,182,193,0.6);
}
p {
  font-size: 18px;
  line-height: 1.6;
}

/* Corazones flotando */
.heart {
  position: fixed;
  bottom: -20px;
  color: rgba(255, 105, 180, 0.8);
  font-size: 20px;
  animation: floatUp 8s linear infinite;
  pointer-events: none;
}

@keyframes floatUp {
  0% {
    transform: translateY(0) scale(1);
    opacity: 0;
  }
  10% { opacity: 1; }
  100% {
    transform: translateY(-110vh) scale(1.5);
    opacity: 0;
  }
}

/* Brillito suave */
.glow {
  animation: glow 3s ease-in-out infinite alternate;
}

@keyframes glow {
  from { text-shadow: 0 0 10px #ffb6c1; }
  to   { text-shadow: 0 0 25px #ff4d6d; }
}
</style>
</head>

<body>

<!-- PÁGINA 1 -->
<section id="p1" class="active">
  <h1 class="glow">Aleja 💖</h1>
  <p>
    Desde que llegaste,<br>
    todo se siente más bonito ✨
  </p>
  <button onclick="go(2)">¿Quieres ser mi San Valentín? 💘</button>
</section>

<!-- PÁGINA 2 -->
<section id="p2">
  <p class="glow">Eres alguien muy especial para mí 💫</p>
  <button onclick="go(3)">Sí, te amo 💖</button>
</section>

<!-- PÁGINA 3 -->
<section id="p3">
  <h2 class="glow">Aleja… 💖</h2>
  <p>
    Gracias por decir sí,<br>
    por existir<br>
    y por hacer mi vida más bonita ✨
  </p>
  <h3>Te amo 💘</h3>
  <p>— Daniel<br>08•02•2026</p>

  <iframe width="300" height="170"
    src="https://www.youtube.com/embed/1DpH-icPpl0?autoplay=1"
    allow="autoplay">
  </iframe>
</section>

<!-- Script navegación -->
<script>
function go(n){
  document.querySelectorAll('section').forEach(s => s.classList.remove('active'));
  document.getElementById('p'+n).classList.add('active');
}

/* Crear corazones */
setInterval(() => {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "💗";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.fontSize = (15 + Math.random() * 20) + "px";
  document.body.appendChild(heart);
  setTimeout(() => heart.remove(), 8000);
}, 500);
</script>

</body>
</html>
