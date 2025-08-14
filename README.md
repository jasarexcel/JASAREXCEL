## Hi there 👋 Aqui aprenderas de forma fácil 

## Hi there 👋 Aqui aprenderas de forma fácil 

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Academia Excel Pro</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-50 text-gray-800">

    <!-- HEADER -->
    <header class="bg-green-700 text-white p-5">
        <div class="container mx-auto flex justify-between items-center">
            <h1 class="text-2xl font-bold">Academia Excel Pro</h1>
            <nav class="space-x-4">
                <a href="#inicio" class="hover:underline">Inicio</a>
                <a href="#cursos" class="hover:underline">Cursos</a>
                <a href="#pruebas" class="hover:underline">Pruebas</a>
                <a href="#registro" class="hover:underline">Registro</a>
            </nav>
        </div>
    </header>

    <!-- HERO -->
    <section id="inicio" class="text-center py-20 bg-green-100">
        <h2 class="text-4xl font-bold mb-4">Aprende Excel desde Cero hasta Experto</h2>
        <p class="text-lg mb-6">Domina las fórmulas, tablas dinámicas, macros y más, con ejemplos y práctica interactiva.</p>
        <a href="#registro" class="bg-green-700 text-white px-6 py-3 rounded-lg hover:bg-green-800">Regístrate Gratis</a>
    </section>

    <!-- CURSOS -->
    <section id="cursos" class="container mx-auto py-16">
        <h3 class="text-3xl font-bold text-center mb-12">Nuestros Niveles</h3>
        <div class="grid md:grid-cols-3 gap-8">
            <div class="bg-white p-6 shadow rounded-xl">
                <h4 class="text-xl font-bold mb-4">Básico</h4>
                <p>Aprende lo esencial: celdas, formatos, fórmulas básicas y organización de datos.</p>
            </div>
            <div class="bg-white p-6 shadow rounded-xl">
                <h4 class="text-xl font-bold mb-4">Intermedio</h4>
                <p>Fórmulas avanzadas, gráficos, validación de datos y funciones condicionales.</p>
            </div>
            <div class="bg-white p-6 shadow rounded-xl">
                <h4 class="text-xl font-bold mb-4">Avanzado</h4>
                <p>Tablas dinámicas, macros con VBA, automatización y análisis de datos.</p>
            </div>
        </div>
    </section>

    <!-- AMBIENTE DE PRUEBAS -->
    <section id="pruebas" class="bg-gray-100 py-16">
        <div class="container mx-auto">
            <h3 class="text-3xl font-bold text-center mb-6">Ambiente de Pruebas</h3>
            <p class="text-center mb-8">Practica fórmulas y funciones en este simulador de Excel básico.</p>
            <div class="bg-white p-6 rounded-xl shadow">
                <textarea id="excelSim" placeholder="Escribe aquí tu fórmula o ejercicio..." class="w-full p-4 border rounded mb-4" rows="5"></textarea>
                <button onclick="simularExcel()" class="bg-green-700 text-white px-4 py-2 rounded hover:bg-green-800">Probar</button>
                <div id="resultado" class="mt-4 p-4 bg-gray-50 border rounded"></div>
            </div>
        </div>
    </section>

    <!-- REGISTRO -->
    <section id="registro" class="py-16 container mx-auto">
        <h3 class="text-3xl font-bold text-center mb-6">Regístrate con tu correo</h3>
        <form class="max-w-lg mx-auto bg-white p-6 rounded-xl shadow" onsubmit="registrarUsuario(event)">
            <input type="email" id="email" placeholder="Tu correo" required class="w-full p-3 border rounded mb-4">
            <button type="submit" class="bg-green-700 text-white px-4 py-2 rounded hover:bg-green-800 w-full">Registrarme</button>
        </form>
        <p id="msgRegistro" class="text-center mt-4 text-green-700"></p>
    </section>

    <!-- FOOTER -->
    <footer class="bg-green-700 text-white text-center py-4">
        &copy; 2025 Academia Excel Pro - Todos los derechos reservados
    </footer>

    <!-- Scripts -->
    <script>
        function simularExcel() {
            let input = document.getElementById('excelSim').value;
            let output = '';
            try {
                // Simulación muy básica: evalúa operaciones simples
                output = 'Resultado: ' + eval(input);
            } catch (e) {
                output = 'Error en la fórmula';
            }
            document.getElementById('resultado').innerText = output;
        }

        function registrarUsuario(e) {
            e.preventDefault();
            let email = document.getElementById('email').value;
            // Aquí conectarías con Firebase, Mailchimp o tu backend
            document.getElementById('msgRegistro').innerText = `¡Gracias por registrarte, ${email}!`;
            document.getElementById('email').value = '';
        }
    </script>
</body>
</html>
