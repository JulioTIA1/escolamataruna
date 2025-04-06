# escolamataruna<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Escola Mataruna - Educação de Qualidade</title>
    <style>
        :root {
            --primary-color: #0066cc;
            --secondary-color: #0099ff;
            --accent-color: #ff9900;
            --text-color: #333333;
            --light-color: #ffffff;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            color: var(--text-color);
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: var(--light-color);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            display: flex;
            align-items: center;
        }
        
        .logo span {
            color: var(--accent-color);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: var(--light-color);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--accent-color);
        }
        
        .hero {
            background: url('/api/placeholder/1200/600') no-repeat center center/cover;
            height: 80vh;
            color: var(--light-color);
            display: flex;
            align-items: center;
            text-align: center;
            position: relative;
            margin-top: 70px;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
        }
        
        .hero-content {
            position: relative;
            z-index: 10;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background: var(--accent-color);
            color: var(--light-color);
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            text-decoration: none;
            font-size: 1rem;
            font-weight: 500;
            transition: background 0.3s;
        }
        
        .btn:hover {
            background: #e68a00;
        }
        
        section {
            padding: 5rem 0;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--primary-color);
        }
        
        .about-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .about-img {
            height: 100%;
            overflow: hidden;
        }
        
        .about-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }
        
        .services {
            background-color: #f9f9f9;
        }
        
        .services-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .service-card {
            background: var(--light-color);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
        }
        
        .service-img {
            height: 200px;
            overflow: hidden;
        }
        
        .service-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .service-card:hover .service-img img {
            transform: scale(1.1);
        }
        
        .service-content {
            padding: 1.5rem;
        }
        
        .service-content h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: var(--primary-color);
        }
        
        .testimonials {
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: var(--light-color);
        }
        
        .testimonials .section-title {
            color: var(--light-color);
        }
        
        .testimonials-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .testimonial-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 2rem;
            backdrop-filter: blur(5px);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 1rem;
        }
        
        .testimonial-author {
            font-weight: bold;
        }
        
        .testimonial-role {
            opacity: 0.8;
            font-size: 0.9rem;
        }
        
        .contact {
            background-color: #f9f9f9;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }
        
        .contact-info p {
            margin-bottom: 1rem;
        }
        
        .contact-form .form-group {
            margin-bottom: 1.5rem;
        }
        
        .contact-form label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }
        
        .contact-form textarea {
            height: 150px;
        }
        
        footer {
            background: var(--primary-color);
            color: var(--light-color);
            padding: 2rem 0;
            text-align: center;
        }
        
        .social-links {
            margin: 1rem 0;
        }
        
        .social-links a {
            color: var(--light-color);
            margin: 0 0.5rem;
            font-size: 1.2rem;
        }
        
        .footer-links {
            margin-top: 1.5rem;
        }
        
        .footer-links a {
            color: var(--light-color);
            margin: 0 0.5rem;
            text-decoration: none;
        }
        
        .footer-links a:hover {
            text-decoration: underline;
        }
        
        /* Mobile responsiveness */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 1rem;
            }
            
            .hero {
                height: 60vh;
                margin-top: 120px;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    Escola <span>Mataruna</span>
                </div>
                <nav>
                    <ul>
                        <li><a href="#home">Início</a></li>
                        <li><a href="#about">Sobre</a></li>
                        <li><a href="#services">Serviços</a></li>
                        <li><a href="#testimonials">Depoimentos</a></li>
                        <li><a href="#contact">Contato</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Bem-vindo à Escola Mataruna</h1>
                <p>Educação de qualidade com foco no desenvolvimento integral dos alunos</p>
                <a href="#contact" class="btn">Agende uma Visita</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">Sobre Nós</h2>
            <div class="about-content">
                <div class="about-img">
                    <img src="/api/placeholder/600/400" alt="Escola Mataruna">
                </div>
                <div class="about-text">
                    <h3>Nossa História</h3>
                    <p>Fundada em 1985, a Escola Mataruna tem se dedicado a oferecer uma educação de excelência, formando cidadãos conscientes e preparados para os desafios do mundo moderno.</p>
                    <p>Com uma metodologia inovadora e professores altamente qualificados, buscamos desenvolver as habilidades cognitivas, sociais e emocionais de nossos alunos, preparando-os não apenas academicamente, mas para a vida.</p>
                    <h3>Nossa Missão</h3>
                    <p>Formar cidadãos críticos, autônomos e participativos, capazes de intervir e transformar a realidade social.</p>
                    <h3>Nossa Visão</h3>
                    <p>Ser reconhecida como uma instituição de referência em educação, que valoriza a diversidade, o respeito e a sustentabilidade.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <h2 class="section-title">Nossos Serviços</h2>
            <div class="services-container">
                <div class="service-card">
                    <div class="service-img">
                        <img src="/api/placeholder/400/300" alt="Educação Infantil">
                    </div>
                    <div class="service-content">
                        <h3>Educação Infantil</h3>
                        <p>Para crianças de 2 a 5 anos, com foco no desenvolvimento integral e estímulo à criatividade e curiosidade natural.</p>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-img">
                        <img src="/api/placeholder/400/300" alt="Ensino Fundamental I">
                    </div>
                    <div class="service-content">
                        <h3>Ensino Fundamental I</h3>
                        <p>Do 1º ao 5º ano, desenvolvendo as habilidades básicas e formando uma base sólida para os estudos futuros.</p>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-img">
                        <img src="/api/placeholder/400/300" alt="Ensino Fundamental II">
                    </div>
                    <div class="service-content">
                        <h3>Ensino Fundamental II</h3>
                        <p>Do 6º ao 9º ano, ampliando conhecimentos e preparando para os desafios do Ensino Médio.</p>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-img">
                        <img src="/api/placeholder/400/300" alt="Ensino Médio">
                    </div>
                    <div class="service-content">
                        <h3>Ensino Médio</h3>
                        <p>Preparação completa para o ENEM e vestibulares, com professores especializados e material didático de qualidade.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <h2 class="section-title">Depoimentos</h2>
            <div class="testimonials-container">
                <div class="testimonial-card">
                    <p class="testimonial-text">"A Escola Mataruna transformou a vida do meu filho. Os professores são dedicados e a metodologia de ensino é excelente. Recomendo a todos!"</p>
                    <p class="testimonial-author">Maria Silva</p>
                    <p class="testimonial-role">Mãe de aluno do 5º ano</p>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">"Estudei na Mataruna durante todo o Ensino Médio e fui aprovado em Medicina. A preparação que recebi foi fundamental para o meu sucesso."</p>
                    <p class="testimonial-author">João Santos</p>
                    <p class="testimonial-role">Ex-aluno</p>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">"Como professora, valorizo muito o ambiente de trabalho e o projeto pedagógico da escola. É um lugar onde realmente podemos fazer a diferença na educação."</p>
                    <p class="testimonial-author">Ana Oliveira</p>
                    <p class="testimonial-role">Professora de Matemática</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">Entre em Contato</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Informações de Contato</h3>
                    <p><strong>Endereço:</strong> Av. Principal, 1000 - Centro</p>
                    <p><strong>Telefone:</strong> (21) 9999-8888</p>
                    <p><strong>Email:</strong> contato@escolamataruna.com.br</p>
                    <p><strong>Horário de Funcionamento:</strong> Segunda a Sexta, das 7h às 18h</p>
                    <iframe 
                        width="100%" 
                        height="300" 
                        frameborder="0" 
                        scrolling="no" 
                        marginheight="0" 
                        marginwidth="0" 
                        src="/api/placeholder/600/300">
                    </iframe>
                </div>
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Nome Completo</label>
                            <input type="text" id="name" name="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" name="email" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">Telefone</label>
                            <input type="tel" id="phone" name="phone">
                        </div>
                        <div class="form-group">
                            <label for="subject">Assunto</label>
                            <input type="text" id="subject" name="subject">
                        </div>
                        <div class="form-group">
                            <label for="message">Mensagem</label>
                            <textarea id="message" name="message" required></textarea>
                        </div>
                        <button type="submit" class="btn">Enviar Mensagem</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="logo">
                Escola <span>Mataruna</span>
            </div>
            <p>Educação de qualidade há mais de 35 anos</p>
            <div class="social-links">
                <a href="#"><span>Facebook</span></a>
                <a href="#"><span>Instagram</span></a>
                <a href="#"><span>YouTube</span></a>
                <a href="#"><span>LinkedIn</span></a>
            </div>
            <div class="footer-links">
                <a href="#">Política de Privacidade</a>
                <a href="#">Termos de Uso</a>
                <a href="#">Trabalhe Conosco</a>
            </div>
            <p>&copy; 2025 Escola Mataruna. Todos os direitos reservados.</p>
        </div>
    </footer>
</body>
</html>
