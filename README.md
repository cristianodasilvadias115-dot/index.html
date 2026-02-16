<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Concessionária Popular</title>

<style>
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
}

header {
    background-color: #111;
    color: white;
    padding: 20px;
    text-align: center;
}

h1 {
    margin: 0;
}

.container {
    padding: 40px 20px;
    max-width: 1200px;
    margin: auto;
}

.carros {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
}

.card {
    background: white;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    transition: 0.3s;
}

.card:hover {
    transform: scale(1.03);
}

.card img {
    width: 100%;
    height: 180px;
    object-fit: cover;
}

.card-content {
    padding: 15px;
}

.card h3 {
    margin: 10px 0;
}

.preco {
    color: green;
    font-weight: bold;
    font-size: 18px;
}

.botao {
    display: block;
    text-align: center;
    background: #25D366;
    color: white;
    padding: 10px;
    border-radius: 5px;
    text-decoration: none;
    margin-top: 10px;
}

footer {
    text-align: center;
    padding: 20px;
    background: #111;
    color: white;
    margin-top: 40px;
}
</style>

</head>
<body>

<header>
    <h1>Concessionária Popular</h1>
    <p>Realize o sonho do seu carro próprio</p>
</header>

<div class="container">
    <h2>Carros Disponíveis</h2>

    <div class="carros">

        <div class="card">
            <img src="https://images.unsplash.com/photo-1549924231-f129b911e442" alt="Carro 1">
            <div class="card-content">
                <h3>Fiat Uno 2015</h3>
                <p class="preco">R$ 29.900</p>
                <a class="botao" href="#">Tenho Interesse</a>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1550355291-bbee04a92027" alt="Carro 2">
            <div class="card-content">
                <h3>Gol 2018</h3>
                <p class="preco">R$ 39.900</p>
                <a class="botao" href="#">Tenho Interesse</a>
            </div>
        </div>

        <div class="card">
            <img src="https://images.unsplash.com/photo-1542362567-b07e54358753" alt="Carro 3">
            <div class="card-content">
                <h3>Onix 2020</h3>
                <p class="preco">R$ 52.900</p>
                <a class="botao" href="#">Tenho Interesse</a>
            </div>
        </div>

    </div>
</div>

<footer>
    © 2026 Concessionária Popular - Luiz Eduardo Magalhães
</footer>

</body>
</html>
