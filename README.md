<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para ti ❤️</title>
    <!-- Tailwind CSS para un diseño limpio y moderno -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght=400;600;700&display=swap');
        body {
            font-family: 'Quicksand', sans-serif;
            background-image: linear-gradient(135deg, #fdf2f2 0%, #ffe4e6 100%);
        }
        .reveal-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 1s ease-out;
        }
        .reveal-content.active {
            max-height: 1200px; /* Suficiente para mostrar todo */
        }
    </style>
</head>
<body class="min-h-screen flex flex-col items-center justify-center p-6 text-center">

    <div id="main-card" class="max-w-md bg-white/90 p-8 rounded-3xl shadow-xl border border-pink-100 transform transition-all duration-300">
        <!-- Icono/Emoji -->
        <div id="initial-icon" class="text-6xl mb-6 animate-bounce">
            🍕❤️
        </div>

        <!-- Mensaje Principal -->
        <h1 class="text-3xl font-bold text-gray-800 mb-4">
            ¿Ya no estemos peleados?
        </h1>
        
        <p class="text-lg text-gray-600 mb-6 leading-relaxed">
            Te amo muchísimo. Te invito a comer pizza, ¿andas? Di que sí.
        </p>

        <!-- Botón de Respuesta -->
        <button id="main-button" onclick="aceptar()" class="bg-red-400 hover:bg-red-500 text-white font-bold py-3 px-8 rounded-full shadow-lg transition duration-200 transform active:scale-95">
            ¡Sii, vamos! 🍕
        </button>
        
        <!-- Contenido Oculto -->
        <div id="reveal-area" class="reveal-content mt-8 space-y-6">
            
            <div class="border-t border-gray-200 pt-6">
                <!-- Imagen Real subida -->
                <div class="rounded-2xl overflow-hidden shadow-inner border border-gray-100">
                    <img src="https://i.ibb.co/qMmXJ5mD/42a275c4-6212-408b-8fcd-243e8fe7d931.jpg" alt="Nosotros" class="w-full h-auto">
                </div>
                
                <!-- Mensaje Final -->
                <p id="final-message" class="text-3xl font-extrabold mt-6 text-red-500 animate-pulse">
                    ¡Que te amo demasiado!
                </p>
                
                <p class="text-xl font-semibold text-green-600 mt-4">
                    ¡Sabía que dirías que sí! Prepárate, yo invito. 🏃‍♂️💨
                </p>
            </div>
        </div>
    </div>

    <script>
        function aceptar() {
            // Desactivar el botón y el icono
            document.getElementById('main-button').style.display = 'none';
            document.getElementById('initial-icon').classList.remove('animate-bounce');
            document.getElementById('initial-icon').innerText = '🎉';

            // Revelar el contenido
            const revealArea = document.getElementById('reveal-area');
            revealArea.classList.add('active');

            // Scroll suave hacia abajo para ver todo
            setTimeout(() => {
                revealArea.scrollIntoView({ behavior: 'smooth' });
            }, 300);
        }
    </script>
</body>
</html>
