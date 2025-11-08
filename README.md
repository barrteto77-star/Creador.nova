<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Creator Nova Local</title>
<style>
body {
  background: #000;
  color: #0ff;
  font-family: Arial, sans-serif;
  text-align: center;
  padding: 20px;
}
textarea {
  width: 90%;
  height: 100px;
  background: #111;
  color: #0ff;
  border: 1px solid #0ff;
  border-radius: 10px;
  padding: 10px;
}
button {
  background: #0ff;
  border: none;
  border-radius: 10px;
  padding: 10px 20px;
  font-size: 16px;
  margin: 10px;
}
video {
  width: 90%;
  margin-top: 20px;
  border-radius: 10px;
}
</style>
</head>
<body>
<h1>🎬 Creator Nova (Local)</h1>
<textarea id="texto" placeholder="Escribí tu guion..."></textarea><br>
<button onclick="hablar()">▶️ Leer Guion</button>
<button onclick="fondo()">🎥 Fondo</button>
<video id="vid" autoplay loop muted></video>

<script>
function hablar() {
  let texto = document.getElementById('texto').value;
  let voz = new SpeechSynthesisUtterance(texto);
  voz.lang = "es-AR";
  speechSynthesis.speak(voz);
}
function fondo() {
  document.getElementById('vid').src = "https://cdn.pixabay.com/video/2024/02/06/200367-906867379_large.mp4";
}
</script>
</body>
</html>
