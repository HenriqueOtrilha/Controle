<!DOCTYPE html>

<html lang="pt-BR">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Produtos - Eagle Agribusiness Holding</title>

    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">

    <style>

        :root {

            --dark-green: #1A5D1A;

            --gold: #D4AF37;

            --navy-blue: #003366;

            --light-gray: #f5f5f5;

            --white: #ffffff;

            --dark-gray: #333333;

        }

        

        * {

            margin: 0;

            padding: 0;

            box-sizing: border-box;

        }

        

        body {

            font-family: 'Open Sans', sans-serif;

            color: var(--dark-gray);

            line-height: 1.6;

        }

        

        h1, h2, h3, h4 {

            font-family: 'Montserrat', sans-serif;

            font-weight: 700;

            color: var(--dark-green);

        }

        

        .container {

            width: 100%;

            max-width: 1200px;

            margin: 0 auto;

            padding: 0 20px;

        }

        

        /* Header Styles */

        header {

            background-color: var(--white);

            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);

            position: fixed;

            width: 100%;

            top: 0;

            z-index: 1000;

        }

        

        .header-container {

            display: flex;

            justify-content: space-between;

            align-items: center;

            padding: 15px 0;

        }

        

        .logo {

            display: flex;

            align-items: center;

        }

        

        .logo img {

            height: 50px;

        }

        

        .logo-text {

            margin-left: 10px;

        }

        

        .logo-text h1 {

            font-size: 1.5rem;

            margin-bottom: 0;

        }

        

        .logo-text p {

            font-size: 0.8rem;

            color: var(--dark-gray);

            margin-top: -5px;

        }

        

        nav ul {

            display: flex;

            list-style: none;

        }

        

        nav ul li {

            margin-left: 30px;

        }

        

        nav ul li a {

            text-decoration: none;

            color: var(--dark-gray);

            font-weight: 600;

            transition: color 0.3s;

        }

        

        nav ul li a:hover {

            color: var(--dark-green);

        }

        

        .search-quote {

            display: flex;

            align-items: center;

        }

        

        .search-box {

            position: relative;

            margin-right: 20px;

        }

        

        .search-box input {

            padding: 8px 15px 8px 35px;

            border: 1px solid #ddd;

            border-radius: 20px;

            outline: none;

        }

        

        .search-box i {

            position: absolute;

            left: 10px;

            top: 50%;

            transform: translateY(-50%);

            color: #777;

        }

        

        .quote-btn {

            background-color: var(--gold);

            color: var(--white);

            border: none;

            padding: 10px 20px;

            border-radius: 5px;

            font-weight: 600;

            cursor: pointer;

            transition: background-color 0.3s;

        }

        

        .quote-btn:hover {

            background-color: #c19d2e;

        }

        

        /* Hero Section */

        .hero {

            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://images.unsplash.com/photo-1500382017468-9049fed747ef?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');

            background-size: cover;

            background-position: center;

            color: var(--white);

            text-align: center;

            padding: 150px 20px 100px;

            margin-top: 80px;

        }

        

        .hero h2 {

            font-size: 2.5rem;

            color: var(--white);

            margin-bottom: 20px;

        }

        

        .hero p {

            font-size: 1.2rem;

            max-width: 700px;

            margin: 0 auto 30px;

        }

        

        .hero-btn {

            background-color: var(--gold);

            color: var(--white);

            border: none;

            padding: 12px 30px;

            border-radius: 5px;

            font-size: 1.1rem;

            font-weight: 600;

            cursor: pointer;

            transition: all 0.3s;

        }

        

        .hero-btn:hover {

            background-color: #c19d2e;

            transform: translateY(-2px);

        }

        

        /* Categories Filter */

        .categories {

            padding: 50px 0;

            background-color: var(--light-gray);

        }

        

        .section-title {

            text-align: center;

            margin-bottom: 40px;

        }

        

        .section-title h2 {

            font-size: 2rem;

            position: relative;

            display: inline-block;

            padding-bottom: 10px;

        }

        

        .section-title h2::after {

            content: '';

            position: absolute;

            bottom: 0;

            left: 50%;

            transform: translateX(-50%);

            width: 80px;

            height: 3px;

            background-color: var(--gold);

        }

        

        .category-filters {

            display: flex;

            justify-content: center;

            flex-wrap: wrap;

            gap: 15px;

            margin-bottom: 30px;

        }

        

        .filter-btn {

            background-color: var(--white);

            border: 1px solid #ddd;

            padding: 10px 20px;

            border-radius: 30px;

            cursor: pointer;

            transition: all 0.3s;

        }

        

        .filter-btn:hover, .filter-btn.active {

            background-color: var(--dark-green);

            color: var(--white);

            border-color: var(--dark-green);

        }

        

        /* Products Grid */

        .products-grid {

            display: grid;

            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));

            gap: 30px;

            padding: 0 20px;

        }

        

        .product-card {

            background-color: var(--white);

            border-radius: 8px;

            overflow: hidden;

            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);

            transition: transform 0.3s, box-shadow 0.3s;

        }

        

        .product-card:hover {

            transform: translateY(-10px);

            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);

        }

        

        .product-img {

            height: 200px;

            overflow: hidden;

        }

        

        .product-img img {

            width: 100%;

            height: 100%;

            object-fit: cover;

            transition: transform 0.5s;

        }

        

        .product-card:hover .product-img img {

            transform: scale(1.1);

        }

        

        .product-info {

            padding: 20px;

        }

        

        .product-info h3 {

            margin-bottom: 10px;

            font-size: 1.3rem;

        }

        

        .product-info p {

            color: #666;

            margin-bottom: 15px;

            font-size: 0.9rem;

        }

        

        .details-btn {

            display: inline-block;

            background-color: var(--dark-green);

            color: var(--white);

            padding: 8px 20px;

            border-radius: 5px;

            text-decoration: none;

            font-weight: 600;

            transition: background-color 0.3s;

        }

        

        .details-btn:hover {

            background-color: #124012;

        }

        

        /* Advantages Section */

        .advantages {

            padding: 70px 0;

            background-color: var(--navy-blue);

            color: var(--white);

        }

        

        .advantages .section-title h2 {

            color: var(--white);

        }

        

        .advantages-grid {

            display: grid;

            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));

            gap: 30px;

            margin-top: 40px;

        }

        

        .advantage-card {

            text-align: center;

            padding: 30px 20px;

            background-color: rgba(255, 255, 255, 0.1);

            border-radius: 8px;

            transition: transform 0.3s;

        }

        

        .advantage-card:hover {

            transform: translateY(-5px);

        }

        

        .advantage-icon {

            font-size: 2.5rem;

            color: var(--gold);

            margin-bottom: 20px;

        }

        

        .advantage-card h3 {

            color: var(--white);

            margin-bottom: 15px;

        }

        

        /* Contact Form */

        .contact-section {

            padding: 70px 0;

            background-color: var(--light-gray);

        }

        

        .contact-container {

            max-width: 800px;

            margin: 0 auto;

            background-color: var(--white);

            padding: 40px;

            border-radius: 8px;

            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);

        }

        

        .contact-title {

            text-align: center;

            margin-bottom: 30px;

        }

        

        .contact-title h2 {

            font-size: 2rem;

            margin-bottom: 10px;

        }

        

        .contact-title p {

            color: #666;

        }

        

        .contact-form {

            display: grid;

            grid-template-columns: 1fr 1fr;

            gap: 20px;

        }

        

        .form-group {

            margin-bottom: 20px;

        }

        

        .form-group.full-width {

            grid-column: span 2;

        }

        

        .form-group label {

            display: block;

            margin-bottom: 8px;

            font-weight: 600;

        }

        

        .form-group input,

        .form-group select,

        .form-group textarea {

            width: 100%;

            padding: 12px 15px;

            border: 1px solid #ddd;

            border-radius: 5px;

            font-family: 'Open Sans', sans-serif;

        }

        

        .form-group textarea {

            min-height: 120px;

            resize: vertical;

        }

        

        .submit-btn {

            grid-column: span 2;

            background-color: var(--gold);

            color: var(--white);

            border: none;

            padding: 15px;

            border-radius: 5px;

            font-size: 1.1rem;

            font-weight: 600;

            cursor: pointer;

            transition: background-color 0.3s;

        }

        

        .submit-btn:hover {

            background-color: #c19d2e;

        }

        

        /* Partners Section */

        .partners {

            padding: 50px 0;

            text-align: center;

        }

        

        .partners-logos {

            display: flex;

            justify-content: center;

            flex-wrap: wrap;

            gap: 40px;

            margin-top: 30px;

        }

        

        .partner-logo {

            height: 60px;

            filter: grayscale(100%);

            opacity: 0.7;

            transition: all 0.3s;

        }

        

        .partner-logo:hover {

            filter: grayscale(0);

            opacity: 1;

        }

        

        /* Footer */

        footer {

            background-color: var(--dark-gray);

            color: var(--white);

            padding: 60px 0 20px;

        }

        

        .footer-container {

            display: grid;

            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));

            gap: 40px;

            margin-bottom: 40px;

        }

        

        .footer-logo {

            margin-bottom: 20px;

        }

        

        .footer-logo img {

            height: 50px;

        }

        

        .footer-about p {

            margin-bottom: 20px;

            color: #bbb;

        }

        

        .social-links {

            display: flex;

            gap: 15px;

        }

        

        .social-links a {

            color: var(--white);

            font-size: 1.2rem;

            transition: color 0.3s;

        }

        

        .social-links a:hover {

            color: var(--gold);

        }

        

        .footer-links h3, .footer-contact h3 {

            font-size: 1.2rem;

            margin-bottom: 20px;

            color: var(--white);

        }

        

        .footer-links ul {

            list-style: none;

        }

        

        .footer-links ul li {

            margin-bottom: 10px;

        }

        

        .footer-links ul li a {

            color: #bbb;

            text-decoration: none;

            transition: color 0.3s;

        }

        

        .footer-links ul li a:hover {

            color: var(--gold);

        }

        

        .contact-info {

            color: #bbb;

        }

        

        .contact-info p {

            margin-bottom: 15px;

            display: flex;

            align-items: flex-start;

        }

        

        .contact-info i {

            margin-right: 10px;

            color: var(--gold);

        }

        

        .footer-bottom {

            text-align: center;

            padding-top: 20px;

            border-top: 1px solid rgba(255, 255, 255, 0.1);

            color: #bbb;

            font-size: 0.9rem;

        }

        

        .certifications {

            display: flex;

            justify-content: center;

            gap: 20px;

            margin-top: 20px;

        }

        

        .certification {

            height: 40px;

        }

        

        /* Responsive Styles */

        @media (max-width: 992px) {

            .header-container {

                flex-direction: column;

                padding: 15px;

            }

            

            .logo {

                margin-bottom: 15px;

            }

            

            nav ul {

                margin-bottom: 15px;

            }

            

            .hero {

                padding: 120px 20px 80px;

            }

            

            .hero h2 {

                font-size: 2rem;

            }

        }

        

        @media (max-width: 768px) {

            .contact-form {

                grid-template-columns: 1fr;

            }

            

            .form-group.full-width {

                grid-column: span 1;

            }

            

            .submit-btn {

                grid-column: span 1;

            }

            

            .products-grid {

                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));

            }

        }

        

        @media (max-width: 576px) {

            nav ul {

                flex-wrap: wrap;

                justify-content: center;

            }

            

            nav ul li {

                margin: 5px 10px;

            }

            

            .search-quote {

                flex-direction: column;

                width: 100%;

            }

            

            .search-box {

                width: 100%;

                margin-right: 0;

                margin-bottom: 15px;

            }

            

            .search-box input {

                width: 100%;

            }

            

            .quote-btn {

                width: 100%;

            }

            

            .hero {

                padding: 100px 15px 60px;

            }

            

            .hero h2 {

                font-size: 1.8rem;

            }

            

            .hero p {

                font-size: 1rem;

            }

        }

    </style>

</head>

<body>

    <!-- Header -->

    <header>

        <div class="container header-container">

            <div class="logo">

                <img src="https://via.placeholder.com/50x50" alt="Eagle Agribusiness Holding Logo">

                <div class="logo-text">

                    <h1>EAGLE AGRIBUSINESS</h1>

                    <p>Global Commodities Trading</p>

                </div>

            </div>

            

            <nav>

                <ul>

                    <li><a href="#">Home</a></li>

                    <li><a href="#">Sobre Nós</a></li>

                    <li><a href="#" class="active">Produtos</a></li>

                    <li><a href="#">Mercados</a></li>

                    <li><a href="#">Logística</a></li>

                    <li><a href="#">Contato</a></li>

                </ul>

            </nav>

            

            <div class="search-quote">

                <div class="search-box">

                    <i class="fas fa-search"></i>

                    <input type="text" placeholder="Buscar produtos...">

                </div>

                <button class="quote-btn">Solicitar Cotação</button>

            </div>

        </div>

    </header>



    <!-- Hero Section -->

    <section class="hero">

        <div class="container">

            <h2>Exportando Excelência em Commodities Globais</h2>

            <p>Açúcar, Café, Grãos, Proteínas, Minérios e muito mais para o mundo</p>

            <button class="hero-btn">Conheça nossos produtos</button>

        </div>

    </section>



    <!-- Categories Filter -->

    <section class="categories">

        <div class="container">

            <div class="section-title">

                <h2>Nossos Produtos</h2>

            </div>

            

            <div class="category-filters">

                <button class="filter-btn active">Todos</button>

                <button class="filter-btn">Açúcar</button>

                <button class="filter-btn">Grãos</button>

                <button class="filter-btn">Café</button>

                <button class="filter-btn">Proteínas</button>

                <button class="filter-btn">Combustíveis</button>

                <button class="filter-btn">Minérios</button>

                <button class="filter-btn">Óleos</button>

                <button class="filter-btn">Fertilizantes</button>

            </div>

            

            <div class="products-grid">

                <!-- Product 1 -->

                <div class="product-card">

                    <div class="product-img">

                        <img src="https://images.unsplash.com/photo-1607619056574-7b8d3ee536b2?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Açúcar">

                    </div>

                    <div class="product-info">

                        <h3>Açúcar Cristal</h3>

                        <p>Açúcar premium para exportação, grau alimentício, embalagens de 25kg e 50kg.</p>

                        <a href="#" class="details-btn">Ver detalhes</a>

                    </div>

                </div>

                

                <!-- Product 2 -->

                <div class="product-card">

                    <div class="product-img">

                        <img src="https://images.unsplash.com/photo-1511920170033-f8396924c348?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Arroz">

                    </div>

                    <div class="product-info">

                        <h3>Arroz Longo Fino</h3>

                        <p>Grão selecionado, tipo 1, embalado a vácuo para máxima preservação.</p>

                        <a href="#" class="details-btn">Ver detalhes</a>

                    </div>

                </div>

                

                <!-- Product 3 -->

                <div class="product-card">

                    <div class="product-img">

                        <img src="https://images.unsplash.com/photo-1442512595331-e89e73853f31?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Café">

                    </div>

                    <div class="product-info">

                        <h3>Café Arábica</h3>

                        <p>Grãos selecionados, torra média, embalagens de 60kg para exportação.</p>

                        <a href="#" class="details-btn">Ver detalhes</a>

                    </div>

                </div>

                

                <!-- Product 4 -->

                <div class="product-card">

                    <div class="product-img">

                        <img src="https://images.unsplash.com/photo-1550583724-b2692b85b150?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Soja">

                    </div>

                    <div class="product-info">

                        <h3>Soja em Grão</h3>

                        <p>Soja não transgênica, alto teor proteico, embalagem a granel ou sacaria.</p>

                        <a href="#" class="details-btn">Ver detalhes</a>

                    </div>

                </div>

                

                <!-- Product 5 -->

                <div class="product-card">

                    <div class="product-img">

                        <img src="https://images.unsplash.com/photo-1589927986089-35812388d1f4?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Etanol">

                    </div>

                    <div class="product-info">

                        <h3>Etanol Combustível</h3>

                        <p>Etanol anidro e hidratado, atendendo especificações internacionais.</p>

                        <a href="#" class="details-btn">Ver detalhes</a>

                    </div>

                </div>

                

                <!-- Product 6 -->

                <div class="product-card">

                    <div class="product-img">

                        <img src="https://images.unsplash.com/photo-1586771107445-d3ca888129ce?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Minério">

                    </div>

                    <div class="product-info">

                        <h3>Minério de Ferro</h3>

                        <p>Minério de alta qualidade, teor de Fe acima de 65%, em granel.</p>

                        <a href="#" class="details-btn">Ver detalhes</a>

                    </div>

                </div>

            </div>

        </div>

    </section>



    <!-- Advantages Section -->

    <section class="advantages">

        <div class="container">

            <div class="section-title">

                <h2>Por que escolher a Eagle Agribusiness?</h2>

            </div>

            

            <div class="advantages-grid">

                <div class="advantage-card">

                    <div class="advantage-icon">

                        <i class="fas fa-ship"></i>

                    </div>

                    <h3>Logística Integrada</h3>

                    <p>Portos, armazéns e transporte multimodal para garantir entrega eficiente em qualquer destino.</p>

                </div>

                

                <div class="advantage-card">

                    <div class="advantage-icon">

                        <i class="fas fa-certificate"></i>

                    </div>

                    <h3>Certificações Internacionais</h3>

                    <p>ISO, Fair Trade, USDA e outras certificações que garantem qualidade e conformidade.</p>

                </div>

                

                <div class="advantage-card">

                    <div class="advantage-icon">

                        <i class="fas fa-qrcode"></i>

                    </div>

                    <h3>Rastreabilidade Total</h3>

                    <p>Do campo ao cliente final, com transparência em toda a cadeia de suprimentos.</p>

                </div>

                

                <div class="advantage-card">

                    <div class="advantage-icon">

                        <i class="fas fa-headset"></i>

                    </div>

                    <h3>Suporte 24/7</h3>

                    <p>Equipe dedicada para atender compradores internacionais em todos os fusos horários.</p>

                </div>

            </div>

        </div>

    </section>



    <!-- Contact Form -->

    <section class="contact-section">

        <div class="container">

            <div class="contact-container">

                <div class="contact-title">

                    <h2>Interessado em nossos produtos?</h2>

                    <p>Preencha o formulário abaixo e nossa equipe entrará em contato</p>

                </div>

                

                <form class="contact-form">

                    <div class="form-group">

                        <label for="name">Nome</label>

                        <input type="text" id="name" required>

                    </div>

                    

                    <div class="form-group">

                        <label for="email">E-mail</label>

                        <input type="email" id="email" required>

                    </div>

                    

                    <div class="form-group">

                        <label for="phone">Telefone</label>

                        <input type="tel" id="phone">

                    </div>

                    

                    <div class="form-group">

                        <label for="product">Produto de Interesse</label>

                        <select id="product">

                            <option value="">Selecione um produto</option>

                            <option value="sugar">Açúcar</option>

                            <option value="rice">Arroz</option>

                            <option value="coffee">Café</option>

                            <option value="soy">Soja</option>

                            <option value="ethanol">Etanol</option>

                            <option value="minerals">Minérios</option>

                            <option value="other">Outro</option>

                        </select>

                    </div>

                    

                    <div class="form-group full-width">

                        <label for="message">Mensagem</label>

                        <textarea id="message"></textarea>

                    </div>

                    

                    <button type="submit" class="submit-btn">Enviar Solicitação</button>

                </form>

            </div>

        </div>

    </section>



    <!-- Partners Section -->

    <section class="partners">

        <div class="container">

            <div class="section-title">

                <h2>Nossos Parceiros</h2>

            </div>

            

            <div class="partners-logos">

                <img src="https://via.placeholder.com/150x60" alt="Partner 1" class="partner-logo">

                <img src="https://via.placeholder.com/150x60" alt="Partner 2" class="partner-logo">

                <img src="https://via.placeholder.com/150x60" alt="Partner 3" class="partner-logo">

                <img src="https://via.placeholder.com/150x60" alt="Partner 4" class="partner-logo">

                <img src="https://via.placeholder.com/150x60" alt="Partner 5" class="partner-logo">

            </div>

        </div>

    </section>



    <!-- Footer -->

    <footer>

        <div class="container">

            <div class="footer-container">

                <div class="footer-about">

                    <div class="footer-logo">

                        <img src="https://via.placeholder.com/150x50" alt="Eagle Agribusiness Holding Logo">

                    </div>

                    <p>Conectando mercados globais com excelência em commodities desde 2005.</p>

                    <div class="social-links">

                        <a href="#"><i class="fab fa-linkedin"></i></a>

                        <a href="#"><i class="fab fa-twitter"></i></a>

                        <a href="#"><i class="fab fa-facebook"></i></a>

                        <a href="#"><i class="fab fa-instagram"></i></a>

                    </div>

                </div>

                

                <div class="footer-links">

                    <h3>Links Rápidos</h3>

                    <ul>

                        <li><a href="#">Home</a></li>

                        <li><a href="#">Sobre Nós</a></li>

                        <li><a href="#">Produtos</a></li>

                        <li><a href="#">Mercados</a></li>

                        <li><a href="#">Logística</a></li>

                        <li><a href="#">Contato</a></li>

                    </ul>

                </div>

                

                <div class="footer-contact">

                    <h3>Contato</h3>

                    <div class="contact-info">

                        <p><i class="fas fa-map-marker-alt"></i> Av. das Nações, 1000, São Paulo - SP, Brasil</p>

                        <p><i class="fas fa-phone"></i> +55 11 1234-5678</p>

                        <p><i class="fas fa-envelope"></i> contact@eagleagri.com</p>

                        <p><i class="fas fa-clock"></i> Seg-Sex: 8h-18h</p>

                    </div>

                </div>

            </div>

            

            <div class="certifications">

                <img src="https://via.placeholder.com/80x40" alt="Certification 1" class="certification">

                <img src="https://via.placeholder.com/80x40" alt="Certification 2" class="certification">

                <img src="https://via.placeholder.com/80x40" alt="Certification 3" class="certification">

            </div>

            

            <div class="footer-bottom">

                <p>&copy; 2024 Eagle Agribusiness Holding. Todos os direitos reservados.</p>

            </div>

        </div>

    </footer>



    <script>

        // Simple filter functionality for demonstration

        document.querySelectorAll('.filter-btn').forEach(btn => {

            btn.addEventListener('click', function() {

                document.querySelector('.filter-btn.active').classList.remove('active');

                this.classList.add('active');

                

                // In a real implementation, this would filter the products

                console.log(`Filtering by: ${this.textContent}`);

            });

        });

        

        // Form submission

        document.querySelector('.contact-form').addEventListener('submit', function(e) {

            e.preventDefault();

            alert('Obrigado pelo seu interesse! Nossa equipe entrará em contato em breve.');

            this.reset();

        });

    </script>

</body>

</html>

