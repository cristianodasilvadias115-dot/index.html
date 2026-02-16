# BR LEM Veículos - Concessionária de Carros

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BR LEM Veículos | Carros Usados em Luís Eduardo Magalhães - BA</title>
    
    <meta name="description" content="BR LEM Veículos - Concessionária de carros usados e seminovos em Luís Eduardo Magalhães, BA. Qualidade, procedência e atendimento personalizado.">
    <meta name="keywords" content="carros usados Luís Eduardo Magalhães, seminovos BA, concessionária LEM, carros procedência">
    <meta name="author" content="BR LEM Veículos">
    <meta name="robots" content="index, follow">
    <meta property="og:title" content="BR LEM Veículos - Carros Usados e Seminovos">
    <meta property="og:description" content="Encontre seu carro dos sonhos na BR LEM Veículos">
    <meta property="og:url" content="https://brlemveiculos.com.br">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary-color: #25d366;
            --dark-color: #111;
            --light-color: #f5f5f5;
            --text-color: #333;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        /* HEADER */
        header {
            background: var(--dark-color);
            padding: 15px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        header h1 {
            color: #fff;
            font-size: 24px;
            font-weight: bold;
        }
        
        header a {
            background: var(--primary-color);
            color: #fff;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background 0.3s;
        }
        
        header a:hover {
            background: #1ea853;
        }
        
        nav {
            display: flex;
            gap: 20px;
            margin-left: auto;
            margin-right: 20px;
        }
        
        nav a {
            color: #fff;
            text-decoration: none;
            padding: 5px 10px;
            transition: color 0.3s;
        }
        
        nav a:hover {
            color: var(--primary-color);
        }
        
        /* SLIDER */
        .slider {
            position: relative;
            overflow: hidden;
            height: 80vh;
            background: #000;
        }
        
        .slides {
            display: flex;
            transition: transform 0.8s ease-in-out;
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
        
        .slide::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0,0,0,0.3);
        }
        
        .slide-content {
            position: absolute;
            bottom: 20%;
            left: 10%;
            color: #fff;
            max-width: 500px;
            z-index: 2;
        }
        
        .slide-content h2 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        .slide-content p {
            margin-bottom: 20px;
            font-size: 1.2rem;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
        }
        
        .btn-slide {
            background: var(--primary-color);
            padding: 12px 25px;
            color: #fff;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            display: inline-block;
            transition: background 0.3s;
        }
        
        .btn-slide:hover {
            background: #1ea853;
        }
        
        .prev, .next {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            font-size: 2rem;
            background: rgba(0,0,0,0.6);
            color: #fff;
            border: none;
            padding: 10px 15px;
            cursor: pointer;
            z-index: 10;
            transition: background 0.3s;
        }
        
        .prev:hover, .next:hover {
            background: rgba(0,0,0,0.9);
        }
        
        .prev { left: 20px; }
        .next { right: 20px; }
        
        .slide-indicators {
            position: absolute;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 10px;
            z-index: 10;
        }
        
        .dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: rgba(255,255,255,0.5);
            cursor: pointer;
            transition: background 0.3s;
        }
        
        .dot.active {
            background: var(--primary-color);
        }
        
        /* SEÇÕES */
        section {
            padding: 60px 20px;
        }
        
        section h2 {
            margin-bottom: 30px;
            font-size: 2rem;
            text-align: center;
            color: var(--text-color);
        }
        
        section p {
            text-align: center;
            color: #666;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* GALERIA DE CARROS */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .car-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .car-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
        }
        
        .car-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }
        
        .car-info {
            padding: 20px;
        }
        
        .car-info h3 {
            color: var(--text-color);
            margin-bottom: 10px;
        }
        
        .car-price {
            color: var(--primary-color);
            font-size: 1.3rem;
            font-weight: bold;
            margin-bottom: 10px;
        }
        
        .car-details {
            color: #666;
            font-size: 0.9rem;
            margin-bottom: 15px;
        }
        
        .btn-contact {
            background: var(--primary-color);
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            width: 100%;
            transition: background 0.3s;
        }
        
        .btn-contact:hover {
            background: #1ea853;
        }
        
        /* FORMULÁRIO DE CONTATO */
        .contact-section {
            background: var(--light-color);
        }
        
        .contact-form {
            max-width: 600px;
            margin: 40px auto;
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            color: var(--text-color);
            font-weight: bold;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: inherit;
            font-size: 1rem;
        }
        
        .form-group textarea {
            resize: vertical;
            min-height: 100px;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 0 0 5px rgba(37, 211, 102, 0.3);
        }
        
        .btn-submit {
            background: var(--primary-color);
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 5px;
            font-weight: bold;
            font-size: 1rem;
            cursor: pointer;
            width: 100%;
            transition: background 0.3s;
        }
        
        .btn-submit:hover {
            background: #1ea853;
        }
        
        /* REDES SOCIAIS */
        .redes {
            margin-top: 30px;
        }
        
        .redes a {
            margin: 10px;
            display: inline-block;
            text-decoration: none;
            color: #fff;
            background: #333;
            padding: 12px 20px;
            border-radius: 5px;
            font-weight: bold;
            transition: background 0.3s;
        }
        
        .redes a:hover {
            background: var(--primary-color);
        }
        
        /* FOOTER */
        footer {
            background: var(--dark-color);
            color: #fff;
            text-align: center;
            padding: 30px 20px;
            margin-top: 60px;
        }
        
        footer p {
            color: #fff;
            margin-bottom: 10px;
        }
        
        /* RESPONSIVO */
        @media (max-width: 768px) {
            header {
                flex-direction: column;
                gap: 15px;
            }
            
            nav {
                display: none;
            }
            
            .slide-content h2 {
                font-size: 1.5rem;
            }
            
            .slide-content p {
                font-size: 1rem;
            }
            
            .slide-content {
                left: 5%;
                max-width: 80%;
            }
            
            section h2 {
                font-size: 1.5rem;
            }
            
            .gallery {
                grid-template-columns: 1fr;
            }
        }
        
        /* ANIMAÇÕES */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .fade-in {
            animation: fadeIn 0.6s ease-in;
        }
    </style>
</head>

<body>

<!-- HEADER -->
<header>
    <h1>🚗 BR LEM Veículos</h1>
    <nav>
        <a href="#galeria">Galeria</a>
        <a href="#contato">Contato</a>
        <a href="#sobre">Sobre</a>
    </nav>
    <a href="https://wa.me/5577999892355" target="_blank">📱 WhatsApp</a>
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
    <div class="slide-indicators">
        <span class="dot active" onclick="currentSlide(0)"></span>
        <span class="dot" onclick="currentSlide(1)"></span>
        <span class="dot" onclick="currentSlide(2)"></span>
    </div>
</section>

<!-- GALERIA DE CARROS -->
<section id="galeria" class="container">
    <h2>🚙 Nossos Veículos</h2>
    <p>Confira nossa seleção de carros disponíveis</p>
    
    <div class="gallery">
        <div class="car-card fade-in">
            <div class="car-image">🚗</div>
            <div class="car-info">
                <h3>Chevrolet Onix</h3>
                <div class="car-price">R$ 45.000</div>
                <div class="car-details">
                    <p>2020 • 45.000 km • Manual</p>
                </div>
                <a href="https://wa.me/5577999892355?text=Tenho%20interesse%20no%20Chevrolet%20Onix" class="btn-contact" target="_blank">Consultar</a>
            </div>
        </div>

        <div class="car-card fade-in">
            <div class="car-image">🏎️</div>
            <div class="car-info">
                <h3>Ford Fiesta</h3>
                <div class="car-price">R$ 38.000</div>
                <div class="car-details">
                    <p>2019 • 52.000 km • Automático</p>
                </div>
                <a href="https://wa.me/5577999892355?text=Tenho%20interesse%20no%20Ford%20Fiesta" class="btn-contact" target="_blank">Consultar</a>
            </div>
        </div>

        <div class="car-card fade-in">
            <div class="car-image">🚕</div>
            <div class="car-info">
                <h3>Fiat Uno</h3>
                <div class="car-price">R$ 32.000</div>
                <div class="car-details">
                    <p>2018 • 60.000 km • Manual</p>
                </div>
                <a href="https://wa.me/5577999892355?text=Tenho%20interesse%20no%20Fiat%20Uno" class="btn-contact" target="_blank">Consultar</a>
            </div>
        </div>

        <div class="car-card fade-in">
            <div class="car-image">🚙</div>
            <div class="car-info">
                <h3>Hyundai HB20</h3>
                <div class="car-price">R$ 42.000</div>
                <div class="car-details">
                    <p>2021 • 38.000 km • Automático</p>
                </div>
                <a href="https://wa.me/5577999892355?text=Tenho%20interesse%20no%20Hyundai%20HB20" class="btn-contact" target="_blank">Consultar</a>
            </div>
        </div>

        <div class="car-card fade-in">
            <div class="car-image">🏎️</div>
            <div class="car-info">
                <h3>Renault Sandero</h3>
                <div class="car-price">R$ 48.000</div>
                <div class="car-details">
                    <p>2021 • 35.000 km • Automático</p>
                </div>
                <a href="https://wa.me/5577999892355?text=Tenho%20interesse%20no%20Renault%20Sandero" class="btn-contact" target="_blank">Consultar</a>
            </div>
        </div>

        <div class="car-card fade-in">
            <div class="car-image">🚗</div>
            <div class="car-info">
                <h3>Volkswagen Gol</h3>
                <div class="car-price">R$ 35.000</div>
                <div class="car-details">
                    <p>2019 • 55.000 km • Manual</p>
                </div>
                <a href="https://wa.me/5577999892355?text=Tenho%20interesse%20no%20Volkswagen%20Gol" class="btn-contact" target="_blank">Consultar</a>
            </div>
        </div>
    </div>
</section>

<!-- SOBRE -->
<section id="sobre">
    <div class="container">
        <h2>ℹ️ Sobre a BR LEM Veículos</h2>
        <p>Localizada em Luís Eduardo Magalhães – BA, somos uma concessionária especializada em carros usados e seminovos com qualidade garantida.</p>
        <br>
        <p><strong>✓ Procedência Comprovada</strong></p>
        <p><strong>✓ Atendimento Personalizado</strong></p>
        <p><strong>✓ Financiamento Facilitado</strong></p>
        <p><strong>✓ Garantia de Qualidade</strong></p>
        <br>
        <p>📍 <strong>Avenida Salvador – Luís Eduardo Magalhães, BA</strong></p>
        <p>📱 <strong>Telefone: (77) 99989-2355</strong></p>
        
        <div class="redes">
            <a href="https://www.instagram.com/brlemveiculos_/" target="_blank">📷 Instagram</a>
            <a href="https://www.facebook.com/lemveiculos/" target="_blank">👍 Facebook</a>
            <a href="https://maps.app.goo.gl/nYveeV8CJq64Aoyr7" target="_blank">📍 Google Maps</a>
        </div>
    </div>
</section>

<!-- CONTATO -->
<section id="contato" class="contact-section">
    <div class="container">
        <h2>📧 Fale Conosco</h2>
        <p>Envie sua mensagem que retornaremos o mais breve possível</p>
        
        <form class="contact-form" onsubmit="handleSubmit(event)">
            <div class="form-group">
                <label for="nome">Nome Completo *</label>
                <input type="text" id="nome" name="nome" required>
            </div>
            
            <div class="form-group">
                <label for="email">Email *</label>
                <input type="email" id="email" name="email" required>
            </div>
            
            <div class="form-group">
                <label for="telefone">Telefone *</label>
                <input type="tel" id="telefone" name="telefone" placeholder="(77) 99999-9999" required>
            </div>
            
            <div class="form-group">
                <label for="mensagem">Mensagem *</label>
                <textarea id="mensagem" name="mensagem" required></textarea>
            </div>
            
            <button type="submit" class="btn-submit">Enviar Mensagem</button>
        </form>
    </div>
</section>

<!-- FOOTER -->
<footer>
    <p>&copy; 2026 BR LEM Veículos – Todos os direitos reservados</p>
    <p>Desenvolvido com ❤️ para sua satisfação</p>
</footer>

<script>
    // SLIDER
    let currentIndex = 0;
    const slides = document.querySelector('.slides');
    const dots = document.querySelectorAll('.dot');
    const totalSlides = document.querySelectorAll('.slide').length;

    function updateSlide() {
        slides.style.transform = `translateX(-${currentIndex * 100}%)`;
        dots.forEach((dot, index) => {
            dot.classList.toggle('active', index === currentIndex);
        });
    }

    function currentSlide(index) {
        currentIndex = index;
        updateSlide();
    }

    document.querySelector('.next').addEventListener('click', () => {
        currentIndex = (currentIndex + 1) % totalSlides;
        updateSlide();
    });

    document.querySelector('.prev').addEventListener('click', () => {
        currentIndex = (currentIndex - 1 + totalSlides) % totalSlides;
        updateSlide();
    });

    // Auto-slide a cada 5 segundos
    setInterval(() => {
        currentIndex = (currentIndex + 1) % totalSlides;
        updateSlide();
    }, 5000);

    // FORMULÁRIO
    function handleSubmit(event) {
        event.preventDefault();
        
        const nome = document.getElementById('nome').value;
        const email = document.getElementById('email').value;
        const telefone = document.getElementById('telefone').value;
        const mensagem = document.getElementById('mensagem').value;
        
        // Criar mensagem WhatsApp
        const whatsappMessage = `Olá! Meu nome é ${nome}. Email: ${email}. Telefone: ${telefone}. Mensagem: ${mensagem}`;
        const whatsappLink = `https://wa.me/5577999892355?text=${encodeURIComponent(whatsappMessage)}`;
        
        // Abrir WhatsApp
        window.open(whatsappLink, '_blank');
        
        // Limpar formulário
        document.querySelector('.contact-form').reset();
        
        alert('Sua mensagem será enviada via WhatsApp!');
    }
</script>

</body>
</html>
```