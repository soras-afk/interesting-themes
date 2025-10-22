<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Blog sobre la vida en los Colegios de Alto Rendimiento (COAR) en Perú. Reflexiones, rutinas y experiencias de estudiantes talentosos.">
    <meta name="keywords" content="COAR Perú, vida en COAR, colegios de alto rendimiento, estudiantes talentosos, educación secundaria Perú">
    <meta name="author" content="Estudiantes COAR">
    <title>COAR Vida: Reflexiones desde los Colegios de Alto Rendimiento | Blog Estudiantil</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* Reset y Estilos Base */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            line-height: 1.7;
            color: #2d3748;
            background-color: #f7fafc;
        }
        a {
            text-decoration: none;
            color: inherit;
        }
        ul {
            list-style: none;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #1a202c 0%, #2d3748 100%);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .logo h1 {
            font-size: 1.8rem;
            font-weight: 700;
        }
        nav ul {
            display: flex;
            gap: 2rem;
        }
        nav ul li a {
            color: white;
            font-weight: 500;
            transition: color 0.3s ease;
            position: relative;
        }
        nav ul li a:hover,
        nav ul li a.active {
            color: #63b3ed;
        }
        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: #63b3ed;
            transition: width 0.3s ease;
        }
        nav ul li a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(26,32,44,0.8), rgba(26,32,44,0.8)), url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%2363b3ed" width="1200" height="600"/><text x="50%" y="50%" font-family="Inter" font-size="48" fill="white" text-anchor="middle" dy=".3em">Vida en COAR Perú</text></svg>');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 4rem 2rem;
        }
        .hero h2 {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 1rem;
        }
        .hero p {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto;
            opacity: 0.9;
        }

        /* Main Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 2rem;
        }

        /* Main Content */
        main {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }
        article {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        article:hover {
            transform: translateY(-4px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }
        article header {
            padding: 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 1.5rem;
        }
        article h2 {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }
        article .meta {
            font-size: 0.9rem;
            opacity: 0.8;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        article .content {
            padding: 1.5rem;
        }
        article p {
            text-align: justify;
            margin-bottom: 1rem;
        }
        .read-more {
            display: inline-block;
            color: #667eea;
            font-weight: 500;
            border-bottom: 1px solid transparent;
            transition: border-color 0.3s ease;
        }
        .read-more:hover {
            border-color: #667eea;
        }
        /* Sección especial para historia de Tito */
        .tito-section {
            background: linear-gradient(135deg, #f0f8ff 0%, #e6f3ff 100%);
            border-left: 4px solid #667eea;
            padding: 1.5rem;
            margin-bottom: 1rem;
        }
        .tito-section h3 {
            color: #2d3748;
            margin-bottom: 1rem;
            font-size: 1.2rem;
            font-weight: 600;
        }
        .tito-section ul {
            list-style: disc;
            padding-left: 1.5rem;
        }
        .tito-section li {
            margin-bottom: 0.5rem;
            color: #4a5568;
        }

        /* Sidebar */
        aside {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }
        .sidebar-section {
            background: white;
            padding: 1.5rem;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        }
        .sidebar-section h3 {
            font-size: 1.2rem;
            font-weight: 600;
            color: #2d3748;
            margin-bottom: 1rem;
            border-bottom: 2px solid #e2e8f0;
            padding-bottom: 0.5rem;
        }
        .sidebar-section ul li {
            margin-bottom: 0.75rem;
            padding: 0.5rem 0;
            border-bottom: 1px solid #f7fafc;
        }
        .sidebar-section ul li a {
            color: #4a5568;
            font-weight: 500;
            transition: color 0.3s ease;
        }
        .sidebar-section ul li a:hover {
            color: #667eea;
        }
        .social-links {
            display: flex;
            gap: 1rem;
            justify-content: center;
        }
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: #e2e8f0;
            border-radius: 50%;
            transition: background 0.3s ease;
        }
        .social-links a:hover {
            background: #667eea;
            color: white;
        }

        /* Footer */
        footer {
            background: #1a202c;
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 4rem;
        }
        footer p {
            opacity: 0.8;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                gap: 1rem;
                padding: 1rem;
            }
            nav ul {
                gap: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }
            .hero h2 {
                font-size: 2rem;
            }
            .hero p {
                font-size: 1rem;
            }
            .container {
                grid-template-columns: 1fr;
                padding: 1rem;
                gap: 1.5rem;
            }
            article header {
                padding: 1rem;
            }
            article .content {
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-container">
            <div class="logo">
                <h1>COAR Vida</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#inicio" class="active">Inicio</a></li>
                    <li><a href="#articulos">Artículos</a></li>
                    <li><a href="#sobre-mi">Sobre COAR</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero">
        <h2>Descubre la Vida en COAR Perú</h2>
        <p>Explora rutinas, experiencias y reflexiones de estudiantes en los Colegios de Alto Rendimiento. Historias inspiradoras de talento y superación en el Perú.</p>
    </section>

    <div class="container">
        <main>
            <article>
                <header>
                    <h2>conoceq la Vida de Tito: Un Día en el COAR de Apurimac</h2>
                    <img src="" alt="">
                    <div class="meta">
                        <span>📅 22 de octubre de 2025</span>
                        <span>👤 Para tito o toti, Estudiante COAR Apurimac</span>
                    </div>
                </header>
                <div class="content">
                    
                    <img src="WhatsApp Image 2025-10-22 at 10.42.57 AM.jpeg" alt="tito" width="1000" height="1200"> <p>Tito es un estudiante de 16 años en el Colegio de Alto Rendimiento (COAR) de Apurimac. Como miles de jóvenes talentosos seleccionados a nivel nacional, Tito representa el espíritu de superación que define estos colegios exclusivos, creados por el Ministerio de Educación para fomentar la excelencia académica en regiones remotas. Su vida es un torbellino de disciplina, descubrimientos y crecimiento personal, lejos de la rutina convencional de un colegio regular.</p>
                    
                    <div class="tito-section">
                        <h3>Un Día Típico en el COAR: De la Alarma al Descanso Merecido</h3>
                        <p>Tito se despierta a las <strong>5:45 AM</strong> en su dormitorio compartido con otros cuatro compañeros. El COAR es un internado, así que vive en un campus moderno con aulas equipadas con laboratorios y espacios para proyectos. No hay tiempo para pereza: a las 6:00 AM, desayuna en el comedor colectivo –un plato nutritivo con quinua, frutas andinas y proteínas para recargar energías.</p>
                        <ul>
                            <li><strong>Mañanas Académicas (7:00 AM - 12:00 PM):</strong> Las clases comienzan con matemáticas avanzadas o física cuántica. Tito resuelve ecuaciones diferenciales en grupo de 25 estudiantes.</li>
                            <li><strong>Almuerzo y Tiempo Libre (12:00 PM - 1:30 PM):</strong> Charla con amigos de regiones diversas, forjando amistades multiculturales.</li>
                            <li><strong>Tardes de Especialización (1:30 PM - 6:00 PM):</strong> Electivas como robótica; Tito diseña un dron para monitorear cultivos en el Valle del Colca.</li>
                            <li><strong>Noches de Estudio y Reflexión (6:00 PM - 10:00 PM):</strong> Tutorías y "círculo de reflexión" grupal para compartir metas.</li>
                        </ul>
                        <p>Apaga luces a las 10:00 PM.</p>
                    </div>

                    <p>La vida en COAR no es solo gloria. Tito enfrenta <strong>presión emocional</strong>: la selección es meritocrática, pero mantener el ritmo es duro. "A veces lloro por extrañar a mi mamá", confiesa en un diario virtual. El aislamiento regional (Tito viene de un pueblo en Moquegua) genera nostalgia, pero los círculos de apoyo ayudan. Físicamente, el agotamiento es real: fines de semana libres permiten visitas familiares o exploraciones en Arequipa, como el Cañón del Colca.</p>

                    <div class="tito-section">
                        <h3>Logros y Desafíos: El Talento Bajo Presión</h3>
                        <p>Los logros de Tito son inspiradores: ganó una olimpiada nacional de matemáticas, lo que le abrió puertas a becas en universidades como la UNSA o incluso programas internacionales. El COAR ofrece alianzas con MIT y becas Fulbright, preparando a estudiantes como él para carreras en STEM o liderazgo social.</p>
                        <ul>
                            <li><strong>Desafíos:</strong> Presión por excelencia (notas mínimas de 16/20), adaptación cultural y burnout ocasional.</li>
                            <li><strong>Logros:</strong> Proyectos colaborativos que simulan el mundo real, amistades duraderas y una visión global desde los Andes peruanos.</li>
                        </ul>
                        <p>Para Tito, el COAR no es solo un colegio; es un puente hacia un futuro brillante. "Aquí aprendo que el talento sin esfuerzo es nada", reflexiona. Si aspiras a un COAR, prepárate para darlo todo –¡vale la pena!</p>
                    </div>

                    <a href="#" class="read-more">Leer más historias como la de Tito →</a>
                </div>
            </article>

            <article>
                <header>
                    <h2>La Rutina Diaria en un COAR: 10 Horas de Estudio y Más</h2>
                    <div class="meta">
                        <span>📅 15 de octubre de 2025</span>
                        <span>👤 Por Juan Pérez, Estudiante COAR Arequipa</span>
                    </div>
                </header>
                <div class="content">
                    <p>En los Colegios de Alto Rendimiento (COAR), la vida es una mezcla intensa de clases avanzadas, talleres creativos y tiempo para el deporte. Despertamos a las 6 AM para desayunar y comenzar con matemáticas de alto nivel, seguido de ciencias y humanidades. Aunque exhaustivo, este ritmo nos prepara para universidades top y transforma nuestra visión del mundo.</p>
                    <p>Lo que diferencia a un COAR de un colegio normal es el enfoque en el desarrollo integral: no solo académicos, sino liderazgo y proyectos colaborativos que simulan el mundo real.</p>
                    <a href="#" class="read-more">Leer artículo completo →</a>
                </div>
            </article>

            <article>
                <header>
                    <h2>Beneficios de Estudiar en COAR: Oportunidades que Cambian Vidas</h2>
                    <div class="meta">
                        <span>📅 10 de octubre de 2025</span>
                        <span>👤 Por María López, Egresada COAR Cusco</span>
                    </div>
                </header>
                <div class="content">
                    <p>Como egresada de un COAR, puedo decir que estos colegios no solo elevan tu GPA, sino que te conectan con aliados globales como universidades de EE.UU. y programas de becas. En mi caso, obtuve una beca completa gracias a los intercambios y talleres de investigación que ofrecemos.</p>
                    <a href="#" class="read-more">Leer artículo completo →</a>
                </div>
            </article>
        </main>

        <aside>
            <div class="sidebar-section">
                <h3>Categorías Populares</h3>
                <ul>
                    <li><a href="#">Rutina y Estudios <span>(12)</span></a></li>
                    <li><a href="#">Historias Personales <span>(8)</span></a></li>
                    <li><a href="#">Consejos para Aspirantes <span>(6)</span></a></li>
                    <li><a href="#">Oportunidades y Becas <span>(10)</span></a></li>
                    <li><a href="#">Vida en COAR por Región <span>(5)</span></a></li>
                </ul>
            </div>

            <div class="sidebar-section">
                <h3>Últimos Artículos</h3>
                <ul>
                    <li><a href="#">La Vida de Tito en COAR</a></li>
                    <li><a href="#">Rutina Diaria en COAR</a></li>
                    <li><a href="#">Beneficios de COAR</a></li>
                    <li><a href="#">Superación en Piura</a></li>
                </ul>
            </div>

            <div class="sidebar-section">
                <h3>Síguenos</h3>
                <div class="social-links">
                    <a href="#" aria-label="Twitter">🐦</a>
                    <a href="#" aria-label="LinkedIn">💼</a>
                    <a href="#" aria-label="Instagram">📷</a>
                </div>
            </div>
        </aside>
    </div>

    <footer>
        <p>&copy; 2025 COAR Vida. Todos los derechos reservados. | Por y para estudiantes de los Colegios de Alto Rendimiento en Perú.</p>
    </footer>
</body>
</html>
