## HOLA CARACOLA


<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adivina el número</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            background: #202b46;
            color: white;
            text-align: center;
            padding: 50px 20px;
        }

        .juego {
            background: #344563;
            padding: 30px;
            border-radius: 15px;
            max-width: 400px;
            margin: auto;
        }

        input {
            padding: 12px;
            width: 100px;
            border-radius: 8px;
            border: none;
            font-size: 18px;
            text-align: center;
        }

        button {
            padding: 12px 20px;
            background: #00c896;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: bold;
            margin: 10px;
        }

        button:hover {
            background: #00a879;
        }

        #mensaje {
            font-size: 18px;
            margin-top: 20px;
        }
    </style>
</head>

<body>

    <div class="juego">
        <h1>🎮 Adivina el número</h1>

        <p>Estoy pensando en un número del 1 al 100.</p>

        <input type="number" id="numero" min="1" max="100">

        <br>

        <button onclick="comprobar()">Comprobar</button>
        <button onclick="reiniciar()">Reiniciar</button>

        <p id="mensaje">¡Empieza a jugar!</p>
        <p id="intentos">Intentos: 0</p>
    </div>

    <script>
        let secreto;
        let contador = 0;
        let terminado = false;

        function nuevaPartida() {
            secreto = Math.floor(Math.random() * 100) + 1;
            contador = 0;
            terminado = false;

            document.getElementById("mensaje").textContent =
                "¡Empieza a jugar!";

            document.getElementById("intentos").textContent =
                "Intentos: 0";

            document.getElementById("numero").value = "";
        }

        function comprobar() {
            if (terminado) return;

            let numero = Number(
                document.getElementById("numero").value
            );

            if (numero < 1 || numero > 100 ||
                !Number.isInteger(numero)) {
                document.getElementById("mensaje").textContent =
                    "Introduce un número válido del 1 al 100.";
                return;
            }

            contador++;

            if (numero === secreto) {
                document.getElementById("mensaje").textContent =
                    "🎉 ¡Correcto! Has ganado.";
                terminado = true;
            } else if (numero < secreto) {
                document.getElementById("mensaje").textContent =
                    "⬆️ El número secreto es más alto.";
            } else {
                document.getElementById("mensaje").textContent =
                    "⬇️ El número secreto es más bajo.";
            }

            document.getElementById("intentos").textContent =
                "Intentos: " + contador;
        }

        function reiniciar() {
            nuevaPartida();
        }

        nuevaPartida();
    </script>

</body>
</html>



[![Ver tutorial de HTML](https://img.youtube.com/vi/LgJCAt2332M/maxresdefault.jpg)](https://www.youtube.com/watch?v=LgJCAt2332M)

**Título:** HTML para principiantes

**Plataforma:** YouTube

**Enlace:** https://www.youtube.com/watch?v=LgJCAt2332M



<img src="./assets/baner.png" alt="Érika Cepeda — Copilot, AI & community" width="100%" />

<h1 align="center">Hi, I’m Érika 👋💖</h1>

<p align="center">
 Me gusta el rosa, las mariposas, el brilli-brilli y tener muchas plantas con flores, casi tanto como la IA Generativa, así que es normal que me chifle Copilot ✨🦋🌸
 <br/><br/>
 I’m a non-technical tech storyteller: I connect AI, business & people to make Copilot and agents practical, approachable and human ✨
 <br/><br/>
 Me encanta explicar tecnología para que todo el mundo pueda entenderla, probarla y utilizarla con criterio. Y cada vez me gusta más enseñar también lo que hay detrás de la magia 💖
</p>
