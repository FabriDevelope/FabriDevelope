   <style>
        /* Variables de color y estilos base */
        :root {
            --primary: #6e44ff;
            --secondary: #ff44cc;
            --accent: #2effcc;
            --dark: #0f1020;
            --darker: #070711;
            --light: #f0f0ff;
            --gradient: linear-gradient(135deg, var(--primary), var(--secondary));
            --card-bg: rgba(30, 30, 50, 0.7);
            --glow: 0 0 15px rgba(110, 68, 255, 0.5);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: var(--darker);
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Animaciones */
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        @keyframes pulse {
            0%, 100% { box-shadow: var(--glow); }
            50% { box-shadow: 0 0 25px rgba(110, 68, 255, 0.8); }
        }

        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
        }

        /* Header y presentación */
        header {
            text-align: center;
            padding: 60px 20px;
            position: relative;
            overflow: hidden;
            border-radius: 20px;
            margin-bottom: 40px;
            background: linear-gradient(-45deg, #0f1020, #1a1b40, #2d1b69, #0f1020);
            background-size: 400% 400%;
            animation: gradient 15s ease infinite;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }

        .profile {
            position: relative;
            z-index: 2;
        }

        .profile h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            background: var(--gradient);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            display: inline-block;
        }

        .tagline {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--accent);
            overflow: hidden;
            white-space: nowrap;
            animation: typing 3.5s steps(40, end);
        }

        .gif-container {
            width: 300px;
            height: 200px;
            margin: 20px auto;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--glow);
            animation: pulse 3s infinite;
        }

        .gif-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* Secciones */
        section {
            background: var(--card-bg);
            border-radius: 20px;
            padding: 30px;
            margin-bottom: 40px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s ease;
        }

        section:hover {
            transform: translateY(-5px);
        }

        h2 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--accent);
            display: flex;
            align-items: center;
        }

        h2 span {
            margin-right: 10px;
        }

        /* Badges de lenguajes */
        .badges-container {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }

        .badge {
            display: flex;
            align-items: center;
            padding: 10px 20px;
            background: rgba(46, 255, 204, 0.1);
            border-radius: 50px;
            transition: all 0.3s ease;
            border: 1px solid rgba(46, 255, 204, 0.3);
        }

        .badge:hover {
            transform: scale(1.05);
            background: rgba(46, 255, 204, 0.2);
            box-shadow: 0 0 15px rgba(46, 255, 204, 0.4);
        }

        .badge span {
            margin-left: 8px;
            font-weight: 600;
        }

        .learning .badge {
            background: rgba(110, 68, 255, 0.1);
            border: 1px solid rgba(110, 68, 255, 0.3);
        }

        .learning .badge:hover {
            background: rgba(110, 68, 255, 0.2);
            box-shadow: 0 0 15px rgba(110, 68, 255, 0.4);
        }

        /* Proyectos */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 20px;
        }

        .project-card {
            background: rgba(20, 20, 40, 0.7);
            border-radius: 15px;
            padding: 20px;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.4);
            border-color: var(--primary);
        }

        .project-card h3 {
            color: var(--accent);
            margin-bottom: 10px;
            font-size: 1.3rem;
        }

        /* Setup */
        .setup-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .setup-item {
            background: rgba(20, 20, 40, 0.7);
            border-radius: 15px;
            padding: 15px;
            border-left: 3px solid var(--primary);
        }

        .setup-item h3 {
            color: var(--accent);
            margin-bottom: 10px;
            font-size: 1.1rem;
        }

        /* Contacto */
        .contact-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }

        .contact-btn {
            display: flex;
            align-items: center;
            padding: 12px 25px;
            background: var(--gradient);
            color: white;
            border: none;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
        }

        .contact-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 0 20px rgba(110, 68, 255, 0.7);
            animation: pulse 1.5s infinite;
        }

        .contact-btn span {
            margin-left: 8px;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 30px;
            margin-top: 40px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .profile h1 {
                font-size: 2.5rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .gif-container {
                width: 250px;
                height: 180px;
            }
            
            .contact-buttons {
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="profile">
                <h1>Fabri 👨‍💻🥁🚀</h1>
                <p class="tagline">Programador, baterista y amante de la tecnología</p>
                <div class="gif-container">
                    <img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" alt="Coding GIF">
                </div>
            </div>
        </header>
