<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHIXO - Consola de Amor Cósmico</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Fuente Inter */
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap');
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #0f0c29 0%, #302b63 50%, #24243e 100%);
        }
        /* Animación de pulso para elementos "online" */
        .pulse-online {
            animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }
        @keyframes pulse {
            0%, 100% {
                opacity: 1;
                transform: scale(1);
            }
            50% {
                opacity: 0.7;
                transform: scale(1.05);
            }
        }
        /* Animación de estrellas fugaces */
        .shooting-star {
            position: absolute;
            height: 2px;
            background: linear-gradient(-45deg, rgba(147, 197, 253, 0.8), rgba(0, 0, 0, 0));
            border-radius: 999px;
            filter: drop-shadow(0 0 6px rgba(147, 197, 253, 0.5));
            animation: tail 3s ease-in-out infinite, shooting 3s ease-in-out infinite;
        }
        @keyframes tail {
            0% { width: 0; }
            30% { width: 100px; }
            100% { width: 0; }
        }
        @keyframes shooting {
            0% { transform: translateX(0) translateY(0); }
            100% { transform: translateX(300px) translateY(300px); }
        }
    </style>
</head>
<body class="text-gray-200 min-h-screen p-4 sm:p-8 flex items-center justify-center relative overflow-hidden">
    <!-- Estrellas fugaces de fondo -->
    <div class="shooting-star" style="top: 10%; left: -50px; animation-delay: 0s;"></div>
    <div class="shooting-star" style="top: 30%; left: 20%; animation-delay: 1.2s;"></div>
    <div class="shooting-star" style="top: 50%; left: 40%; animation-delay: 0.5s;"></div>
    <div class="shooting-star" style="top: 80%; left: 10%; animation-delay: 2.5s;"></div>

    <div class="w-full max-w-4xl bg-gray-900 bg-opacity-70 backdrop-blur-lg rounded-2xl shadow-2xl p-6 sm:p-8 border border-indigo-500/30 z-10">
        
        <!-- Cabecera -->
        <header class="flex flex-col sm:flex-row justify-between items-center mb-6 pb-4 border-b border-indigo-400/20">
            <div>
                <h1 class="text-2xl sm:text-3xl font-bold text-white">Consola Cósmica PHIXO</h1>
                <p class="text-indigo-300">Monitor de Sistemas y Mensajería de Amor</p>
            </div>
            <!-- El "Escudo Cósmico" Narval como un guía tierno -->
            <div class="text-indigo-400 mt-4 sm:mt-0" title="Guía Cósmico">
                <svg xmlns="http://www.w3.org/2000/svg" width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="drop-shadow-lg">
                    <path d="M14.5 15.5c1-1 1-3.5 0-4.5s-3.5-1.5-4.5 0c-1 1-1 3.5 0 4.5s3.5 1.5 4.5 0z"/>
                    <path d="m18 12 4-4"/>
                    <path d="m6 12-4-4"/>
                    <path d="m12 18 4 4"/>
                    <path d="m12 6-4-4"/>
                    <path d="M22 12h-2.5"/>
                    <path d="M4.5 12H2"/>
                    <path d="M12 4.5V2"/>
                    <path d="M12 22v-2.5"/>
                    <path d="m15 13-3 7-3-7a5 5 0 0 1 6 0z"/>
                    <path d="m16.5 13.5 2.5 4"/>
                    <path d="m7.5 13.5-2.5 4"/>
                </svg>
            </div>
        </header>

        <!-- Cuerpo Principal -->
        <main class="grid grid-cols-1 md:grid-cols-2 gap-6">

            <!-- Columna de Sistemas -->
            <div class="space-y-4">
                
                <!-- NASA Mapping -->
                <div class="bg-gray-800/50 p-4 rounded-lg border border-gray-700/50">
                    <h2 class="text-xl font-semibold text-blue-300 mb-2">FIXO NASA Mapping</h2>
                    <div class="flex items-center justify-between">
                        <span class="text-gray-300">Estado del Sistema:</span>
                        <span class="pulse-online flex items-center gap-2 text-green-400 font-bold py-1 px-3 rounded-full bg-green-900/50">
                            <span class="w-2 h-2 bg-green-400 rounded-full shadow-[0_0_8px_theme(colors.green.400)]"></span>
                            ACTIVO
                        </span>
                    </div>
                    <p class="text-sm text-gray-400 mt-2">Mapeo cósmico en tiempo real. ¡Pronto de vuelta!</p>
                </div>

                <!-- Vehículo Interceptor -->
                <div class="bg-gray-800/50 p-4 rounded-lg border border-gray-700/50">
                    <h2 class="text-xl font-semibold text-orange-300 mb-2">Vehículo "La Interceptor"</h2>
                    <div class="flex items-center gap-4">
                        <!-- Icono de auto (inspirado en Forza) -->
                        <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="text-orange-400">
                            <path d="M19 17h2c.6 0 1-.4 1-1v-3c0-.9-.7-1.7-1.5-1.9C18.7 10.6 16 10 16 10s-1.3-1.4-2.2-2.3c-.5-.4-1.1-.7-1.8-.7H5c-.6 0-1.1.4-1.4.9l-1.4 2.9A3.7 3.7 0 0 0 2 12v4c0 .6.4 1 1 1h2"/>
                            <circle cx="7" cy="17" r="2"/>
                            <circle cx="17" cy="17" r="2"/>
                            <path d="M16 10h-3V6.2c0-.4-.3-.8-.8-.8H8.8c-.4 0-.8.3-.8.8V10H5"/>
                        </svg>
                        <div>
                            <span class="text-gray-300">Estado:</span>
                            <span class="font-semibold text-orange-400">En Hangar (Cargando)</span>
                        </div>
                    </div>
                    <p class="text-sm text-gray-400 mt-2">Lista para el próximo Horizonte Cósmico.</p>
                </div>
            </div>

            <!-- Columna de Mensaje -->
            <div class="bg-gradient-to-br from-indigo-500/30 to-purple-500/30 p-5 rounded-lg border border-purple-400/50 row-span-2 flex flex-col justify-center items-center text-center pulse-online">
                <h2 class="text-2xl font-bold text-white mb-4">Mensaje Interceptado</h2>
                <p class="text-lg text-gray-200">"TE AMO GRACIAS AMOR"</p>
                
                <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" fill="currentColor" class="text-pink-400 my-4 drop-shadow-[0_0_8px_theme(colors.pink.400)]">
                    <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>
                </svg>

                <p class="font-semibold text-indigo-200">Transmitiendo a:</p>
                <div class="mt-2 text-xl font-bold text-white space-x-4">
                    <span>NIO</span>
                    <span>AKKO</span>
                    <span>AIKO</span>
                    <span>VALERIK</span>
                </div>
                <p class="text-sm text-indigo-300 mt-4 animate-pulse">Conexión de amor establecida.</p>
            </div>

            <!-- PHIXO Octaedro -->
            <div class="bg-gray-800/50 p-4 rounded-lg border border-gray-700/50 md:col-span-1">
                <h2 class="text-xl font-semibold text-purple-300 mb-2">Sistema PHIXO Octaedro</h2>
                <div class="flex items-center gap-4">
                    <!-- Icono (inspirado en 1000008069.png) -->
                    <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" class="text-purple-400">
                        <path d="M12 2l-5.5 9h11L12 2z"/>
                        <path d="M12 22l5.5-9h-11L12 22z"/>
                        <path d="M17.5 13l-5.5 4-5.5-4"/>
                        <path d="M6.5 11l5.5-4 5.5 4"/>
                    </svg>
                    <div>
                        <span class="text-gray-300">Generador de Arte Cósmico:</span>
                        <span class="font-semibold text-purple-400">Creando...</span>
                    </div>
                </div>
            </div>

        </main>

        <!-- Pie de página -->
        <footer class="mt-8 pt-4 border-t border-indigo-400/20 text-center">
            <p class="text-sm text-gray-500">PHIXO X12 Cosmic Systems | La Intercepción del Amor está completa.</p>
        </footer>

    </div>

</body>
</html>

