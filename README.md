[8:25 a.m., 13/4/2026] Henry Palma: <!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Folkafe - Menú Digital</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Bebas+Neue&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #e63946; /* Rojo Tex-Mex */
            --dark-color: #1a1a1a;
            --light-color: #f8f9fa;
            --accent-color: #ffb703;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background-color: var(--light-color);
            color: var(--da…
[8:50 a.m., 13/4/2026] H3nrys: “Haz que el diseño sea similar a apps como Uber Eats o Rappi.”
[8:53 a.m., 13/4/2026] Henry Palma: <!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Folkafe | Pedir Online</title>
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --uber-green: #06C167;
            --rappi-orange: #FF441F;
            --bg-gray: #F6F6F6;
            --text-main: #000000;
            --text-muted: #545454;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Outfit', sans-serif;
            background-color: white;
            color: var(--text-main);
            padding-bottom: 80px;
        }

        /* Header Estilo App */
        header {
            padding: 20px;
            background: white;
            border-bottom: 1px solid #eee;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .brand {
            font-size: 24px;
            font-weight: 700;
            letter-spacing: -0.5px;
        }

        .delivery-info {
            font-size: 14px;
            color: var(--text-muted);
            margin-top: 4px;
        }

        /* Barra de Categorías Horizontal (Estilo Uber Eats) */
        .category-nav {
            display: flex;
            overflow-x: auto;
            white-space: nowrap;
            padding: 15px 20px;
            background: white;
            border-bottom: 1px solid #eee;
            gap: 20px;
            scrollbar-width: none;
        }
        .category-nav::-webkit-scrollbar { display: none; }

        .category-nav a {
            text-decoration: none;
            color: var(--text-main);
            font-weight: 600;
            font-size: 15px;
        }

        /* Contenedor de Productos */
        .section-container { padding: 20px; }

        .category-heading {
            font-size: 22px;
            font-weight: 700;
            margin: 20px 0 15px;
        }

        /* Card estilo Horizontal */
        .product-card {
            display: flex;
            justify-content: space-between;
            padding: 16px 0;
            border-bottom: 1px solid #eee;
            cursor: pointer;
            transition: background 0.2s;
        }

        .product-info {
            flex: 1;
            padding-right: 15px;
        }

        .product-name {
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 4px;
        }

        .product-desc {
            font-size: 14px;
            color: var(--text-muted);
            line-height: 1.3;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
            margin-bottom: 8px;
        }

        .product-price {
            font-weight: 600;
            font-size: 15px;
        }

        /* Imagen o Placeholder cuadrado lateral */
        .product-img {
            width: 100px;
            height: 100px;
            background: #eee;
            border-radius: 8px;
            position: relative;
            background-size: cover;
            background-position: center;
        }

        .add-btn {
            position: absolute;
            bottom: -8px;
            right: 10px;
            background: white;
            color: var(--uber-green);
            border: 1px solid #ddd;
            border-radius: 50%;
            width: 32px;
            height: 32px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            font-weight: bold;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        /* Botón Flotante de Carrito/WhatsApp */
        .cart-footer {
            position: fixed;
            bottom: 20px;
            left: 20px;
            right: 20px;
            background: var(--text-main);
            color: white;
            padding: 16px 24px;
            border-radius: 12px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            text-decoration: none;
            box-shadow: 0 4px 15px rgba(0,0,0,0.3);
            z-index: 1000;
        }

        .cart-footer:hover { transform: scale(1.02); transition: 0.2s; }

        @media (min-width: 768px) {
            .section-container {
                display: grid;
                grid-template-columns: 1fr 1fr;
                gap: 30px;
            }
        }
    </style>
</head>
<body>

<header>
    <div class="brand">Folkafe</div>
    <div class="delivery-info">Cerrado • Abre a las 17:00 • Lago Agrio</div>
</header>

<div class="category-nav">
    <a href="#hamburguesas">Hamburguesas</a>
    <a href="#entradas">Entradas</a>
    <a href="#tacos">Tacos</a>
    <a href="#alitas">Alitas</a>
    <a href="#bebidas">Bebidas</a>
</div>

<div class="section-container" id="main-menu">
    </div>

<a href="https://wa.me/593984592931" class="cart-footer" id="whatsapp-trigger">
    <span style="font-weight: 600;">Ver pedido</span>
    <span>Folkafe Online</span>
</a>

<script>
    const menuData = [
        {
            category: "Hamburguesas",
            id: "hamburguesas",
            items: [
                { name: "Normal", price: "3.50", desc: "Carne al grill, lechuga, cebolla, tomate y papas.", img: "🍔" },
                { name: "Champiñón y Mozzarella", price: "5.50", desc: "Tocino, champiñones salteados y mozzarella.", img: "🍄" },
                { name: "Folks Timer Burguer", price: "5.00", desc: "Cebolla salteada, tocino, queso cheddar y papas.", img: "🥓" },
                { name: "Big Mouth Burguer", price: "7.50", desc: "Doble carne, doble cheddar y tocino.", img: "🔥" }
            ]
        },
        {
            category: "Tacos & Más",
            id: "tacos",
            items: [
                { name: "Tacos Pork Carnitas", price: "5.00", desc: "Tacos de costilla de cerdo con sazón tex-mex.", img: "🌮" },
                { name: "Enchilada de Pollo", price: "6.50", desc: "Pollo ranchero, queso y crema agria.", img: "🥘" }
            ]
        },
        {
            category: "Entradas",
            id: "entradas",
            items: [
                { name: "Nachos Grande", price: "5.00", desc: "Chillicarne, pico de gallo, queso fundido y guacamole.", img: "🍟" },
                { name: "Chesse Poppers", price: "6.00", desc: "Bocaditos de mozzarella y cheddar con cilantro.", img: "🧀" }
            ]
        }
    ];

    const menuContainer = document.getElementById('main-menu');
    const whatsappBase = "https://wa.me/593984592931?text=";

    menuData.forEach(section => {
        const header = document.createElement('h2');
        header.className = 'category-heading';
        header.id = section.id;
        header.innerText = section.category;
        menuContainer.appendChild(header);

        section.items.forEach(item => {
            const card = document.createElement('div');
            card.className = 'product-card';
            const msg = encodeURIComponent(¡Hola! Quisiera ordenar: ${item.name} ($${item.price}));
            
            card.onclick = () => window.open(whatsappBase + msg, '_blank');

            card.innerHTML = `
                <div class="product-info">
                    <div class="product-name">${item.name}</div>
                    <div class="product-desc">${item.desc}</div>
                    <div class="product-price">$${item.price}</div>
                </div>
                <div class="product-img">
                    <span style="font-size:40px; position:absolute; top:25%; left:25%;">${item.img}</span>
                    <div class="add-btn">+</div>
                </div>
            `;
            menuContainer.appendChild(card);
        });
    });
</script>

</body>
</html>
