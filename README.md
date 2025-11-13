# victorfuentes08.github.io
Mi tienda de electrónica y ropa
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TechStyle Store - Electrónica y Moda de Marca</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }

        /* Header Moderno */
        header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .logo {
            font-size: 2rem;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
            padding: 0.5rem 1rem;
            border-radius: 25px;
        }

        .nav-links a:hover {
            background: rgba(255,255,255,0.2);
            transform: translateY(-2px);
        }

        .search-bar {
            display: flex;
            align-items: center;
            background: rgba(255,255,255,0.2);
            border-radius: 25px;
            padding: 0.5rem 1rem;
            backdrop-filter: blur(10px);
        }

        .search-bar input {
            border: none;
            outline: none;
            background: transparent;
            color: white;
            padding: 0.5rem;
            width: 200px;
        }

        .search-bar input::placeholder {
            color: rgba(255,255,255,0.7);
        }

        .cart-icon {
            position: relative;
            cursor: pointer;
            font-size: 1.5rem;
        }

        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: #ff4757;
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            font-weight: bold;
        }

        /* Hero Section */
        .hero {
            margin-top: 80px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 4rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="25" cy="25" r="1" fill="white" opacity="0.1"/><circle cx="75" cy="75" r="1" fill="white" opacity="0.1"/><circle cx="50" cy="10" r="0.5" fill="white" opacity="0.1"/><circle cx="10" cy="60" r="0.5" fill="white" opacity="0.1"/><circle cx="90" cy="40" r="0.5" fill="white" opacity="0.1"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.2s both;
        }

        .cta-button {
            display: inline-block;
            padding: 1rem 2rem;
            background: white;
            color: #667eea;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: all 0.3s ease;
            animation: fadeInUp 1s ease 0.4s both;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        /* Categorías */
        .categories {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 2px;
        }

        .category-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 4rem;
        }

        .category-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .category-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .category-image {
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            color: white;
        }

        .category-info {
            padding: 1.5rem;
        }

        .category-info h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: #333;
        }

        .category-info p {
            color: #666;
            margin-bottom: 1rem;
        }

        .category-link {
            color: #667eea;
            text-decoration: none;
            font-weight: bold;
            display: inline-flex;
            align-items: center;
            gap: 5px;
            transition: gap 0.3s ease;
        }

        .category-link:hover {
            gap: 10px;
        }

        /* Productos */
        .products {
            padding: 4rem 2rem;
            background: white;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .product-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            position: relative;
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .product-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background: #ff4757;
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
            z-index: 2;
        }

        .product-image {
            height: 250px;
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 5rem;
            color: white;
            position: relative;
            overflow: hidden;
        }

        .product-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="dots" width="20" height="20" patternUnits="userSpaceOnUse"><circle cx="10" cy="10" r="2" fill="white" opacity="0.1"/></pattern></defs><rect width="100" height="100" fill="url(%23dots)"/></svg>');
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-title {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: #333;
        }

        .product-description {
            color: #666;
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }

        .product-price {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .price-current {
            font-size: 1.5rem;
            font-weight: bold;
            color: #667eea;
        }

        .price-original {
            text-decoration: line-through;
            color: #999;
            font-size: 1.1rem;
        }

        .product-rating {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }

        .stars {
            color: #ffd700;
        }

        .add-to-cart {
            width: 100%;
            padding: 0.8rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 25px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .add-to-cart:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        /* Características */
        .features {
            padding: 4rem 2rem;
            background: #f8f9fa;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .feature-card {
            text-align: center;
            padding: 2rem;
            background: white;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-5px);
        }

        .feature-icon {
            font-size: 3rem;
            color: #667eea;
            margin-bottom: 1rem;
        }

        .feature-title {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: #333;
        }

        .feature-description {
            color: #666;
        }

        /* Footer */
        footer {
            background: #2c3e50;
            color: white;
            padding: 3rem 2rem 1rem;
            margin-top: 4rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            margin-bottom: 1rem;
            color: #667eea;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 0.5rem;
        }

        .footer-section ul li a {
            color: #bdc3c7;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section ul li a:hover {
            color: white;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid #34495e;
            color: #bdc3c7;
        }

        /* Modal del carrito */
        .cart-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            z-index: 2000;
            backdrop-filter: blur(5px);
        }

        .cart-content {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: white;
            border-radius: 20px;
            padding: 2rem;
            max-width: 500px;
            width: 90%;
            max-height: 80vh;
            overflow-y: auto;
        }

        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
            padding-bottom: 1rem;
            border-bottom: 2px solid #eee;
        }

        .close-cart {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #999;
        }

        .cart-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1rem 0;
            border-bottom: 1px solid #eee;
        }

        .cart-item-image {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
        }

        .cart-item-info {
            flex: 1;
        }

        .cart-item-title {
            font-weight: bold;
            margin-bottom: 0.3rem;
        }

        .cart-item-price {
            color: #667eea;
            font-weight: bold;
        }

        .cart-total {
            text-align: right;
            margin-top: 1rem;
            font-size: 1.3rem;
            font-weight: bold;
            color: #333;
        }

        .checkout-btn {
            width: 100%;
            padding: 1rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 25px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            margin-top: 1rem;
            transition: all 0.3s ease;
        }

        .checkout-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        /* Animaciones */
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
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .search-bar {
                display: none;
            }
            
            .product-grid,
            .category-grid,
            .features-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Notificación de agregado al carrito */
        .notification {
            position: fixed;
            top: 100px;
            right: 20px;
            background: #4CAF50;
            color: white;
            padding: 1rem 1.5rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transform: translateX(400px);
            transition: transform 0.3s ease;
            z-index: 3000;
        }

        .notification.show {
            transform: translateX(0);
        }
    </style>
<base target="_blank">
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">
                <i class="fas fa-store"></i>
                TechStyle
            </div>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#electronica">Electrónica</a></li>
                <li><a href="#ropa">Ropa</a></li>
                <li><a href="#ofertas">Ofertas</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
            <div class="search-bar">
                <input type="text" placeholder="Buscar productos..." id="searchInput">
                <i class="fas fa-search"></i>
            </div>
            <div class="cart-icon" onclick="toggleCart()">
                <i class="fas fa-shopping-cart"></i>
                <span class="cart-count" id="cartCount">0</span>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="hero-content">
            <h1>Bienvenido a TechStyle</h1>
            <p>Descubre la mejor selección de electrónica y ropa de marca con precios increíbles</p>
            <a href="#productos" class="cta-button">Ver Productos</a>
        </div>
    </section>

    <!-- Categorías -->
    <section class="categories">
        <h2 class="section-title">Categorías Populares</h2>
        <div class="category-grid">
            <div class="category-card" onclick="filterProducts('electronica')">
                <div class="category-image">
                    <i class="fas fa-headphones"></i>
                </div>
                <div class="category-info">
                    <h3>Electrónica</h3>
                    <p>AirPods, smartphones, accesorios tecnológicos de última generación</p>
                    <a href="#" class="category-link">Ver más <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
            <div class="category-card" onclick="filterProducts('ropa')">
                <div class="category-image">
                    <i class="fas fa-tshirt"></i>
                </div>
                <div class="category-info">
                    <h3>Ropa de Marca</h3>
                    <p>Ropa de diseñador, moda urbana, estilos exclusivos</p>
                    <a href="#" class="category-link">Ver más <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
            <div class="category-card" onclick="filterProducts('accesorios')">
                <div class="category-image">
                    <i class="fas fa-gem"></i>
                </div>
                <div class="category-info">
                    <h3>Accesorios</h3>
                    <p>Relojes inteligentes, joyería, bolsos de lujo</p>
                    <a href="#" class="category-link">Ver más <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
            <div class="category-card" onclick="filterProducts('ofertas')">
                <div class="category-image">
                    <i class="fas fa-tag"></i>
                </div>
                <div class="category-info">
                    <h3>Ofertas Especiales</h3>
                    <p>Descuentos exclusivos, promociones por tiempo limitado</p>
                    <a href="#" class="category-link">Ver más <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
        </div>
    </section>

    <!-- Productos -->
    <section class="products" id="productos">
        <h2 class="section-title">Productos Destacados</h2>
        <div class="product-grid" id="productGrid">
            <!-- AirPods Pro -->
            <div class="product-card" data-category="electronica">
                <div class="product-badge">-20%</div>
                <div class="product-image">
                    <i class="fas fa-headphones"></i>
                </div>
                <div class="product-info">
                    <h3 class="product-title">AirPods Pro 2ª Generación</h3>
                    <p class="product-description">Cancelación de ruido activa, audio espacial, estuche de carga MagSafe</p>
                    <div class="product-price">
                        <span class="price-current">$199</span>
                        <span class="price-original">$249</span>
                    </div>
                    <div class="product-rating">
                        <span class="stars">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star-half-alt"></i>
                        </span>
                        <span>(4.5)</span>
                    </div>
                    <button class="add-to-cart" onclick="addToCart('AirPods Pro 2ª Gen', 199, 'fas fa-headphones')">
                        <i class="fas fa-cart-plus"></i> Agregar al Carrito
                    </button>
                </div>
            </div>

            <!-- iPhone 15 -->
            <div class="product-card" data-category="electronica">
                <div class="product-badge">Nuevo</div>
                <div class="product-image">
                    <i class="fas fa-mobile-alt"></i>
                </div>
                <div class="product-info">
                    <h3 class="product-title">iPhone 15 Pro Max</h3>
                    <p class="product-description">Chip A17 Pro, cámara de 48MP, titanio natural</p>
                    <div class="product-price">
                        <span class="price-current">$1,199</span>
                    </div>
                    <div class="product-rating">
                        <span class="stars">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </span>
                        <span>(5.0)</span>
                    </div>
                    <button class="add-to-cart" onclick="addToCart('iPhone 15 Pro Max', 1199, 'fas fa-mobile-alt')">
                        <i class="fas fa-cart-plus"></i> Agregar al Carrito
                    </button>
                </div>
            </div>

            <!-- Chaqueta Nike -->
            <div class="product-card" data-category="ropa">
                <div class="product-image">
                    <i class="fas fa-tshirt"></i>
                </div>
                <div class="product-info">
                    <h3 class="product-title">Chaqueta Nike Air Jordan</h3>
                    <p class="product-description">Edición limitada, diseño urbano, materiales premium</p>
                    <div class="product-price">
                        <span class="price-current">$179</span>
                    </div>
                    <div class="product-rating">
                        <span class="stars">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="far fa-star"></i>
                        </span>
                        <span>(4.0)</span>
                    </div>
                    <button class="add-to-cart" onclick="addToCart('Chaqueta Nike Air Jordan', 179, 'fas fa-tshirt')">
                        <i class="fas fa-cart-plus"></i> Agregar al Carrito
                    </button>
                </div>
            </div>

            <!-- Apple Watch -->
            <div class="product-card" data-category="accesorios">
                <div class="product-badge">-15%</div>
                <div class="product-image">
                    <i class="fas fa-clock"></i>
                </div>
                <div class="product-info">
                    <h3 class="product-title">Apple Watch Series 9</h3>
                    <p class="product-description">GPS + Cellular, sensor de temperatura, resistente al agua</p>
                    <div class="product-price">
                        <span class="price-current">$379</span>
                        <span class="price-original">$449</span>
                    </div>
                    <div class="product-rating">
                        <span class="stars">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star-half-alt"></i>
                        </span>
                        <span>(4.7)</span>
                    </div>
                    <button class="add-to-cart" onclick="addToCart('Apple Watch Series 9', 379, 'fas fa-clock')">
                        <i class="fas fa-cart-plus"></i> Agregar al Carrito
                    </button>
                </div>
            </div>

            <!-- Zapatillas Adidas -->
            <div class="product-card" data-category="ropa">
                <div class="product-badge">Oferta</div>
                <div class="product-image">
                    <i class="fas fa-shoe-prints"></i>
                </div>
                <div class="product-info">
                    <h3 class="product-title">Zapatillas Adidas Yeezy</h3>
                    <p class="product-description">Edición exclusiva, comodidad premium, estilo urbano</p>
                    <div class="product-price">
                        <span class="price-current">$299</span>
                        <span class="price-original">$399</span>
                    </div>
                    <div class="product-rating">
                        <span class="stars">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </span>
                        <span>(4.8)</span>
                    </div>
                    <button class="add-to-cart" onclick="addToCart('Adidas Yeezy', 299, 'fas fa-shoe-prints')">
                        <i class="fas fa-cart-plus"></i> Agregar al Carrito
                    </button>
                </div>
            </div>

            <!-- MacBook Pro -->
            <div class="product-card" data-category="electronica">
                <div class="product-badge">-10%</div>
                <div class="product-image">
                    <i class="fas fa-laptop"></i>
                </div>
                <div class="product-info">
                    <h3 class="product-title">MacBook Pro 14" M3</h3>
                    <p class="product-description">Chip M3, 16GB RAM, 512GB SSD, pantalla Liquid Retina XDR</p>
                    <div class="product-price">
                        <span class="price-current">$1,799</span>
                        <span class="price-original">$1,999</span>
                    </div>
                    <div class="product-rating">
                        <span class="stars">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star-half-alt"></i>
                        </span>
                        <span>(4.6)</span>
                    </div>
                    <button class="add-to-cart" onclick="addToCart('MacBook Pro 14" M3', 1799, 'fas fa-laptop')">
                        <i class="fas fa-cart-plus"></i> Agregar al Carrito
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Características -->
    <section class="features">
        <h2 class="section-title">Por Qué Elegirnos</h2>
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-shipping-fast"></i>
                </div>
                <h3 class="feature-title">Envío Gratis</h3>
                <p class="feature-description">Envío gratuito en todos los pedidos superiores a $50</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-shield-alt"></i>
                </div>
                <h3 class="feature-title">Pago Seguro</h3>
                <p class="feature-description">Pagos 100% seguros con encriptación SSL</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-undo"></i>
                </div>
                <h3 class="feature-title">Devoluciones Fáciles</h3>
                <p class="feature-description">30 días para devoluciones sin complicaciones</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-headset"></i>
                </div>
                <h3 class="feature-title">Soporte 24/7</h3>
                <p class="feature-description">Atención al cliente disponible todo el día</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contacto">
        <div class="footer-content">
            <div class="footer-section">
                <h3>TechStyle Store</h3>
                <p>Tu tienda de confianza para electrónica y moda de marca. Ofrecemos los mejores productos con garantía de calidad.</p>
                <div style="margin-top: 1rem;">
                    <i class="fab fa-facebook" style="font-size: 1.5rem; margin-right: 1rem; cursor: pointer;"></i>
                    <i class="fab fa-twitter" style="font-size: 1.5rem; margin-right: 1rem; cursor: pointer;"></i>
                    <i class="fab fa-instagram" style="font-size: 1.5rem; cursor: pointer;"></i>
                </div>
            </div>
            <div class="footer-section">
                <h3>Enlaces Rápidos</h3>
                <ul>
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#electronica">Electrónica</a></li>
                    <li><a href="#ropa">Ropa</a></li>
                    <li><a href="#ofertas">Ofertas</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Atención al Cliente</h3>
                <ul>
                    <li><a href="#">Preguntas Frecuentes</a></li>
                    <li><a href="#">Política de Devoluciones</a></li>
                    <li><a href="#">Envíos y Entregas</a></li>
                    <li><a href="#">Términos y Condiciones</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Contacto</h3>
                <ul>
                    <li><i class="fas fa-phone"></i> +1 (555) 123-4567</li>
                    <li><i class="fas fa-envelope"></i> info@techstyle.com</li>
                    <li><i class="fas fa-map-marker-alt"></i> 123 Calle Principal, Ciudad</li>
                    <li><i class="fas fa-clock"></i> Lunes - Domingo: 9:00 - 21:00</li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2024 TechStyle Store. Todos los derechos reservados.</p>
        </div>
    </footer>

    <!-- Modal del Carrito -->
    <div class="cart-modal" id="cartModal">
        <div class="cart-content">
            <div class="cart-header">
                <h2>Carrito de Compras</h2>
                <button class="close-cart" onclick="toggleCart()">
                    <i class="fas fa-times"></i>
                </button>
            </div>
            <div id="cartItems"></div>
            <div class="cart-total" id="cartTotal">Total: $0</div>
            <button class="checkout-btn" onclick="checkout()">
                <i class="fas fa-credit-card"></i> Proceder al Pago
            </button>
        </div>
    </div>

    <!-- Notificación -->
    <div class="notification" id="notification"></div>

    <script>
        // Carrito de compras
        let cart = [];
        let cartCount = 0;

        // Función para agregar productos al carrito
        function addToCart(name, price, icon) {
            const existingItem = cart.find(item => item.name === name);
            
            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push({
                    name: name,
                    price: price,
                    icon: icon,
                    quantity: 1
                });
            }
            
            updateCartCount();
            showNotification(`${name} agregado al carrito`);
            
            // Animación del botón
            const button = event.target;
            button.innerHTML = '<i class="fas fa-check"></i> ¡Agregado!';
            button.style.background = '#4CAF50';
            
            setTimeout(() => {
                button.innerHTML = '<i class="fas fa-cart-plus"></i> Agregar al Carrito';
                button.style.background = '';
            }, 2000);
        }

        // Actualizar contador del carrito
        function updateCartCount() {
            cartCount = cart.reduce((total, item) => total + item.quantity, 0);
            document.getElementById('cartCount').textContent = cartCount;
        }

        // Mostrar/ocultar carrito
        function toggleCart() {
            const modal = document.getElementById('cartModal');
            if (modal.style.display === 'block') {
                modal.style.display = 'none';
            } else {
                modal.style.display = 'block';
                renderCart();
            }
        }

        // Renderizar carrito
        function renderCart() {
            const cartItems = document.getElementById('cartItems');
            const cartTotal = document.getElementById('cartTotal');
            
            if (cart.length === 0) {
                cartItems.innerHTML = '<p style="text-align: center; color: #999; padding: 2rem;">Tu carrito está vacío</p>';
                cartTotal.textContent = 'Total: $0';
                return;
            }
            
            let html = '';
            let total = 0;
            
            cart.forEach(item => {
                const itemTotal = item.price * item.quantity;
                total += itemTotal;
                
                html += `
                    <div class="cart-item">
                        <div class="cart-item-image">
                            <i class="${item.icon}"></i>
                        </div>
                        <div class="cart-item-info">
                            <div class="cart-item-title">${item.name}</div>
                            <div class="cart-item-price">$${item.price} x ${item.quantity}</div>
                        </div>
                        <div style="display: flex; align-items: center; gap: 0.5rem;">
                            <button onclick="updateQuantity('${item.name}', -1)" style="background: #ff4757; color: white; border: none; border-radius: 50%; width: 25px; height: 25px; cursor: pointer;">-</button>
                            <span>${item.quantity}</span>
                            <button onclick="updateQuantity('${item.name}', 1)" style="background: #2ed573; color: white; border: none; border-radius: 50%; width: 25px; height: 25px; cursor: pointer;">+</button>
                        </div>
                    </div>
                `;
            });
            
            cartItems.innerHTML = html;
            cartTotal.textContent = `Total: $${total.toFixed(2)}`;
        }

        // Actualizar cantidad
        function updateQuantity(name, change) {
            const item = cart.find(item => item.name === name);
            if (item) {
                item.quantity += change;
                if (item.quantity <= 0) {
                    cart = cart.filter(item => item.name !== name);
                }
                updateCartCount();
                renderCart();
            }
        }

        // Checkout
        function checkout() {
            if (cart.length === 0) {
                showNotification('Tu carrito está vacío', 'error');
                return;
            }
            
            showNotification('¡Gracias por tu compra! Serás redirigido al pago...');
            setTimeout(() => {
                cart = [];
                updateCartCount();
                toggleCart();
            }, 2000);
        }

        // Mostrar notificación
        function showNotification(message, type = 'success') {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            notification.className = 'notification show';
            
            if (type === 'error') {
                notification.style.background = '#ff4757';
            } else {
                notification.style.background = '#4CAF50';
            }
            
            setTimeout(() => {
                notification.classList.remove('show');
            }, 3000);
        }

        // Filtrar productos
        function filterProducts(category) {
            const products = document.querySelectorAll('.product-card');
            
            products.forEach(product => {
                if (category === 'ofertas') {
                    const badge = product.querySelector('.product-badge');
                    if (badge && badge.textContent.includes('%')) {
                        product.style.display = 'block';
                    } else {
                        product.style.display = 'none';
                    }
                } else {
                    const productCategory = product.getAttribute('data-category');
                    if (productCategory === category) {
                        product.style.display = 'block';
                    } else {
                        product.style.display = 'none';
                    }
                }
            });
            
            // Scroll a productos
            document.getElementById('productos').scrollIntoView({ behavior: 'smooth' });
        }

        // Búsqueda de productos
        document.getElementById('searchInput').addEventListener('input', function(e) {
            const searchTerm = e.target.value.toLowerCase();
            const products = document.querySelectorAll('.product-card');
            
            products.forEach(product => {
                const title = product.querySelector('.product-title').textContent.toLowerCase();
                const description = product.querySelector('.product-description').textContent.toLowerCase();
                
                if (title.includes(searchTerm) || description.includes(searchTerm)) {
                    product.style.display = 'block';
                } else {
                    product.style.display = 'none';
                }
            });
        });

        // Cerrar carrito al hacer clic fuera
        window.onclick = function(event) {
            const modal = document.getElementById('cartModal');
            if (event.target === modal) {
                modal.style.display = 'none';
            }
        }

        // Animaciones al hacer scroll
        window.addEventListener('scroll', function() {
            const elements = document.querySelectorAll('.product-card, .category-card, .feature-card');
            
            elements.forEach(element => {
                const elementTop = element.getBoundingClientRect().top;
                const elementVisible = 150;
                
                if (elementTop < window.innerHeight - elementVisible) {
                    element.style.opacity = '1';
                    element.style.transform = 'translateY(0)';
                }
            });
        });

        // Inicializar animaciones
        document.addEventListener('DOMContentLoaded', function() {
            const elements = document.querySelectorAll('.product-card, .category-card, .feature-card');
            elements.forEach(element => {
                element.style.opacity = '0';
                element.style.transform = 'translateY(20px)';
                element.style.transition = 'all 0.6s ease';
            });
        });

        // Mostrar todos los productos
        function showAllProducts() {
            const products = document.querySelectorAll('.product-card');
            products.forEach(product => {
                product.style.display = 'block';
            });
        }
    </script>
</body>
</html>
