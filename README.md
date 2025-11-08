<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- META TAG SEO: Descripción para Google -->
    <meta name="description" content="No te pierdas 'ACRO EN TELAS', el gran evento de Acrobacia en Tela con alumnas de Sara. Compra tus entradas, conoce a la profesora y descubre sus clases.">
    
    <title>Acrobacia en Tela en Zavalla, Santa Fe, Argentina</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Configuración de Tailwind para un tema oscuro moderno y fuente Inter -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'dark-bg': '#121212', // Gris oscuro suave para el fondo
                        'dark-surface': '#1E1E1E', // Superficie para secciones
                        'dark-card': '#2D2D2D', // Fondo de tarjetas
                        'accent': '#A855F7', // Violeta Vibrante (Moderno y Artístico)
                        'secondary-accent': '#34D399', // Verde Esmeralda/Menta (Contraste amigable)
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap');
        html { scroll-behavior: smooth; }
        
        /* Estilo para el fondo del Hero Section con efecto de gradiente/sombra */
        .hero-bg {
            /* Fondo ajustado para un mosaico con transparencia media (0.7 opacidad) */
            background-image: linear-gradient(rgba(18, 18, 18, 0.7), #121212), url('https://placehold.co/1920x1080/1F1F1F/A855F7?text=MOSAICO+DE+POSES+EN+TELA');
            background-size: cover;
            background-position: center;
        }
        /* Clase para un efecto de luz suave, usando el nuevo acento violeta */
        .glow-text {
            text-shadow: 0 0 10px rgba(168, 85, 247, 0.6), 0 0 20px rgba(168, 85, 247, 0.3);
        }
        /* Estilo para las tarjetas con transiciones más suaves */
        .performer-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .performer-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(168, 85, 247, 0.2);
        }
    </style>
</head>
<body class="bg-dark-bg text-gray-100 font-sans">

    <!-- Navbar Fija y Responsiva -->
    <header class="sticky top-0 z-50 bg-dark-bg/95 backdrop-blur-sm shadow-xl border-b border-gray-700">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <a href="#hero" class="text-xl font-bold text-secondary-accent hover:text-white transition duration-200">Acrobacia en Tela</a>
            
            <!-- Menú Desktop -->
            <div class="hidden md:flex space-x-6">
                <a href="#hero" class="text-gray-300 hover:text-accent transition duration-200 font-medium">Evento</a>
                <a href="#classes" class="text-gray-300 hover:text-accent transition duration-200 font-medium">Clases</a>
                <a href="#podcasts" class="text-gray-300 hover:text-accent transition duration-200 font-medium">Podcasts</a>
                <a href="#research" class="text-gray-300 hover:text-accent transition duration-200 font-medium">Investigación</a>
                <a href="https://chat.whatsapp.com/HTfPk2DtG4NDHu85YmwHWq?mode=wwt" target="_blank" class="px-4 py-2 bg-accent rounded-lg text-white hover:bg-violet-600 transition duration-200 font-semibold shadow-md">Tickets</a>
            </div>

            <!-- Botón de Menú Móvil (Placeholder simple) -->
            <button id="mobile-menu-button" class="md:hidden text-gray-300 focus:outline-none">
                <!-- Icono de Menú (Hamburguer) -->
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-menu"><line x1="4" x2="20" y1="12" y2="12"/><line x1="4" x2="20" y1="6" y2="6"/><line x1="4" x2="20" y1="18" y2="18"/></svg>
            </button>
        </nav>
        
        <!-- Menú Móvil Desplegable (Hidden by default) -->
        <div id="mobile-menu" class="hidden md:hidden bg-dark-bg/95">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3 flex flex-col items-center">
                <a href="#hero" class="block py-2 text-gray-300 hover:bg-dark-surface hover:text-accent rounded-md w-full text-center">Evento</a>
                <a href="#classes" class="block py-2 text-gray-300 hover:bg-dark-surface hover:text-accent rounded-md w-full text-center">Clases</a>
                <a href="#podcasts" class="block py-2 text-gray-300 hover:bg-dark-surface hover:text-accent rounded-md w-full text-center">Podcasts</a>
                <a href="#research" class="block py-2 text-gray-300 hover:bg-dark-surface hover:text-accent rounded-md w-full text-center">Investigación</a>
                <a href="https://chat.whatsapp.com/HTfPk2DtG4NDHu85YmwHWq?mode=wwt" target="_blank" class="block py-2 text-white bg-accent hover:bg-violet-600 rounded-lg mt-2 w-1/2 text-center font-semibold">Tickets</a>
            </div>
        </div>
    </header>
    
    <!-- Script para el menú móvil -->
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const button = document.getElementById('mobile-menu-button');
            const menu = document.getElementById('mobile-menu');
            
            button.addEventListener('click', () => {
                menu.classList.toggle('hidden');
            });

            // Ocultar menú al hacer clic en un enlace (para navegación smooth)
            menu.querySelectorAll('a').forEach(link => {
                link.addEventListener('click', () => {
                    menu.classList.add('hidden');
                });
            });
        });
    </script>


    <!-- Sección Hero (Evento) -->
    <section id="hero" class="hero-bg h-[calc(100vh-64px)] flex items-center justify-center text-center p-4 pt-16">
        <div class="max-w-4xl mx-auto backdrop-blur-md bg-dark-bg/70 p-8 md:p-12 rounded-xl shadow-2xl border border-accent/20">
            <h1 class="text-5xl md:text-7xl font-extrabold mb-4 uppercase leading-tight text-accent glow-text">
                ACRO EN TELAS
            </h1>
            <h2 class="text-2xl md:text-4xl font-light mb-8 text-gray-200">
                Acrobacia en Tela: La Fusión de Fuerza, Danza y Emoción
            </h2>
            <!-- Nueva línea sobre la temática sonora -->
            <p class="text-lg md:text-xl font-medium mb-10 text-secondary-accent border-b border-accent/50 pb-3 inline-block">
                🎵 Temática Sonora: Un Tributo Épico a **COLDPLAY** 🎵
            </p>
            <!-- Horarios detallados en Hero -->
            <div class="mb-10 font-medium text-secondary-accent text-xl md:text-2xl space-y-2">
                <p>🗓️ Sábado 15 de Noviembre | 🕖 Funciones: 19:00 hs y 20:30 hs</p>
                <p>🗓️ Domingo 16 de Noviembre | 🕗 Función: 20:00 hs</p>
            </div>
            
            <!-- CTA Principal - ENLACE A WHATSAPP -->
            <a href="https://chat.whatsapp.com/HTfPk2DtG4NDHu85YmwHWq?mode=wwt" target="_blank" class="inline-block px-12 py-4 text-xl font-bold uppercase rounded-full bg-accent text-white hover:bg-violet-600 transition duration-300 shadow-xl hover:shadow-2xl hover:scale-[1.02]">
                🎟️ Comprar Entradas Ahora
            </a>
            <p class="mt-4 text-sm text-gray-400">¡Cupos limitados! Asegura tu lugar en las alturas.</p>
        </div>
    </section>

    <!-- Sección Sobre el Show -->
    <section id="about" class="py-20 px-4 bg-dark-bg">
        <div class="max-w-6xl mx-auto">
            <h2 class="text-4xl md:text-5xl font-bold text-center mb-16 text-secondary-accent">Una Noche Inolvidable</h2>
            <div class="grid md:grid-cols-3 gap-8">
                <div class="p-8 bg-dark-card rounded-2xl performer-card border border-gray-700 hover:border-accent/50">
                    <div class="text-4xl text-accent mb-4 text-center">✨</div>
                    <h3 class="text-2xl font-semibold mb-3 text-white">Arte Suspendido</h3>
                    <p class="text-gray-300">Descubre la belleza de la danza aérea, donde cada movimiento se convierte en una pincelada de elegancia y riesgo en el espacio vertical.</p>
                </div>
                <div class="p-8 bg-dark-card rounded-2xl performer-card border border-gray-700 hover:border-accent/50">
                    <div class="text-4xl text-accent mb-4 text-center">🎶</div>
                    <h3 class="text-2xl font-semibold mb-3 text-white">Música de Coldplay</h3>
                    <p class="text-gray-300">Las acrobacias cobran vida al ritmo épico y emotivo de Coldplay, fusionando la disciplina con una banda sonora universalmente inspiradora.</p>
                </div>
                <div class="p-8 bg-dark-card rounded-2xl performer-card border border-gray-700 hover:border-accent/50">
                    <div class="text-4xl text-accent mb-4 text-center">🎭</div>
                    <h3 class="text-2xl font-semibold mb-3 text-white">Narrativa Emocional</h3>
                    <p class="text-gray-300">Cada acto cuenta una historia. Una banda sonora épica y una iluminación dramática te sumergirán en un viaje de emociones intensas.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Disciplinas Invitadas (Ahora solo Columpio Aéreo) -->
    <section id="performers" class="py-20 px-4 bg-dark-surface">
        <div class="max-w-6xl mx-auto">
            <h2 class="text-4xl md:text-5xl font-bold text-center mb-16 text-accent">Acto Invitado Especial: Columpio Aéreo</h2>
            <p class="text-xl text-center text-gray-300 mb-10 max-w-3xl mx-auto">El evento de Acrobacia en Tela será complementado por un acto vibrante y dinámico: la sorprendente disciplina del Columpio Aéreo.</p>
            
            <div class="flex justify-center">

                <!-- Disciplina Única: Columpio Aéreo -->
                <div class="w-full sm:w-1/2 lg:w-1/3 bg-dark-card rounded-xl overflow-hidden performer-card shadow-lg hover:shadow-xl">
                    <img src="https://placehold.co/600x400/1F2937/FFFFFF?text=COLUMPIO+AEREO+DESTACADO" alt="Acróbata realizando un acto dinámico en Columpio Aéreo (Swing)" class="w-full h-72 object-cover transition duration-300 hover:opacity-90">
                    <div class="p-6 text-center">
                        <h4 class="text-2xl font-bold text-secondary-accent">Columpio Aéreo (Swing)</h4>
                        <p class="text-lg text-gray-400 mt-2">Movimientos pendulares de alta energía que desafían los límites del espacio y la velocidad.</p>
                    </div>
                </div>

            </div>
        </div>
    </section>
    
    <!-- Sección Historia Personal de la Profe (ELIMINADA) -->
    <!-- Se eliminó la sección #history. El contenido de Clases es la siguiente sección. -->

    <!-- NUEVA SECCIÓN: Información sobre las Clases -->
    <section id="classes" class="py-20 px-4 bg-dark-bg">
        <div class="max-w-6xl mx-auto">
            <h2 class="text-4xl md:text-5xl font-bold text-center mb-16 text-accent">Encuentra Tu Clase Ideal</h2>

            <p class="text-xl text-center text-gray-300 mb-10 max-w-4xl mx-auto">Nuestras clases son **multinivel** y están diseñadas con un enfoque **personalizado**. Agrupamos a los estudiantes por edad para asegurar un ambiente y ritmo de aprendizaje óptimo para cada persona.</p>

            <div class="space-y-10">
                
                <!-- Clase 1: Niños (Antes Principiantes) -->
                <div class="md:flex md:items-center bg-dark-card rounded-2xl p-8 shadow-xl hover:bg-dark-card/80 transition duration-300 border border-gray-700 hover:border-secondary-accent">
                    <div class="md:w-1/3 mb-4 md:mb-0">
                        <h3 class="text-3xl font-bold text-secondary-accent">Grupo Infantil</h3>
                        <p class="text-lg text-gray-400">Edades: 6 a 12 años</p>
                    </div>
                    <div class="md:w-2/3 md:pl-8">
                        <p class="text-gray-300 mb-3">Foco en el juego, la coordinación motora y la seguridad. Introducción a la tela aérea con nudos y ascensos básicos, adaptando la dificultad a la capacidad de cada niño.</p>
                        <ul class="text-sm text-accent list-disc list-inside space-y-1">
                            <li>Clases Multinivel, enfoque en la progresión personal.</li>
                            <li>Frecuencia: 1 vez por semana</li>
                            <li>Duración: 60 minutos</li>
                        </ul>
                    </div>
                </div>

                <!-- Clase 2: Adolescentes (Antes Intermedio) -->
                <div class="md:flex md:items-center bg-dark-card rounded-2xl p-8 shadow-xl hover:bg-dark-card/80 transition duration-300 border border-gray-700 hover:border-secondary-accent">
                    <div class="md:w-1/3 mb-4 md:mb-0">
                        <h3 class="text-3xl font-bold text-secondary-accent">Grupo Adolescentes</h3>
                        <p class="text-lg text-gray-400">Edades: 13 a 17 años</p>
                    </div>
                    <div class="md:w-2/3 md:pl-8">
                        <p class="text-gray-300 mb-3">Trabajo en la resistencia, la expresión artística y secuencias coreográficas. El aprendizaje es multinivel, respetando el ritmo y los objetivos individuales de cada alumno.</p>
                        <ul class="text-sm text-accent list-disc list-inside space-y-1">
                            <li>Clases Multinivel, enfoque en la progresión personal.</li>
                            <li>Frecuencia: 1 vez por semana</li>
                            <li>Duración: 60 minutos</li>
                        </ul>
                    </div>
                </div>

                <!-- Clase 3: Adultos (Antes Avanzado) -->
                <div class="md:flex md:items-center bg-dark-card rounded-2xl p-8 shadow-xl hover:bg-dark-card/80 transition duration-300 border border-gray-700 hover:border-secondary-accent">
                    <div class="md:w-1/3 mb-4 md:mb-0">
                        <h3 class="text-3xl font-bold text-secondary-accent">Grupo Adultos</h3>
                        <p class="text-lg text-gray-400">Edades: 18 años en adelante</p>
                    </div>
                    <div class="md:w-2/3 md:pl-8">
                        <p class="text-gray-300 mb-3">Desde iniciación hasta performance. Clases totalmente personalizadas para trabajar fuerza, flexibilidad, técnica y creación de actos, sin importar tu nivel actual.</p>
                        <ul class="text-sm text-accent list-disc list-inside space-y-1">
                            <li>Clases Multinivel, enfoque en la progresión personal.</li>
                            <li>Frecuencia: 1 vez por semana</li>
                            <li>Duración: 60 minutos</li>
                        </ul>
                    </div>
                </div>
            </div>

            <div class="text-center mt-12">
                <!-- CTA Agenda Clase - ENLACE A WHATSAPP -->
                <a href="https://chat.whatsapp.com/HTfPk2DtG4NDHu85YmwHWq?mode=wwt" target="_blank" class="inline-block px-10 py-3 text-xl font-bold uppercase rounded-full bg-accent text-white hover:bg-violet-600 transition duration-300 shadow-xl">
                    ¡Agenda una Clase de Prueba!
                </a>
            </div>
        </div>
    </section>

    <!-- NUEVA SECCIÓN: Podcasts/Entrevistas -->
    <section id="podcasts" class="py-20 px-4 bg-dark-surface">
        <div class="max-w-4xl mx-auto">
            <h2 class="text-4xl md:text-5xl font-bold text-center mb-16 text-secondary-accent">Podcast Destacado: Sara en el Aire</h2>
            
            <p class="text-xl text-center text-gray-300 mb-10 max-w-3xl mx-auto">Escucha la entrevista completa donde Sara cuenta su trayectoria, los desafíos de la disciplina aérea y la importancia de la mente en el entrenamiento.</p>

            <div class="flex justify-center">
                
                <!-- Podcast Único Destacado con Enlace a Spotify -->
                <div class="w-full max-w-lg items-start p-6 bg-dark-card rounded-xl shadow-2xl border border-secondary-accent/50 transition duration-300 hover:scale-[1.01]">
                    <div class="flex items-center mb-4">
                        <div class="flex-shrink-0 text-5xl text-accent mr-4">🎧</div>
                        <div>
                            <h4 class="text-2xl font-semibold text-white">Episodio Especial: "La Mentalidad del Artista Aéreo"</h4>
                            <p class="text-gray-400 text-sm">Disponible en Spotify (Podcast: *Mundo Vertical*)</p>
                        </div>
                    </div>
                    
                    <p class="text-gray-300 mb-4 border-l-4 border-accent pl-3 italic">"Explora cómo la fuerza mental es tan crucial como la fuerza física para dominar las telas y vencer el miedo a la altura."</p>

                    <a href="https://open.spotify.com/episode/1WskSANRsbGAlJcAHNhEli?si=vk-5_6PFSmSOXbX8yvPlyQ" target="_blank" class="flex items-center justify-center mt-4 px-6 py-3 bg-secondary-accent rounded-lg text-dark-bg font-bold hover:bg-emerald-500 transition duration-300 shadow-md">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="currentColor" class="mr-2"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm4 14l-6-4V8l6 4z"/></svg>
                        Escuchar en Spotify
                    </a>
                </div>
            </div>
        </div>
    </section>
    
    <!-- NUEVA SECCIÓN: Investigación y Fundamentos -->
    <section id="research" class="py-20 px-4 bg-dark-bg">
        <div class="max-w-4xl mx-auto">
            <h2 class="text-4xl md:text-5xl font-bold text-center mb-16 text-accent">Fundamentos: Etnografía de la Acrobacia Aérea</h2>

            <div class="flex justify-center">
                
                <!-- Artículo 1: Etnografía (Furiasse) - AHORA CENTRADO Y DETALLADO -->
                <div class="w-full max-w-3xl p-8 bg-dark-card rounded-2xl shadow-xl border border-secondary-accent/50">
                    <h3 class="text-3xl font-bold mb-3 text-secondary-accent">Cuerpos en el Aire: El Trabajo Etnográfico de Furiasse (2020)</h3>
                    <p class="text-gray-300 mb-4">La investigación de Furiasse examina las **Trayectorias Formativas de la Acrobacia en Tela**, trascendiendo la técnica para enfocarse en la **dimensión social y cultural** de la disciplina. Sus hallazgos definen la acrobacia en tela no solo como un espectáculo, sino como una **práctica comunitaria**.</p>
                    
                    <ul class="text-lg text-gray-300 list-disc list-inside ml-6 space-y-2 mb-6">
                        <li>Construcción del Cuerpo Aéreo: El estudio describe cómo la identidad acrobática se construye a través de la formación de un "cuerpo aéreo" disciplinado y sensorial.</li>
                        <li>Comunidad y Cuidado: La investigación resalta la importancia de la ética del cuidado (prevención de lesiones y apoyo mutuo) como pilar fundamental en los rituales de entrenamiento y la vida colectiva del estudio.</li>
                        <li>Espacio de Resignificación: El espacio del estudio, y el aire mismo, funcionan como un lugar donde las y los acróbatas experimentan la superación personal y transforman su relación con la gravedad.</li>
                    </ul>
                    
                    <a href="https://www.circonteudo.com/cuerpos-en-el-aire-trayectorias-formativas-de-la-acrobacia-en-tela-una-aproximacion-etnografica-pdf/" target="_blank" class="text-accent hover:text-violet-600 font-medium underline text-sm block mt-4">
                        Leer el Estudio Completo de Furiasse (PDF)
                    </a>
                    <p class="mt-4 text-sm text-gray-400 italic">La filosofía de nuestra enseñanza se basa en estos principios etnográficos de seguridad, arte y comunidad.</p>
                </div>

            </div>
        </div>
    </section>

    <!-- Sección Tickets y Ubicación (Existing Content) -->
    <section id="tickets" class="py-20 px-4 bg-dark-surface">
        <div class="max-w-6xl mx-auto grid lg:grid-cols-2 gap-12">
            
            <!-- Bloque de Entradas -->
            <div class="p-8 bg-dark-card rounded-2xl shadow-2xl border-2 border-accent/50">
                <h2 class="text-4xl font-bold mb-6 text-accent">Consigue Tus Entradas</h2>
                <p class="text-lg text-gray-300 mb-8">¡Entrada única! Elige tu función y asegura tu asiento para este espectáculo aéreo.</p>

                <!-- Tarjeta de Precio Único -->
                <div class="p-6 bg-dark-surface rounded-xl border border-secondary-accent/50 mb-8 text-center">
                    <h4 class="text-2xl font-semibold text-secondary-accent mb-1">Precio Único</h4>
                    <p class="text-5xl font-extrabold text-white">$7000 ARS</p>
                    <p class="text-sm text-gray-400 mt-1">Válido para una función a elegir.</p>
                </div>

                <!-- Eliminadas las opciones VIP/General para dejar solo el precio único -->
                
                <!-- CTA Comprar Ahora - ENLACE A WHATSAPP -->
                <a href="https://chat.whatsapp.com/HTfPk2DtG4NDHu85YmwHWq?mode=wwt" target="_blank" class="mt-4 block w-full text-center px-8 py-4 text-xl font-extrabold uppercase rounded-lg bg-secondary-accent text-dark-bg hover:bg-emerald-500 transition duration-300 shadow-xl">
                    ¡Comprar Ahora! (Vía WhatsApp)
                </a>
                <p class="mt-4 text-sm text-center text-gray-400">Serás redirigido a WhatsApp para confirmar tu compra y elegir tu función.</p>

            </div>

            <!-- Bloque de Ubicación y Horarios -->
            <div class="p-8 bg-dark-card rounded-2xl shadow-2xl border-2 border-secondary-accent/50">
                <h2 class="text-4xl font-bold mb-6 text-secondary-accent">Fechas y Horarios</h2>
                
                <!-- Detalle de Funciones -->
                <div class="space-y-6 mb-8">
                    <div class="p-4 bg-dark-surface rounded-lg">
                        <h4 class="text-2xl font-bold text-accent mb-2">🗓️ Sábado 15 de Noviembre</h4>
                        <ul class="text-lg text-gray-300 list-disc list-inside ml-4 space-y-1">
                            <li><span class="font-semibold text-secondary-accent">19:00 hs:</span> Primera Función</li>
                            <li><span class="font-semibold text-secondary-accent">20:30 hs:</span> Segunda Función</li>
                        </ul>
                    </div>
                    <div class="p-4 bg-dark-surface rounded-lg">
                        <h4 class="text-2xl font-bold text-accent mb-2">🗓️ Domingo 16 de Noviembre</h4>
                        <ul class="text-lg text-gray-300 list-disc list-inside ml-4">
                            <li><span class="font-semibold text-secondary-accent">20:00 hs:</span> Función Única</li>
                        </ul>
                    </div>
                </div>

                <h2 class="text-4xl font-bold mb-6 text-secondary-accent">Ubicación</h2>
                <ul class="space-y-4 text-lg text-gray-300">
                    <li class="flex items-center">
                        <span class="text-accent mr-3">📍</span>
                        Lugar: Stylo Pilates, Zavalla, Santa Fe
                    </li>
                </ul>
                
                <div class="mt-8 rounded-lg overflow-hidden border-2 border-gray-700">
                    <!-- Mapa de Google Maps embebido (reemplazando el placeholder) -->
                    <a href="https://maps.app.goo.gl/qkBZuu9j25kx67oL8" target="_blank" class="block">
                        <img src="https://placehold.co/600x300/2D2D2D/34D399?text=VER+UBICACION+EN+MAPS" alt="Mapa de la ubicación de Stylo Pilates en Zavalla, Santa Fe" class="w-full h-48 object-cover">
                    </a>
                </div>
                <!-- El texto ahora dirige al mapa, ya no a WhatsApp para esta consulta -->
                <a href="https://maps.app.goo.gl/qkBZuu9j25kx67oL8" target="_blank" class="mt-4 text-sm text-gray-400 hover:text-white transition duration-200 block text-center underline">Haz clic aquí para ver la ubicación exacta en Google Maps.</a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black py-8 px-4 border-t border-accent/30">
        <div class="max-w-6xl mx-auto text-center">
            <p class="text-gray-400 mb-4">&copy; 2025. Todos los derechos reservados.</p>
            <div class="flex justify-center space-x-6 text-xl">
                <!-- Se recomienda que los enlaces a redes sociales sí sean los enlaces directos a las redes, no a WhatsApp -->
                <a href="#" class="text-gray-400 hover:text-accent transition duration-200" aria-label="Instagram">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="20" height="20" x="2" y="2" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" x2="17.51" y1="6.5" y2="6.5"/></svg>
                </a>
                <a href="#" class="text-gray-400 hover:text-accent transition duration-200" aria-label="Facebook">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="currentColor"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg>
                </a>
                <a href="#" class="text-gray-400 hover:text-accent transition duration-200" aria-label="TikTok">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-tiktok"><path d="M21 8a2 2 0 0 0-2-2h-5v11.75c0 1.25-.72 2.25-2 2.25s-2-.72-2-2.25V6h-2v11.75c0 1.25-.72 2.25-2 2.25s-2-.72-2-2.25V6H3a2 2 0 0 0-2 2v10a2 2 0 0 0 2 2h2v2h2v-2h2v2h2v-2h2v2h2a2 2 0 0 0 2-2z"/></svg>
                </a>
            </div>
        </div>
    </footer>

</body>
</html>
