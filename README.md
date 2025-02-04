<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Quieres ser mi San Valentín? ❤️</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: pink;
            flex-direction: column;
            font-family: Arial, sans-serif;
            text-align: center;
        }
        h1 {
            font-size: 2.5em;
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            font-size: 1.5em;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        .yes {
            background-color: red;
            color: white;
        }
        .no {
            background-color: white;
            color: red;
            position: absolute;
        }
        .image-container {
            margin-top: 20px;
            display: none;
        }
        img {
            max-width: 300px;
            border-radius: 15px;
        }
    </style>
</head>
<body>
    <h1>¿Quieres ser mi San Valentín, Scarlett? ❤️</h1>
    <div class="buttons">
        <button class="yes" onclick="accepted()">Sí 💖</button>
        <button class="no" onmouseover="moveButton()">No 😢</button>
    </div>
    <div class="image-container" id="imageContainer">
        <h2>¡Sabía que dirías que sí! ❤️😍</h2>
        <img src="https://lh3.googleusercontent.com/d/1jl2MHU9BYZAj4dO1w87ILPQT1F-mKuwy" alt="Nuestra foto juntos">
    </div>
    <script>
        function moveButton() {
            let button = document.querySelector('.no');
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            button.style.left = `${x}px`;
            button.style.top = `${y}px`;
        }
        function accepted() {
            document.querySelector('.buttons').style.display = 'none';
            document.getElementById('imageContainer').style.display = 'block';
        }
    </script>
</body>
</html>
