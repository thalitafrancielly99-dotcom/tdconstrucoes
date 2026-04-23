<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TD Construções - Depósito de Materiais para Construção</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #2c3e50, #3498db);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #f39c12;
        }

        .whatsapp-btn {
            background: #25D366;
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 25px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .whatsapp-btn:hover {
            background: #128C7E;
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%232c3e50" width="1200" height="600"/><path fill="%233498db" d="M0 300 Q300 100 600 300 T1200 300 V600 H0 Z"/></svg>');
            background-size: cover;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 70px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease 0.2s both;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }

        .btn-primary {
            background: #e74c3c;
            color: white;
        }

        .btn-primary:hover {
            background: #c0392b;
            transform: translateY(-3px);
        }

        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid white;
        }

        .btn-secondary:hover {
            background: white;
            color: #333;
        }

        /* Sections */
        section {
            padding: 5rem 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #2c3e50;
        }

        /* Products */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .product-card {
            background: white;
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }

        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }

        .product-icon {
            font-size: 3rem;
            color: #3498db;
            margin-bottom: 1rem;
        }

        .product-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #2c3e50;
        }

        .price {
            font-size: 1.8rem;
            font-weight: bold;
            color: #27ae60;
            margin: 1rem 0;
        }

        .product-card ul {
            text-align: left;
            margin: 1rem 0;
            padding-left: 1.5rem;
        }

        .product-card li {
            margin: 0.3rem 0;
        }

        /* Payment Methods */
        .payment-methods {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .payment-card {
            background: linear-gradient(135deg, #f8f9fa, #e9ecef);
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            border-left: 5px solid #3498db;
        }

        /* Contact */
        .contact-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .contact-info h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        .contact-info p {
            margin-bottom: 1rem;
            opacity: 0.9;
        }

        .whatsapp-large {
            display: block;
            background: #25D366;
            color: white;
            padding: 1.5rem 3rem;
            border-radius: 50px;
            text-decoration: none;
            font-size: 1.2rem;
            font-weight: bold;
            margin-top: 2rem;
            transition: all 0.3s;
        }

        .whatsapp-large:hover {
            background: #128C7E;
            transform: scale(1.05);
        }

        /* Footer */
        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .contact-content {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }
        }

        /* Floating WhatsApp */
        .floating-whatsapp {
            position: fixed;
            width: 60px;
            height: 60px;
            bottom: 40px;
            right: 40px;
            background: #25D366;
            color: white;
            border-radius: 50px;
            text-align: center;
            font-size: 30px;
            box-shadow: 2px 2px 3px #999;
            z-index: 100;
            animation: bounce 2s infinite;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-10px);
            }
            60% {
                transform: translateY(-5px);
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">
                <i class="fas fa-hammer"></i> TD Construções
            </div>
            <ul class="nav-links">
                <li><a href="#home">Início</a></li>
                <li><a href="#produtos">Produtos</a></li>
                <li><a href="#pagamentos">Pagamentos</a></li>
                <li><a href="#contato">Contato</a></li>
            </ul>
            <a href="https://wa.me/5511999999999" class="whatsapp-btn" target="_blank">
                <i class="fab fa-whatsapp"></i> WhatsApp
            </a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>TD Construções</h1>
            <p>O melhor depósito de materiais para construção da região!<br>Materiais de qualidade com o melhor preço.</p>
            <div class="cta-buttons">
                <a href="#produtos" class="btn btn-primary">
                    <i class="fas fa-shopping-cart"></i> Ver Produtos
                </a>
                <a href="https://wa.me/5511999999999" class="btn btn-secondary" target="_blank">
                    <i class="fab fa-whatsapp"></i> Fazer Orçamento
                </a>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section id="produtos" class="container">
        <h2>Nossos Produtos</h2>
        <div class="products-grid">
            <div class="product-card">
                <div class="product-icon">
                    <i class="fas fa-cube"></i>
                </div>
                <h3>Cimento</h3>
                <div class="price">R$ 28,90</div>
                <p>Saco 50kg - Todas as marcas</p>
                <ul>
                    <li>Votorantim</li>
                    <li>CSN</li>
                    <li>InterCement</li>
                </ul>
                <a href="https://wa.me/5511999999999?text=Olá! Gostaria de um orçamento para Cimento." class="whatsapp-btn" style="margin-top: 1rem;" target="_blank">
                    <i class="fab fa-whatsapp"></i> Pedir Orçamento
                </a>
            </div>

            <div class="product-card">
                <div class="product-icon">
                    <i class="fas fa-brick"></i>
                </div>
                <h3>Tijolo Baiano</h3>
                <div class="price">R$ 0,85</div>
                <p>Unidade - Cerâmico ecológico</p>
                <ul>
                    <li>9 furos</li>
                    <li>Alta durabilidade</li>
                    <li>Entrega rápida</li>
                </ul>
                <a href="https://wa.me/5511999999999?text=Olá! Gostaria de um orçamento para Tijolo Baiano." class="whatsapp-btn" style="margin-top: 1rem;" target="_blank">
                    <i class="fab fa-whatsapp"></i> Pedir Orçamento
                </a>
            </div>

            <div class="product-card">
                <div class="product-icon">
                    <i class="fas fa-hard-hat"></i>
                </div>
                <h3>Areia e Brita</h3>
                <div class="price">R$ 85,00</div>
                <p>M³ - Lavada e peneirada</p>
                <ul>
                    <li>Areia média</li>
                    <li>Brita 0, 1 e 2</li>
                    <li>Pedra tosca</li>
                </ul>
                <a href="https://wa.me/5511999999999?text=Olá! Gostaria de um orçamento para Areia e Brita." class="whatsapp-btn" style="margin-top: 1rem;" target="_blank">
                    <i class="fab fa-whatsapp"></i> Pedir Orçamento
                </a>
            </div>

            <div class="product-card">
                <div class="product-icon">
                    <i class="fas fa-paint-roller"></i>
                </div>
                <h3>Tintas e Ferragens</h3>
                <div class="price">A partir de R$ 89,90</div>
                <p>Variedade completa</p>
                <ul>
                    <li>Suvinil, Coral, Sherwin</li>
                    <li>Parafusos e brocas</li>
                    <li>Ferramentas elétricas</li>
                </ul>
                <a href="https://wa.me/5511999999999?text=Olá! Gostaria de um orçamento para Tintas e Ferragens." class="whatsapp-btn" style="margin-top: 1rem;" target="_blank">
                    <i class="fab fa-whatsapp"></i> Pedir Orçamento
                </a>
            </div>

            <div class="product-card">
                <div class="product-icon">
                    <i class="fas fa-tools"></i>
                </div>
                <h3>Elétrica e Hidráulica</h3>
                <div class="price">A partir de R$ 12,90</div>
                <p>Materiais elétricos e hidráulicos</p>
                <ul>
                    <li>Fios e cabos</li>
                    <li>Disjuntores</li>
                    <li>Torneiras e registros</li>
                </ul>
                <a href="https://wa.me/5511999999999?text=Olá! Gostaria de um orçamento para Elétrica e Hidráulica." class="whatsapp-btn" style="margin-top: 1rem;" target="_blank">
                    <i class="fab fa-whatsapp"></i> Pedir Orçamento
                </a>
            </div>

            <div class="product-card">
                <div class="product-icon">
                    <i class="fas fa-truck"></i>
                </div>
                <h3>Entrega</h3>
                <div class="price">Grátis acima de R$ 500</div>
                <p>Entrega em toda região</p>
                <ul>
                    <li>Carroceria baú</li>
                    <li>Entrega no mesmo dia*</li>
                    <li>Orçamento sem compromisso</li>
                </ul>
                <a href="https://wa.me/5511999999999?text=Olá! Gostaria de saber sobre entrega." class="whatsapp-btn" style="margin-top: 1rem;" target="_blank">
                    <i class="fab fa-whatsapp"></i> Consultar Entrega
                </a>
            </div>
        </div>
    </section>

    <!-- Payment Methods -->
    <section id="pagamentos">
        <div class="container">
            <h2>Formas de Pagamento</h2>
            <div class="payment-methods">
                <div class="payment-card">
                    <i class="fas fa-credit-card" style="font-size: 3rem; color: #3498db; margin-bottom: 1rem;"></i>
                    <h3>Cartão</h3>
                    <p>Parcelamos em até 10x sem juros</p>
                    <ul style="text-align: left; margin-top: 1rem;">
                        <li>Visa, Mastercard</li>
                        <li>Débito imediato</li>
                        <li>Crédito parcelado</li>
                    </ul>
                </div>
                <div class="payment-card">
                    <i class="fas fa-money-bill-wave" style="font-size: 3rem; color: #27ae60; margin-bottom: 1rem;"></i>
                    <h3>Dinheiro</h3>
                    <p>5% de desconto à vista</p>
                    <ul style="text-align: left; margin-top: 1rem;">
                        <li>Dinheiro</li>
                        <li>PIX imediato</li>
                        <li>TED/DOC</li>
                    </ul>
                </div>
                <div class="payment-card">
                    <i class="fas fa-receipt" style="font-size: 3rem; color: #f39c12; margin-bottom: 1rem;"></i>
                    <h3>Crediário</h3>
                    <p>Para clientes cadastrados</p>
                    <ul style="text-align: left; margin-top: 1rem;">
                        <li>Pagamento em 30 dias</li>
                        <li>Consulta SPC/Serasa</li>
                        <li>Contrato assinado</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contato" class="contact-section">
        <div class="
