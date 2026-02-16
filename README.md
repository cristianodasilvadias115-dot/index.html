# index.html
Concessionária BRL veículos
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BR LEM Veículos | Carros em Luís Eduardo Magalhães</title>

<meta name="description" content="BR LEM Veículos em Luís Eduardo Magalhães. Carros usados e seminovos com procedência e atendimento personalizado.">
<meta name="keywords" content="carros Luís Eduardo Magalhães, concessionária LEM, carros usados Bahia">
<meta name="author" content="BR LEM Veículos">

<style>

/* RESET */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

/* HEADER */
header {
  background: #111;
  padding: 15px 30px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

header h1 {
  color: #fff;
  font-size: 20px;
}

header a {
  background: #25d366;
  color: #fff;
  padding: 10px 15px;
  text-decoration: none;
  border-radius: 5px;
  font-weight: bold;
}

/* SLIDER */
.slider {
  position: relative;
  overflow: hidden;
  height: 80vh;
}

.slides {
  display: flex;
  transition: transform 0.6s ease-in-out;
}

.slide {
  min-width: 100%;
  position: relative;
}

.slide img {
  width: 100%;
  height: 80vh;
  object-fit: cover;
}

.slide-content {
  position: absolute;
  bottom: 20%;
  left: 10%;
  color: #fff;
  max-width: 500px;
}

.slide-content h2 {
  font-size: 2.5rem;
  margin-bottom: 10px;
}

.slide-content p {
  margin-bottom: 20px;
  font-size: 1.2rem;
}

.btn-slide {
  background: #25d366;
  padding: 12px 20px;
  color: #fff;
  text-decoration: none;
  border-radius: 5px;
  font-weight: bold;
}

/* BOTÕES */
.prev, .next {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  font-size: 2rem;
  background: rgba(0,0,0,0.5);
  color: #fff;
  border: none;
  padding: 10px;
  cursor: pointer;
}

.prev { left: 20px; }
.next { right: 20px; }

/* SOBRE */
section {
  padding: 60px 20px;
  text-align: center;
}

section h2 {
  margin-bottom: 20px;
  font-size: 28px;
}

.redes a {
  margin: 10px;
  display: inline-block;
  text-decoration: none;
  color: #111;
  font-weight: bold;
}

/* FOOTER */
footer {
  background: #111;
  color: #fff;
  text-align: center;
  padding: 20px;
}

/* RESPONSIVO */
@media (max-width: 768px) {
  .slide-content h2 {
    font-size: 1.5rem;
  }
  .slide-content p {
    font-size: 1rem;
  }
}

</style>
</head>

<body>

<header>
  <h1>BR LEM Veículos</h1>
  <a href="https://wa.me/5577999892355" target="_blank">WhatsApp</a>
</header>

<!-- SLIDER -->
<section class="slider">
  <div class="slides">

    <div class="slide">
      <img src="imagens/camaro.jpg" alt="Chevrolet Camaro">
      <div class="slide-content">
        <h2>A chave da sua próxima conquista começa aqui.</h2>
        <p>Carros selecionados • Procedência garantida • Atendimento personalizado</p>
        <a href="https://wa.me/5577999892355" class="btn-slide" target="_blank">Falar com Consultor</a>
      </div>
    </div>

    <div class="slide">
      <img src="imagens/carro2.jpg" alt="Carro disponível">
      <div class="slide-content">
        <h2>Estoque Atualizado</h2>
        <p>Seminovos revisados e prontos para você</p>
        <a href="https://wa.me/5577999892355" class="btn-slide" target="_blank">Consultar Agora</a>
      </div>
    </div>

    <div class="slide">
      <img src="imagens/carro3.jpg" alt="Carros em LEM">
      <div class="slide-content">
        <h2>Compra Segura e Transparente</h2>
        <p>Atendimento direto, sem complicação</p>
        <a href="https://maps.app.goo.gl/nYveeV8CJq64Aoyr7" class="btn-slide" target="_blank">Ver Localização</a>
      </div>
    </div>

  </div>

  <button class="prev">&#10094;</button>
  <button class="next">&#10095;</button>
</section>

<!-- SOBRE -->
<section>
  <h2>Sobre a BR LEM Veículos</h2>
  <p>Localizada em Luís Eduardo Magalhães – BA, oferecemos carros usados e seminovos com qualidade, procedência e atendimento personalizado.</p>
  <p>📍 Avenida Salvador – LEM/BA</p>

  <div class="redes">
    <a href="https://www.instagram.com/brlemveiculos_/" target="_blank">Instagram</a>
    <a href="https://www.facebook.com/lemveiculos/" target="_blank">Facebook</a>
    <a href="https://maps.app.goo.gl/nYveeV8CJq64Aoyr7" target="_blank">Google Maps</a>
  </div>
</section>

<footer>
  <p>© 2026 BR LEM Veículos – Todos os direitos reservados</p>
</footer>

<script>

let currentIndex = 0;
const slides = document.querySelector('.slides');
const totalSlides = document.querySelectorAll('.slide').length;

function updateSlide() {
  slides.style.transform = `translateX(-${currentIndex * 100}%)`;
}

document.querySelector('.next').addEventListener('click', () => {
  currentIndex = (currentIndex + 1) % totalSlides;
  updateSlide();
});

document.querySelector('.prev').addEventListener('click', () => {
  currentIndex = (currentIndex - 1 + totalSlides) % totalSlides;
  updateSlide();
});

setInterval(() => {
  currentIndex = (currentIndex + 1) % totalSlides;
  updateSlide();
}, 5000);

</script>

</body>
</html>
