<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- META TAG SEO: Descripción para Google -->
    <meta name="description" content="No te pierdas 'ACRO EN TELAS', el gran evento de Acrobacia en Tela con alumnas de Sara. Compra tus entradas, conoce a la profesora y descubre sus clases.">
    
    <title>Evento de Acrobacia en TEL: Arte en el Aire</title>
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
            background-image: linear-gradient(rgba(18, 18, 18, 0.8), #121212), url('https://placehold.co/1920x1080/121212/A855F7?text=ARTE+AEREO+MODERNO');
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
                <a href="#history" class="text-gray-300 hover:text-accent transition duration-200 font-medium">Profe</a>
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
                <a href="#history" class="block py-2 text-gray-300 hover:bg-dark-surface hover:text-accent rounded-md w-full text-center">Profe</a>
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
                    <p class="text-gray-300">Descubre la belleza de la danza aérea, donde cada movimiento se convierte en una pincelada de elegancia y riesgo a más de 10 metros de altura.</p>
                </div>
                <div class="p-8 bg-dark-card rounded-2xl performer-card border border-gray-700 hover:border-accent/50">
                    <div class="text-4xl text-accent mb-4 text-center">💪</div>
                    <h3 class="text-2xl font-semibold mb-3 text-white">Fuerza y Disciplina</h3>
                    <p class="text-gray-300">Sé testigo del increíble poder físico y la disciplina de nuestros acróbatas, ejecutando complejas figuras que desafían la gravedad.</p>
                </div>
                <div class="p-8 bg-dark-card rounded-2xl performer-card border border-gray-700 hover:border-accent/50">
                    <div class="text-4xl text-accent mb-4 text-center">🎭</div>
                    <h3 class="text-2xl font-semibold mb-3 text-white">Narrativa Emocional</h3>
                    <p class="text-gray-300">Cada acto cuenta una historia. Una banda sonora épica y una iluminación dramática te sumergirán en un viaje de emociones intensas.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Programa/Artistas Destacados -->
    <section id="performers" class="py-20 px-4 bg-dark-surface">
        <div class="max-w-6xl mx-auto">
            <h2 class="text-4xl md:text-5xl font-bold text-center mb-16 text-accent">Estrellas de la Noche</h2>
            <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-8">

                <!-- Artista 1 -->
                <div class="bg-dark-card rounded-xl overflow-hidden performer-card shadow-lg hover:shadow-xl">
                    <img src="https://placehold.co/400x400/1F2937/FFFFFF?text=Artista+A" alt="Retrato de la acróbata Sofía 'El Vuelo'" class="w-full h-48 object-cover transition duration-300 hover:opacity-90">
                    <div class="p-4 text-center">
                        <h4 class="text-xl font-bold text-secondary-accent">Sara 'El Vuelo'</h4>
                        <p class="text-sm text-gray-400">Especialidad: Danza Libre</p>
                    </div>
                </div>

                <!-- Artista 2 -->
                <div class="bg-dark-card rounded-xl overflow-hidden performer-card shadow-lg hover:shadow-xl">
                    <img src="https://placehold.co/400x400/1F2937/FFFFFF?text=Artista+B" alt="Foto del equipo 'Gravedad Cero' en pose de dúo" class="w-full h-48 object-cover transition duration-300 hover:opacity-90">
                    <div class="p-4 text-center">
                        <h4 class="text-xl font-bold text-secondary-accent">Equipo 'Gravedad Cero'</h4>
                        <p class="text-sm text-gray-400">Especialidad: Coreografía en Dúo</p>
                    </div>
                </div>

                <!-- Artista 3 -->
                <div class="bg-dark-card rounded-xl overflow-hidden performer-card shadow-lg hover:shadow-xl">
                    <img src="https://placehold.co/400x400/1F2937/FFFFFF?text=Artista+C" alt="Martín 'La Caída' realizando un drop en tela" class="w-full h-48 object-cover transition duration-300 hover:opacity-90">
                    <div class="p-4 text-center">
                        <h4 class="text-xl font-bold text-secondary-accent">Martín 'La Caída'</h4>
                        <p class="text-sm text-gray-400">Especialidad: Acto de Suspenso</p>
                    </div>
                </div>

                <!-- Artista 4 -->
                <div class="bg-dark-card rounded-xl overflow-hidden performer-card shadow-lg hover:shadow-xl">
                    <img src="https://placehold.co/400x400/1F2937/FFFFFF?text=Artista+D" alt="Invitado realizando una figura en aro aéreo" class="w-full h-48 object-cover transition duration-300 hover:opacity-90">
                    <div class="p-4 text-center">
                        <h4 class="text-xl font-bold text-secondary-accent">Invitado Especial</h4>
                        <p class="text-sm text-gray-400">Especialidad: Aro Aéreo</p>
                    </div>
                </div>

            </div>
        </div>
    </section>
    
    <!-- NUEVA SECCIÓN: Historia Personal de la Profe de TEL -->
    <section id="history" class="py-20 px-4 bg-dark-bg">
        <div class="max-w-6xl mx-auto grid lg:grid-cols-3 gap-12 items-center">
            
            <div class="lg:col-span-1">
                <img src="https://placehold.co/500x700/A855F7/121212?text=PROFESORA+SARA" alt="Retrato artístico de Sara, profesora de acrobacia en tela." class="w-full h-auto object-cover rounded-xl shadow-2xl border-4 border-secondary-accent/50 transform hover:scale-[1.01] transition duration-300">
            </div>

            <div class="lg:col-span-2">
                <h2 class="text-4xl md:text-5xl font-bold mb-6 text-accent">Nuestra Historia: El Vuelo de Sara</h2>
                <h3 class="text-2xl font-semibold mb-4 text-secondary-accent">De la Danza Clásica a la Magia Aérea</h3>
                <p class="text-lg text-gray-300 mb-6">Sara, fundadora de [Nombre del Estudio], comenzó su camino en el arte a la edad de 5 años con ballet clásico. Su vida dio un giro de 180 grados al descubrir la acrobacia en tela, encontrando en la verticalidad una forma de expresión sin límites.</p>
                
                <p class="text-lg text-gray-300 mb-6">Después de formarse en [Ciudad o País] con maestros de renombre mundial, Sara dedicó los últimos 10 años a perfeccionar su técnica y, lo más importante, a desarrollar un método de enseñanza que prioriza la seguridad, la progresión consciente y el desarrollo artístico de cada estudiante.</p>

                <p class="text-lg font-italic text-accent border-l-4 border-secondary-accent pl-4 py-2 bg-dark-surface/50 rounded-lg">"Para mí, la tela no es solo un deporte o una disciplina; es un diálogo constante con la gravedad. Es la forma más honesta de encontrar tu propia fuerza." - Sara</p>
                
                <!-- CTA Clases - ENLACE A WHATSAPP -->
                <a href="https://chat.whatsapp.com/HTfPk2DtG4NDHu85YmwHWq?mode=wwt" target="_blank" class="mt-8 inline-block text-lg font-semibold text-white bg-secondary-accent px-6 py-3 rounded-full hover:bg-emerald-500 transition duration-300 shadow-md">Ver y Consultar Clases</a>
            </div>
        </div>
    </section>

    <!-- NUEVA SECCIÓN: Información sobre las Clases -->
    <section id="classes" class="py-20 px-4 bg-dark-surface">
        <div class="max-w-6xl mx-auto">
            <h2 class="text-4xl md:text-5xl font-bold text-center mb-16 text-accent">Encuentra Tu Clase Ideal</h2>

            <div class="space-y-10">
                
                <!-- Clase 1: Principiantes -->
                <div class="md:flex md:items-center bg-dark-card rounded-2xl p-8 shadow-xl hover:bg-dark-card/80 transition duration-300 border border-gray-700 hover:border-secondary-accent">
                    <div class="md:w-1/3 mb-4 md:mb-0">
                        <h3 class="text-3xl font-bold text-secondary-accent">Nivel 1: Primer Vuelo</h3>
                        <p class="text-lg text-gray-400">Sin experiencia previa</p>
                    </div>
                    <div class="md:w-2/3 md:pl-8">
                        <p class="text-gray-300 mb-3">Introducción a la tela aérea. Aprenderás nudos básicos, ascenso seguro, y las primeras figuras de pie. Ideal para construir fuerza fundamental y confianza.</p>
                        <ul class="text-sm text-accent list-disc list-inside space-y-1">
                            <li>Frecuencia: 2 veces por semana</li>
                            <li>Duración: 60 minutos</li>
                            <li>Focus: Seguridad y Ascensos</li>
                        </ul>
                    </div>
                </div>

                <!-- Clase 2: Intermedio -->
                <div class="md:flex md:items-center bg-dark-card rounded-2xl p-8 shadow-xl hover:bg-dark-card/80 transition duration-300 border border-gray-700 hover:border-secondary-accent">
                    <div class="md:w-1/3 mb-4 md:mb-0">
                        <h3 class="text-3xl font-bold text-secondary-accent">Nivel 2: Exploración Vertical</h3>
                        <p class="text-lg text-gray-400">Requisito: Ascenso básico dominado</p>
                    </div>
                    <div class="md:w-2/3 md:pl-8">
                        <p class="text-gray-300 mb-3">Transiciones, drops pequeños y series coreográficas simples. Enfocado en aumentar la resistencia y la fluidez de los movimientos en el aire.</p>
                        <ul class="text-sm text-accent list-disc list-inside space-y-1">
                            <li>Frecuencia: 3 veces por semana</li>
                            <li>Duración: 90 minutos</li>
                            <li>Focus: Resistencia y Drops</li>
                        </ul>
                    </div>
                </div>

                <!-- Clase 3: Avanzado -->
                <div class="md:flex md:items-center bg-dark-card rounded-2xl p-8 shadow-xl hover:bg-dark-card/80 transition duration-300 border border-gray-700 hover:border-secondary-accent">
                    <div class="md:w-1/3 mb-4 md:mb-0">
                        <h3 class="text-3xl font-bold text-secondary-accent">Nivel 3: Alto Rendimiento</h3>
                        <p class="text-lg text-gray-400">Con experiencia en acrobacia</p>
                    </div>
                    <div class="md:w-2/3 md:pl-8">
                        <p class="text-gray-300 mb-3">Creación de secuencias complejas, drops avanzados y perfeccionamiento de la técnica artística. Preparación para presentaciones y competencias.</p>
                        <ul class="text-sm text-accent list-disc list-inside space-y-1">
                            <li>Frecuencia: 3-5 veces por semana</li>
                            <li>Duración: 120 minutos</li>
                            <li>Focus: Técnica y Coreografía</li>
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
    <section id="podcasts" class="py-20 px-4 bg-dark-bg">
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
    <section id="research" class="py-20 px-4 bg-dark-surface">
        <div class="max-w-6xl mx-auto">
            <h2 class="text-4xl md:text-5xl font-bold text-center mb-16 text-accent">Ciencia y Etnografía de la Acrobacia</h2>

            <div class="grid lg:grid-cols-2 gap-12 items-start">
                
                <!-- Artículo 1: Etnografía (Furiasse) - ENLACE ACTUALIZADO AL PDF -->
                <div class="p-8 bg-dark-card rounded-2xl shadow-xl border border-secondary-accent/50">
                    <h3 class="text-3xl font-bold mb-3 text-secondary-accent">La Dimensión Social del Tel</h3>
                    <p class="text-gray-300 mb-4">Investigaciones como la de **Furiasse (2020)** profundizan en la acrobacia aérea no solo como disciplina física, sino como un fenómeno etnográfico y cultural. Este enfoque explora la construcción de identidad, el sentido de comunidad y los rituales de entrenamiento en los estudios de tela.</p>
                    <ul class="text-sm text-gray-400 list-disc list-inside space-y-1 mb-4">
                        <li>Se analiza el espacio aéreo como un lugar de resignificación personal.</li>
                        <li>Se enfatiza la ética del cuidado y la progresión consciente en el colectivo.</li>
                    </ul>
                    <a href="https://www.circonteudo.com/cuerpos-en-el-aire-trayectorias-formativas-de-la-acrobacia-en-tela-una-aproximacion-etnografica-pdf/" target="_blank" class="text-accent hover:text-violet-600 font-medium underline text-sm">Leer el Artículo Científico (PDF)</a>
                </div>

                <!-- Artículo 2: Físico y Biomecánica (Mantiene consulta a WhatsApp) -->
                <div class="p-8 bg-dark-card rounded-2xl shadow-xl border border-secondary-accent/50">
                    <h3 class="text-3xl font-bold mb-3 text-secondary-accent">Biomecánica y Rendimiento Físico</h3>
                    <p class="text-gray-300 mb-4">Estudios biomecánicos demuestran el altísimo nivel de fuerza isométrica y coordinación requerida en la acrobacia en tela. El entrenamiento mejora la conciencia corporal, la propiocepción y la densidad ósea de manera integral.</p>
                    <ul class="text-sm text-gray-400 list-disc list-inside space-y-1 mb-4">
                        <li>Foco en la prevención de lesiones y la técnica de la fuerza excéntrica.</li>
                        <li>Análisis de la secuencia motora en drops y figuras complejas.</li>
                    </ul>
                    <a href="https://chat.whatsapp.com/HTfPk2DtG4NDHu85YmwHWq?mode=wwt" target="_blank" class="text-accent hover:text-violet-600 font-medium underline text-sm">Consultar sobre Biomecánica</a>
                </div>
            </div>
            <div class="text-center mt-12 text-gray-400 text-sm italic">
                La enseñanza de Sara integra estos fundamentos académicos para una práctica segura y profunda.
            </div>
        </div>
    </section>

    <!-- Sección Tickets y Ubicación (Existing Content) -->
    <section id="tickets" class="py-20 px-4 bg-dark-bg">
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
                        **Lugar:** [Nombre del Teatro o Estudio] - [Dirección Completa]
                    </li>
                </ul>
                
                <div class="mt-8 rounded-lg overflow-hidden border-2 border-gray-700">
                    <!-- Mapa de Google Maps embebido (reemplazando el placeholder) -->
                    <a href="https://maps.app.goo.gl/qkBZuu9j25kx67oL8" target="_blank" class="block">
                        <img src="https://placehold.co/600x300/2D2D2D/34D399?text=VER+UBICACION+EN+MAPS" alt="Mapa de la ubicación del Teatro o Estudio" class="w-full h-48 object-cover">
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
