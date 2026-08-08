<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rave Ceremony - Authentic Punjabi & North Indian Catering</title>
    <!-- Google Fonts & Font Awesome Icons -->
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@500;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/between/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #8B0000; /* Deep Royal Red */
            --gold: #D4AF37; /* Elegant Gold */
            --gold-light: #F4E07D;
            --dark: #1A1A1A;
            --light: #FAF9F6;
            --gray: #666;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }

        h1, h2, h3, .brand-font {
            font-family: 'Cinzel', serif;
        }

        /* Navigation */
        header {
            background: rgba(26, 26, 26, 0.95);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 2px solid var(--gold);
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 1rem 2rem;
        }

        .logo {
            font-size: 1.8rem;
            color: var(--gold);
            font-weight: 700;
            text-decoration: none;
            letter-spacing: 2px;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: var(--light);
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 400;
        }

        .nav-links a:hover {
            color: var(--gold);
        }

        .btn-gold {
            background: linear-gradient(45deg, var(--gold), var(--gold-light));
            color: var(--dark);
            padding: 0.6rem 1.5rem;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 600;
            border: none;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .btn-gold:hover {
            transform: scale(1.05);
        }

        /* Hero Section */
        .hero {
            height: 90vh;
            background: linear-gradient(rgba(0,0,0,0.65), rgba(0,0,0,0.65)), 
                        url('https://images.unsplash.com/photo-1585937421612-70a008356fbe?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: var(--light);
            padding: 0 1rem;
            margin-top: 60px;
        }

        .hero h1 {
            font-size: 3.5rem;
            color: var(--gold);
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 700px;
            margin-bottom: 2rem;
        }

        /* Menu Section */
        .menu-section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .section-subtitle {
            text-align: center;
            color: var(--gold);
            font-size: 1.2rem;
            margin-bottom: 3rem;
            font-weight: bold;
        }

        .menu-tabs {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 2.5rem;
            flex-wrap: wrap;
        }

        .tab-btn {
            padding: 0.6rem 1.8rem;
            border: 2px solid var(--gold);
            background: transparent;
            color: var(--dark);
            font-weight: 600;
            cursor: pointer;
            border-radius: 20px;
            transition: all 0.3s;
        }

        .tab-btn.active, .tab-btn:hover {
            background: var(--gold);
            color: var(--dark);
        }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .menu-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
            border-top: 4px solid var(--primary);
        }

        .menu-card:hover {
            transform: translateY(-5px);
        }

        .menu-card-content {
            padding: 1.5rem;
        }

        .menu-card h3 {
            color: var(--primary);
            margin-bottom: 0.5rem;
            display: flex;
            justify-content: space-between;
        }

        .veg-tag {
            font-size: 0.8rem;
            padding: 2px 8px;
            border-radius: 4px;
            border: 1px solid green;
            color: green;
        }

        .nonveg-tag {
            font-size: 0.8rem;
            padding: 2px 8px;
            border-radius: 4px;
            border: 1px solid red;
            color: red;
        }

        /* Booking / Contact Form */
        .contact-section {
            background: var(--dark);
            color: var(--light);
            padding: 5rem 2rem;
        }

        .contact-container {
            max-width: 800px;
            margin: 0 auto;
            background: #252525;
            padding: 2.5rem;
            border-radius: 10px;
            border: 1px solid var(--gold);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--gold);
        }

        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border-radius: 5px;
            border: 1px solid #444;
            background: #333;
            color: white;
        }

        /* Footer */
        footer {
            background: #111;
            color: #888;
            text-align: center;
            padding: 1.5rem;
            border-top: 1px solid #333;
        }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            .nav-links { display: none; }
        }
    </style>
</head>
<body>

    <!-- Header & Navigation -->
    <header>
        <nav class="navbar">
            <a href="#" class="logo">RAVE CEREMONY</a>
            <ul class="nav-links">
                <li><a href="#about">About Us</a></li>
                <li><a href="#menu">Menu Highlights</a></li>
                <li><a href="#contact">Book Catering</a></li>
            </ul>
            <a href="#contact" class="btn-gold">Enquire Now</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Rave Ceremony</h1>
        <p>Exquisite Punjabi &amp; Royal North Indian Culinary Experience for Weddings, Galas &amp; Special Events.</p>
        <a href="#menu" class="btn-gold">Explore Menu Book</a>
    </section>

    <!-- Menu Section -->
    <section class="menu-section" id="menu">
        <h2 class="section-title">Grand Ceremony Menu</h2>
        <p class="section-subtitle">Authentic Flavors • Tandoori Delights • Rich Gravies • Royal Desserts</p>

        <!-- Category Tabs -->
        <div class="menu-tabs">
            <button class="tab-btn active" onclick="filterMenu('all')">Full Menu</button>
            <button class="tab-btn" onclick="filterMenu('starters')">Starters &amp; Tandoor</button>
            <button class="tab-btn" onclick="filterMenu('mains')">Main Course</button>
            <button class="tab-btn" onclick="filterMenu('breads')">Breads &amp; Rice</button>
            <button class="tab-btn" onclick="filterMenu('desserts')">Desserts &amp; Beverages</button>
        </div>

        <!-- Menu Grid -->
        <div class="menu-grid">
            <!-- Item 1 -->
            <div class="menu-card starters">
                <div class="menu-card-content">
                    <h3>Amritsari Paneer Tikka <span class="veg-tag">VEG</span></h3>
                    <p>Cottage cheese marinated in carom seeds, spiced yogurt, cooked to perfection in clay oven.</p>
                </div>
            </div>

            <!-- Item 2 -->
            <div class="menu-card starters">
                <div class="menu-card-content">
                    <h3>Bhatti Da Murgh <span class="nonveg-tag">NON-VEG</span></h3>
                    <p>Traditional Punjabi rustic charcoal-grilled chicken infused with whole spices.</p>
                </div>
            </div>

            <!-- Item 3 -->
            <div class="menu-card mains">
                <div class="menu-card-content">
                    <h3>Dal Makhani (Rave Signature) <span class="veg-tag">VEG</span></h3>
                    <p>Slow-cooked black lentils overnight with white butter, cream, and rich spices.</p>
                </div>
            </div>

            <!-- Item 4 -->
            <div class="menu-card mains">
                <div class="menu-card-content">
                    <h3>Butter Chicken Deluxe <span class="nonveg-tag">NON-VEG</span></h3>
                    <p>Tender tandoori chicken cooked in an iconic velvety tomato and butter gravy.</p>
                </div>
            </div>

            <!-- Item 5 -->
            <div class="menu-card mains">
                <div class="menu-card-content">
                    <h3>Kadhai Paneer Punjabi <span class="veg-tag">VEG</span></h3>
                    <p>Cottage cheese tossed with bell peppers, onion, and fresh hand-ground spices.</p>
                </div>
            </div>

            <!-- Item 6 -->
            <div class="menu-card breads">
                <div class="menu-card-content">
                    <h3>Assorted Tandoori Breads <span class="veg-tag">VEG</span></h3>
                    <p>Garlic Naan, Butter Naan, Lachha Paratha, and Missi Roti straight from the tandoor.</p>
                </div>
            </div>

            <!-- Item 7 -->
            <div class="menu-card breads">
                <div class="menu-card-content">
                    <h3>Hyderabadi Subz / Chicken Biryani</h3>
                    <p>Fragrant basmati rice layered with aromatic spices, saffron, served with Burani Raita.</p>
                </div>
            </div>

            <!-- Item 8 -->
            <div class="menu-card desserts">
                <div class="menu-card-content">
                    <h3>Kesari Rasmalai &amp; Gulab Jamun <span class="veg-tag">VEG</span></h3>
                    <p>Soft cottage cheese dumplings soaked in saffron milk &amp; hot ghee Gulab Jamun.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Booking Form -->
    <section class="contact-section" id="contact">
        <div class="contact-container">
            <h2 class="section-title" style="color: var(--gold);">Book Rave Ceremony Catering</h2>
            <p style="text-align: center; margin-bottom: 2rem; color: #ccc;">Let us bring authentic royal dining to your special event.</p>
            
            <form>
                <div class="form-group">
                    <label>Full Name</label>
                    <input type="text" placeholder="Enter your name" required>
                </div>
                <div class="form-group">
                    <label>Contact Number / Email</label>
                    <input type="text" placeholder="Enter phone or email" required>
                </div>
                <div class="form-group">
                    <label>Event Type</label>
                    <select>
                        <option>Wedding / Reception</option>
                        <option>Sangeet / Mehendi</option>
                        <option>Corporate Gala</option>
                        <option>Private Ceremony</option>
                    </select>
                </div>
                <div class="form-group">
                    <label>Guest Count</label>
                    <input type="number" placeholder="Estimated number of guests">
                </div>
                <div class="form-group">
                    <label>Custom Menu Notes</label>
                    <textarea rows="4" placeholder="Mention any specific items from the menu book..."></textarea>
                </div>
                <button type="submit" class="btn-gold" style="width: 100%;">Submit Booking Request</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Rave Ceremony Catering Services. All Rights Reserved.</p>
    </footer>

    <!-- JavaScript for Filtering Menu Categories -->
    <script>
        function filterMenu(category) {
            const cards = document.querySelectorAll('.menu-card');
            const buttons = document.querySelectorAll('.tab-btn');

            buttons.forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');

            cards.forEach(card => {
                if (category === 'all') {
                    card.style.display = 'block';
                } else {
                    if (card.classList.contains(category)) {
                        card.style.display = 'block';
                    } else {
                        card.style.display = 'none';
                    }
                }
            });
        }
    </script>
</body>
</html>
