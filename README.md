[3d.html](https://github.com/user-attachments/files/29357483/3d.html)

<html lang="uk">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ремонт Апаратів Bianchi | Premium сервіс</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Raleway:wght@300;400;500;600&display=swap" rel="stylesheet" />
    <style>
        /* ============================================================
           RESET & VARIABLES
        ============================================================ */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #7e57c2;
            --primary-dark: #673ab7;
            --primary-light: #b085f5;
            --accent: #ff4081;
            --accent-neon: #ff2a92;
            --text-light: #f5f5f5;
            --bg-dark: #1a1a2e;
            --bg-card: #2d2b55;
            --shadow: 0 5px 20px rgba(0, 0, 0, 0.4);
            --radius: 16px;
            --transition: 0.3s ease;
            --header-height: 80px;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: var(--bg-dark);
            color: var(--text-light);
            font-family: 'Raleway', sans-serif;
            line-height: 1.7;
            padding-top: var(--header-height);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* ============================================================
           HEADER
        ============================================================ */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(26, 26, 46, 0.92);
            backdrop-filter: blur(12px);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 30px;
            height: var(--header-height);
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.6);
            transition: box-shadow var(--transition);
        }

        header.scrolled {
            box-shadow: 0 2px 40px rgba(0, 0, 0, 0.8);
        }

        .logo {
            font-family: 'Montserrat', sans-serif;
            font-size: 26px;
            font-weight: 700;
            background: linear-gradient(45deg, var(--primary-light), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: -0.5px;
            flex-shrink: 0;
        }
        .logo span {
            font-weight: 300;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 8px;
        }

        nav ul li a {
            color: var(--text-light);
            text-decoration: none;
            font-weight: 500;
            padding: 8px 18px;
            border-radius: 30px;
            transition: var(--transition);
            font-size: 0.95rem;
        }

        nav ul li a:hover,
        nav ul li a:focus {
            color: var(--primary-light);
            background: rgba(255, 255, 255, 0.06);
        }

        .header-right {
            display: flex;
            align-items: center;
            gap: 18px;
            flex-shrink: 0;
        }

        .language-switcher {
            display: flex;
            gap: 6px;
        }

        .language-switcher button {
            background: rgba(255, 255, 255, 0.08);
            border: 1px solid rgba(255, 255, 255, 0.15);
            color: #ccc;
            padding: 4px 12px;
            border-radius: 20px;
            cursor: pointer;
            font-size: 0.8rem;
            transition: var(--transition);
            font-family: inherit;
        }

        .language-switcher button.active {
            background: linear-gradient(45deg, var(--primary), var(--accent));
            color: #fff;
            border-color: transparent;
        }

        .language-switcher button:hover {
            background: rgba(255, 255, 255, 0.15);
        }

        .cart-icon {
            font-size: 26px;
            cursor: pointer;
            position: relative;
            transition: transform var(--transition);
        }
        .cart-icon:hover {
            transform: scale(1.08);
        }

        .cart-count {
            background: var(--accent);
            border-radius: 50%;
            padding: 1px 8px;
            font-size: 13px;
            font-weight: 700;
            position: absolute;
            top: -10px;
            right: -14px;
            min-width: 22px;
            text-align: center;
        }

        /* ============================================================
           HAMBURGER (mobile)
        ============================================================ */
        .hamburger {
            display: none;
            flex-direction: column;
            gap: 5px;
            background: none;
            border: none;
            cursor: pointer;
            padding: 6px;
        }
        .hamburger span {
            display: block;
            width: 28px;
            height: 3px;
            background: #fff;
            border-radius: 4px;
            transition: var(--transition);
        }
        .hamburger.active span:nth-child(1) {
            transform: rotate(45deg) translate(5px, 5px);
        }
        .hamburger.active span:nth-child(2) {
            opacity: 0;
        }
        .hamburger.active span:nth-child(3) {
            transform: rotate(-45deg) translate(5px, -5px);
        }

        /* ============================================================
           HERO
        ============================================================ */
        .hero {
            min-height: 70vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 40px 20px;
            background: radial-gradient(circle at 20% 30%, rgba(126, 87, 194, 0.15), transparent 60%),
                radial-gradient(circle at 80% 70%, rgba(255, 64, 129, 0.10), transparent 50%);
        }

        .hero h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: clamp(2.2rem, 6vw, 4rem);
            background: linear-gradient(135deg, var(--primary-light), var(--accent-neon));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            max-width: 800px;
            margin-bottom: 16px;
        }

        .hero p {
            font-size: clamp(1rem, 1.4vw, 1.25rem);
            color: rgba(255, 255, 255, 0.8);
            max-width: 640px;
            margin-bottom: 28px;
        }

        .btn {
            background: linear-gradient(45deg, var(--primary), var(--accent));
            color: #fff;
            padding: 14px 38px;
            border-radius: 40px;
            font-weight: 600;
            border: none;
            cursor: pointer;
            transition: var(--transition);
            font-family: inherit;
            font-size: 1rem;
            box-shadow: 0 4px 20px rgba(126, 87, 194, 0.35);
            display: inline-block;
            text-decoration: none;
        }

        .btn:hover,
        .btn:focus {
            transform: translateY(-3px);
            box-shadow: 0 8px 30px rgba(126, 87, 194, 0.5);
        }

        .btn:active {
            transform: translateY(0);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary-light);
            box-shadow: none;
        }
        .btn-outline:hover {
            background: rgba(126, 87, 194, 0.15);
        }

        /* ============================================================
           SECTIONS
        ============================================================ */
        .section {
            padding: 70px 0;
        }

        .section-title {
            text-align: center;
            font-size: clamp(1.8rem, 4vw, 2.6rem);
            margin-bottom: 50px;
            font-weight: 600;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            margin: 14px auto 0;
            border-radius: 4px;
        }

        /* ============================================================
           BLOG
        ============================================================ */
        .blog {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .blog-post {
            background: var(--bg-card);
            border-radius: var(--radius);
            overflow: hidden;
            transition: var(--transition);
            box-shadow: var(--shadow);
        }

        .blog-post:hover {
            transform: translateY(-6px);
            box-shadow: 0 12px 40px rgba(0, 0, 0, 0.5);
        }

        .blog-post img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            display: block;
        }

        .blog-content {
            padding: 22px 24px 26px;
        }

        .blog-content .date {
            font-size: 0.85rem;
            color: rgba(255, 255, 255, 0.5);
            display: block;
            margin-bottom: 6px;
        }

        .blog-content h3 {
            font-size: 1.2rem;
            margin-bottom: 8px;
        }

        .blog-content p {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.95rem;
            margin-bottom: 16px;
        }

        .read-more {
            color: var(--primary-light);
            text-decoration: none;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: var(--transition);
        }

        .read-more:hover {
            color: var(--accent);
            gap: 12px;
        }

        /* ============================================================
           SERVICES
        ============================================================ */
        .services {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 28px;
        }

        .service {
            background: var(--bg-card);
            border-radius: var(--radius);
            padding: 32px 24px;
            text-align: center;
            transition: var(--transition);
            box-shadow: var(--shadow);
        }

        .service:hover {
            transform: translateY(-4px);
        }

        .service i {
            font-size: 44px;
            color: var(--primary-light);
            margin-bottom: 16px;
        }

        .service h3 {
            font-size: 1.15rem;
            margin-bottom: 8px;
        }

        .service p {
            font-size: 0.95rem;
            color: rgba(255, 255, 255, 0.7);
        }

        /* ============================================================
           CATALOG
        ============================================================ */
        .catalog-categories {
            display: flex;
            justify-content: center;
            gap: 14px;
            margin-bottom: 36px;
            flex-wrap: wrap;
        }

        .catalog-categories .btn {
            font-size: 0.95rem;
            padding: 10px 26px;
            background: rgba(255, 255, 255, 0.06);
            border: 1px solid rgba(255, 255, 255, 0.12);
            box-shadow: none;
        }

        .catalog-categories .btn.active {
            background: linear-gradient(45deg, var(--primary), var(--accent));
            border-color: transparent;
            box-shadow: 0 4px 20px rgba(126, 87, 194, 0.35);
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
            gap: 26px;
        }

        .product-card {
            background: var(--bg-card);
            border-radius: var(--radius);
            overflow: hidden;
            display: flex;
            flex-direction: column;
            transition: var(--transition);
            box-shadow: var(--shadow);
        }

        .product-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 12px 40px rgba(0, 0, 0, 0.5);
        }

        .product-card img {
            width: 100%;
            height: 180px;
            object-fit: cover;
            display: block;
            background: #1a1a2e;
        }

        .product-card .info {
            padding: 18px 20px 22px;
            flex: 1;
            display: flex;
            flex-direction: column;
        }

        .product-card .info h3 {
            font-size: 1.05rem;
            margin-bottom: 4px;
        }

        .product-card .info p {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.65);
            margin-bottom: 10px;
            flex: 1;
        }

        .product-card .price {
            font-size: 1.25rem;
            font-weight: 700;
            color: var(--accent-neon);
            margin-bottom: 12px;
        }

        .product-card .btn {
            width: 100%;
            padding: 12px;
            font-size: 0.95rem;
        }

        /* ============================================================
           PAGINATION
        ============================================================ */
        .pagination {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 8px;
            margin-top: 40px;
            flex-wrap: wrap;
        }

        .pagination button {
            background: rgba(255, 255, 255, 0.06);
            border: 1px solid rgba(255, 255, 255, 0.12);
            color: #ccc;
            padding: 8px 16px;
            border-radius: 8px;
            cursor: pointer;
            transition: var(--transition);
            font-family: inherit;
            font-size: 0.9rem;
        }

        .pagination button.active {
            background: linear-gradient(45deg, var(--primary), var(--accent));
            border-color: transparent;
            color: #fff;
        }

        .pagination button:hover:not(.active) {
            background: rgba(255, 255, 255, 0.12);
        }

        .pagination button:disabled {
            opacity: 0.3;
            cursor: not-allowed;
        }

        /* ============================================================
           CONTACT
        ============================================================ */
        .contact-info {
            max-width: 600px;
            margin: 0 auto;
            background: var(--bg-card);
            border-radius: var(--radius);
            padding: 40px;
            text-align: center;
            box-shadow: var(--shadow);
        }

        .contact-info h3 {
            font-size: 1.3rem;
            margin-bottom: 18px;
        }

        .contact-info p {
            margin: 8px 0;
            font-size: 1.05rem;
        }

        .contact-info i {
            color: var(--primary-light);
            width: 28px;
            margin-right: 6px;
        }

        .contact-info a {
            color: var(--text-light);
            text-decoration: none;
            transition: var(--transition);
        }
        .contact-info a:hover {
            color: var(--primary-light);
        }

        /* ============================================================
           CART MODAL
        ============================================================ */
        .cart-modal {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, 0.75);
            backdrop-filter: blur(6px);
            z-index: 2000;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .cart-modal.active {
            display: flex;
        }

        .cart-content {
            background: var(--bg-card);
            border-radius: var(--radius);
            padding: 28px 30px 32px;
            max-width: 680px;
            width: 100%;
            max-height: 90vh;
            overflow-y: auto;
            position: relative;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.7);
            animation: fadeUp 0.25s ease;
        }

        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .cart-content .close-btn {
            position: absolute;
            top: 14px;
            right: 20px;
            background: none;
            border: none;
            color: #fff;
            font-size: 1.6rem;
            cursor: pointer;
            transition: var(--transition);
            line-height: 1;
        }
        .cart-content .close-btn:hover {
            transform: rotate(90deg);
            color: var(--accent);
        }

        .cart-items {
            list-style: none;
            margin: 12px 0;
        }

        .cart-item {
            display: flex;
            gap: 16px;
            align-items: center;
            padding: 14px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.06);
        }

        .cart-item:last-child {
            border-bottom: none;
        }

        .cart-item-img {
            width: 64px;
            height: 64px;
            object-fit: cover;
            border-radius: 10px;
            background: #1a1a2e;
            flex-shrink: 0;
        }

        .cart-item-info {
            flex: 1;
            min-width: 0;
        }
        .cart-item-info strong {
            display: block;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        .cart-item-info small {
            color: rgba(255, 255, 255, 0.6);
        }

        .cart-item-controls {
            display: flex;
            align-items: center;
            gap: 8px;
            flex-shrink: 0;
        }

        .qty-btn {
            background: rgba(255, 255, 255, 0.08);
            border: none;
            color: #fff;
            width: 32px;
            height: 32px;
            border-radius: 50%;
            cursor: pointer;
            transition: var(--transition);
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .qty-btn:hover {
            background: var(--primary);
        }

        .remove {
            background: none;
            border: none;
            color: rgba(255, 255, 255, 0.3);
            cursor: pointer;
            font-size: 1.1rem;
            transition: var(--transition);
            padding: 4px;
        }
        .remove:hover {
            color: var(--accent);
        }

        .cart-total {
            text-align: right;
            font-size: 1.4rem;
            font-weight: 700;
            color: var(--accent-neon);
            margin: 16px 0 10px;
        }

        /* ============================================================
           ORDER FORM
        ============================================================ */
        .order-form label {
            display: block;
            margin-top: 14px;
            margin-bottom: 4px;
            font-weight: 500;
            font-size: 0.95rem;
        }

        .order-form input,
        .order-form select {
            width: 100%;
            padding: 12px 16px;
            border-radius: 10px;
            border: 1px solid rgba(255, 255, 255, 0.12);
            background: rgba(0, 0, 0, 0.35);
            color: #fff;
            font-size: 1rem;
            font-family: inherit;
            transition: var(--transition);
        }

        .order-form input:focus,
        .order-form select:focus {
            outline: none;
            border-color: var(--primary-light);
            box-shadow: 0 0 0 3px rgba(126, 87, 194, 0.2);
        }

        .order-form .radio-group {
            display: flex;
            gap: 18px;
            margin: 8px 0 12px;
            flex-wrap: wrap;
        }

        .order-form .radio-group label {
            display: flex;
            align-items: center;
            gap: 6px;
            font-weight: 400;
            margin: 0;
            cursor: pointer;
        }

        .order-form .radio-group input[type="radio"] {
            width: auto;
            accent-color: var(--primary-light);
        }

        .back-to-cart {
            background: none;
            border: none;
            color: var(--primary-light);
            cursor: pointer;
            font-size: 0.95rem;
            padding: 0;
            margin-bottom: 14px;
            transition: var(--transition);
            font-family: inherit;
        }

        .back-to-cart:hover {
            color: var(--accent);
        }

        /* ============================================================
           FOOTER
        ============================================================ */
        footer {
            text-align: center;
            padding: 36px 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.06);
            color: rgba(255, 255, 255, 0.4);
            font-size: 0.9rem;
        }

        /* ============================================================
           RESPONSIVE
        ============================================================ */
        @media (max-width: 992px) {
            :root {
                --header-height: 70px;
            }

            header {
                padding: 10px 18px;
                flex-wrap: wrap;
            }

            .hamburger {
                display: flex;
            }

            nav {
                display: none;
                width: 100%;
                order: 3;
                padding-top: 12px;
            }

            nav.open {
                display: block;
            }

            nav ul {
                flex-direction: column;
                align-items: center;
                gap: 4px;
            }

            nav ul li a {
                display: block;
                padding: 10px 20px;
                width: 100%;
                text-align: center;
                border-radius: 10px;
            }
        }

        @media (max-width: 600px) {
            .header-right {
                gap: 10px;
            }

            .language-switcher button {
                font-size: 0.7rem;
                padding: 3px 10px;
            }

            .cart-icon {
                font-size: 22px;
            }

            .hero {
                min-height: 60vh;
                padding: 30px 16px;
            }

            .section {
                padding: 40px 0;
            }

            .contact-info {
                padding: 26px 18px;
            }

            .cart-content {
                padding: 20px 16px 24px;
            }

            .cart-item {
                flex-wrap: wrap;
            }

            .cart-item-controls {
                margin-left: auto;
            }
        }
    </style>
</head>
<body>

    <!-- ============================================================
    HEADER
    ============================================================ -->
    <header id="mainHeader">
        <div class="logo">BIANCHI<span>PROF</span></div>

        <button class="hamburger" id="hamburger" aria-label="Toggle navigation">
            <span></span><span></span><span></span>
        </button>

        <nav id="mainNav">
            <ul>
                <li><a href="#blog" data-lang-key="blog">Блог</a></li>
                <li><a href="#services" data-lang-key="services">Послуги</a></li>
                <li><a href="#products" data-lang-key="products">Каталог</a></li>
                <li><a href="#contact" data-lang-key="contact">Контакти</a></li>
            </ul>
        </nav>

        <div class="header-right">
            <div class="language-switcher">
                <button class="active" data-lang="uk" aria-label="Українська">UA</button>
                <button data-lang="ru" aria-label="Русский">RU</button>
            </div>
            <div class="cart-icon" id="cartIcon" role="button" aria-label="Кошик" tabindex="0">
                <i class="fas fa-shopping-cart"></i>
                <span class="cart-count" id="cartCount">0</span>
            </div>
        </div>
    </header>

    <!-- ============================================================
    CART MODAL
    ============================================================ -->
    <div class="cart-modal" id="cartModal" role="dialog" aria-modal="true" aria-label="Кошик">
        <div class="cart-content" id="cartContent"></div>
    </div>

    <!-- ============================================================
    HERO
    ============================================================ -->
    <section class="hero" id="home">
        <h1 data-lang-key="heroTitle">Преміум сервіс для апаратів Bianchi</h1>
        <p data-lang-key="heroText">Професійний ремонт, обслуговування та запчастини для вендингових апаратів італійського виробника. Гарантія якості та швидкий виїзд майстра.</p>
        <a href="#contact" class="btn" data-lang-key="contactUs">Зв'язатися з нами</a>
    </section>

    <!-- ============================================================
    BLOG
    ============================================================ -->
    <section id="blog" class="section">
        <div class="container">
            <h2 class="section-title" data-lang-key="ourBlog">Останні публікації</h2>
            <div class="blog">
                <article class="blog-post">
                    <img src="https://images.unsplash.com/photo-1495474472287-4d71bcdd2085?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Догляд за апаратом" loading="lazy" />
                    <div class="blog-content">
                        <span class="date">15 травня 2023</span>
                        <h3 data-lang-key="blogTitle1">Як правильно доглядати за апаратом Bianchi</h3>
                        <p data-lang-key="blogDesc1">Поради щодо регулярного обслуговування та догляду за вашим апаратом для продовження терміну служби.</p>
                        <a href="#" class="read-more" data-lang-key="readMore">Детальніше <i class="fas fa-arrow-right"></i></a>
                    </div>
                </article>
                <article class="blog-post">
                    <img src="https://images.unsplash.com/photo-1559056199-641a0ac8b55e?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Поширені поломки" loading="lazy" />
                    <div class="blog-content">
                        <span class="date">2 червня 2023</span>
                        <h3 data-lang-key="blogTitle2">Найпоширеніші поломки апаратів Bianchi</h3>
                        <p data-lang-key="blogDesc2">Огляд типових проблем, з якими стикаються власники апаратів Bianchi та способи їх вирішення.</p>
                        <a href="#" class="read-more" data-lang-key="readMore">Детальніше <i class="fas fa-arrow-right"></i></a>
                    </div>
                </article>
                <article class="blog-post">
                    <img src="https://images.unsplash.com/photo-1517433670267-08bbd4be890f?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Оновлення моделей" loading="lazy" />
                    <div class="blog-content">
                        <span class="date">28 червня 2023</span>
                        <h3 data-lang-key="blogTitle3">Оновлення модельного ряду Bianchi 2026</h3>
                        <p data-lang-key="blogDesc3">Огляд нових моделей апаратів Bianchi, їх переваги та вдосконалення в порівнянні з попередніми версіями.</p>
                        <a href="#" class="read-more" data-lang-key="readMore">Детальніше <i class="fas fa-arrow-right"></i></a>
                    </div>
                </article>
            </div>
        </div>
    </section>

    <!-- ============================================================
    SERVICES
    ============================================================ -->
    <section id="services" class="section">
        <div class="container">
            <h2 class="section-title" data-lang-key="ourServices">Наші послуги</h2>
            <div class="services">
                <div class="service">
                    <i class="fas fa-money-bill-wave"></i>
                    <h3 data-lang-key="service1">Ремонт платіжної системи</h3>
                    <p data-lang-key="service1Desc">Усунення несправностей купюроприймачів, монетоприймачів, банківських терміналів.</p>
                </div>
                <div class="service">
                    <i class="fas fa-truck"></i>
                    <h3 data-lang-key="service2">Виїзд до апарата</h3>
                    <p data-lang-key="service2Desc">Швидкий виїзд майстра на об'єкт для діагностики та ремонту.</p>
                </div>
                <div class="service">
                    <i class="fas fa-search"></i>
                    <h3 data-lang-key="service3">Діагностика</h3>
                    <p data-lang-key="service3Desc">Повна перевірка апарата, виявлення несправностей та консультація.</p>
                </div>
                <div class="service">
                    <i class="fas fa-microchip"></i>
                    <h3 data-lang-key="service4">Прошивка та ремонт плат</h3>
                    <p data-lang-key="service4Desc">Оновлення програмного забезпечення та ремонт електронних компонентів.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ============================================================
    CATALOG
    ============================================================ -->
    <section id="products" class="section">
        <div class="container">
            <h2 class="section-title" data-lang-key="ourProducts">Наші товари</h2>
            <div class="catalog-categories" id="catalogButtons">
                <button class="btn active" data-category="parts" data-lang-key="product1">Запчастини</button>
                <button class="btn" data-category="dispensers" data-lang-key="product2">Диспенсери для стаканів</button>
                <button class="btn" data-category="machines" data-lang-key="product3">Апарати Bianchi</button>
            </div>
            <div class="products-grid" id="productsGrid"></div>
            <div class="pagination" id="paginationControls"></div>
        </div>
    </section>

    <!-- ============================================================
    CONTACT
    ============================================================ -->
    <section id="contact" class="section">
        <div class="container">
            <h2 class="section-title" data-lang-key="contactUs">Контактна інформація</h2>
            <div class="contact-info">
                <h3 data-lang-key="contactText">Зв'яжіться з нами для консультації чи ремонту</h3>
                <p><i class="fas fa-phone"></i> <a href="tel:+380634407365">+38 (063) 440-73-65</a></p>
                <p><i class="fas fa-envelope"></i> <a href="mailto:ssalamov2106.ss@gmail.com">ssalamov2106.ss@gmail.com</a></p>
                <p><i class="fas fa-map-marker-alt"></i> Обслуговуємо Харків та область</p>
                <p><i class="fas fa-clock"></i> Пн-Пт: 9:00 – 18:00, Сб: 10:00 – 16:00</p>
            </div>
        </div>
    </section>

    <!-- ============================================================
    FOOTER
    ============================================================ -->
    <footer>
        <div class="container">&copy; 2025 Сервісний центр BianchiPRO</div>
    </footer>

    <!-- ============================================================
    JAVASCRIPT
    ============================================================ -->
    <script>
        // ============================================================
        // 1. TRANSLATIONS
        // ============================================================
        const TRANSLATIONS = {
            uk: {
                blog: 'Блог',
                services: 'Послуги',
                products: 'Каталог',
                contact: 'Контакти',
                heroTitle: 'Преміум сервіс для апаратів Bianchi',
                heroText: 'Професійний ремонт, обслуговування та запчастини для вендингових апаратів італійського виробника. Гарантія якості та швидкий виїзд майстра.',
                contactUs: 'Зв\'язатися з нами',
                ourServices: 'Наші послуги',
                service1: 'Ремонт платіжної системи',
                service1Desc: 'Усунення несправностей купюроприймачів, монетоприймачів, банківських терміналів.',
                service2: 'Виїзд до апарата',
                service2Desc: 'Швидкий виїзд майстра на об\'єкт для діагностики та ремонту.',
                service3: 'Діагностика',
                service3Desc: 'Повна перевірка апарата, виявлення несправностей та консультація.',
                service4: 'Прошивка та ремонт плат',
                service4Desc: 'Оновлення програмного забезпечення та ремонт електронних компонентів.',
                ourProducts: 'Наші товари',
                product1: 'Запчастини',
                product2: 'Диспенсери для стаканів',
                product3: 'Апарати Bianchi',
                cartTitle: 'Кошик',
                buyBtn: 'В кошик',
                cartEmpty: 'Кошик порожній',
                total: 'Загалом',
                remove: 'Видалити',
                checkout: 'Оформити замовлення',
                back: '← Назад до кошика',
                orderTitle: 'Оформлення замовлення',
                fio: 'ПІБ',
                fioPlaceholder: 'Прізвище Ім\'я По-батькові',
                phone: 'Телефон',
                phonePlaceholder: '+38',
                city: 'Місто',
                cityPlaceholder: 'Введіть місто',
                delivery: 'Спосіб доставки',
                pickCourier: 'Нова Пошта',
                pickUkr: 'Укрпошта',
                pickSelf: 'Самовивіз',
                department: 'Відділення',
                departmentPlaceholder: 'Номер або адреса відділення',
                confirmOrder: 'Підтвердити замовлення',
                success: '✅ Замовлення успішно надіслано!',
                ourBlog: 'Останні публікації',
                blogTitle1: 'Як правильно доглядати за апаратом Bianchi',
                blogDesc1: 'Поради щодо регулярного обслуговування та догляду за вашим апаратом для продовження терміну служби.',
                blogTitle2: 'Найпоширеніші поломки апаратів Bianchi',
                blogDesc2: 'Огляд типових проблем, з якими стикаються власники апаратів Bianchi та способи їх вирішення.',
                blogTitle3: 'Оновлення модельного ряду Bianchi 2023',
                blogDesc3: 'Огляд нових моделей апаратів Bianchi, їх переваги та вдосконалення в порівнянні з попередніми версіями.',
                readMore: 'Детальніше',
                contactText: 'Зв\'яжіться з нами для консультації чи ремонту'
            },
            ru: {
                blog: 'Блог',
                services: 'Услуги',
                products: 'Каталог',
                contact: 'Контакты',
                heroTitle: 'Премиум сервис для аппаратов Bianchi',
                heroText: 'Профессиональный ремонт, обслуживание и запчасти для вендинговых аппаратов итальянского производителя. Гарантия качества и быстрый выезд мастера.',
                contactUs: 'Связаться с нами',
                ourServices: 'Наши услуги',
                service1: 'Ремонт платежной системы',
                service1Desc: 'Устранение неисправностей купюроприемников, монетоприемников, банковских терминалов.',
                service2: 'Выезд к аппарату',
                service2Desc: 'Быстрый выезд мастера на объект для диагностики и ремонта.',
                service3: 'Диагностика',
                service3Desc: 'Полная проверка аппарата, выявление неисправностей и консультация.',
                service4: 'Прошивка и ремонт плат',
                service4Desc: 'Обновление программного обеспечения и ремонт электронных компонентов.',
                ourProducts: 'Наши товары',
                product1: 'Запчасти',
                product2: 'Диспенсеры для стаканов',
                product3: 'Аппараты Bianchi',
                cartTitle: 'Корзина',
                buyBtn: 'В корзину',
                cartEmpty: 'Корзина пуста',
                total: 'Итого',
                remove: 'Удалить',
                checkout: 'Оформить заказ',
                back: '← Назад в корзину',
                orderTitle: 'Оформление заказа',
                fio: 'ФИО',
                fioPlaceholder: 'Фамилия Имя Отчество',
                phone: 'Телефон',
                phonePlaceholder: '+7',
                city: 'Город',
                cityPlaceholder: 'Введите город',
                delivery: 'Способ доставки',
                pickCourier: 'Новая Почта',
                pickUkr: 'Укрпочта',
                pickSelf: 'Самовывоз',
                department: 'Отделение',
                departmentPlaceholder: 'Номер или адрес отделения',
                confirmOrder: 'Подтвердить заказ',
                success: '✅ Заказ успешно отправлен!',
                ourBlog: 'Последние публикации',
                blogTitle1: 'Как правильно ухаживать за аппаратом Bianchi',
                blogDesc1: 'Советы по регулярному обслуживанию и уходу за вашим аппаратом для продления срока службы.',
                blogTitle2: 'Наиболее распространенные поломки аппаратов Bianchi',
                blogDesc2: 'Обзор типичных проблем, с которыми сталкиваются владельцы аппаратов Bianchi и способы их решения.',
                blogTitle3: 'Обновление модельного ряда Bianchi 2023',
                blogDesc3: 'Обзор новых моделей аппаратов Bianchi, их преимущества и усовершенствования по сравнению с предыдущими версиями.',
                readMore: 'Подробнее',
                contactText: 'Свяжитесь с нами для консультации или ремонта'
            }
        };

        // ============================================================
        // 2. PRODUCT DATA (с переведёнными названиями и описанием)
        // ============================================================
        function buildProduct(id, titleUk, titleRu, descUk, descRu, price, image) {
            return {
                id,
                title_uk: titleUk,
                title_ru: titleRu,
                description_uk: descUk,
                description_ru: descRu,
                price,
                image: image || `https://picsum.photos/seed/${id}/300/200`
            };
        }

        // ---- ЗАПЧАСТИНИ: 48 позиций с переведёнными названиями ----
        const partData = [
            { uk: 'Підставка під чашку Rhea black', ru: 'Подставка под чашку Rhea black', price: 85,
                img: '/catalog-3d/IMG_3583E5378B33-1.jpeg' },
            { uk: '251797 Пластиковий фіксатор видачі (Necta)', ru: '251797 Пластиковый фиксатор выдачи (Necta)',
                price: 50, img: '/catalog-3d/IMG_3583E5378B33-2.jpeg' },
            { uk: 'Кріплення підставки під чашку Cino eC, XS Grande, Rhea black',
                ru: 'Крепление подставки под чашку Cino eC, XS Grande, Rhea black', price: 15,
                img: '/catalog-3d/IMG_3583E5378B33-3.jpeg' },
            { uk: 'Гайка на трубку подачі кави XS-E, Cino Rhea', ru: 'Гайка на трубку подачи кофе XS-E, Cino Rhea',
                price: 23, img: '/catalog-3d/IMG_3583E5378B33-4.jpeg' },
            { uk: 'Підставка/піддон для чашку KORINTO, NECTA - 260186 (252451)',
                ru: 'Подставка/поддон для чашки KORINTO, NECTA - 260186 (252451)', price: 420,
                img: '/catalog-3d/IMG_3583E5378B33-5.jpeg' },
            { uk: 'Фіксатор пружини', ru: 'Фиксатор пружины', price: 35,
                img: '/catalog-3d/IMG_3583E5378B33-6.jpeg' },
            { uk: 'Запчастина №7', ru: 'Запчасть №7', price: 36,
                img: '/catalog-3d/IMG_3583E5378B33-7.jpeg' },
            { uk: 'Шестерня/Вал/Магніт Rhea', ru: 'Шестерня/Вал/Магнит Rhea', price: 60,
                img: '/catalog-3d/IMG_0739.JPG' },
            { uk: 'Стопор двигуна міксера RAL2011 Rhea', ru: 'Стопор двигателя миксера RAL2011 Rhea', price: 55,
                img: '/catalog-3d/IMG_3583E5378B33-9.jpeg' },
            { uk: 'піддон краплесбірникник, NECTA (KORO) - 260187 (251788)',
                ru: 'поддон каплесборника, NECTA (KORO) - 260187 (251788)', price: 1100,
                img: '/catalog-3d/IMG_3583E5378B33-10.jpeg' },
            { uk: 'Носик подачі молотої кави Multibona', ru: 'Носик подачи молотого кофе Multibona', price: 35,
                img: '/catalog-3d/IMG_3583E5378B33-11.jpeg' },
            { uk: 'Кріплення для носиків видачі напоїв — Bianchi 05246215-01M09 — 05246215M37',
                ru: 'Крепление для носиков выдачи напитков — Bianchi 05246215-01M09 — 05246215M37', price: 60,
                img: '/catalog-3d/IMG_3583E5378B33-12.jpeg' },
            { uk: 'Решітка, NECTA - 260188', ru: 'Решетка, NECTA - 260188', price: 280,
                img: '/catalog-3d/IMG_3583E5378B33-13.jpeg' },
            { uk: 'Тримач носиків видачі напоїв Talia', ru: 'Держатель носиков выдачи напитков Talia', price: 85,
                img: '/catalog-3d/IMG_3583E5378B33-14.jpeg' },
            { uk: '251790 Фіксатор підскляника Necta Koro', ru: '251790 Фиксатор подстаканника Necta Koro', price: 250,
                img: '/catalog-3d/IMG_3583E5378B33-15.jpeg' },
            { uk: 'Противибраційна втулка Rhea', ru: 'Провибрационная втулка Rhea', price: 28,
                img: '/catalog-3d/IMG_3583E5378B33-16.jpeg' },
            { uk: 'Засувка бункера зерна Gaia', ru: 'Задвижка бункера зерна Gaia', price: 57,
                img: '/catalog-3d/IMG_3583E5378B33-17.jpeg' },
            { uk: 'Запчастина №18', ru: 'Запчасть №18', price: 72,
                img: '/catalog-3d/IMG_3583E5378B33-18.jpeg' },
            { uk: 'Кріплення для тримача стаканів Bianchi Talia', ru: 'Крепление для держателя стаканов Bianchi Talia',
                price: 75, img: '/catalog-3d/IMG_3583E5378B33-19.jpeg' },
            { uk: 'Тримач стаканів Bianchi Talia', ru: 'Держатель стаканов Bianchi Talia', price: 135,
                img: '/catalog-3d/IMG_3583E5378B33-20.jpeg' },
            { uk: '251791 Підстаканник Necta Koro', ru: '251791 Подстаканник Necta Koro', price: 190,
                img: '/catalog-3d/IMG_3583E5378B33-21.jpeg' },
            { uk: 'Заглушка монетника Rhea (Black)', ru: 'Заглушка монетника Rhea (Black)', price: 47,
                img: '/catalog-3d/IMG_3583E5378B33-22.jpeg' },
            { uk: 'Заглушка отвору корпуса Rhea', ru: 'Заглушка отверстия корпуса Rhea', price: 28,
                img: '/catalog-3d/IMG_3583E5378B33-23.jpeg' },
            { uk: 'Жолоб подачі меленої кави Rhea', ru: 'Желоб подачи молотого кофе Rhea', price: 50,
                img: '/catalog-3d/IMG_3583E5378B33-24.jpeg' },
            { uk: 'Тримач трубок Cino Rhea (Grey)', ru: 'Держатель трубок Cino Rhea (Grey)', price: 240,
                img: '/catalog-3d/IMG_3583E5378B33-25.jpeg' },
            { uk: 'Кришка бункера Gaia style', ru: 'Крышка бункера Gaia style', price: 320,
                img: '/catalog-3d/IMG_3583E5378B33-26.jpeg' },
            { uk: 'Кришка розчинного бункера Rhea', ru: 'Крышка растворимого бункера Rhea', price: 190,
                img: '/catalog-3d/IMG_3583E5378B33-27.jpeg' },
            { uk: 'Запчастина №28', ru: 'Запчасть №28', price: 25,
                img: '/catalog-3d/IMG_3583E5378B33-28.jpeg' },
            { uk: 'Ведена шестерня редуктора кавомолки Rhea', ru: 'Ведомая шестерня редуктора кофемолки Rhea', price: 72,
                img: '/catalog-3d/IMG_3583E5378B33-29.jpeg' },
            { uk: 'Провідна шестерня редуктора кавомолки Rhea', ru: 'Ведущая шестерня редуктора кофемолки Rhea',
                price: 75, img: '/catalog-3d/IMG_3583E5378B33-30.jpeg' },
            { uk: 'Решітка краплезбірника Rheavendors', ru: 'Решетка каплесборника Rheavendors', price: 780,
                img: '/catalog-3d/IMG_3583E5378B33-31.jpeg' },
            { uk: 'Направляюча моленої кави, Rheavendors - 0250008036',
                ru: 'Направляющая молотого кофе, Rheavendors - 0250008036', price: 180,
                img: '/catalog-3d/IMG_3583E5378B33-32.jpeg' },
            { uk: 'Основа Сигналізатора рівня води в краплесбірнику Gaia',
                ru: 'Основа Сигнализатора уровня воды в каплесборнике Gaia', price: 12,
                img: '/catalog-3d/IMG_3583E5378B33-33.jpeg' },
            { uk: 'Сигналізатор рівня води в краплесбірнику Gaia', ru: 'Сигнализатор уровня воды в каплесборнике Gaia',
                price: 22, img: '/catalog-3d/IMG_3583E5378B33-34.jpeg' },
            { uk: '05262815М09 Кришка корпусу для наливу води', ru: '05262815М09 Крышка корпуса для налива воды',
                price: 115, img: '/catalog-3d/IMG_3583E5378B33-35.jpeg' },
            { uk: 'Транспортер кави (крильчатка)', ru: 'Транспортер кофе (крыльчатка)', price: 38,
                img: '/Desktop/catalog-3d/IMG_3583E5378B33-36.jpeg' },
            { uk: 'Заглушка канала монет Bianchi Talia', ru: 'Заглушка канала монет Bianchi Talia', price: 250,
                img: '/catalog-3d/IMG_3583E5378B33-37.jpeg' },
            { uk: 'Засувка бункера зерна Bianchi Talia', ru: 'Задвижка бункера зерна Bianchi Talia', price: 85,
                img: '/catalog-3d/IMG_3583E5378B33-38.jpeg' },
            { uk: 'Заглушка канала монет внутрішня Rhea', ru: 'Заглушка канала монет внутренняя Rhea', price: 85,
                img: '/catalog-3d/IMG_3583E5378B33-39.jpeg' },
            { uk: 'Запчастина №40', ru: 'Запчасть №40', price: 60,
                img: '/catalog-3d/IMG_3583E5378B33-40.jpeg' },
            { uk: 'Запчастина №41', ru: 'Запчасть №41', price: 80,
                img: '/catalog-3d/IMG_3583E5378B33-41.jpeg' },
            { uk: 'Основа дверей Necta Korinto', ru: 'Основа дверей Necta Korinto', price: 1850,
                img: '/catalog-3d/IMG_3583E5378B33-42.jpeg' },
            { uk: 'Тримач носиків видачі напоїв NECTA (KORO / KORINTO) - 251798',
                ru: 'Держатель носиков выдачи напитков NECTA (KORO / KORINTO) - 251798', price: 850,
                img: '/catalog-3d/IMG_3583E5378B33-43.jpeg' },
            { uk: '0010024154 Бункер жмиху Rheavendors', ru: '0010024154 Бункер жмыха Rheavendors', price: 850,
                img: 'https://picsum.photos/seed/parts44/300/200' },
            { uk: 'Решітка підстаканника NECTA KORINTO', ru: 'Решетка подстаканника NECTA KORINTO', price: 2300,
                img: 'https://picsum.photos/seed/parts45/300/200' },
            { uk: 'Запчастина №46', ru: 'Запчасть №46', price: 650,
                img: 'https://picsum.photos/seed/parts46/300/200' },
            { uk: 'Запчастина №47', ru: 'Запчасть №47', price: 3600,
                img: 'https://picsum.photos/seed/parts47/300/200' },
            { uk: 'Запчастина №48', ru: 'Запчасть №48', price: 1040,
                img: 'https://picsum.photos/seed/parts48/300/200' }
        ];

        const descUk = '3D-запчастина для кавового обладнання.';
        const descRu = '3D-запчасть для кофейного оборудования.';

        const partsData = partData.map((item, index) => {
            const n = index + 1;
            return buildProduct(
                `parts-${n}`,
                item.uk,
                item.ru,
                descUk,
                descRu,
                item.price,
                item.img
            );
        });

        // ---- ДИСПЕНСЕРИ: 4 позиции ----
        const dispensersData = [];
        for (let i = 1; i <= 4; i++) {
            const price = Math.round((Math.random() * 3500) + 400);
            dispensersData.push(buildProduct(
                `dispensers-${i}`,
                `Диспенсер №${i}`,
                `Диспенсер №${i}`,
                'Диспенсер для стаканів, надійний механізм.',
                'Диспенсер для стаканов, надежный механизм.',
                price,
                `/images/dispensers-${i}.jpg`
            ));
        }

        // ---- АПАРАТИ: 12 позиций ----
        const machinesData = [];
        for (let i = 1; i <= 12; i++) {
            const price = Math.round((Math.random() * 25000) + 15000);
            machinesData.push(buildProduct(
                `machines-${i}`,
                `Апарат №${i}`,
                `Аппарат №${i}`,
                'Апарат Bianchi для приготування напоїв.',
                'Аппарат Bianchi для приготовления напитков.',
                price,
                `/images/machines-${i}.jpg`
            ));
        }

        const ALL_PRODUCTS = { parts: partsData, dispensers: dispensersData, machines: machinesData };
        const ITEMS_PER_PAGE = 12;

        // ============================================================
        // 3. STATE
        // ============================================================
        let currentLang = 'uk';
        let currentCategory = 'parts';
        let currentPage = 1;
        let cart = [];
        let modalState = 'cart';

        // ============================================================
        // 4. DOM REFS
        // ============================================================
        const $ = (sel) => document.querySelector(sel);
        const $$ = (sel) => document.querySelectorAll(sel);

        const grid = $('#productsGrid');
        const paginationEl = $('#paginationControls');
        const cartModal = $('#cartModal');
        const cartContent = $('#cartContent');
        const cartCount = $('#cartCount');

        // ============================================================
        // 5. HELPERS
        // ============================================================
        function getProductById(id) {
            const cat = id.split('-')[0];
            return ALL_PRODUCTS[cat]?.find(p => p.id === id);
        }

        function getLang() { return currentLang; }

        function t(key) {
            return TRANSLATIONS[currentLang]?.[key] || key;
        }

        function getProductTitle(p) {
            return currentLang === 'uk' ? p.title_uk : p.title_ru;
        }

        function getProductDesc(p) {
            return currentLang === 'uk' ? p.description_uk : p.description_ru;
        }

        // ============================================================
        // 6. LANGUAGE
        // ============================================================
        function setLanguage(lang) {
            currentLang = lang;
            $$('[data-lang-key]').forEach(el => {
                const key = el.dataset.langKey;
                if (TRANSLATIONS[lang][key] !== undefined) {
                    el.textContent = TRANSLATIONS[lang][key];
                }
            });
            $$('#catalogButtons .btn').forEach(btn => {
                const cat = btn.dataset.category;
                const key = cat === 'parts' ? 'product1' : cat === 'dispensers' ? 'product2' : 'product3';
                btn.textContent = TRANSLATIONS[lang][key] || btn.textContent;
            });
            $$('.language-switcher button').forEach(btn => {
                btn.classList.toggle('active', btn.dataset.lang === lang);
            });
            renderProducts(currentCategory, currentPage);
            if (cartModal.classList.contains('active')) renderModalContent();
        }

        // ============================================================
        // 7. PRODUCT RENDERING + PAGINATION
        // ============================================================
        function renderProducts(category, page = 1) {
            currentCategory = category;
            currentPage = page;

            const products = ALL_PRODUCTS[category] || [];
            const totalPages = Math.ceil(products.length / ITEMS_PER_PAGE);
            const start = (page - 1) * ITEMS_PER_PAGE;
            const pageItems = products.slice(start, start + ITEMS_PER_PAGE);

            grid.innerHTML = '';
            if (!pageItems.length) {
                grid.innerHTML =
                    `<p style="grid-column:1/-1;text-align:center;color:rgba(255,255,255,0.5);padding:40px 0;">${t('cartEmpty')}</p>`;
            } else {
                pageItems.forEach(p => {
                    const card = document.createElement('div');
                    card.className = 'product-card';
                    card.innerHTML = `
                        <img src="${p.image}" alt="${getProductTitle(p)}" loading="lazy" onerror="this.src='https://picsum.photos/seed/${p.id}/300/200'">
                        <div class="info">
                            <h3>${getProductTitle(p)}</h3>
                            <p>${getProductDesc(p)}</p>
                            <div class="price">${p.price} грн</div>
                            <button class="btn buy-btn" data-id="${p.id}">${t('buyBtn')}</button>
                        </div>
                    `;
                    grid.appendChild(card);
                });

                grid.querySelectorAll('.buy-btn').forEach(btn => {
                    btn.addEventListener('click', () => addToCart(btn.dataset.id));
                });
            }

            renderPagination(totalPages, page);
        }

        function renderPagination(total, current) {
            paginationEl.innerHTML = '';
            if (total <= 1) return;

            const prevBtn = document.createElement('button');
            prevBtn.textContent = '‹';
            prevBtn.disabled = current === 1;
            prevBtn.addEventListener('click', () => {
                if (current > 1) renderProducts(currentCategory, current - 1);
            });
            paginationEl.appendChild(prevBtn);

            const startPage = Math.max(1, current - 2);
            const endPage = Math.min(total, current + 2);

            for (let i = startPage; i <= endPage; i++) {
                const btn = document.createElement('button');
                btn.textContent = i;
                btn.classList.toggle('active', i === current);
                btn.addEventListener('click', () => renderProducts(currentCategory, i));
                paginationEl.appendChild(btn);
            }

            const nextBtn = document.createElement('button');
            nextBtn.textContent = '›';
            nextBtn.disabled = current === total;
            nextBtn.addEventListener('click', () => {
                if (current < total) renderProducts(currentCategory, current + 1);
            });
            paginationEl.appendChild(nextBtn);
        }

        // ============================================================
        // 8. CART
        // ============================================================
        function addToCart(id) {
            const existing = cart.find(item => item.id === id);
            if (existing) existing.quantity++;
            else cart.push({ id, quantity: 1 });
            updateCartUI();
            const btn = document.querySelector(`.buy-btn[data-id="${id}"]`);
            if (btn) {
                const orig = btn.textContent;
                btn.textContent = '✓';
                btn.style.background = '#2e7d32';
                setTimeout(() => { btn.textContent = orig;
                    btn.style.background = ''; }, 800);
            }
        }

        function updateQuantity(id, delta) {
            const item = cart.find(i => i.id === id);
            if (!item) return;
            item.quantity += delta;
            if (item.quantity <= 0) cart = cart.filter(i => i.id !== id);
            updateCartUI();
        }

        function removeFromCart(id) {
            cart = cart.filter(i => i.id !== id);
            updateCartUI();
        }

        function getCartTotal() {
            return cart.reduce((sum, item) => {
                const p = getProductById(item.id);
                return sum + (p ? p.price * item.quantity : 0);
            }, 0);
        }

        function updateCartUI() {
            const count = cart.reduce((s, i) => s + i.quantity, 0);
            cartCount.textContent = count;
            if (cartModal.classList.contains('active')) renderModalContent();
        }

        // ============================================================
        // 9. CART MODAL
        // ============================================================
        function renderModalContent() {
            if (modalState === 'cart') renderCartView();
            else if (modalState === 'order') renderOrderForm();
            else if (modalState === 'success') {
                cartContent.innerHTML = `
                    <div style="text-align:center;padding:40px 20px;color:lightgreen;font-size:1.2rem;">
                        ${t('success')}
                        <br><br>
                        <button class="btn" onclick="closeCartModal()">OK</button>
                    </div>
                `;
            }
        }

        function renderCartView() {
            const lang = currentLang;
            let html = `
                <button class="close-btn" id="closeCart" aria-label="Закрити кошик">&times;</button>
                <h2>${t('cartTitle')}</h2>
            `;

            if (cart.length === 0) {
                html += `<p style="text-align:center;padding:20px 0;">${t('cartEmpty')}</p>`;
            } else {
                html += `<ul class="cart-items">`;
                cart.forEach(item => {
                    const p = getProductById(item.id);
                    if (!p) return;
                    const title = getProductTitle(p);
                    html += `
                        <li class="cart-item">
                            <img src="${p.image}" alt="${title}" class="cart-item-img" onerror="this.src='https://picsum.photos/seed/${p.id}/100/100'">
                            <div class="cart-item-info">
                                <strong>${title}</strong>
                                <small>${p.price} грн × ${item.quantity} = ${p.price * item.quantity} грн</small>
                            </div>
                            <div class="cart-item-controls">
                                <button class="qty-btn" data-id="${item.id}" data-delta="-1">−</button>
                                <span>${item.quantity}</span>
                                <button class="qty-btn" data-id="${item.id}" data-delta="1">+</button>
                                <button class="remove" data-id="${item.id}"><i class="fas fa-trash-alt"></i></button>
                            </div>
                        </li>
                    `;
                });
                html += `</ul>
                    <div class="cart-total">${t('total')}: ${getCartTotal()} грн</div>
                    <button class="btn" id="goToCheckout" style="width:100%;">${t('checkout')}</button>
                `;
            }

            cartContent.innerHTML = html;
            document.getElementById('closeCart')?.addEventListener('click', closeCartModal);
            cartContent.querySelectorAll('.qty-btn').forEach(btn => {
                btn.addEventListener('click', () => updateQuantity(btn.dataset.id, parseInt(btn.dataset.delta)));
            });
            cartContent.querySelectorAll('.remove').forEach(btn => {
                btn.addEventListener('click', () => removeFromCart(btn.dataset.id));
            });
            document.getElementById('goToCheckout')?.addEventListener('click', () => {
                if (cart.length === 0) return;
                modalState = 'order';
                renderModalContent();
            });
        }

        function renderOrderForm() {
            const lang = currentLang;
            const html = `
                <button class="close-btn" id="closeCart" aria-label="Закрити">&times;</button>
                <button class="back-to-cart" id="backToCart">${t('back')}</button>
                <h2>${t('orderTitle')}</h2>
                <div class="order-form">
                    <label for="orderFio">${t('fio')}</label>
                    <input type="text" id="orderFio" placeholder="${t('fioPlaceholder')}">

                    <label for="orderPhone">${t('phone')}</label>
                    <input type="tel" id="orderPhone" placeholder="${t('phonePlaceholder')}">

                    <label>${t('delivery')}</label>
                    <div class="radio-group">
                        <label><input type="radio" name="delivery" value="nova" checked> ${t('pickCourier')}</label>
                        <label><input type="radio" name="delivery" value="ukr"> ${t('pickUkr')}</label>
                        <label><input type="radio" name="delivery" value="self"> ${t('pickSelf')}</label>
                    </div>

                    <div id="deliveryFields">
                        <label for="orderCity">${t('city')}</label>
                        <input type="text" id="orderCity" placeholder="${t('cityPlaceholder')}">
                        <label for="orderDepartment">${t('department')}</label>
                        <input type="text" id="orderDepartment" placeholder="${t('departmentPlaceholder')}">
                    </div>

                    <button class="btn" id="confirmOrderBtn" style="width:100%; margin-top:20px;">${t('confirmOrder')}</button>
                </div>
            `;
            cartContent.innerHTML = html;
            document.getElementById('closeCart')?.addEventListener('click', closeCartModal);
            document.getElementById('backToCart')?.addEventListener('click', () => {
                modalState = 'cart';
                renderModalContent();
            });

            const deliveryFields = document.getElementById('deliveryFields');
            document.querySelectorAll('input[name="delivery"]').forEach(r => {
                r.addEventListener('change', () => {
                    deliveryFields.style.display = document.querySelector('input[name="delivery"]:checked')
                        .value === 'self' ? 'none' : 'block';
                });
            });
            deliveryFields.style.display = 'block';

            document.getElementById('confirmOrderBtn').addEventListener('click', submitOrder);
        }

        async function submitOrder() {
            const lang = currentLang;
            const fio = document.getElementById('orderFio').value.trim();
            const phone = document.getElementById('orderPhone').value.trim();
            const delivery = document.querySelector('input[name="delivery"]:checked').value;
            const city = document.getElementById('orderCity')?.value.trim() || '';
            const department = document.getElementById('orderDepartment')?.value.trim() || '';

            if (!fio || !phone || (delivery !== 'self' && (!city || !department))) {
                alert(lang === 'uk' ? 'Заповніть обов\'язкові поля' : 'Заполните обязательные поля');
                return;
            }

            let orderText = `Нове замовлення з сайту!\nПІБ: ${fio}\nТелефон: ${phone}\n`;
            const deliveryNames = { nova: 'Нова Пошта', ukr: 'Укрпошта', self: 'Самовивіз' };
            orderText += `Доставка: ${deliveryNames[delivery]}`;
            if (delivery !== 'self') orderText += `\nМісто: ${city}\nВідділення: ${department}`;
            orderText += `\n\nТовари:\n`;
            cart.forEach(item => {
                const p = getProductById(item.id);
                if (p) {
                    const title = getProductTitle(p);
                    orderText += `${title} x${item.quantity} = ${p.price * item.quantity} грн\n`;
                }
            });
            orderText += `\nЗагальна сума: ${getCartTotal()} грн`;

            const formData = new FormData();
            formData.append('email', 'ssalamov2106.ss@gmail.com');
            formData.append('_subject', 'Нове замовлення з сайту BianchiPRO');
            formData.append('message', orderText);
            formData.append('_captcha', 'false');

            try {
                const response = await fetch('https://formsubmit.co/ajax/ssalamov2106.ss@gmail.com', {
                    method: 'POST',
                    body: formData
                });
                if (response.ok) {
                    modalState = 'success';
                    renderModalContent();
                    cart = [];
                    updateCartUI();
                    setTimeout(() => { closeCartModal();
                        modalState = 'cart'; }, 3000);
                } else {
                    alert('Помилка надсилання');
                }
            } catch {
                alert('Помилка мережі');
            }
        }

        function closeCartModal() {
            cartModal.classList.remove('active');
            modalState = 'cart';
        }

        // ============================================================
        // 10. EVENTS & INIT
        // ============================================================
        document.getElementById('cartIcon').addEventListener('click', () => {
            modalState = 'cart';
            cartModal.classList.add('active');
            renderModalContent();
        });
        window.addEventListener('click', (e) => {
            if (e.target === cartModal) closeCartModal();
        });

        document.querySelectorAll('.language-switcher button').forEach(btn => {
            btn.addEventListener('click', () => setLanguage(btn.dataset.lang));
        });

        document.querySelectorAll('#catalogButtons .btn').forEach(btn => {
            btn.addEventListener('click', function() {
                document.querySelectorAll('#catalogButtons .btn').forEach(b => b.classList.remove('active'));
                this.classList.add('active');
                renderProducts(this.dataset.category, 1);
            });
        });

        const hamburger = document.getElementById('hamburger');
        const nav = document.getElementById('mainNav');
        hamburger.addEventListener('click', () => {
            hamburger.classList.toggle('active');
            nav.classList.toggle('open');
        });
        nav.querySelectorAll('a').forEach(link => {
            link.addEventListener('click', () => {
                hamburger.classList.remove('active');
                nav.classList.remove('open');
            });
        });

        renderProducts('parts', 1);
        setLanguage('uk');

        window.addEventListener('scroll', () => {
            document.getElementById('mainHeader')
                .classList.toggle('scrolled', window.scrollY > 20);
        });
    </script>
</body>
</html>
