# avrilsportwear
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Avril Sport Wear - Termos Stanley y Accesorios</title>
  <style>
    /* Reset y base */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
    }
    body {
      background: #fafafa;
      color: #222;
      line-height: 1.6;
      font-weight: 300;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }
    a {
      color: #222;
      text-decoration: none;
      transition: color 0.3s ease;
    }
    a:hover {
      color: #bfa06a;
    }

    /* Contenedor principal */
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 1rem 3rem;
      flex-grow: 1;
    }

    /* Header */
    header {
      background: #fff;
      border-bottom: 1px solid #ddd;
      padding: 1rem 0;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 100;
    }
    .logo {
      font-weight: 700;
      font-size: 1.8rem;
      letter-spacing: 2px;
      color: #bfa06a;
      font-family: 'Georgia', serif;
    }
    nav ul {
      list-style: none;
      display: flex;
      gap: 2rem;
      font-weight: 500;
      font-size: 0.95rem;
    }
    nav ul li {
      position: relative;
    }
    nav ul li a {
      padding: 0.25rem 0;
      border-bottom: 2px solid transparent;
    }
    nav ul li a:hover,
    nav ul li a.active {
      border-bottom: 2px solid #bfa06a;
    }

    /* Banner envío gratis */
    .banner-envio {
      background: #bfa06a;
      color: #fff;
      text-align: center;
      font-weight: 600;
      padding: 0.5rem 1rem;
      font-size: 1rem;
      letter-spacing: 1px;
    }

    /* Hero / Edición de verano */
    .hero {
      background: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1350&q=80') center/cover no-repeat;
      height: 400px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      color: #fff;
      text-shadow: 0 0 10px rgba(0,0,0,0.7);
      margin-bottom: 3rem;
      border-radius: 8px;
      position: relative;
      overflow: hidden;
    }
    .hero::after {
      content: "";
      position: absolute;
      inset: 0;
      background: rgba(0,0,0,0.3);
      z-index: 0;
    }
    .hero-content {
      position: relative;
      z-index: 1;
      text-align: center;
      max-width: 600px;
      padding: 0 1rem;
    }
    .hero h1 {
      font-size: 3rem;
      font-weight: 700;
      margin-bottom: 1rem;
      font-family: 'Georgia', serif;
    }
    .hero p {
      font-size: 1.25rem;
      margin-bottom: 2rem;
      font-weight: 400;
    }
    .btn-primary {
      background: #bfa06a;
      color: #fff;
      padding: 0.75rem 2rem;
      font-weight: 600;
      font-size: 1.1rem;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      transition: background 0.3s ease;
      text-transform: uppercase;
      letter-spacing: 1.5px;
      box-shadow: 0 4px 8px rgba(191,160,106,0.4);
    }
    .btn-primary:hover {
      background: #a88c44;
      box-shadow: 0 6px 12px rgba(168,140,68,0.6);
    }

    /* Sección productos */
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(280px,1fr));
      gap: 2rem;
      margin-bottom: 3rem;
    }
    .product-card {
      background: #fff;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
      overflow: hidden;
      display: flex;
      flex-direction: column;
      transition: transform 0.3s ease;
    }
    .product-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 20px rgba(0,0,0,0.1);
    }
    .product-image {
      width: 100%;
      aspect-ratio: 4 / 3;
      object-fit: cover;
    }
    .product-info {
      padding: 1rem 1.25rem 1.5rem;
      flex-grow: 1;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    .product-title {
      font-weight: 600;
      font-size: 1.1rem;
      margin-bottom: 0.5rem;
      color: #333;
      font-family: 'Georgia', serif;
    }
    .product-desc {
      font-size: 0.9rem;
      color: #666;
      margin-bottom: 1rem;
      flex-grow: 1;
    }
    .product-price {
      font-weight: 700;
      font-size: 1.15rem;
      color: #bfa06a;
      margin-bottom: 1rem;
    }
    .btn-secondary {
      background: transparent;
      border: 2px solid #bfa06a;
      color: #bfa06a;
      padding: 0.5rem 1.5rem;
      font-weight: 600;
      border-radius: 30px;
      cursor: pointer;
      text-transform: uppercase;
      letter-spacing: 1.2px;
      transition: all 0.3s ease;
      align-self: flex-start;
    }
    .btn-secondary:hover {
      background: #bfa06a;
      color: #fff;
      box-shadow: 0 4px 12px rgba(191,160,106,0.5);
    }

    /* Footer */
    footer {
      background: #222;
      color: #bbb;
      text-align: center;
      padding: 2rem 1rem;
      font-size: 0.9rem;
      letter-spacing: 0.5px;
      margin-top: auto;
    }
    footer a {
      color: #bfa06a;
      text-decoration: none;
    }
    footer a:hover {
      text-decoration: underline;
    }

    /* Suscripción */
    .subscribe {
      background: #fff;
      border-radius: 8px;
      padding: 2rem 1.5rem;
      max-width: 480px;
      margin: 0 auto 3rem;
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
      text-align: center;
    }
    .subscribe h2 {
      font-family: 'Georgia', serif;
      font-weight: 700;
      font-size: 1.8rem;
      margin-bottom: 1rem;
      color: #222;
    }
    .subscribe p {
      font-size: 1rem;
      margin-bottom: 1.5rem;
      color: #555;
    }
    .subscribe form {
      display: flex;
      gap: 0.5rem;
      justify-content: center;
      flex-wrap: wrap;
    }
    .subscribe input[type="email"] {
      padding: 0.75rem 1rem;
      font-size: 1rem;
      border: 1.5px solid #ccc;
      border-radius: 30px;
      flex-grow: 1;
      min-width: 220px;
      transition: border-color 0.3s ease;
    }
    .subscribe input[type="email"]:focus {
      outline: none;
      border-color: #bfa06a;
      box-shadow: 0 0 8px rgba(191,160,106,0.5);
    }
    .subscribe button {
      background: #bfa06a;
      border: none;
      color: #fff;
      padding: 0.75rem 1.8rem;
      font-weight: 600;
      font-size: 1rem;
      border-radius: 30px;
      cursor: pointer;
      transition: background 0.3s ease;
      text-transform: uppercase;
      letter-spacing: 1.2px;
    }
    .subscribe button:hover {
      background: #a88c44;
    }

    /* Responsive */
    @media (max-width: 600px) {
      header {
        flex-direction: column;
        gap: 0.5rem;
      }
      nav ul {
        flex-wrap: wrap;
        justify-content: center;
        gap: 1rem;
      }
      .hero h1 {
        font-size: 2.2rem;
      }
      .hero p {
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>
  <div class="banner-envio">ENVÍO GRATIS A PARTIR DE $50</div>
  <header>
    <div class="logo">Avril Sport Wear</div>
    <nav>
      <ul>
        <li><a href="#" class="active">Inicio</a></li>
        <li><a href="#productos">Productos</a></li>
        <li><a href="#accesorios">Accesorios</a></li>
        <li><a href="#repuestos">Repuestos</a></li>
        <li><a href="#contacto">Contacto</a></li>
      </ul>
    </nav>
  </header>

  <main class="container">
    <section class="hero" aria-label="Edición de verano - Comprar ahora">
      <div class="hero-content">
        <h1>EDICIÓN DE VERANO</h1>
        <p>Descubre los termos Stanley con diseño exclusivo y accesorios únicos.</p>
        <button class="btn-primary" onclick="alert('Redirigiendo a la tienda...')">COMPRAR AHORA</button>
      </div>
    </section>

    <section id="productos">
      <h2 style="font-family: 'Georgia', serif; font-weight: 700; font-size: 2rem; margin-bottom: 1.5rem; color: #222;">Productos Destacados</h2>
      <div class="products">
        <article class="product-card" tabindex="0" aria-label="Termo Stanley Stay-Hot Camp Mug Mocha Latte 24oz">
          <img src="https://cdn.shopify.com/s/files/1/0267/4327/4791/products/stanley-stay-hot-camp-mug-mocha-latte-24oz_600x.jpg?v=1661367890" alt="Termo Stanley Stay-Hot Camp Mug Mocha Latte 24oz" class="product-image" />
          <div class="product-info">
            <h3 class="product-title">Stay-Hot Camp Mug - Mocha Latte 24oz</h3>
            <p class="product-desc">Mantiene tu bebida caliente por horas con estilo y elegancia.</p>
            <div class="product-price">$28.00</div>
            <button class="btn-secondary" onclick="alert('Añadido Stay-Hot Camp Mug al carrito')">Comprar</button>
          </div>
        </article>

        <article class="product-card" tabindex="0" aria-label="Vaso Stanley IceFlow Flip Straw Tumbler Mocha Latte 30oz">
          <img src="https://cdn.shopify.com/s/files/1/0267/4327/4791/products/stanley-iceflow-flip-straw-tumbler-mocha-latte-30oz_600x.jpg?v=1661367890" alt="Vaso Stanley IceFlow Flip Straw Tumbler Mocha Latte 30oz" class="product-image" />
          <div class="product-info">
            <h3 class="product-title">IceFlow™ Flip Straw Tumbler - Mocha Latte 30oz</h3>
            <p class="product-desc">Disfruta de tus bebidas frías con comodidad y diseño sofisticado.</p>
            <div class="product-price">$35.00</div>
            <button class="btn-secondary" onclick="alert('Añadido IceFlow Flip Straw Tumbler al carrito')">Comprar</button>
          </div>
        </article>

        <article class="product-card" tabindex="0" aria-label="Botella Stanley AeroLight Transit Mocha Latte 24oz">
          <img src="https://cdn.shopify.com/s/files/1/0267/4327/4791/products/stanley-aerolight-transit-bottle-mocha-latte-24oz_600x.jpg?v=1661367890" alt="Botella Stanley AeroLight Transit Mocha Latte 24oz" class="product-image" />
          <div class="product-info">
            <h3 class="product-title">AeroLight™ Transit Bottle - Mocha Latte 24oz</h3>
            <p class="product-desc">Ligera, elegante y perfecta para tus aventuras al aire libre.</p>
            <div class="product-price">$40.00</div>
            <button class="btn-secondary" onclick="alert('Añadido AeroLight Transit Bottle al carrito')">Comprar</button>
          </div>
        </article>
      </div>
    </section>

    <section id="accesorios" style="margin-top: 4rem;">
      <h2 style="font-family: 'Georgia', serif; font-weight: 700; font-size: 2rem; margin-bottom: 1.5rem; color: #222;">Accesorios</h2>
      <div class="products">
        <article class="product-card" tabindex="0" aria-label="Pajita IceFlow Flip para vaso Stanley">
          <img src="https://cdn.shopify.com/s/files/1/0267/4327/4791/products/stanley-iceflow-flip-straw_600x.jpg?v=1661367890" alt="Pajita IceFlow Flip para vaso Stanley" class="product-image" />
          <div class="product-info">
            <h3 class="product-title">Pajita IceFlow™ Flip</h3>
            <p class="product-desc">Complemento ideal para tus vasos Stanley, fácil de usar y limpiar.</p>
            <div class="product-price">$5.00</div>
            <button class="btn-secondary" onclick="alert('Añadido Pajita IceFlow Flip al carrito')">Comprar</button>
          </div>
        </article>

        <article class="product-card" tabindex="0" aria-label="Tapa Stay-Hot para termo Stanley">
          <img src="https://cdn.shopify.com/s/files/1/0267/4327/4791/products/stanley-stay-hot-lid_600x.jpg?v=1661367890" alt="Tapa Stay-Hot para termo Stanley" class="product-image" />
          <div class="product-info">
            <h3 class="product-title">Tapa Stay-Hot</h3>
            <p class="product-desc">Repuesto original para mantener la temperatura y evitar derrames.</p>
            <div class="product-price">$8.00</div>
            <button class="btn-secondary" onclick="alert('Añadido Tapa Stay-Hot al carrito')">Comprar</button>
          </div>
        </article>
      </div>
    </section>

    <section id="repuestos" style="margin-top: 4rem;">
      <h2 style="font-family: 'Georgia', serif; font-weight: 700; font-size: 2rem; margin-bottom: 1.5rem; color: #222;">Repuestos</h2>
      <div class="products">
        <article class="product-card" tabindex="0" aria-label="Junta de silicona para termo Stanley">
          <img src="https://cdn.shopify.com/s/files/1/0267/4327/4791/products/stanley-silicone-gasket_600x.jpg?v=1661367890" alt="Junta de silicona para termo Stanley" class="product-image" />
          <div class="product-info">
            <h3 class="product-title">Junta de Silicona</h3>
            <p class="product-desc">Repuesto para asegurar el sellado perfecto de tu termo Stanley.</p>
            <div class="product-price">$3.50</div>
            <button class="btn-secondary" onclick="alert('Añadido Junta de Silicona al carrito')">Comprar</button>
          </div>
        </article>

        <article class="product-card" tabindex="0" aria-label="Filtro para botella Stanley AeroLight">
          <img src="https://cdn.shopify.com/s/files/1/0267/4327/4791/products/stanley-filter_600x.jpg?v=1661367890" alt="Filtro para botella Stanley AeroLight" class="product-image" />
          <div class="product-info">
            <h3 class="product-title">Filtro AeroLight</h3>
            <p class="product-desc">Mantén tu agua limpia y fresca con este filtro original Stanley.</p>
            <div class="product-price">$7.00</div>
            <button class="btn-secondary" onclick="alert('Añadido Filtro AeroLight al carrito')">Comprar</button>
          </div>
        </article>
     
