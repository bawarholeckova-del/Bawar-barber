<!DOCTYPE html>  
<html lang="cs">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>Bawar Barber | Královský Střih Praha</title>  
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;700;800&family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">  
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">  
      
    <style>  
        :root {  
            --bg-color: #0a0a0c;  
            --card-bg: #141418;  
            --accent-gold: #d4af37;  
            --gold-gradient: linear-gradient(135deg, #bf953f, #fcf6ba, #b38728, #fbf5b7, #aa771c);  
            --text-main: #f0f0f0;  
            --text-muted: #a0a0a0;  
            --border-color: #2a2a30;  
        }  
  
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Montserrat', sans-serif; }  
        body { background-color: var(--bg-color); color: var(--text-main); line-height: 1.6; overflow-x: hidden; }  
        h1, h2, h3 { font-family: 'Cinzel', serif; letter-spacing: 1px; }  
  
        header {  
            position: fixed; top: 0; width: 100%;  
            background: rgba(10, 10, 12, 0.95); backdrop-filter: blur(10px);  
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);  
            z-index: 1000; padding: 15px 5%;  
            display: flex; justify-content: space-between; align-items: center;  
        }  
  
        .logo-container { display: flex; align-items: center; gap: 12px; text-decoration: none; color: var(--text-main); }  
        .logo-badge {  
            width: 45px; height: 45px; border-radius: 50%; border: 2px solid var(--accent-gold);  
            display: flex; align-items: center; justify-content: center; background: #000; color: var(--accent-gold);  
        }  
        .logo-text h1 { font-size: 1.2rem; color: var(--accent-gold); line-height: 1.1; }  
        .logo-text span { font-size: 0.65rem; letter-spacing: 2px; color: var(--text-muted); text-transform: uppercase; }  
  
        .nav-controls { display: flex; align-items: center; gap: 10px; }  
        .lang-btn {  
            background: transparent; border: 1px solid var(--accent-gold); color: var(--accent-gold);  
            padding: 5px 10px; border-radius: 20px; cursor: pointer; font-weight: 600; font-size: 0.8rem;  
        }  
        .lang-btn.active { background: var(--accent-gold); color: #000; }  
        .book-nav-btn {  
            background: var(--gold-gradient); color: #000; border: none; padding: 8px 18px;  
            border-radius: 25px; font-weight: 700; cursor: pointer; text-decoration: none; font-size: 0.85rem;  
        }  
  
        .hero {  
            min-height: 80vh; padding: 120px 5% 60px;  
            display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center;  
            background: linear-gradient(rgba(10, 10, 12, 0.85), rgba(10, 10, 12, 0.95)), radial-gradient(circle at center, #2a2010 0%, #0a0a0c 70%);  
            border-bottom: 1px solid var(--border-color);  
        }  
        .hero h2 { font-size: 2.8rem; color: var(--accent-gold); margin-bottom: 15px; }  
        .hero p { font-size: 1.1rem; color: var(--text-muted); max-width: 650px; margin-bottom: 30px; }  
        .hero-actions { display: flex; gap: 15px; flex-wrap: wrap; justify-content: center; }  
  
        .btn-primary {  
            background: var(--gold-gradient); color: #000; border: none; padding: 14px 32px;  
            border-radius: 30px; font-size: 1rem; font-weight: 700; cursor: pointer; text-decoration: none;  
            box-shadow: 0 4px 15px rgba(212, 175, 55, 0.3); transition: all 0.3s ease;  
        }  
        .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 6px 20px rgba(212, 175, 55, 0.5); }  
        .btn-secondary {  
            background: transparent; color: var(--text-main); border: 1px solid var(--border-color);  
            padding: 14px 28px; border-radius: 30px; font-size: 1rem; font-weight: 600; text-decoration: none;  
        }  
  
        .container { max-width: 1100px; margin: 0 auto; padding: 70px 20px; }  
        .section-title { text-align: center; margin-bottom: 40px; }  
        .section-title h2 { font-size: 2.2rem; color: var(--accent-gold); margin-bottom: 8px; }  
  
        /* About Section */  
        .about-card {  
            background: var(--card-bg); border: 1px solid var(--border-color);  
            border-radius: 16px; padding: 40px; display: grid; grid-template-columns: 1fr 1.5fr; gap: 30px; align-items: center;  
        }  
        .about-img img { width: 100%; border-radius: 12px; border: 2px solid var(--accent-gold); }  
        .about-text h3 { color: var(--accent-gold); font-size: 1.5rem; margin-bottom: 15px; }  
  
        /* Gallery Grid */  
        .gallery-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 15px; }  
        .gallery-item img { width: 100%; height: 280px; object-fit: cover; border-radius: 12px; border: 1px solid var(--border-color); transition: transform 0.3s; }  
        .gallery-item img:hover { transform: scale(1.03); border-color: var(--accent-gold); }  
  
        /* Price Grid */  
        .services-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 15px; }  
        .service-card {  
            background: var(--card-bg); border: 1px solid var(--border-color); border-radius: 12px; padding: 20px;  
            display: flex; justify-content: space-between; align-items: center;  
        }  
        .service-price { color: var(--accent-gold); font-weight: 700; font-size: 1.2rem; }  
  
        /* Booking Frame */  
        .booking-card { background: var(--card-bg); border: 1px solid var(--border-color); border-radius: 16px; padding: 15px; overflow: hidden; }  
  
        footer { background: #050507; padding: 40px 5% 20px; border-top: 1px solid var(--border-color); text-align: center; font-size: 0.85rem; color: var(--text-muted); }  
        .social-links { display: flex; justify-content: center; gap: 20px; margin: 20px 0; }  
        .social-links a { color: var(--accent-gold); font-size: 1.5rem; }  
  
        @media (max-width: 768px) {  
            .about-card { grid-template-columns: 1fr; text-align: center; }  
            .hero h2 { font-size: 2rem; }  
        }  
    </style>  
</head>  
<body>  
  
    <header>  
        <a href="#" class="logo-container">  
            <div class="logo-badge"><i class="fa-solid fa-scissors"></i></div>  
            <div class="logo-text">  
                <h1>BAWAR BARBER</h1>  
                <span>KRÁLOVSKÝ STŘIH</span>  
            </div>  
        </a>  
        <div class="nav-controls">  
            <button class="lang-btn active" onclick="setLang('cs')">CZ</button>  
            <button class="lang-btn" onclick="setLang('en')">EN</button>  
            <button class="lang-btn" onclick="setLang('ku')">KU</button>  
            <a href="https://services.bookio.com/bawar-barbershop/widget?lang=cs" target="_blank" class="book-nav-btn">REZERVACE</a>  
        </div>  
    </header>  
  
    <section class="hero">  
        <h2 id="hero-title">KRÁLOVSKÝ STŘIH V PRAZE</h2>  
        <p id="hero-desc">Prvotřídní pánské kadeřnictví na Branické. Dopřejte si profesionální péči o vlasy a vousy v příjemném prostředí.</p>  
        <div class="hero-actions">  
            <a href="https://services.bookio.com/bawar-barbershop/widget?lang=cs" target="_blank" class="btn-primary" id="btn-book">Rezervovat termín</a>  
            <a href="#services" class="btn-secondary" id="btn-prices">Ceník služeb</a>  
        </div>  
    </section>  
  
    <!-- About Me -->  
    <section class="container" id="about">  
        <div class="section-title">  
            <h2 id="about-title">O MNĚ</h2>  
        </div>  
        <div class="about-card">  
            <div class="about-img">  
                <img src="https://images.unsplash.com/photo-1503951914875-452162b0f3f1?auto=format&fit=crop&w=600&q=80" alt="Bawar Barber">  
            </div>  
            <div class="about-text">  
                <h3>Bawar Jamal</h3>  
                <p id="about-desc">  
                    Vítejte! Jmenuji se Bawar, pocházím z Kurdistánu a v České republice žiji již 6 let. Mluvím česky, anglicky a kurdsky. Barberingu se věnuji s láskou a precizností. Mým cílem je, aby každý zákazník odcházel spokojený s perfektním střih a úpravou vousů.  
                </p>  
            </div>  
        </div>  
    </section>  
  
    <!-- Gallery -->  
    <section class="container" id="gallery">  
        <div class="section-title">  
            <h2 id="gallery-title">GALERIE</h2>  
        </div>  
        <div class="gallery-grid">  
            <div class="gallery-item"><img src="https://images.unsplash.com/photo-1622286342621-4bd786c2447c?auto=format&fit=crop&w=500&q=80" alt="Cut 1"></div>  
            <div class="gallery-item"><img src="https://images.unsplash.com/photo-1599351431202-1e0f0137899a?auto=format&fit=crop&w=500&q=80" alt="Cut 2"></div>  
            <div class="gallery-item"><img src="https://images.unsplash.com/photo-1517832606299-7ae9b720a186?auto=format&fit=crop&w=500&q=80" alt="Cut 3"></div>  
            <div class="gallery-item"><img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=500&q=80" alt="Cut 4"></div>  
        </div>  
    </section>  
  
    <!-- Prices -->  
    <section class="container" id="services">  
        <div class="section-title">  
            <h2 id="prices-title">CENÍK SLUŽEB</h2>  
        </div>  
        <div class="services-grid">  
            <div class="service-card"><div><h3>Střih vlasů</h3><p>Pánský střih & styling</p></div><div class="service-price">499 Kč</div></div>  
            <div class="service-card"><div><h3>Úprava a holení vousů</h3><p>Horký ručník & péče</p></div><div class="service-price">299 Kč</div></div>  
            <div class="service-card"><div><h3>Komplet: Střih + Vousy</h3><p>Kompletní péče</p></div><div class="service-price">799 Kč</div></div>  
            <div class="service-card"><div><h3>Dětský střih</h3><p>Do 12 let</p></div><div class="service-price">350 Kč</div></div>  
            <div class="service-card"><div><h3>Barvení vlasů</h3><p>Profesionální tónování</p></div><div class="service-price">400 Kč</div></div>  
            <div class="service-card"><div><h3>Barvení vousů</h3><p>Přirozená barva</p></div><div class="service-price">200 Kč</div></div>  
            <div class="service-card"><div><h3>Barvení: Vlasy + Vousy</h3><p>Kompletní servis</p></div><div class="service-price">500 Kč</div></div>  
            <div class="service-card"><div><h3>Wax (Depilace)</h3><p>Nos / Uši</p></div><div class="service-price">100 Kč</div></div>  
            <div class="service-card"><div><h3>Úprava obočí</h3><p>Precizní úprava</p></div><div class="service-price">100 Kč</div></div>  
        </div>  
    </section>  
  
    <!-- Bookio Widget Integration -->  
    <section class="container" id="booking">  
        <div class="section-title">  
            <h2 id="booking-title">ONLINE REZERVACE</h2>  
        </div>  
        <div class="booking-card">  
            <iframe src="https://services.bookio.com/bawar-barbershop/widget?lang=cs" style="width:100%; height:700px; border:none; border-radius:12px;" title="Bookio Online Rezervace"></iframe>  
        </div>  
    </section>  
  
    <footer>  
        <p><strong>Bawar Barber</strong> - Bránická 81, Praha 4 | Tel: +420 777 311 461</p>  
        <div class="social-links">  
            <a href="https://instagram.com/bawar_barber11" target="_blank"><i class="fa-brands fa-instagram"></i></a>  
            <a href="https://maps.google.com/?q=Bránická+81,+Praha+4" target="_blank"><i class="fa-solid fa-map-location-dot"></i></a>  
        </div>  
        <p>© 2026 Bawar Barber. Všechna práva vyhrazena.</p>  
    </footer>  
  
    <script>  
        const translations = {  
            cs: {  
                heroTitle: "KRÁLOVSKÝ STŘIH V PRAZE",  
                heroDesc: "Prvotřídní pánské kadeřnictví na Branické. Dopřejte si profesionální péči o vlasy a vousy.",  
                btnBook: "Rezervovat termín",  
                btnPrices: "Ceník služeb",  
                aboutTitle: "O MNĚ",  
                aboutDesc: "Vítejte! Jmenuji se Bawar, pocházím z Kurdistánu a v ČR žiji 6 let. Mluvím česky, anglicky a kurdsky. Nabízím vám profesionální střih a péči o vousy.",  
                galleryTitle: "GALERIE",  
                pricesTitle: "CENÍK SLUŽEB",  
                bookingTitle: "ONLINE REZERVACE"  
            },  
            en: {  
                heroTitle: "ROYAL CUT IN PRAGUE",  
                heroDesc: "Premium barbershop in Braník. Treat yourself to professional hair and beard care.",  
                btnBook: "Book Appointment",  
                btnPrices: "View Pricing",  
                aboutTitle: "ABOUT ME",  
                aboutDesc: "Welcome! My name is Bawar, I'm from Kurdistan and I've lived in Czechia for 6 years. I speak Czech, English, and Kurdish. I provide top quality hair and beard care.",  
                galleryTitle: "GALLERY",  
                pricesTitle: "PRICING",  
                bookingTitle: "ONLINE BOOKING"  
            },  
            ku: {  
                heroTitle: "**تۆقینی** **شاهانە** **لە** **پڕاگ**",  
                heroDesc: "**باشترین** **سەرتاشخانەی** **پیاوان** **لە** **براک**. **گرنگی** **بە** **قژ** **و** **ڕیشت** **بدە** **لە** **ژینگەیەکی** **ئارامدا**.",  
                btnBook: "**نۆرە** **بگرە** (**حجز**)",  
                btnPrices: "**نرخی** **خزمەتگوزارییەکان**",  
                aboutTitle: "**دەربارەی** **من**",  
                aboutDesc: "**بەخێربێن**! **ناوم** **باوەرە،** **خەڵکی** **کوردستانم** **و** **زاتی** **٦** **ساڵە** **لە** **کۆماری** **چیک** **دەژیم**. **بە** **زمانەکانی** **چیکی،** **ئینگلیزی** **و** **کوردی** **قسە** **دەکەم**.",  
                galleryTitle: "**گەلەری** **وێنەکان**",  
                pricesTitle: "**لیستی** **نرخەکان**",  
                bookingTitle: "**حجزکردنی** **ئۆنلاین**"  
            }  
        };  
  
        function setLang(lang) {  
            document.querySelectorAll('.lang-btn').forEach(btn => btn.classList.remove('active'));  
            event.target.classList.add('active');  
  
            document.getElementById('hero-title').innerText = translations[lang].heroTitle;  
            document.getElementById('hero-desc').innerText = translations[lang].heroDesc;  
            document.getElementById('btn-book').innerText = translations[lang].btnBook;  
            document.getElementById('btn-prices').innerText = translations[lang].btnPrices;  
            document.getElementById('about-title').innerText = translations[lang].aboutTitle;  
            document.getElementById('about-desc').innerText = translations[lang].aboutDesc;  
            document.getElementById('gallery-title').innerText = translations[lang].galleryTitle;  
            document.getElementById('prices-title').innerText = translations[lang].pricesTitle;  
            document.getElementById('booking-title').innerText = translations[lang].bookingTitle;  
        }  
    </script>  
</body>  
</html>  
