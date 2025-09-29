```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dulces Delicias - Tu dulcería de confianza</title>
    <style>
        /* Estilos generales */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        :root {
            --color-primario: #FF6B8B;
            --color-secundario: #FFD166;
            --color-terciario: #06D6A0;
            --color-texto: #333;
            --color-fondo: #FFF9F2;
        }
        
        body {
            background-color: var(--color-fondo);
            color: var(--color-texto);
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Estilos del encabezado */
        header {
            background: linear-gradient(135deg, var(--color-primario), var(--color-secundario));
            color: white;
            padding: 20px 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo h1 {
            font-size: 1.8rem;
            margin-left: 10px;
        }
        
        .logo-icon {
            font-size: 2rem;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        nav ul li a:hover {
            color: var(--color-terciario);
        }
        
        /* Estilos del héroe */
        .hero {
            background-image: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)), url('https://images.unsplash.com/photo-1555507036-ab794f27d2e9?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 100px 0;
        }
        
        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--color-primario);
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: var(--color-terciario);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        /* Estilos de secciones */
        section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            color: var(--color-primario);
        }
        
        /* Estilos de productos */
        .productos-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .producto-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }
        
        .producto-card:hover {
            transform: translateY(-10px);
        }
        
        .producto-img {
            height: 200px;
            background-color: #f8f8f8;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
        }
        
        .producto-info {
            padding: 20px;
        }
        
        .producto-info h3 {
            margin-bottom: 10px;
            color: var(--color-primario);
        }
        
        .producto-precio {
            font-weight: bold;
            color: var(--color-terciario);
            margin-bottom: 15px;
        }
        
        /* Estilos de servicios */
        .servicios {
            background-color: #fff;
        }
        
        .servicios-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .servicio-card {
            text-align: center;
            padding: 30px 20px;
            border-radius: 10px;
            background-color: var(--color-fondo);
            transition: all 0.3s ease;
        }
        
        .servicio-card:hover {
            background-color: white;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .servicio-icon {
            font-size: 2.5rem;
            color: var(--color-primario);
            margin-bottom: 20px;
        }
        
        /* Estilos de sobre nosotros */
        .sobre-nosotros {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .sobre-texto {
            flex: 1;
        }
        
        .sobre-imagen {
            flex: 1;
            height: 400px;
            background-color: #f8f8f8;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 5rem;
        }
        
        /* Estilos de contacto */
        .contacto {
            background-color: #fff;
        }
        
        .contacto-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }
        
        .info-contacto {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .info-item {
            display: flex;
            align-items: center;
        }
        
        .info-icon {
            font-size: 1.5rem;
            margin-right: 15px;
            color: var(--color-primario);
        }
        
        /* Estilos del pie de página */
        footer {
            background-color: #333;
            color: white;
            padding: 50px 0 20px;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-logo h3 {
            color: var(--color-secundario);
            margin-bottom: 15px;
        }
        
        .footer-links h4,
        .footer-redes h4 {
            margin-bottom: 20px;
            color: var(--color-secundario);
        }
        
        .footer-links ul {
            list-style: none;
        }
        
        .footer-links ul li {
            margin-bottom: 10px;
        }
        
        .footer-links ul li a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-links ul li a:hover {
            color: var(--color-terciario);
        }
        
        .redes-sociales {
            display: flex;
            gap: 15px;
        }
        
        .red-social {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .red-social:hover {
            background-color: var(--color-primario);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            color: #aaa;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
            }
            
            nav ul {
                margin-top: 20px;
            }
            
            .sobre-nosotros {
                flex-direction: column;
            }
            
            .contacto-container {
                grid-template-columns: 1fr;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Encabezado -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <span class="logo-icon">🍬</span>
                <h1>Dulces Delicias</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#productos">Productos</a></li>
                    <li><a href="#servicios">Servicios</a></li>
                    <li><a href="#nosotros">Nosotros</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Sección Hero -->
    <section id="inicio" class="hero">
        <div class="container">
            <h2>Endulzando tus momentos especiales</h2>
            <p>En Dulces Delicias encontrarás la más amplia variedad de dulces artesanales, chocolates, caramelos y golosinas para todos los gustos y ocasiones.</p>
            <a href="#productos" class="btn">Ver Productos</a>
        </div>
    </section>

    <!-- Sección Productos -->
    <section id="productos">
        <div class="container">
            <h2 class="section-title">Nuestros Productos</h2>
            <div class="productos-grid">
                <div class="producto-card">
                    <div class="producto-img">🍫</div>
                    <div class="producto-info">
                        <h3>Chocolates Artesanales</h3>
                        <p>Deliciosos chocolates elaborados con cacao de primera calidad.</p>
                        <div class="producto-precio">Desde $5.000</div>
                        <a href="#contacto" class="btn">Pedir Ahora</a>
                    </div>
                </div>
                
                <div class="producto-card">
                    <div class="producto-img">🍭</div>
                    <div class="producto-info">
                        <h3>Caramelos Caseros</h3>
                        <p>Caramelos de todos los sabores, elaborados con ingredientes naturales.</p>
                        <div class="producto-precio">Desde $2.000</div>
                        <a href="#contacto" class="btn">Pedir Ahora</a>
                    </div>
                </div>
                
                <div class="producto-card">
                    <div class="producto-img">🍬</div>
                    <div class="producto-info">
                        <h3>Golosinas Variadas</h3>
                        <p>Gran selección de golosinas para niños y adultos.</p>
                        <div class="producto-precio">Desde $1.500</div>
                        <a href="#contacto" class="btn">Pedir Ahora</a>
                    </div>
                </div>
                
                <div class="producto-card">
                    <div class="producto-img">🎂</div>
                    <div class="producto-info">
                        <h3>Postres Especiales</h3>
                        <p>Postres y dulces para ocasiones especiales y celebraciones.</p>
                        <div class="producto-precio">Desde $15.000</div>
                        <a href="#contacto" class="btn">Pedir Ahora</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Servicios -->
    <section id="servicios" class="servicios">
        <div class="container">
            <h2 class="section-title">Nuestros Servicios</h2>
            <div class="servicios-grid">
                <div class="servicio-card">
                    <div class="servicio-icon">🚚</div>
                    <h3>Delivery Express</h3>
                    <p>Entrega rápida a domicilio para que disfrutes tus dulces sin salir de casa.</p>
                </div>
                
                <div class="servicio-card">
                    <div class="servicio-icon">🎁</div>
                    <h3>Cajas Personalizadas</h3>
                    <p>Creamos cajas de dulces personalizadas para regalos y eventos especiales.</p>
                </div>
                
                <div class="servicio-card">
                    <div class="servicio-icon">🎉</div>
                    <h3>Dulces para Eventos</h3>
                    <p>Servicio especial para fiestas, bodas, cumpleaños y eventos corporativos.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Sobre Nosotros -->
    <section id="nosotros">
        <div class="container">
            <h2 class="section-title">Sobre Nosotros</h2>
            <div class="sobre-nosotros">
                <div class="sobre-texto">
                    <h3>Nuestra Historia</h3>
                    <p>Dulces Delicias nació hace más de 10 años con el sueño de endulzar la vida de nuestros clientes. Comenzamos como un pequeño emprendimiento familiar y hoy somos reconocidos por la calidad y sabor único de nuestros productos.</p>
                    <p>Utilizamos ingredientes naturales y técnicas artesanales para crear dulces que evocan recuerdos de la infancia y crean nuevos momentos felices.</p>
                    <p>Nuestra misión es seguir endulzando vidas, un dulce a la vez, manteniendo siempre la calidad y el sabor que nos caracteriza.</p>
                </div>
                <div class="sobre-imagen">
                    🍭🍬🍫
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Contacto -->
    <section id="contacto" class="contacto">
        <div class="container">
            <h2 class="section-title">Contáctanos</h2>
            <div class="contacto-container">
                <div class="formulario">
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="nombre">Nombre</label>
                            <input type="text" id="nombre" name="nombre" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" name="email" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="telefono">Teléfono</label>
                            <input type="tel" id="telefono" name="telefono">
                        </div>
                        
                        <div class="form-group">
                            <label for="mensaje">Mensaje</label>
                            <textarea id="mensaje" name="mensaje" rows="5" required></textarea>
                        </div>
                        
                        <button type="submit" class="btn">Enviar Mensaje</button>
                    </form>
                </div>
                
                <div class="info-contacto">
                    <div class="info-item">
                        <span class="info-icon">📍</span>
                        <div>
                            <h4>Dirección</h4>
                            <p>Calle Dulce 123, Centro</p>
                        </div>
                    </div>
                    
                    <div class="info-item">
                        <span class="info-icon">📞</span>
                        <div>
                            <h4>Teléfono</h4>
                            <p>+57 123 456 7890</p>
                        </div>
                    </div>
                    
                    <div class="info-item">
                        <span class="info-icon">✉️</span>
                        <div>
                            <h4>Email</h4>
                            <p>info@dulcesdelicias.com</p>
                        </div>
                    </div>
                    
                    <div class="info-item">
                        <span class="info-icon">🕒</span>
                        <div>
                            <h4>Horario</h4>
                            <p>Lunes a Sábado: 9:00 AM - 8:00 PM</p>
                            <p>Domingos: 10:00 AM - 6:00 PM</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Pie de página -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-logo">
                    <h3>Dulces Delicias</h3>
                    <p>Endulzando tus momentos especiales desde 2012.</p>
                </div>
                
                <div class="footer-links">
                    <h4>Enlaces Rápidos</h4>
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#productos">Productos</a></li>
                        <li><a href="#servicios">Servicios</a></li>
                        <li><a href="#nosotros">Nosotros</a></li>
                        <li><a href="#contacto">Contacto</a></li>
                    </ul>
                </div>
                
                <div class="footer-redes">
                    <h4>Síguenos</h4>
                    <div class="redes-sociales">
                        <a href="#" class="red-social">FB</a>
                        <a href="#" class="red-social">IG</a>
                        <a href="#" class="red-social">TW</a>
                        <a href="#" class="red-social">YT</a>
                    </div>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 Dulces Delicias. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>

    <script>
        // Formulario de contacto
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('¡Gracias por tu mensaje! Te contactaremos pronto.');
            this.reset();
        });
        
        // Navegación suave
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
```
