<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Catálogo MBO con Filtros Funcionales</title>
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
            padding: 8px 0;
        }
        
  .nav-links a:hover {
            color: #d32f2f;
        }
        
  .nav-links a.active {
            color: #d32f2f;
            font-weight: 600;
        }
        
 .nav-links a.active::after {
            content: '';
            position: absolute;
            bottom: 0;
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
        
        /* Banner Styles */
 .category-banner {
            height: 300px;
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), 
                        url('https://images.unsplash.com/photo-1441984904996-e0b6ba687e04?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-align: center;
            margin: 20px 0;
            border-radius: 8px;
        }
        
 .banner-content h1 {
            font-size: 42px;
            margin-bottom: 15px;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
        }
        
 .banner-content p {
            font-size: 18px;
            max-width: 600px;
            margin: 0 auto;
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
        .color-option.pink { background-color: #ff69b4; }
        .color-option.purple { background-color: #9370db; }
        .color-option.green { background-color: #2e8b57; }
        .color-option.yellow { background-color: #ffd700; }
        .color-option.gray { background-color: #808080; }
        
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
            
  .banner-content h1 {
                font-size: 32px;
            }
        }
        
  @media (max-width: 576px) {
            .product-grid {
                grid-template-columns: 1fr;
            }
            
 .products-header {
                flex-direction: column;
                align-items: flex-start;
            }
            
 .banner-content h1 {
                font-size: 28px;
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
                <a href="#" class="category-link active" data-category="hombre">HOMBRE</a>
                <a href="#" class="category-link" data-category="mujer">MUJER</a>
                <a href="#" class="category-link" data-category="ninos">NIÑOS</a>
                <a href="#" class="category-link" data-category="ofertas">OFERTAS</a>
                <a href="#" class="category-link" data-category="novedades">NOVEDADES</a>
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
        <div class="category-banner">
            <div class="banner-content">
                <h1>MODA PARA HOMBRE</h1>
                <p>Descubre nuestra colección de polos, camisas y más prendas básicas con estilo</p>
            </div>
        </div>
        
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
                    <div class="filter-options" id="availability-options">
                        <!-- Dynamically populated -->
                    </div>
                </div>
                
 <div class="filter-section">
                    <h3>TIPO DE PRODUCTO</h3>
                    <div class="filter-options" id="type-options">
                        <!-- Dynamically populated -->
                    </div>
                </div>
                
 <div class="filter-section">
                    <h3>COLOR</h3>
                    <div class="filter-options" id="color-options">
                        <!-- Dynamically populated -->
                    </div>
                </div>
                
 <div class="filter-section">
                    <h3>PRECIO</h3>
                    <div class="filter-options" id="price-options">
                        <!-- Dynamically populated -->
                    </div>
                    <div class="price-range">
                        <span id="min-price">S/ 0</span>
                        <span id="max-price">S/ 0</span>
                    </div>
                </div>
                
 <button class="add-to-cart" id="applyFilters">Aplicar Filtros</button>
                <button class="add-to-cart" id="resetFilters" style="background-color: #555; margin-top: 10px;">Reiniciar Filtros</button>
            </aside>
            
            <!-- Products Section -->
 <section class="products-section">
                <div class="products-header">
                    <div class="products-count">8 artículos</div>
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
    
 <script>
        // Product data by category
        const categories = {
            hombre: [
                {
                    id: 1,
                    baseName: "POLO MANGA CORTA BÁSICO",
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
                    baseName: "POLO CUADROS MANGA CORTA",
                    colorPart: "AZUL MARINO",
                    code: "0231",
                    price: 89.00,
                    promo: "2 x 80,00",
                    colors: ["blue", "white"],
                    colorNames: ["AZUL MARINO", "BLANCO"],
                    type: "polo",
                    availability: "stock",
                    color: "blue",
                    priceRange: "price2",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='%231e3c72'/%3E%3Crect x='60' y='80' width='80' height='90' fill='white'/%3E%3C/svg%3E"
                },
                {
                    id: 3,
                    baseName: "CAMISA FORMAL MANGA LARGA",
                    colorPart: "BLANCO",
                    code: "0456",
                    price: 129.00,
                    promo: "",
                    colors: ["white", "blue"],
                    colorNames: ["BLANCO", "AZUL MARINO"],
                    type: "camisa",
                    availability: "stock",
                    color: "white",
                    priceRange: "price3",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='white'/%3E%3C/svg%3E"
                },
                {
                    id: 4,
                    baseName: "JEANS SLIM FIT",
                    colorPart: "AZUL OSCURO",
                    code: "0789",
                    price: 149.00,
                    promo: "3 x 130,00",
                    colors: ["blue", "black"],
                    colorNames: ["AZUL OSCURO", "NEGRO"],
                    type: "pantalon",
                    availability: "stock",
                    color: "blue",
                    priceRange: "price3",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M80,50 L120,50 L140,150 L60,150 Z' fill='%231e3c72'/%3E%3C/svg%3E"
                },
                {
                    id: 5,
                    baseName: "POLO RAYAS HORIZONTALES",
                    colorPart: "ROJO Y BLANCO",
                    code: "0532",
                    price: 85.00,
                    promo: "3 x 7,50",
                    colors: ["red", "blue"],
                    colorNames: ["ROJO Y BLANCO", "AZUL Y BLANCO"],
                    type: "polo",
                    availability: "stock",
                    color: "red",
                    priceRange: "price2",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='%23b22222'/%3E%3Crect x='60' y='90' width='80' height='10' fill='white'/%3E%3Crect x='60' y='110' width='80' height='10' fill='white'/%3E%3Crect x='60' y='130' width='80' height='10' fill='white'/%3E%3C/svg%3E"
                },
                {
                    id: 6,
                    baseName: "SUETER LIGERO",
                    colorPart: "GRIS",
                    code: "0612",
                    price: 119.00,
                    promo: "2 x 100,00",
                    colors: ["gray", "black"],
                    colorNames: ["GRIS", "NEGRO"],
                    type: "sueter",
                    availability: "stock",
                    color: "gray",
                    priceRange: "price3",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,30 L140,30 L160,70 L160,170 L40,170 L40,70 Z' fill='%23808080'/%3E%3C/svg%3E"
                },
                {
                    id: 7,
                    baseName: "SHORT DEPORTIVO",
                    colorPart: "NEGRO",
                    code: "0987",
                    price: 65.00,
                    promo: "3 x 6,00",
                    colors: ["black", "blue"],
                    colorNames: ["NEGRO", "AZUL MARINO"],
                    type: "short",
                    availability: "stock",
                    color: "black",
                    priceRange: "price1",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M80,50 L120,50 L140,100 L60,100 Z' fill='%23333'/%3E%3C/svg%3E"
                },
                {
                    id: 8,
                    baseName: "CAMISETA ESTAMPADA",
                    colorPart: "BLANCO",
                    code: "0128",
                    price: 69.00,
                    promo: "3 x 6,50",
                    colors: ["white", "black"],
                    colorNames: ["BLANCO", "NEGRO"],
                    type: "camiseta",
                    availability: "stock",
                    color: "white",
                    priceRange: "price1",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='white'/%3E%3Ccircle cx='100' cy='100' r='30' fill='%23d32f2f'/%3E%3C/svg%3E"
                }
            ],
            mujer: [
                {
                    id: 9,
                    baseName: "VESTIDO FLOREADO",
                    colorPart: "ROSA",
                    code: "M201",
                    price: 129.00,
                    promo: "2 x 110,00",
                    colors: ["pink", "purple"],
                    colorNames: ["ROSA", "LILA"],
                    type: "vestido",
                    availability: "stock",
                    color: "pink",
                    priceRange: "price3",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M100,30 Q150,70 100,120 Q50,70 100,30 Z' fill='%23ff69b4'/%3E%3C/svg%3E"
                },
                {
                    id: 10,
                    baseName: "BLUSA DE ENCAJE",
                    colorPart: "BLANCO",
                    code: "M305",
                    price: 89.00,
                    promo: "",
                    colors: ["white", "black"],
                    colorNames: ["BLANCO", "NEGRO"],
                    type: "blusa",
                    availability: "stock",
                    color: "white",
                    priceRange: "price2",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='white'/%3E%3C/svg%3E"
                },
                {
                    id: 11,
                    baseName: "FALDA PLISADA",
                    colorPart: "NEGRO",
                    code: "M412",
                    price: 75.00,
                    promo: "3 x 6,50",
                    colors: ["black", "red"],
                    colorNames: ["NEGRO", "ROJO"],
                    type: "falda",
                    availability: "stock",
                    color: "black",
                    priceRange: "price1",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M80,50 L120,50 L140,150 L60,150 Z' fill='%23333'/%3E%3C/svg%3E"
                },
                {
                    id: 12,
                    baseName: "JEANS SKINNY",
                    colorPart: "AZUL CLARO",
                    code: "M523",
                    price: 99.00,
                    promo: "",
                    colors: ["blue", "black"],
                    colorNames: ["AZUL CLARO", "NEGRO"],
                    type: "pantalon",
                    availability: "stock",
                    color: "blue",
                    priceRange: "price2",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M80,50 L120,50 L140,150 L60,150 Z' fill='%234b7bec'/%3E%3C/svg%3E"
                },
                {
                    id: 13,
                    baseName: "TOP CROP",
                    colorPart: "AMARILLO",
                    code: "M615",
                    price: 55.00,
                    promo: "3 x 5,00",
                    colors: ["yellow", "pink"],
                    colorNames: ["AMARILLO", "ROSA"],
                    type: "top",
                    availability: "stock",
                    color: "yellow",
                    priceRange: "price1",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M80,100 L120,100 L130,150 L70,150 Z' fill='%23ffd700'/%3E%3C/svg%3E"
                },
                {
                    id: 14,
                    baseName: "CARDIGAN LIGERO",
                    colorPart: "BEIGE",
                    code: "M704",
                    price: 109.00,
                    promo: "2 x 95,00",
                    colors: ["brown", "gray"],
                    colorNames: ["BEIGE", "GRIS"],
                    type: "cardigan",
                    availability: "stock",
                    color: "brown",
                    priceRange: "price3",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,30 L140,30 L160,70 L160,170 L40,170 L40,70 Z' fill='%238B4513'/%3E%3C/svg%3E"
                },
                {
                    id: 15,
                    baseName: "VESTIDO DE VERANO",
                    colorPart: "AZUL",
                    code: "M808",
                    price: 139.00,
                    promo: "",
                    colors: ["blue", "green"],
                    colorNames: ["AZUL", "VERDE"],
                    type: "vestido",
                    availability: "stock",
                    color: "blue",
                    priceRange: "price3",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M100,30 Q150,70 100,150 Q50,70 100,30 Z' fill='%231e3c72'/%3E%3C/svg%3E"
                },
                {
                    id: 16,
                    baseName: "SHORT JEANS",
                    colorPart: "AZUL DESGASTADO",
                    code: "M912",
                    price: 79.00,
                    promo: "3 x 7,00",
                    colors: ["blue", "black"],
                    colorNames: ["AZUL DESGASTADO", "NEGRO"],
                    type: "short",
                    availability: "stock",
                    color: "blue",
                    priceRange: "price2",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M80,50 L120,50 L140,100 L60,100 Z' fill='%234b7bec'/%3E%3C/svg%3E"
                }
            ],
            ninos: [
                {
                    id: 17,
                    baseName: "POLO NIÑO ESTAMPADO",
                    colorPart: "ROJO",
                    code: "N101",
                    price: 45.00,
                    promo: "3 x 4,00",
                    colors: ["red", "blue"],
                    colorNames: ["ROJO", "AZUL"],
                    type: "polo",
                    availability: "stock",
                    color: "red",
                    priceRange: "price1",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='%23b22222'/%3E%3Ccircle cx='100' cy='100' r='20' fill='yellow'/%3E%3C/svg%3E"
                },
                {
                    id: 18,
                    baseName: "JEANS NIÑO",
                    colorPart: "AZUL",
                    code: "N205",
                    price: 65.00,
                    promo: "2 x 60,00",
                    colors: ["blue", "black"],
                    colorNames: ["AZUL", "NEGRO"],
                    type: "pantalon",
                    availability: "stock",
                    color: "blue",
                    priceRange: "price1",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M80,50 L120,50 L140,150 L60,150 Z' fill='%234b7bec'/%3E%3C/svg%3E"
                },
                {
                    id: 19,
                    baseName: "VESTIDO NIÑA FLORES",
                    colorPart: "ROSA",
                    code: "N312",
                    price: 59.00,
                    promo: "3 x 5,50",
                    colors: ["pink", "purple"],
                    colorNames: ["ROSA", "LILA"],
                    type: "vestido",
                    availability: "stock",
                    color: "pink",
                    priceRange: "price1",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M100,30 Q150,70 100,120 Q50,70 100,30 Z' fill='%23ff69b4'/%3E%3Ccircle cx='120' cy='80' r='8' fill='white'/%3E%3Ccircle cx='140' cy='100' r='8' fill='white'/%3E%3C/svg%3E"
                },
                {
                    id: 20,
                    baseName: "SUETER NIÑO",
                    colorPart: "VERDE",
                    code: "N408",
                    price: 55.00,
                    promo: "",
                    colors: ["green", "blue"],
                    colorNames: ["VERDE", "AZUL"],
                    type: "sueter",
                    availability: "stock",
                    color: "green",
                    priceRange: "price1",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,30 L140,30 L160,70 L160,170 L40,170 L40,70 Z' fill='%232e8b57'/%3E%3C/svg%3E"
                }
            ],
            ofertas: [
                {
                    id: 21,
                    baseName: "POLO OFERTA ESPECIAL",
                    colorPart: "NEGRO",
                    code: "OF001",
                    price: 39.00,
                    promo: "3 x 3,50",
                    colors: ["black", "gray"],
                    colorNames: ["NEGRO", "GRIS"],
                    type: "polo",
                    availability: "stock",
                    color: "black",
                    priceRange: "price1",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='%23333'/%3E%3C/svg%3E"
                },
                {
                    id: 22,
                    baseName: "JEANS OFERTA",
                    colorPart: "AZUL",
                    code: "OF102",
                    price: 79.00,
                    promo: "2 x 70,00",
                    colors: ["blue", "black"],
                    colorNames: ["AZUL", "NEGRO"],
                    type: "pantalon",
                    availability: "stock",
                    color: "blue",
                    priceRange: "price2",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M80,50 L120,50 L140,150 L60,150 Z' fill='%231e3c72'/%3E%3C/svg%3E"
                },
                {
                    id: 23,
                    baseName: "CAMISA OFERTA",
                    colorPart: "BLANCO",
                    code: "OF203",
                    price: 59.00,
                    promo: "3 x 5,50",
                    colors: ["white", "blue"],
                    colorNames: ["BLANCO", "AZUL"],
                    type: "camisa",
                    availability: "stock",
                    color: "white",
                    priceRange: "price1",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='white'/%3E%3C/svg%3E"
                },
                {
                    id: 24,
                    baseName: "CHAQUETA OFERTA",
                    colorPart: "GRIS",
                    code: "OF304",
                    price: 99.00,
                    promo: "2 x 90,00",
                    colors: ["gray", "black"],
                    colorNames: ["GRIS", "NEGRO"],
                    type: "chaqueta",
                    availability: "stock",
                    color: "gray",
                    priceRange: "price2",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,30 L140,30 L160,70 L160,170 L40,170 L40,70 Z' fill='%23808080'/%3E%3C/svg%3E"
                }
            ],
            novedades: [
                {
                    id: 25,
                    baseName: "POLO ULTRA LIGERO",
                    colorPart: "VERDE MENTA",
                    code: "NV001",
                    price: 89.00,
                    promo: "3 x 8,00",
                    colors: ["green", "blue"],
                    colorNames: ["VERDE MENTA", "AZUL CIELO"],
                    type: "polo",
                    availability: "stock",
                    color: "green",
                    priceRange: "price2",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='%2338c172'/%3E%3C/svg%3E"
                },
                {
                    id: 26,
                    baseName: "JEANS ROTO",
                    colorPart: "AZUL CLARO",
                    code: "NV102",
                    price: 139.00,
                    promo: "",
                    colors: ["blue", "black"],
                    colorNames: ["AZUL CLARO", "NEGRO"],
                    type: "pantalon",
                    availability: "stock",
                    color: "blue",
                    priceRange: "price3",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M80,50 L120,50 L140,150 L60,150 Z' fill='%234b7bec'/%3E%3Crect x='100' y='100' width='20' height='30' fill='white'/%3E%3C/svg%3E"
                },
                {
                    id: 27,
                    baseName: "CAMISA ESTAMPADA FLORES",
                    colorPart: "BLANCO Y ROSA",
                    code: "NV203",
                    price: 109.00,
                    promo: "2 x 100,00",
                    colors: ["pink", "white"],
                    colorNames: ["BLANCO Y ROSA", "BLANCO Y AZUL"],
                    type: "camisa",
                    availability: "stock",
                    color: "pink",
                    priceRange: "price3",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,50 L140,50 L160,80 L160,170 L40,170 L40,80 Z' fill='white'/%3E%3Ccircle cx='100' cy='100' r='10' fill='%23ff69b4'/%3E%3Ccircle cx='130' cy='80' r='8' fill='%23ff69b4'/%3E%3Ccircle cx='80' cy='130' r='8' fill='%23ff69b4'/%3E%3C/svg%3E"
                },
                {
                    id: 28,
                    baseName: "ABRIGO ULTRA LIGERO",
                    colorPart: "BEIGE",
                    code: "NV304",
                    price: 199.00,
                    promo: "",
                    colors: ["brown", "gray"],
                    colorNames: ["BEIGE", "GRIS"],
                    type: "abrigo",
                    availability: "stock",
                    color: "brown",
                    priceRange: "price3",
                    image: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Crect width='200' height='200' fill='%23f5f5f5'/%3E%3Cpath d='M60,30 L140,30 L160,70 L160,170 L40,170 L40,70 Z' fill='%238B4513'/%3E%3C/svg%3E"
                }
            ]
        };

        // Shopping cart
        let cart = [];
        
        // DOM elements
        const productGrid = document.getElementById('productGrid');
        const filterToggle = document.getElementById('filterToggle');
        const filters = document.getElementById('filters');
        const closeFilters = document.getElementById('closeFilters');
        const applyFiltersBtn = document.getElementById('applyFilters');
        const resetFiltersBtn = document.getElementById('resetFilters');
        const sortSelect = document.getElementById('sort');
        const cartIcon = document.getElementById('cart-icon');
        const cartSidebar = document.getElementById('cartSidebar');
        const closeCart = document.getElementById('closeCart');
        const cartItems = document.getElementById('cartItems');
        const cartTotal = document.getElementById('cartTotal');
        const cartCount = document.querySelector('.cart-count');
        const categoryLinks = document.querySelectorAll('.category-link');
        const bannerContent = document.querySelector('.banner-content');
        
        // Filter containers
        const availabilityOptions = document.getElementById('availability-options');
        const typeOptions = document.getElementById('type-options');
        const colorOptions = document.getElementById('color-options');
        const priceOptions = document.getElementById('price-options');
        const minPriceSpan = document.getElementById('min-price');
        const maxPriceSpan = document.getElementById('max-price');
        
        // Current category
        let currentCategory = 'hombre';
        
        // Filter state
        let filterState = {
            availability: [],
            type: [],
            color: [],
            price: []
        };
        
        // Initialize the page
        function init() {
            renderProducts(categories[currentCategory]);
            updateFilters();
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
            
            // Reset filters
            resetFiltersBtn.addEventListener('click', resetFilters);
            
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
            
            // Category links
            categoryLinks.forEach(link => {
                link.addEventListener('click', (e) => {
                    e.preventDefault();
                    
                    // Update active category
                    categoryLinks.forEach(l => l.classList.remove('active'));
                    link.classList.add('active');
                    
                    // Set new category
                    currentCategory = link.dataset.category;
                    
                    // Update banner
                    updateBanner(currentCategory);
                    
                    // Reset filters
                    resetFilters();
                    
                    // Render products
                    renderProducts(categories[currentCategory]);
                    
                    // Update filters
                    updateFilters();
                });
            });
        }
        
        // Update banner based on category
        function updateBanner(category) {
            const banners = {
                hombre: {
                    title: "MODA PARA HOMBRE",
                    description: "Descubre nuestra colección de polos, camisas y más prendas básicas con estilo"
                },
                mujer: {
                    title: "MODA PARA MUJER",
                    description: "Encuentra las últimas tendencias en vestidos, blusas y accesorios femeninos"
                },
                ninos: {
                    title: "MODA PARA NIÑOS",
                    description: "Ropa cómoda y divertida para los más pequeños de la casa"
                },
                ofertas: {
                    title: "OFERTAS ESPECIALES",
                    description: "Aprovecha nuestras promociones exclusivas con descuentos increíbles"
                },
                novedades: {
                    title: "ÚLTIMAS NOVEDADES",
                    description: "Descubre nuestra nueva colección con las últimas tendencias de la temporada"
                }
            };
            
            bannerContent.querySelector('h1').textContent = banners[category].title;
            bannerContent.querySelector('p').textContent = banners[category].description;
        }
        
        // Update filters based on current category
        function updateFilters() {
            const products = categories[currentCategory];
            
            // Reset filter state
            filterState = {
                availability: [],
                type: [],
                color: [],
                price: []
            };
            
            // Calculate min and max prices
            let minPrice = Infinity;
            let maxPrice = 0;
            
            products.forEach(product => {
                if (product.price < minPrice) minPrice = product.price;
                if (product.price > maxPrice) maxPrice = product.price;
            });
            
            minPriceSpan.textContent = `S/ ${Math.floor(minPrice)}`;
            maxPriceSpan.textContent = `S/ ${Math.ceil(maxPrice)}`;
            
            // Calculate filter counts
            const availabilityCounts = {};
            const typeCounts = {};
            const colorCounts = {};
            const priceCounts = {
                low: 0,
                medium: 0,
                high: 0
            };
            
            // Price ranges
            const lowPrice = minPrice;
            const mediumPrice = minPrice + (maxPrice - minPrice) / 3;
            const highPrice = minPrice + (maxPrice - minPrice) * 2 / 3;
            
            products.forEach(product => {
                // Availability counts
                availabilityCounts[product.availability] = (availabilityCounts[product.availability] || 0) + 1;
                
                // Type counts
                typeCounts[product.type] = (typeCounts[product.type] || 0) + 1;
                
                // Color counts
                product.colors.forEach(color => {
                    colorCounts[color] = (colorCounts[color] || 0) + 1;
                });
                
                // Price counts
                if (product.price <= mediumPrice) {
                    priceCounts.low++;
                } else if (product.price <= highPrice) {
                    priceCounts.medium++;
                } else {
                    priceCounts.high++;
                }
            });
            
            // Render availability options
            availabilityOptions.innerHTML = '';
            for (const availability in availabilityCounts) {
                const option = document.createElement('div');
                option.className = 'filter-option';
                option.innerHTML = `
                    <input type="checkbox" id="${availability}" class="filter-check" data-filter="availability" value="${availability}">
                    <label for="${availability}">${availability === 'stock' ? 'En stock' : 'Preventa'} (${availabilityCounts[availability]})</label>
                `;
                availabilityOptions.appendChild(option);
            }
            
            // Render type options
            typeOptions.innerHTML = '';
            for (const type in typeCounts) {
                const option = document.createElement('div');
                option.className = 'filter-option';
                option.innerHTML = `
                    <input type="checkbox" id="${type}" class="filter-check" data-filter="type" value="${type}">
                    <label for="${type}">${getTypeName(type)} (${typeCounts[type]})</label>
                `;
                typeOptions.appendChild(option);
            }
            
            // Render color options
            colorOptions.innerHTML = '';
            for (const color in colorCounts) {
                const option = document.createElement('div');
                option.className = 'filter-option';
                option.innerHTML = `
                    <input type="checkbox" id="${color}" class="filter-check" data-filter="color" value="${color}">
                    <label for="${color}">${getColorName(color)} (${colorCounts[color]})</label>
                `;
                colorOptions.appendChild(option);
            }
            
            // Render price options
            priceOptions.innerHTML = '';
            const priceRanges = [
                { id: 'low', name: `S/ ${Math.floor(minPrice)} - S/ ${Math.ceil(mediumPrice)}`, count: priceCounts.low },
                { id: 'medium', name: `S/ ${Math.ceil(mediumPrice)} - S/ ${Math.ceil(highPrice)}`, count: priceCounts.medium },
                { id: 'high', name: `S/ ${Math.ceil(highPrice)} - S/ ${Math.ceil(maxPrice)}`, count: priceCounts.high }
            ];
            
            priceRanges.forEach(range => {
                const option = document.createElement('div');
                option.className = 'filter-option';
                option.innerHTML = `
                    <input type="checkbox" id="${range.id}" class="filter-check" data-filter="price" value="${range.id}">
                    <label for="${range.id}">${range.name} (${range.count})</label>
                `;
                priceOptions.appendChild(option);
            });
            
            // Add event listeners to filter checkboxes
            document.querySelectorAll('.filter-check').forEach(checkbox => {
                checkbox.addEventListener('change', function() {
                    const filterType = this.dataset.filter;
                    const value = this.value;
                    
                    if (this.checked) {
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
            });
        }
        
        // Get type name
        function getTypeName(type) {
            const typeNames = {
                'polo': 'Polos',
                'camisa': 'Camisas',
                'pantalon': 'Pantalones',
                'short': 'Shorts',
                'sueter': 'Súeteres',
                'camiseta': 'Camisetas',
                'vestido': 'Vestidos',
                'blusa': 'Blusas',
                'falda': 'Faldas',
                'top': 'Tops',
                'cardigan': 'Cardigans',
                'chaqueta': 'Chaquetas',
                'abrigo': 'Abrigos',
                'zapatos': 'Zapatos',
                'bolso': 'Bolsos',
                'gorra': 'Gorras'
            };
            
            return typeNames[type] || type;
        }
        
        // Get color name
        function getColorName(color) {
            const colorNames = {
                'olive': 'Verde Olivo',
                'brown': 'Marrón',
                'mustard': 'Mostaza',
                'blue': 'Azul Marino',
                'black': 'Negro',
                'red': 'Rojo',
                'white': 'Blanco',
                'pink': 'Rosa',
                'purple': 'Lila',
                'green': 'Verde',
                'yellow': 'Amarillo',
                'gray': 'Gris'
            };
            
            return colorNames[color] || color;
        }
        
        // Reset filters
        function resetFilters() {
            filterState = {
                availability: [],
                type: [],
                color: [],
                price: []
            };
            
            // Uncheck all filter checkboxes
            document.querySelectorAll('.filter-check').forEach(checkbox => {
                checkbox.checked = false;
            });
            
            // Render all products
            renderProducts(categories[currentCategory]);
        }
        
        // Apply filters to products
        function applyFilters() {
            const products = categories[currentCategory];
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
                if (filterState.color.length > 0) {
                    let hasColor = false;
                    for (const color of filterState.color) {
                        if (product.colors.includes(color)) {
                            hasColor = true;
                            break;
                        }
                    }
                    if (!hasColor) return false;
                }
                
                // Price filter
                if (filterState.price.length > 0) {
                    // Calculate price ranges
                    let minPrice = Infinity;
                    let maxPrice = 0;
                    
                    products.forEach(p => {
                        if (p.price < minPrice) minPrice = p.price;
                        if (p.price > maxPrice) maxPrice = p.price;
                    });
                    
                    const mediumPrice = minPrice + (maxPrice - minPrice) / 3;
                    const highPrice = minPrice + (maxPrice - minPrice) * 2 / 3;
                    
                    let inRange = false;
                    for (const range of filterState.price) {
                        if (range === 'low' && product.price <= mediumPrice) {
                            inRange = true;
                            break;
                        } else if (range === 'medium' && product.price > mediumPrice && product.price <= highPrice) {
                            inRange = true;
                            break;
                        } else if (range === 'high' && product.price > highPrice) {
                            inRange = true;
                            break;
                        }
                    }
                    if (!inRange) return false;
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
            let sortedProducts = [...categories[currentCategory]];
            
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
            
            // Update products count
            document.querySelector('.products-count').textContent = `${productsToRender.length} artículos`;
        }
        
        // Change product color and name
        function changeProductColor(e) {
            const colorOption = e.target;
            const productId = parseInt(colorOption.dataset.product);
            const color = colorOption.dataset.color;
            const colorName = colorOption.dataset.colorName;
            
            // Find the product in the current category
            const product = categories[currentCategory].find(p => p.id === productId);
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
                case 'pink':
                    imgElement.style.filter = 'hue-rotate(320deg) saturate(200%)';
                    break;
                case 'purple':
                    imgElement.style.filter = 'hue-rotate(240deg)';
                    break;
                case 'green':
                    imgElement.style.filter = 'hue-rotate(80deg)';
                    break;
                case 'yellow':
                    imgElement.style.filter = 'hue-rotate(40deg) brightness(120%)';
                    break;
                case 'gray':
                    imgElement.style.filter = 'grayscale(100%)';
                    break;
            }
        }
        
        // Add product to cart
        function addToCart(e) {
            const button = e.target;
            const productId = parseInt(button.dataset.id);
            
            // Find the product in the current category
            const product = categories[currentCategory].find(p => p.id === productId);
            if (!product) return;
            
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
