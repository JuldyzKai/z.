<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Қазақ Жыраулары Поэзиясы</title>
    <style>
        :root {
            --qogam-color: #8B4513;
            --altin-color: #D4AF37;
            --step-color: #2E8B57;
            --background-color: #F5F5DC;
            --text-color: #333;
            --white: #fff;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            background-color: var(--background-color);
            color: var(--text-color);
            line-height: 1.6;
            min-height: 100vh;
        }
        
        /* Контейнерді толық енімен жасау */
        .container {
            width: 100%;
            max-width: 1400px; /* Кеңейтеміз */
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(to right, var(--qogam-color), var(--altin-color));
            color: var(--white);
            padding: 30px 0; /* Үлкейтеміз */
            text-align: center;
            border-bottom: 5px solid var(--step-color);
            width: 100%;
        }
        
        .logo {
            font-size: 3rem; /* Үлкейтеміз */
            font-weight: bold;
            margin-bottom: 15px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        .tagline {
            font-size: 1.5rem; /* Үлкейтеміз */
            font-style: italic;
        }
        
        /* Navigation */
        nav {
            background-color: var(--step-color);
            padding: 20px 0; /* Үлкейтеміз */
            width: 100%;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        nav ul li {
            margin: 0 25px; /* Арақашықтықты ұлғайтамыз */
        }
        
        nav ul li a {
            color: var(--white);
            text-decoration: none;
            font-weight: bold;
            font-size: 1.3rem; /* Үлкейтеміз */
            padding: 10px 20px; /* Үлкейтеміз */
            border-radius: 5px;
            transition: all 0.3s;
        }
        
        nav ul li a:hover {
            background-color: rgba(255,255,255,0.2);
            transform: translateY(-2px);
        }
        
        /* Section Styles */
        section {
            padding: 60px 0; /* Үлкейтеміз */
            width: 100%;
        }
        
        h2 {
            text-align: center;
            margin-bottom: 40px; /* Үлкейтеміз */
            color: var(--qogam-color);
            font-size: 2.5rem; /* Үлкейтеміз */
            border-bottom: 3px solid var(--altin-color);
            padding-bottom: 15px;
        }
        
        /* Home Page */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                        url('https://images.unsplash.com/photo-1546975490-a79abddaeaeb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80') 
                        no-repeat center center/cover;
            height: 70vh; /* Экран биіктігінің 70% */
            min-height: 600px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--white);
            position: relative;
            width: 100%;
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 900px;
            padding: 0 40px;
        }
        
        .hero h1 {
            font-size: 4rem; /* Үлкейтеміз */
            margin-bottom: 30px;
            text-shadow: 2px 2px 8px rgba(0,0,0,0.7);
        }
        
        .hero p {
            font-size: 1.5rem; /* Үлкейтеміз */
            margin-bottom: 40px;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--altin-color);
            color: var(--white);
            padding: 15px 35px; /* Үлкейтеміз */
            border-radius: 8px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.2rem;
            transition: all 0.3s;
            border: 2px solid transparent;
        }
        
        .btn:hover {
            background-color: var(--qogam-color);
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.2);
        }
        
        .features {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-top: 50px;
            gap: 30px;
        }
        
        .feature {
            flex: 1;
            min-width: 350px; /* Үлкейтеміз */
            margin: 0;
            padding: 30px;
            background-color: var(--white);
            border-radius: 15px;
            box-shadow: 0 6px 15px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.3s;
        }
        
        .feature:hover {
            transform: translateY(-10px);
        }
        
        .feature i {
            font-size: 4rem; /* Үлкейтеміз */
            color: var(--step-color);
            margin-bottom: 20px;
        }
        
        .feature h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }
        
        .feature p {
            font-size: 1.1rem;
            line-height: 1.7;
        }
        
        /* Gallery */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); /* Үлкейтеміз */
            gap: 30px;
        }
        
        .poet-card {
            background-color: var(--white);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 6px 15px rgba(0,0,0,0.1);
            transition: all 0.3s;
        }
        
        .poet-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.15);
        }
        
        .poet-img {
            width: 100%;
            height: 350px; /* Үлкейтеміз */
            object-fit: cover;
            transition: transform 0.3s;
        }
        
        .poet-card:hover .poet-img {
            transform: scale(1.05);
        }
        
        .poet-info {
            padding: 25px;
        }
        
        .poet-info h3 {
            color: var(--qogam-color);
            margin-bottom: 15px;
            font-size: 1.4rem;
        }
        
        .poet-info p {
            margin-bottom: 20px;
            line-height: 1.6;
        }
        
        /* Poems Collection */
        .poems-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); /* Үлкейтеміз */
            gap: 30px;
        }
        
        .poem-card {
            background-color: var(--white);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 6px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .poem-card:hover {
            transform: translateY(-8px);
        }
        
        .poem-title {
            color: var(--qogam-color);
            margin-bottom: 20px;
            border-bottom: 2px solid var(--altin-color);
            padding-bottom: 15px;
            font-size: 1.4rem;
        }
        
        .poem-text {
            margin-bottom: 20px;
            line-height: 1.8;
            font-size: 1.1rem;
        }
        
        .audio-player {
            width: 100%;
            margin-top: 15px;
            border-radius: 25px;
        }
        
        .poem-explanation {
            margin-top: 20px;
            padding: 20px;
            background-color: rgba(139, 69, 19, 0.05);
            border-radius: 8px;
            border-left: 4px solid var(--step-color);
        }
        
        /* Videos & Animations */
        .media-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(500px, 1fr)); /* Үлкейтеміз */
            gap: 30px;
        }
        
        .media-item {
            background-color: var(--white);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 6px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .media-item:hover {
            transform: translateY(-8px);
        }
        
        .media-item iframe {
            width: 100%;
            height: 300px; /* Үлкейтеміз */
            display: block;
        }
        
        .media-info {
            padding: 25px;
        }
        
        .media-info h3 {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--qogam-color);
        }
        
        /* Footer */
        footer {
            background: linear-gradient(to right, var(--qogam-color), var(--step-color));
            color: var(--white);
            padding: 50px 0;
            text-align: center;
            width: 100%;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            max-width: 1400px;
            margin: 0 auto;
            gap: 40px;
        }
        
        .footer-section {
            flex: 1;
            min-width: 300px;
            margin: 0;
        }
        
        .footer-section h3 {
            margin-bottom: 20px;
            color: var(--altin-color);
            font-size: 1.4rem;
        }
        
        .footer-section p, .footer-section li {
            font-size: 1.1rem;
            line-height: 1.7;
        }
        
        .footer-section ul {
            list-style: none;
        }
        
        .footer-section ul li {
            margin: 12px 0;
        }
        
        .footer-section ul li a {
            color: var(--white);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-section ul li a:hover {
            color: var(--altin-color);
        }
        
        .copyright {
            margin-top: 40px;
            padding-top: 30px;
            border-top: 2px solid rgba(255,255,255,0.2);
            font-size: 1.1rem;
        }
        
        /* Responsive Design */
        @media (max-width: 1200px) {
            .container {
                padding: 20px 40px;
            }
            
            .hero h1 {
                font-size: 3.5rem;
            }
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 20px;
            }
            
            nav ul {
                flex-direction: column;
                align-items: center;
                gap: 10px;
            }
            
            nav ul li {
                margin: 5px 0;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .features {
                flex-direction: column;
            }
            
            .media-container {
                grid-template-columns: 1fr;
            }
            
            .gallery {
                grid-template-columns: 1fr;
            }
            
            .logo {
                font-size: 2.5rem;
            }
        }
        
        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero {
                height: 50vh;
                min-height: 400px;
            }
            
            h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="container">
            <div class="logo">ЖЫРАУЛАР ПОЭЗИЯСЫ</div>
            <div class="tagline">Ұлттық мінездің рухани айнасы</div>
        </div>
    </header>
    
    <!-- Navigation -->
    <nav>
        <div class="container">
            <ul>
                <li><a href="#home">Басты бет</a></li>
                <li><a href="#gallery">Жыраулар</a></li>
                <li><a href="#poems">Толғаулар</a></li>
                <li><a href="#media">Бейнелер</a></li>
                <li><a href="#about">Біз туралы</a></li>
            </ul>
        </div>
    </nav>
    
    <!-- Home Page Section -->
    <section id="home">
        <div class="hero">
            <div class="hero-content">
                <h1>Қазақ жыраулары Поэзиясы</h1>
                <p>Халықтың рухани байлығы, ұлттық мінездің айнасы</p>
                <a href="#gallery" class="btn">Жыраулармен танысу</a>
            </div>
        </div>
        
        <div class="container">
            <h2>Жыраулық поэзияның ұлттық мінездегі орны</h2>
            <p style="font-size: 1.2rem; line-height: 1.8; text-align: center; max-width: 1000px; margin: 0 auto 40px;">Қазақ жырауларының поэзиясы - біздің ұлтымыздың рухани қазынасы. Олардың шығармалары арқылы біз қазақ халқының тарихын, мәдениетін, дүниетанымын және ұлттық мінезін тереңірек түсіне аламыз.</p>
            
            <div class="features">
                <div class="feature">
                    <i>📚</i>
                    <h3>Тарихи мұра</h3>
                    <p>Жыраулар поэзиясы қазақ халқының тарихи тәжірибесін, күрестерін және жеңістерін бейнелейді.</p>
                </div>
                <div class="feature">
                    <i>💭</i>
                    <h3>Философиялық ойлар</h3>
                    <p>Толғауларда терең философиялық ойлар, даналық кеңестер мен афоризмдер жиі кездеседі.</p>
                </div>
                <div class="feature">
                    <i>🌱</i>
                    <h3>Рухани тәрбие</h3>
                    <p>Жыраулар шығармалары жаңа буынның рухани тәрбиесіне үлкен ықпал етеді.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Gallery Section -->
    <section id="gallery">
        <div class="container">
            <h2>Жыраулар галереясы</h2>
            <div class="gallery">
                <div class="poet-card">
                    <img src="Ақтамберді САРЫҰЛЫ.png" alt="Ақтамберді Сарыұлы" class="poet-img">
                    <div class="poet-info">
                        <h3>Ақтамберді Сарыұлы</h3>
                        <p>1675-1768 жж. өмір сүрген. Қол бастаған батыр, сөз бастаған шешен, жорықтың жалынды жырауы.</p>
                        <a href="#" class="btn">Толығырақ</a>
                    </div>
                </div>
                
                <div class="poet-card">
                    <img src="ЖИЕМБЕТ ЖЫРАУ.png" alt="Жиембет Бортоғашұлы" class="poet-img">
                    <div class="poet-info">
                        <h3>Жиембет Бортоғашұлы</h3>
                        <p>XVII ғасырда өмір сүрген. "Еңсегей бойлы Ер Есім" толғауының авторы.</p>
                        <a href="#" class="btn">Толығырақ</a>
                    </div>
                </div>
                
                <div class="poet-card">
                    <img src="1АСАНҚАЙҒЫ.png" alt="Асан Қайғы" class="poet-img">
                    <div class="poet-info">
                        <h3>Асан Қайғы</h3>
                        <p>XIV-XV ғасырларда өмір сүрген. "Жәнібекке айтқаны" толғауының авторы.</p>
                        <a href="#" class="btn">Толығырақ</a>
                    </div>
                </div>
                
                <div class="poet-card">
                    <img src="Шалкиіз жырау Тіленшіұлы.png" alt="Қазтуған жырау" class="poet-img">
                    <div class="poet-info">
                        <h3>Қазтуған жырау</h3>
                        <p>XV ғасырда өмір сүрген. Қазақ жыраулық поэзиясының негізін салушылардың бірі.</p>
                        <a href="#" class="btn">Толығырақ</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Poems Collection Section -->
    <section id="poems">
        <div class="container">
            <h2>Толғаулар жинағы</h2>
            <div class="poems-container">
                <div class="poem-card">
                    <h3 class="poem-title">"Қарағайға қарсы біткен бұтақпын"</h3>
                    <p class="poem-author">Ақтамберді Сарыұлы</p>
                    <div class="poem-text">
                        <p>Торлаусыз өскен құланымын,</p>
                        <p>Мезгілсіз жусап өлермін.</p>
                        <p>Байраққа біткен құрақпын,</p>
                        <p>Саусағым жерге түсірмен.</p>
                        <p>Жапанға біткен теректін,</p>
                        <p>Еңсемнен жел сокса да теңселмен.</p>
                        <p>Қарағайға қарсы біткен бұтақпын,</p>
                        <p>Балталасаң да айрылман.</p>
                    </div>
                    <audio controls class="audio-player">
                        <source src="АҚТАМБЕРДІ.mp3" type="audio/mpeg">
                        Сіздің браузеріңіз аудио элементін қолдамайды.
                    </audio>
                    <div class="poem-explanation">
                        <h4>Түсіндірме:</h4>
                        <p>Бұл өлең жолдарында Ақтамберді жырау өзін қарағайға қарсы біткен бұтаққа теңейді. Бұл оның тәуелсіз, қайсар және ешқандай қиындыққа бағынбайтын мінезін білдіреді.</p>
                    </div>
                </div>
                
                <div class="poem-card">
                    <h3 class="poem-title">"Еңсегей бойлы Ер Есім"</h3>
                    <p class="poem-author">Жиембет Бортоғашұлы</p>
                    <div class="poem-text">
                        <p>Менің ерлігімді сұрасаң,</p>
                        <p>Жолбарыс пен аюдай.</p>
                        <p>Өрлігімді сұрасаң,</p>
                        <p>Жылқының асау тайындай.</p>
                        <p>Зорлығымды сұрасаң,</p>
                        <p>Бекіре мен жайындай.</p>
                        <p>Беріктігім сұраса,</p>
                        <p>Қарағай мен қайындай.</p>
                    </div>
                    <audio controls class="audio-player">
                        <source src="Еңсегей бойлы ер есім.mp3" type="audio/mpeg">
                        Сіздің браузеріңіз аудио элементін қолдамайды.
                    </audio>
                    <div class="poem-explanation">
                        <h4>Түсіндірме:</h4>
                        <p>Жиембет жырау өз қасиеттерін табиғаттағы күшті жануарлар мен өсімдіктерге теңеуді арқылы өзін сипаттайды. Бұл оның батылдығын, күшін және беріктігін көрсетеді.</p>
                    </div>
                </div>
                
                <div class="poem-card">
                    <h3 class="poem-title">"Жәнібекке айтқаны"</h3>
                    <p class="poem-author">Асан Қайғы</p>
                    <div class="poem-text">
                        <p>Суда жүрген ақ шортан</p>
                        <p>Қарағай басын шалмай ма?</p>
                        <p>Қилы-қилы заман болып,</p>
                        <p>Қарағай басын шортан шалды.</p>
                    </div>
                    <audio controls class="audio-player">
                        <source src="АСАНН.mp3" type="audio/mpeg">
                        Сіздің браузеріңіз аудио элементін қолдамайды.
                    </audio>
                    <div class="poem-explanation">
                        <h4>Түсіндірме:</h4>
                        <p>Асан Қайғы бұл өлең жолдарында қиын замандарда әдеттегі тәртіптің бұзылатынын, күтпеген оқиғалардың болуы мүмкін екенін білдіреді.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Videos & Animations Section -->
    <section id="media">
        <div class="container">
            <h2>Бейнелер мен анимациялар</h2>
            <div class="media-container">
                <div class="media-item">
                    <iframe src="Қазақ жырауларының тарихы». Ақтамберді жырау.mp4" frameborder="0" allowfullscreen></iframe>
                    <div class="media-info">
                        <h3>Ақтамберді жырау Сарыұлы</h3>
                        <p>Қазақ жыраулары поэзиясының даму тарихына арналған қысқаша баяндама.</p>
                    </div>
                </div>
                
                <div class="media-item">
                    <iframe src="Жыраулар.mp4" frameborder="0" allowfullscreen></iframe>
                    <div class="media-info">
                        <h3>Жыраулар тарихы</h3>
                        <p>Қазақ жырауларының тарихи даму жолы мен әдеби мұрасы.</p>
                    </div>
                </div>
                
                <div class="media-item">
                    <iframe src="«Асанқайғының жерге айтқан сыны» аңызы..mp4" frameborder="0" allowfullscreen></iframe>
                    <div class="media-info">
                        <h3>Асан қайғы Сәбитұлы</h3>
                        <p>Асан қайғының жерге айтқан сындары</p>
                    </div>
                </div>
                
                <div class="media-item">
                    <iframe src="Қазақ жырауларының тарихы». Жиембет жырау.mp4" frameborder="0" allowfullscreen></iframe>
                    <div class="media-info">
                        <h3>Жиембет жырау Бортоғашұлы</h3>
                        <p>Жырау жайлы мәлімет</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Байланыс ақпараты</h3>
                    <p>Email: Juldiz8469@gmail.com</p>
                    <p>Телефон: +7 747 153 56 76</p>
                    <p>Мекенжай:  Қазақстан Алматы Наурызбай ауданы №206 мектеп-гимназия</p>
                </div>
                
                <div class="footer-section">
                    <h3>Жылдам сілтемелер</h3>
                    <ul>
                        <li><a href="#home">Басты бет</a></li>
                        <li><a href="#gallery">Жыраулар</a></li>
                        <li><a href="#poems">Толғаулар</a></li>
                        <li><a href="#media">Бейнелер</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h3>Біздің миссиямыз</h3>
                    <p>Қазақ жыраулары поэзиясын зерттеу, насихаттау және жаңа буынға жеткізу арқылы ұлттық рухани құндылықтарды сақтау.</p>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2025 жыл. Қазақ Жыраулары Поэзиясы. Барлық құқықтар қорғалған.</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 100,
                    behavior: 'smooth'
                });
            });
        });
        
        // Simple animation for poet cards
        const poetCards = document.querySelectorAll('.poet-card');
        
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        const observer = new IntersectionObserver(function(entries, observer) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);
        
        poetCards.forEach(card => {
            card.style.opacity = 0;
            card.style.transform = 'translateY(20px)';
            card.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
            observer.observe(card);
        });

        // Audio player enhancement
        const audioPlayers = document.querySelectorAll('audio');
        audioPlayers.forEach(audio => {
            audio.addEventListener('play', function() {
                // Pause other audio players when one starts playing
                audioPlayers.forEach(otherAudio => {
                    if (otherAudio !== audio && !otherAudio.paused) {
                        otherAudio.pause();
                    }
                });
            });
        });
    </script>
</body>
</html>
