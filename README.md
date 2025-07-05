<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lizpaz Sound - Professional Audio Solutions</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #4a00e0;
            --secondary: #8e2de2;
            --dark: #121212;
            --light: #f8f9fa;
            --accent: #ff6b6b;
        }
        
        body {
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        header {
            background: rgba(18, 18, 18, 0.8);
            backdrop-filter: blur(10px);
            padding: 1.5rem 5%;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo i {
            font-size: 2rem;
            color: var(--accent);
        }
        
        .logo h1 {
            font-size: 1.8rem;
            background: linear-gradient(to right, #8e2de2, #4a00e0);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 700;
        }
        
        .nav-links {
            display: flex;
            gap: 2rem;
        }
        
        .nav-links a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
            position: relative;
        }
        
        .nav-links a:hover {
            color: var(--accent);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .hero {
            padding: 6rem 5% 4rem;
            text-align: center;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            background: linear-gradient(to right, #ff6b6b, #8e2de2);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
            color: #e0e0e0;
        }
        
        .cta-btn {
            display: inline-block;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 15px rgba(142, 45, 226, 0.4);
        }
        
        .cta-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(142, 45, 226, 0.6);
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin: 3rem 0 2rem;
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
            background: linear-gradient(to right, var(--accent), var(--secondary));
            border-radius: 2px;
        }
        
        .products {
            padding: 2rem 5%;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .product-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }
        
        .product-img {
            height: 200px;
            background: linear-gradient(45deg, #2c3e50, #4a00e0);
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 4rem;
            color: white;
        }
        
        .product-info {
            padding: 1.5rem;
        }
        
        .product-info h3 {
            font-size: 1.4rem;
            margin-bottom: 0.5rem;
            color: var(--accent);
        }
        
        .product-info p {
            color: #ccc;
            margin-bottom: 1rem;
        }
        
        .contact {
            padding: 4rem 5%;
            background: rgba(18, 18, 18, 0.7);
            margin-top: 3rem;
            text-align: center;
        }
        
        .contact-info {
            max-width: 600px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.05);
            padding: 2.5rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            margin: 1.5rem 0;
            font-size: 1.2rem;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.5rem;
        }
        
        .contact-details a {
            color: var(--accent);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .contact-details a:hover {
            color: white;
            text-decoration: underline;
        }
        
        footer {
            background: rgba(10, 10, 10, 0.95);
            padding: 2rem 5%;
            text-align: center;
            margin-top: 3rem;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        
        .social-links a {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 45px;
            height: 45px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            transform: translateY(-5px);
        }
        
        .copyright {
            color: #aaa;
            font-size: 0.9rem;
            margin-top: 1.5rem;
        }
        
        @media (max-width: 768px) {
            .nav-links {
                gap: 1.2rem;
            }
            
            .hero h2 {
                font-size: 2.5rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .product-grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
        
        @media (max-width: 480px) {
            .navbar {
                flex-direction: column;
                gap: 1rem;
            }
            
            .hero {
                padding: 4rem 5% 2rem;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
            
            .contact-info {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <nav class="navbar">
            <div class="logo">
                <i class="fas fa-volume-up"></i>
                <h1>Lizpaz Sound</h1>
            </div>
            <div class="nav-links">
                <a href="#products">Products</a>
                <a href="#about">About</a>
                <a href="#contact">Contact</a>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h2>Professional Audio Solutions</h2>
        <p>Premium audio equipment for studios, live performances, and events. Experience crystal clear sound with our cutting-edge technology and professional-grade gear.</p>
        <a href="#products" class="cta-btn">Explore Products</a>
    </section>

    <!-- Products Section -->
    <section class="products" id="products">
        <h2 class="section-title">Our Products</h2>
        <div class="product-grid">
            <!-- Microphones -->
            <div class="product-card">
                <div class="product-img">
                    <i class="fas fa-microphone"></i>
                </div>
                <div class="product-info">
                    <h3>Professional Microphones</h3>
                    <p>Studio-grade condenser and dynamic microphones for vocals and instruments. Perfect for recording and live performances.</p>
                </div>
            </div>
            
            <!-- PA Speakers -->
            <div class="product-card">
                <div class="product-img">
                    <i class="fas fa-bullhorn"></i>
                </div>
                <div class="product-info">
                    <h3>PA Speakers</h3>
                    <p>High-power public address systems for clear audio delivery in any venue. Built for durability and exceptional sound quality.</p>
                </div>
            </div>
            
            <!-- Audio Cables -->
            <div class="product-card">
                <div class="product-img">
                    <i class="fas fa-plug"></i>
                </div>
                <div class="product-info">
                    <h3>Audio Cables</h3>
                    <p>Premium XLR, TRS, and instrument cables with gold-plated connectors for noise-free signal transmission.</p>
                </div>
            </div>
            
            <!-- Power Amplifiers -->
            <div class="product-card">
                <div class="product-img">
                    <i class="fas fa-bolt"></i>
                </div>
                <div class="product-info">
                    <h3>Power Amplifiers</h3>
                    <p>High-fidelity amplifiers with exceptional power efficiency and thermal management for all sound systems.</p>
                </div>
            </div>
            
            <!-- Power Sequencers -->
            <div class="product-card">
                <div class="product-img">
                    <i class="fas fa-power-off"></i>
                </div>
                <div class="product-info">
                    <h3>Power Sequencers</h3>
                    <p>Protect your equipment with sequential power management systems that prevent damaging power surges.</p>
                </div>
            </div>
            
            <!-- Sound Mixers -->
            <div class="product-card">
                <div class="product-img">
                    <i class="fas fa-sliders-h"></i>
                </div>
                <div class="product-info">
                    <h3>Sound Mixers</h3>
                    <p>Digital and analog mixing consoles with advanced features for professional audio production and live sound.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <h2 class="section-title">Contact Us</h2>
        <div class="contact-info">
            <div class="contact-item">
                <div class="contact-icon">
                    <i class="fas fa-phone"></i>
                </div>
                <div class="contact-details">
                    <a href="tel:+254701378339">+254 701 378 339</a>
                </div>
            </div>
            
            <div class="contact-item">
                <div class="contact-icon">
                    <i class="fas fa-envelope"></i>
                </div>
                <div class="contact-details">
                    <a href="mailto:jmbuthia393@gmail.com">jmbuthia393@gmail.com</a>
                </div>
            </div>
            
            <p style="margin-top: 2rem; color: #bbb;">We're available 24/7 for inquiries, technical support, and equipment consultations.</p>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="social-links">
            <a href="#"><i class="fab fa-facebook-f"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-youtube"></i></a>
        </div>
        <div class="logo" style="justify-content: center; margin-top: 1rem;">
            <i class="fas fa-volume-up"></i>
            <h1>Lizpaz Sound</h1>
        </div>
        <p class="copyright">© 2023 Lizpaz Sound. All rights reserved. Professional audio solutions for Kenya and beyond.</p>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Add animation on scroll
        const observerOptions = {
            root: null,
            rootMargin: '0px',
            threshold: 0.1
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animated');
                }
            });
        }, observerOptions);
        
        // Observe product cards
        document.querySelectorAll('.product-card').forEach(card => {
            observer.observe(card);
        });
        
        // Add animation class when in view
        document.querySelectorAll('.product-card').forEach(card => {
            card.classList.add('animated');
        });
    </script>
</body>
</html>
