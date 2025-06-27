<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Polos Básicos Hombre - MBO</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
 body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
        }
        
 .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Header Styles */
  header {
            background-color: #fff;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
 .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
        }
        
 .logo {
            font-size: 28px;
            font-weight: 700;
            color: #d32f2f;
        }
        
 .nav-links {
            display: flex;
            gap: 25px;
        }
        
 .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            position: relative;
        }
        
 .nav-links a:hover {
            color: #d32f2f;
        }
        
 .nav-links a.active::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 100%;
            height: 2px;
            background-color: #d32f2f;
        }
        
 .header-icons {
            display: flex;
            gap: 20px;
        }
        
 .header-icons i {
            font-size: 20px;
            cursor: pointer;
            position: relative;
        }
        
 .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: #d32f2f;
            color: white;
            border-radius: 50%;
            width: 18px;
            height: 18px;
            font-size: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        /* Main Content Styles */
 .main-content {
            display: flex;
            gap: 30px;
            margin-top: 30px;
        }
        
        /* Filters Section */
 .filters {
            width: 250px;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            height: fit-content;
            transition: transform 0.3s ease;
        }
        
 .filter-toggle {
            display: none;
            padding: 10px 15px;
            background: #d32f2f;
            color: white;
            border: none;
            border-radius: 4px;
            margin-bottom: 15px;
            cursor: pointer;
            font-weight: 600;
            width: 100%;
        }
        
 .filter-title {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #eee;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
 .close-filters {
            display: none;
            font-size: 20px;
            cursor: pointer;
        }
        
  .filter-section {
            margin-bottom: 25px;
        }
        
  .filter-section h3 {
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 12px;
            color: #555;
            text-transform: uppercase;
        }
        
  .filter-options {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        
  .filter-option {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
  .filter-option input[type="checkbox"] {
            width: 16px;
            height: 16px;
            cursor: pointer;
        }
        
  .filter-option label {
            font-size: 14px;
            cursor: pointer;
            flex: 1;
        }
        
  .price-range {
            display: flex;
            justify-content: space-between;
            margin-top: 10px;
        }
        
 .price-range span {
            font-size: 13px;
            color: #777;
        }
        
        /* Products Section */
  .products-section {
            flex: 1;
        }
        
 .products-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            background: #fff;
            padding: 15px 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            flex-wrap: wrap;
            gap: 15px;
        }
        
  .products-count {
            font-size: 14px;
            color: #555;
        }
        
  .sort-options {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
 .sort-options select {
            padding: 8px 12px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 14px;
            cursor: pointer;
        }
        
 .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 25px;
        }
        
 .product-card {
            background: #fff;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            position: relative;
        }
        
 .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
 .product-image {
            height: 280px;
            background-color: #f5f5f5;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
        }
        
 .product-image img {
            max-width: 90%;
            max-height: 90%;
            object-fit: contain;
            transition: transform 0.3s ease;
        }
        
 .product-card:hover .product-image img {
            transform: scale(1.05);
        }
        
 .promo-badge {
            position: absolute;
            top: 10px;
            left: 10px;
            background-color: #d32f2f;
            color: white;
            padding: 5px 10px;
            border-radius: 4px;
            font-size: 14px;
            font-weight: 600;
        }
        
  .product-info {
            padding: 15px;
        }
        
  .product-name {
            font-size: 14px;
            color: #555;
            margin-bottom: 8px;
            height: 40px;
            overflow: hidden;
        }
        
 .product-price {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
  .current-price {
            font-size: 18px;
            font-weight: 700;
            color: #d32f2f;
        }
        
  .original-price {
            font-size: 14px;
            color: #999;
            text-decoration: line-through;
        }
        
  .product-colors {
            display: flex;
            gap: 6px;
            margin-top: 12px;
        }
        
  .color-option {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            cursor: pointer;
            border: 1px solid #eee;
            position: relative;
        }
        
  .color-option.active::after {
            content: '';
            position: absolute;
            top: -3px;
            left: -3px;
            right: -3px;
            bottom: -3px;
            border: 1px solid #333;
            border-radius: 50%;
        }
        
 .color-option.olive { background-color: #556B2F; }
        .color-option.brown { background-color: #8B4513; }
        .color-option.mustard { background-color: #FFDB58; }
        .color-option.blue { background-color: #1e3c72; }
        .color-option.black { background-color: #333; }
        .color-option.red { background-color: #b22222; }
        .color-option.white { background-color: #f0f0f0; border: 1px solid #ddd; }
        
  .add-to-cart {
            width: 100%;
            padding: 10px;
            background-color: #333;
            color: white;
            border: none;
            border-radius: 4px;
            margin-top: 15px;
            cursor: pointer;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
 .add-to-cart:hover {
            background-color: #d32f2f;
        }
        
 .add-to-cart.added {
            background-color: #4CAF50;
        }
        
        /* Footer Styles */
 footer {
            background-color: #333;
            color: #fff;
            padding: 40px 0 20px;
            margin-top: 50px;
        }
        
 .footer-content {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
  .footer-column h3 {
            font-size: 18px;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
  .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 2px;
            background-color: #d32f2f;
        }
        
  .footer-column ul {
            list-style: none;
        }
        
  .footer-column ul li {
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
  .footer-column ul li a {
            color: #bbb;
            text-decoration: none;
            transition: color 0.3s;
        }
        
 .footer-column ul li a:hover {
            color: #fff;
        }
        
  .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }
        
 .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 36px;
            height: 36px;
            background-color: #444;
            border-radius: 50%;
            color: #fff;
            transition: background-color 0.3s;
        }
        
 .social-icons a:hover {
            background-color: #d32f2f;
        }
        
  .copyright {
            text-align: center;
            padding-top: 30px;
            margin-top: 30px;
            border-top: 1px solid #444;
            color: #bbb;
            font-size: 14px;
        }
        
        /* Cart Sidebar */
  .cart-sidebar {
            position: fixed;
            top: 0;
            right: -400px;
            width: 380px;
            height: 100%;
            background: #fff;
            box-shadow: -2px 0 10px rgba(0,0,0,0.1);
            z-index: 1000;
            transition: right 0.4s ease;
            padding: 20px;
            overflow-y: auto;
        }
        
 .cart-sidebar.active {
            right: 0;
        }
        
 .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
            margin-bottom: 20px;
        }
        
 .close-cart {
            font-size: 24px;
            cursor: pointer;
            color: #333;
        }
        
 .cart-items {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
 .cart-item {
            display: flex;
            gap: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }
        
 .cart-item-img {
            width: 80px;
            height: 100px;
            background: #f5f5f5;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 4px;
        }
        
 .cart-item-img img {
            max-width: 90%;
            max-height: 90%;
        }
        
 .cart-item-info {
            flex: 1;
        }
        
  .cart-item-name {
            font-size: 14px;
            margin-bottom: 5px;
        }
        
  .cart-item-price {
            font-weight: 600;
            color: #d32f2f;
            margin-bottom: 8px;
        }
        
  .cart-item-actions {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
 .cart-item-quantity {
            display: flex;
            align-items: center;
            border: 1px solid #ddd;
            border-radius: 4px;
            overflow: hidden;
        }
        
 .quantity-btn {
            width: 30px;
            height: 30px;
            background: #f5f5f5;
            border: none;
            cursor: pointer;
            font-size: 16px;
        }
        
  .quantity-input {
            width: 40px;
            height: 30px;
            border: none;
            text-align: center;
            font-size: 14px;
        }
        
  .remove-item {
            color: #d32f2f;
            background: none;
            border: none;
            cursor: pointer;
            font-size: 14px;
        }
        
 .cart-total {
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #eee;
            display: flex;
            justify-content: space-between;
            font-size: 18px;
            font-weight: 600;
        }
        
  .checkout-btn {
            width: 100%;
            padding: 12px;
            background: #d32f2f;
            color: white;
            border: none;
            border-radius: 4px;
            margin-top: 20px;
            font-weight: 600;
            cursor: pointer;
            transition: background 0.3s;
        }
        
 .checkout-btn:hover {
            background: #b71c1c;
        }
        
        /* Responsive Styles */
  @media (max-width: 992px) {
            .main-content {
                flex-direction: column;
            }
            
  .filters {
                width: 100%;
                position: fixed;
                top: 0;
                left: -100%;
                height: 100vh;
                z-index: 1000;
                overflow-y: auto;
                padding-top: 60px;
            }
            
 .filters.active {
                left: 0;
            }
            
 .filter-toggle {
                display: block;
            }
            
 .close-filters {
                display: block;
            }
            
  .footer-content {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
 @media (max-width: 768px) {
            .product-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
 .nav-links {
                display: none;
            }
            
  .header-top {
                flex-wrap: wrap;
                gap: 15px;
            }
            
  .cart-sidebar {
                width: 100%;
                right: -100%;
            }
        }
        
  @media (max-width: 576px) {
            .product-grid {
                grid-template-columns: 1fr;
            }
            
 .footer-content {
                grid-template-columns: 1fr;
            }
            
.products-header {
                flex-direction: column;
                align-items: flex-start;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-top">
            <div class="logo">MBO</div>
            <div class="nav-links">
                <a href="#">HOMBRE</a>
                <a href="#">MUJER</a>
                <a href="#">NIÑOS</a>
                <a href="#" class="active">OFERTAS</a>
                <a href="#">NOVEDADES</a>
            </div>
            <div class="header-icons">
                <i class="fas fa-search"></i>
                <i class="fas fa-user"></i>
                <i class="fas fa-shopping-bag" id="cart-icon">
                    <span class="cart-count">0</span>
                </i>
            </div>
        </div>
    </header>

<div class="container">
        <button class="filter-toggle" id="filterToggle">
            <i class="fas fa-filter"></i> Filtrar Productos
        </button>
        
        <!-- Main Content -->
 <div class="main-content">
            <!-- Filters Section -->
            <aside class="filters" id="filters">
                <h2 class="filter-title">
                    FILTRAR POR
                    <span class="close-filters" id="closeFilters">&times;</span>
                </h2>
                
<div class="filter-section">
                    <h3>DISPONIBILIDAD</h3>
                    <div class="filter-options">
                        <div class="filter-option">
                            <input type="checkbox" id="stock" class="filter-check" data-filter="availability" value="stock" checked>
                            <label for="stock">En stock (76)</label>
                        </div>
                        <div class="filter-option">
                            <input type="checkbox" id="preorder" class="filter-check" data-filter="availability" value="preorder">
                            <label for="preorder">Preventa (12)</label>
                        </div>
                    </div>
                </div>
                
 <div class="filter-section">
                    <h3>TIPO DE PRODUCTO</h3>
                    <div class="filter-options">
                        <div class="filter-option">
                            <input type="checkbox" id="polo" class="filter-check" data-filter="type" value="polo" checked>
                            <label for="polo">Polos (76)</label>
                        </div>
                        <div class="filter-option">
                            <input type="checkbox" id="camisa" class="filter-check" data-filter="type" value="camisa">
                            <label for="camisa">Camisas (32)</label>
                        </div>
                        <div class="filter-option">
                            <input type="checkbox" id="pantalon" class="filter-check" data-filter="type" value="pantalon">
                            <label for="pantalon">Pantalones (24)</label>
                        </div>
                    </div>
                </div>
                
  <div class="filter-section">
                    <h3>COLOR</h3>
                    <div class="filter-options">
                        <div class="filter-option">
                            <input type="checkbox" id="verde" class="filter-check" data-filter="color" value="olive" checked>
                            <label for="verde">Verde Olivo (18)</label>
                        </div>
                        <div class="filter-option">
                            <input type="checkbox" id="marron" class="filter-check" data-filter="color" value="brown" checked>
                            <label for="marron">Marrón (15)</label>
                        </div>
                        <div class="filter-option">
                            <input type="checkbox" id="mostaza" class="filter-check" data-filter="color" value="mustard" checked>
                            <label for="mostaza">Mostaza (12)</label>
                        </div>
                        <div class="filter-option">
                            <input type="checkbox" id="azul" class="filter-check" data-filter="color" value="blue">
                            <label for="azul">Azul Marino (21)</label>
                        </div>
                        <div class="filter-option">
                            <input type="checkbox" id="negro" class="filter-check" data-filter="color" value="black">
                            <label for="negro">Negro (10)</label>
                        </div>
                    </div>
                </div>
                
 <div class="filter-section">
                    <h3>PRECIO</h3>
                    <div class="filter-options">
                        <div class="filter-option">
                            <input type="checkbox" id="price1" class="filter-check" data-filter="price" value="price1">
                            <label for="price1">S/ 20 - S/ 50 (12)</label>
                        </div>
                        <div class="filter-option">
                            <input type="checkbox" id="price2" class="filter-check" data-filter="price" value="price2" checked>
                            <label for="price2">S/ 50 - S/ 80 (42)</label>
                        </div>
                        <div class="filter-option">
                            <input type="checkbox" id="price3" class="filter-check" data-filter="price" value="price3">
                            <label for="price3">S/ 80 - S/ 120 (22)</label>
                        </div>
                    </div>
                    <div class="price-range">
                        <span>S/ 20</span>
                        <span>S/ 120</span>
                    </div>
                </div>
                
 <button class="add-to-cart" id="applyFilters">Aplicar Filtros</button>
            </aside>
            
            <!-- Products Section -->
<section class="products-section">
                <div class="products-header">
                    <div class="products-count">76 artículos</div>
                    <div class="sort-options">
                        <label for="sort">Ordenar por:</label>
                        <select id="sort">
                            <option value="default">Recomendados</option>
                            <option value="price_asc">Precio: Menor a Mayor</option>
                            <option value="price_desc">Precio: Mayor a Menor</option>
                            <option value="newest">Novedades</option>
                            <option value="bestseller">Más vendidos</option>
                        </select>
                    </div>
                </div>
                
 <div class="product-grid" id="productGrid">
                    <!-- Products will be dynamically inserted here -->
                </div>
            </section>
        </div>
    </div>
    
    <!-- Cart Sidebar -->
<div class="cart-sidebar" id="cartSidebar">
        <div class="cart-header">
            <h2>Tu Carrito</h2>
            <span class="close-cart" id="closeCart">&times;</span>
        </div>
        <div class="cart-items" id="cartItems">
            <!-- Cart items will be dynamically inserted here -->
        </div>
        <div class="cart-total">
            <span>Total:</span>
            <span id="cartTotal">S/.0.00</span>
        </div>
        <button class="checkout-btn">Proceder al Pago</button>
    </div>
    
    <!-- Footer -->
<footer>
        <div class="footer-content">
            <div class="footer-column">
                <h3>MBO</h3>
                <ul>
                    <li><a href="#">Quiénes somos</a></li>
                    <li><a href="#">Nuestras tiendas</a></li>
                    <li><a href="#">Trabaja con nosotros</a></li>
                    <li><a href="#">Responsabilidad social</a></li>
                </ul>
            </div>
            
 <div class="footer-column">
                <h3>Servicio al cliente</h3>
                <ul>
                    <li><a href="#">Preguntas frecuentes</a></li>
                    <li><a href="#">Cambios y devoluciones</a></li>
                    <li><a href="#">Términos y condiciones</a></li>
                    <li><a href="#">Política de privacidad</a></li>
                </ul>
            </div>
            
 <div class="footer-column">
                <h3>Contáctanos</h3>
                <ul>
                    <li><i class="fas fa-phone"></i> (01) 640-9999</li>
                    <li><i class="fas fa-envelope"></i> servicioalcliente@mbo.com.pe</li>
                    <li><i class="fas fa-map-marker-alt"></i> Tiendas a nivel nacional</li>
                </ul>
                <div class="social-icons">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                    <a href="#"><i class="fab fa-tiktok"></i></a>
                </div>
            </div>
            
 <div class="footer-column">
                <h3>Suscríbete</h3>
                <p>Recibe nuestras promociones y novedades</p>
                <form style="margin-top: 15px;">
                    <input type="email" placeholder="Tu correo electrónico" style="width: 100%; padding: 10px; margin-bottom: 10px; border-radius: 4px; border: none;">
                    <button type="submit" style="width: 100%; padding: 10px; background-color: #d32f2f; color: white; border: none; border-radius: 4px; cursor: pointer;">Suscribirme</button>
                </form>
            </div>
        </div>
        
 <div class="copyright">
            © 2023 MBO - Todos los derechos reservados
        </div>
    </footer>
    
 <script>
        // Product data with base names and color parts
        const products = [
            {
                id: 1,
                baseName: "FOLO MANGA CORTA BASICO CUELLO RE-DONDO",
                colorPart: "VERDE OLIVO",
                code: "0125",
                price: 79.00,
                promo: "3 x 7,00",
                colors: ["olive", "brown", "mustard"],
                colorNames: ["VERDE OLIVO", "MARRÓN", "MOSTAZA"],
                type: "polo",
                availability: "stock",
                color: "olive",
                priceRange: "price2",
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='%23556B2F'/%3E%3Ccircle cx='100' cy='90' r='20' fill='white'/%3E%3C/svg%3E"
            },
            {
                id: 2,
                baseName: "FOLO MANGA CORTA BASICO CUELLO RE-DONDO",
                colorPart: "MARRÓN",
                code: "0125",
                price: 79.00,
                promo: "3 x 6,00",
                colors: ["olive", "brown", "mustard"],
                colorNames: ["VERDE OLIVO", "MARRÓN", "MOSTAZA"],
                type: "polo",
                availability: "stock",
                color: "brown",
                priceRange: "price2",
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='%238B4513'/%3E%3Ccircle cx='100' cy='90' r='20' fill='white'/%3E%3C/svg%3E"
            },
            {
                id: 3,
                baseName: "FOLO MANGA CORTA BASICO CUELLO RE-DONDO",
                colorPart: "MOSTAZA",
                code: "0125",
                price: 79.00,
                promo: "3 x 6,00",
                colors: ["olive", "brown", "mustard"],
                colorNames: ["VERDE OLIVO", "MARRÓN", "MOSTAZA"],
                type: "polo",
                availability: "stock",
                color: "mustard",
                priceRange: "price2",
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='%23FFDB58'/%3E%3Ccircle cx='100' cy='90' r='20' fill='white'/%3E%3C/svg%3E"
            },
            {
                id: 4,
                baseName: "FOLO MANGA CORTA BASICO CUELLO RE-DONDO",
                colorPart: "AZUL MARINO",
                code: "0125",
                price: 79.00,
                promo: "3 x 7,00",
                colors: ["olive", "blue", "mustard"],
                colorNames: ["VERDE OLIVO", "AZUL MARINO", "MOSTAZA"],
                type: "polo",
                availability: "stock",
                color: "blue",
                priceRange: "price2",
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='%231e3c72'/%3E%3Ccircle cx='100' cy='90' r='20' fill='white'/%3E%3C/svg%3E"
            },
            {
                id: 5,
                baseName: "FOLO MANGA CORTA BASICO CUELLO RE-DONDO",
                colorPart: "NEGRO",
                code: "0125",
                price: 79.00,
                promo: "3 x 7,00",
                colors: ["black", "brown", "mustard"],
                colorNames: ["NEGRO", "MARRÓN", "MOSTAZA"],
                type: "polo",
                availability: "stock",
                color: "black",
                priceRange: "price2",
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='%23333'/%3E%3Ccircle cx='100' cy='90' r='20' fill='white'/%3E%3C/svg%3E"
            },
            {
                id: 6,
                baseName: "FOLO MANGA CORTA BASICO CUELLO RE-DONDO",
                colorPart: "ROJO",
                code: "0125",
                price: 79.00,
                promo: "3 x 7,00",
                colors: ["red", "olive", "mustard"],
                colorNames: ["ROJO", "VERDE OLIVO", "MOSTAZA"],
                type: "polo",
                availability: "stock",
                color: "red",
                priceRange: "price2",
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='%23b22222'/%3E%3Ccircle cx='100' cy='90' r='20' fill='white'/%3E%3C/svg%3E"
            },
            {
                id: 7,
                baseName: "CAMISA MANGA LARGA CUADROS",
                colorPart: "AZUL Y BLANCO",
                code: "",
                price: 99.00,
                promo: "2 x 85,00",
                colors: ["blue", "white"],
                colorNames: ["AZUL MARINO", "BLANCO"],
                type: "camisa",
                availability: "stock",
                color: "blue",
                priceRange: "price3",
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='%231e3c72'/%3E%3Crect x='60' y='80' width='80' height='90' fill='white'/%3E%3C/svg%3E"
            },
            {
                id: 8,
                baseName: "PANTALÓN JEANS SLIM FIT",
                colorPart: "AZUL OSCURO",
                code: "",
                price: 129.00,
                promo: "",
                colors: ["blue"],
                colorNames: ["AZUL MARINO"],
                type: "pantalon",
                availability: "preorder",
                color: "blue",
                priceRange: "price3",
                image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M80,50 L120,50 L140,150 L60,150 Z' fill='%231e3c72'/%3E%3C/svg%3E"
            }
        ];

        // Shopping cart
        let cart = [];
        
        // DOM elements
        const productGrid = document.getElementById('productGrid');
        const filterToggle = document.getElementById('filterToggle');
        const filters = document.getElementById('filters');
        const closeFilters = document.getElementById('closeFilters');
        const applyFiltersBtn = document.getElementById('applyFilters');
        const sortSelect = document.getElementById('sort');
        const cartIcon = document.getElementById('cart-icon');
        const cartSidebar = document.getElementById('cartSidebar');
        const closeCart = document.getElementById('closeCart');
        const cartItems = document.getElementById('cartItems');
        const cartTotal = document.getElementById('cartTotal');
        const cartCount = document.querySelector('.cart-count');
        const filterChecks = document.querySelectorAll('.filter-check');
        
        // Filter state
        const filterState = {
            availability: ['stock'],
            type: ['polo'],
            color: ['olive', 'brown', 'mustard'],
            price: ['price2']
        };
        
        // Initialize the page
        function init() {
            renderProducts(products);
            setupEventListeners();
            updateCartCount();
        }
        
        // Set up event listeners
        function setupEventListeners() {
            // Filter toggle
            filterToggle.addEventListener('click', () => {
                filters.classList.add('active');
            });
            
            closeFilters.addEventListener('click', () => {
                filters.classList.remove('active');
            });
            
            // Apply filters
            applyFiltersBtn.addEventListener('click', applyFilters);
            
            // Sort products
            sortSelect.addEventListener('change', sortProducts);
            
            // Cart functionality
            cartIcon.addEventListener('click', () => {
                cartSidebar.classList.add('active');
                renderCartItems();
            });
            
            closeCart.addEventListener('click', () => {
                cartSidebar.classList.remove('active');
            });
            
            // Filter checkboxes
            filterChecks.forEach(check => {
                check.addEventListener('change', updateFilterState);
            });
        }
        
        // Update filter state based on checkboxes
        function updateFilterState() {
            filterChecks.forEach(check => {
                const filterType = check.dataset.filter;
                const value = check.value;
                
                if (check.checked) {
                    if (!filterState[filterType].includes(value)) {
                        filterState[filterType].push(value);
                    }
                } else {
                    const index = filterState[filterType].indexOf(value);
                    if (index > -1) {
                        filterState[filterType].splice(index, 1);
                    }
                }
            });
        }
        
        // Apply filters to products
        function applyFilters() {
            const filteredProducts = products.filter(product => {
                // Availability filter
                if (filterState.availability.length > 0 && !filterState.availability.includes(product.availability)) {
                    return false;
                }
                
                // Type filter
                if (filterState.type.length > 0 && !filterState.type.includes(product.type)) {
                    return false;
                }
                
                // Color filter
                if (filterState.color.length > 0 && !filterState.color.includes(product.color)) {
                    return false;
                }
                
                // Price filter
                if (filterState.price.length > 0 && !filterState.price.includes(product.priceRange)) {
                    return false;
                }
                
                return true;
            });
            
            renderProducts(filteredProducts);
            document.querySelector('.products-count').textContent = `${filteredProducts.length} artículos`;
            filters.classList.remove('active');
        }
        
        // Sort products
        function sortProducts() {
            const sortValue = sortSelect.value;
            let sortedProducts = [...products];
            
            switch(sortValue) {
                case 'price_asc':
                    sortedProducts.sort((a, b) => a.price - b.price);
                    break;
                case 'price_desc':
                    sortedProducts.sort((a, b) => b.price - a.price);
                    break;
                case 'newest':
                    // Simulate newest by ID (higher ID is newer)
                    sortedProducts.sort((a, b) => b.id - a.id);
                    break;
                case 'bestseller':
                    // Simulate bestsellers by random
                    sortedProducts.sort(() => Math.random() - 0.5);
                    break;
            }
            
            renderProducts(sortedProducts);
        }
        
        // Render products to the grid
        function renderProducts(productsToRender) {
            productGrid.innerHTML = '';
            
            productsToRender.forEach(product => {
                const productCard = document.createElement('div');
                productCard.className = 'product-card';
                productCard.innerHTML = `
                    <div class="product-image">
                        ${product.promo ? `<div class="promo-badge">${product.promo}</div>` : ''}
                        <img src="${product.image}" alt="${product.baseName} ${product.colorPart} ${product.code}">
                    </div>
                    <div class="product-info">
                        <div class="product-name">${product.baseName} ${product.colorPart} ${product.code}</div>
                        <div class="product-price">
                            <span class="current-price">S/.${product.price.toFixed(2)}</span>
                        </div>
                        <div class="product-colors">
                            ${product.colors.map((color, index) => `
                                <div class="color-option ${color} ${color === product.color ? 'active' : ''}" 
                                     data-product="${product.id}" 
                                     data-color="${color}" 
                                     data-color-name="${product.colorNames[index]}"
                                     title="${product.colorNames[index]}"></div>
                            `).join('')}
                        </div>
                        <button class="add-to-cart" data-id="${product.id}">Añadir al carrito</button>
                    </div>
                `;
                productGrid.appendChild(productCard);
            });
            
            // Add event listeners to new elements
            document.querySelectorAll('.add-to-cart').forEach(button => {
                button.addEventListener('click', addToCart);
            });
            
            document.querySelectorAll('.color-option').forEach(color => {
                color.addEventListener('click', changeProductColor);
            });
        }
        
        // Change product color and name
        function changeProductColor(e) {
            const colorOption = e.target;
            const productId = parseInt(colorOption.dataset.product);
            const color = colorOption.dataset.color;
            const colorName = colorOption.dataset.colorName;
            
            // Find the product
            const product = products.find(p => p.id === productId);
            if (!product) return;
            
            // Update the product's color and colorPart
            product.color = color;
            product.colorPart = colorName;
            
            // Find the product card in the DOM
            const productCard = colorOption.closest('.product-card');
            
            // Remove active class from all color options for this product
            productCard.querySelectorAll('.color-option').forEach(option => {
                option.classList.remove('active');
            });
            
            // Add active class to selected color
            colorOption.classList.add('active');
            
            // Update the product name
            const productNameElement = productCard.querySelector('.product-name');
            productNameElement.textContent = `${product.baseName} ${colorName} ${product.code}`;
            
            // Update the product image (simulate with CSS filter)
            const productImage = productCard.querySelector('.product-image img');
            updateImageColor(productImage, color);
        }
        
        // Update image color with CSS filter
        function updateImageColor(imgElement, color) {
            // Reset any previous filters
            imgElement.style.filter = '';
            
            // Apply color-specific filters
            switch(color) {
                case 'olive':
                    imgElement.style.filter = 'hue-rotate(100deg)';
                    break;
                case 'brown':
                    imgElement.style.filter = 'hue-rotate(200deg)';
                    break;
                case 'mustard':
                    imgElement.style.filter = 'hue-rotate(300deg)';
                    break;
                case 'blue':
                    imgElement.style.filter = 'hue-rotate(180deg)';
                    break;
                case 'black':
                    imgElement.style.filter = 'grayscale(100%) brightness(30%)';
                    break;
                case 'red':
                    imgElement.style.filter = 'hue-rotate(0deg)';
                    break;
                case 'white':
                    imgElement.style.filter = 'brightness(150%)';
                    break;
            }
        }
        
        // Add product to cart
        function addToCart(e) {
            const button = e.target;
            const productId = parseInt(button.dataset.id);
            const product = products.find(p => p.id === productId);
            
            // Check if product is already in cart
            const existingItem = cart.find(item => item.id === productId);
            
            if (existingItem) {
                existingItem.quantity++;
            } else {
                cart.push({
                    id: product.id,
                    name: `${product.baseName} ${product.colorPart} ${product.code}`,
                    price: product.price,
                    image: product.image,
                    quantity: 1
                });
            }
            
            // Update button state
            button.textContent = '✓ Añadido';
            button.classList.add('added');
            
            setTimeout(() => {
                button.textContent = 'Añadir al carrito';
                button.classList.remove('added');
            }, 2000);
            
            updateCartCount();
            
            // Show cart sidebar if not already open
            if (!cartSidebar.classList.contains('active')) {
                cartSidebar.classList.add('active');
                renderCartItems();
            } else {
                renderCartItems();
            }
        }
        
        // Render cart items
        function renderCartItems() {
            cartItems.innerHTML = '';
            
            if (cart.length === 0) {
                cartItems.innerHTML = '<p>Tu carrito está vacío</p>';
                cartTotal.textContent = 'S/.0.00';
                return;
            }
            
            let total = 0;
            
            cart.forEach(item => {
                const itemTotal = item.price * item.quantity;
                total += itemTotal;
                
                const cartItem = document.createElement('div');
                cartItem.className = 'cart-item';
                cartItem.innerHTML = `
                    <div class="cart-item-img">
                        <img src="${item.image}" alt="${item.name}">
                    </div>
                    <div class="cart-item-info">
                        <div class="cart-item-name">${item.name}</div>
                        <div class="cart-item-price">S/.${item.price.toFixed(2)}</div>
                        <div class="cart-item-actions">
                            <div class="cart-item-quantity">
                                <button class="quantity-btn minus" data-id="${item.id}">-</button>
                                <input type="text" class="quantity-input" value="${item.quantity}" readonly>
                                <button class="quantity-btn plus" data-id="${item.id}">+</button>
                            </div>
                            <button class="remove-item" data-id="${item.id}">
                                <i class="fas fa-trash"></i>
                            </button>
                        </div>
                    </div>
                `;
                cartItems.appendChild(cartItem);
            });
            
            cartTotal.textContent = `S/.${total.toFixed(2)}`;
            
            // Add event listeners to quantity buttons
            document.querySelectorAll('.quantity-btn.minus').forEach(btn => {
                btn.addEventListener('click', decreaseQuantity);
            });
            
            document.querySelectorAll('.quantity-btn.plus').forEach(btn => {
                btn.addEventListener('click', increaseQuantity);
            });
            
            document.querySelectorAll('.remove-item').forEach(btn => {
                btn.addEventListener('click', removeFromCart);
            });
        }
        
        // Decrease item quantity
        function decreaseQuantity(e) {
            const productId = parseInt(e.target.dataset.id);
            const item = cart.find(item => item.id === productId);
            
            if (item.quantity > 1) {
                item.quantity--;
            } else {
                cart = cart.filter(item => item.id !== productId);
            }
            
            renderCartItems();
            updateCartCount();
        }
        
        // Increase item quantity
        function increaseQuantity(e) {
            const productId = parseInt(e.target.dataset.id);
            const item = cart.find(item => item.id === productId);
            item.quantity++;
            renderCartItems();
            updateCartCount();
        }
        
        // Remove item from cart
        function removeFromCart(e) {
            const productId = parseInt(e.target.closest('.remove-item').dataset.id);
            cart = cart.filter(item => item.id !== productId);
            renderCartItems();
            updateCartCount();
        }
        
        // Update cart count in header
        function updateCartCount() {
            const count = cart.reduce((total, item) => total + item.quantity, 0);
            cartCount.textContent = count;
        }
        
        // Initialize the application
        init();
    </script>
</body>
</html>
