<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Everon | Consultoría Estratégica B2B</title>
    <meta name="description" content="Estrategia y marketing que convierten incertidumbre en crecimiento. Consultoría B2B data-driven.">
    
    <!-- Favicon SVG generado dinámicamente con el logo de Everon -->
    <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32' fill='white'%3E%3Cpath d='M24 8c-1.5-2-4-3-7-3-6 0-11 4.5-11 11s5 11 11 11c3 0 5.5-1 7-3' stroke='white' stroke-width='4' stroke-linecap='round' fill='none'/%3E%3Cpath d='M12 16h8' stroke='white' stroke-width='4' stroke-linecap='round'/%3E%3C/svg%3E">

    <style>
        /* --- VARIABLES & RESET --- */
        :root {
            /* Palette: Everon Blue Extraction */
            --bg-dark: #000839; /* RGB(0, 8, 57) */
            --primary: #2556d6; /* RGB(37, 86, 214) */
            --primary-glow: #4d7cff; 
            --secondary: #1a3c8a; 
            --text-main: #ffffff;
            --text-muted: #cbd5e1;
            
            --bg-card: rgba(255, 255, 255, 0.05);
            --bg-card-hover: rgba(37, 86, 214, 0.15);
            --border-glass: rgba(255, 255, 255, 0.1);
            
            --font-main: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            --container-width: 1200px;
            --nav-height: 80px;
            --ease-out: cubic-bezier(0.16, 1, 0.3, 1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }
        
        body {
            background-color: var(--bg-dark);
            background-image: radial-gradient(circle at 50% 0%, #102a70 0%, var(--bg-dark) 60%);
            color: var(--text-main);
            font-family: var(--font-main);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* --- UTILITIES --- */
        .container {
            width: 90%;
            max-width: var(--container-width);
            margin: 0 auto;
        }
        
        .section-padding { padding: 80px 0; }
        
        h1, h2, h3, h4 { line-height: 1.2; font-weight: 700; letter-spacing: -0.02em; }
        h1 { font-size: clamp(2.5rem, 5vw, 4rem); margin-bottom: 1.5rem; }
        h2 { font-size: clamp(2rem, 4vw, 3rem); margin-bottom: 1rem; text-align: center; }
        h3 { font-size: 1.5rem; margin-bottom: 1rem; color: var(--text-main); }
        
        p { color: var(--text-muted); margin-bottom: 1.5rem; }
        
        .text-center { text-align: center; }
        .text-gradient {
            background: linear-gradient(135deg, #ffffff 0%, var(--primary-glow) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* --- BUTTONS --- */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 12px 28px;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s var(--ease-out);
            cursor: pointer;
            border: none;
            font-size: 1rem;
        }

        .btn-primary {
            background: linear-gradient(90deg, var(--secondary) 0%, var(--primary) 100%);
            color: white;
            box-shadow: 0 4px 15px rgba(37, 86, 214, 0.4);
        }
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(37, 86, 214, 0.6);
            background: linear-gradient(90deg, var(--primary) 0%, var(--primary-glow) 100%);
        }
        .btn-primary:disabled {
            opacity: 0.7;
            cursor: not-allowed;
            transform: none;
        }

        .btn-outline {
            background: transparent;
            border: 1px solid var(--border-glass);
            color: var(--text-main);
            backdrop-filter: blur(5px);
        }
        .btn-outline:hover {
            border-color: var(--primary);
            background: rgba(37, 86, 214, 0.1);
        }

        /* --- HEADER --- */
        .header {
            position: fixed;
            top: 0;
            width: 100%;
            height: var(--nav-height);
            z-index: 1000;
            background: rgba(0, 8, 57, 0.85); 
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border-glass);
            display: flex;
            align-items: center;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
            letter-spacing: -0.03em;
        }
        .logo svg { width: 36px; height: 36px; fill: none; stroke: white; stroke-width: 2.5; stroke-linecap: round; }

        .nav-links {
            display: flex;
            gap: 30px;
            list-style: none;
        }

        .nav-link {
            color: var(--text-muted);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            transition: color 0.3s;
            position: relative;
        }
        .nav-link:hover, .nav-link.active { color: white; }
        .nav-link.active::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 100%;
            height: 2px;
            background: var(--primary);
            box-shadow: 0 0 10px var(--primary);
        }

        .hamburger { display: none; background: none; border: none; cursor: pointer; }
        .hamburger span { display: block; width: 25px; height: 2px; background: white; margin: 5px 0; transition: 0.3s; }

        /* --- HERO --- */
        .hero {
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding-top: var(--nav-height);
            overflow: hidden;
        }

        .wave-bg {
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            z-index: -1;
            overflow: hidden;
            pointer-events: none;
        }
        .wave-svg {
            position: absolute;
            width: 200%;
            height: 100%;
            opacity: 0.5;
            animation: waveMove 20s linear infinite;
        }
        .wave-svg.secondary {
            top: 10%;
            opacity: 0.3;
            animation: waveMove 25s linear infinite reverse;
        }

        @keyframes waveMove {
            0% { transform: translateX(0); }
            50% { transform: translateX(-25%); }
            100% { transform: translateX(0); }
        }

        .hero-content { max-width: 800px; z-index: 1; }

        .trust-bullets {
            display: flex;
            gap: 20px;
            margin-top: 40px;
            flex-wrap: wrap;
        }
        .bullet-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
            color: var(--text-muted);
            background: rgba(255,255,255,0.05);
            padding: 8px 16px;
            border-radius: 20px;
            border: 1px solid var(--border-glass);
        }
        .bullet-icon { color: var(--primary-glow); }

        .cta-group {
            display: flex;
            gap: 15px;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        /* --- SERVICES (Cards) --- */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .card {
            background: var(--bg-card);
            border: 1px solid var(--border-glass);
            padding: 30px;
            border-radius: 16px;
            transition: all 0.3s var(--ease-out);
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(5px);
            display: flex;
            flex-direction: column;
        }
        .card:hover {
            transform: translateY(-10px);
            background: var(--bg-card-hover);
            border-color: var(--primary);
            box-shadow: 0 20px 40px rgba(0,0,0,0.4);
        }
        .card::before {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 100%; height: 4px;
            background: linear-gradient(90deg, var(--secondary), var(--primary));
            opacity: 0;
            transition: opacity 0.3s;
        }
        .card:hover::before { opacity: 1; }

        .card-icon {
            width: 50px; height: 50px;
            background: rgba(37, 86, 214, 0.1);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
            color: var(--primary-glow);
        }
        .card-list {
            list-style: none;
            margin-top: 15px;
            font-size: 0.9rem;
            color: var(--text-muted);
        }
        .card-list li { margin-bottom: 5px; display: flex; align-items: center; gap: 8px; }
        .card-list li::before { content: '•'; color: var(--primary); font-size: 1.2rem; }

        /* --- METHODOLOGY --- */
        .timeline {
            position: relative;
            margin-top: 60px;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }
        .timeline::before {
            content: '';
            position: absolute;
            top: 25px; left: 50px; right: 50px;
            height: 2px;
            background: linear-gradient(90deg, rgba(37, 86, 214, 0.1), var(--primary), rgba(37, 86, 214, 0.1));
            z-index: 0;
        }

        .step {
            position: relative;
            z-index: 1;
            flex: 1;
            min-width: 220px;
            text-align: center;
            padding: 0 15px;
            margin-bottom: 30px;
        }
        .step-circle {
            width: 50px; height: 50px;
            background: var(--bg-dark);
            border: 2px solid var(--primary);
            border-radius: 50%;
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            color: var(--primary-glow);
            box-shadow: 0 0 15px rgba(37, 86, 214, 0.3);
        }

        /* --- AI DEMO --- */
        #ai-demo {
            background: radial-gradient(circle at center, rgba(37, 86, 214, 0.15) 0%, transparent 70%);
        }
        .ai-interface {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            margin-top: 50px;
            align-items: start;
        }
        .ai-input-panel {
            background: var(--bg-card);
            border: 1px solid var(--border-glass);
            padding: 30px;
            border-radius: 16px;
        }
        .ai-output-panel {
            background: rgba(0, 0, 0, 0.4);
            border: 1px solid var(--primary);
            padding: 30px;
            border-radius: 16px;
            min-height: 300px;
            position: relative;
            box-shadow: 0 0 20px rgba(37, 86, 214, 0.1);
        }
        .ai-output-content { font-size: 0.95rem; color: var(--text-main); white-space: pre-wrap; }
        .ai-output-content ul { margin-left: 20px; margin-top: 10px; }
        .ai-output-content li { margin-bottom: 8px; }
        .ai-loading {
            position: absolute;
            top: 50%; left: 50%;
            transform: translate(-50%, -50%);
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
            color: var(--primary);
            display: none;
        }
        .spinner {
            width: 40px; height: 40px;
            border: 4px solid rgba(255, 255, 255, 0.1);
            border-top: 4px solid var(--primary);
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }
        
        /* Email Simulation Styles */
        .email-preview-header {
            background: rgba(255,255,255,0.05);
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 15px;
            border: 1px dashed var(--primary);
            font-size: 0.85rem;
            color: var(--primary-glow);
        }
        .email-success-badge {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            background: rgba(16, 185, 129, 0.2);
            color: #34d399;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-bottom: 15px;
        }

        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }

        @media (max-width: 900px) {
            .ai-interface { grid-template-columns: 1fr; }
        }
        
        /* --- BLOG SECTION --- */
        .blog-meta {
            font-size: 0.8rem;
            color: var(--primary-glow);
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 10px;
            display: block;
            font-weight: 600;
        }
        .blog-link {
            margin-top: auto;
            color: var(--primary-glow);
            text-decoration: none;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: gap 0.3s;
        }
        .blog-link:hover { gap: 10px; color: white; }

        /* --- CASES --- */
        .cases-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        .case-stat {
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--primary-glow);
            margin: 15px 0;
            display: block;
        }
        .case-tag {
            text-transform: uppercase;
            font-size: 0.75rem;
            letter-spacing: 1px;
            color: var(--secondary);
            font-weight: 700;
        }

        /* --- TESTIMONIALS --- */
        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        .quote-icon {
            font-size: 3rem;
            color: rgba(255,255,255,0.1);
            line-height: 1;
            margin-bottom: 10px;
        }
        .client-info { display: flex; align-items: center; gap: 15px; margin-top: 20px; }
        .client-avatar {
            width: 40px; height: 40px;
            background: var(--border-glass);
            border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            font-weight: bold; color: var(--text-muted);
        }

        /* --- CONTACT --- */
        .cta-section {
            position: relative;
            background: linear-gradient(180deg, var(--bg-dark) 0%, #00041a 100%);
            overflow: hidden;
            text-align: center;
        }
        .form-container {
            max-width: 600px;
            margin: 40px auto 0;
            background: rgba(255, 255, 255, 0.05);
            padding: 40px;
            border-radius: 20px;
            border: 1px solid var(--border-glass);
            backdrop-filter: blur(10px);
            position: relative;
            z-index: 2;
        }
        .form-group { margin-bottom: 20px; text-align: left; }
        .form-label { display: block; margin-bottom: 8px; font-size: 0.9rem; font-weight: 500; }
        .form-input, .form-textarea {
            width: 100%;
            padding: 12px 15px;
            background: rgba(0, 0, 0, 0.3);
            border: 1px solid var(--border-glass);
            border-radius: 8px;
            color: white;
            font-family: inherit;
            transition: 0.3s;
            resize: none; /* Evita que el usuario redimensione el cuadro de texto */
        }
        .form-input:focus, .form-textarea:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(37, 86, 214, 0.2);
        }
        .form-checkbox-group {
            display: flex;
            align-items: flex-start;
            gap: 10px;
            font-size: 0.85rem;
            color: var(--text-muted);
            margin-bottom: 25px;
            text-align: left;
        }
        .error-msg { color: #ef4444; font-size: 0.8rem; margin-top: 5px; display: none; }
        .success-overlay {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 8, 57, 0.95);
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            border-radius: 20px;
            opacity: 0; pointer-events: none;
            transition: opacity 0.3s;
        }
        .success-overlay.visible { opacity: 1; pointer-events: all; }

        /* --- FOOTER --- */
        .footer {
            border-top: 1px solid var(--border-glass);
            padding: 50px 0;
            margin-top: 0;
            background: #00041a;
            font-size: 0.9rem;
            color: var(--text-muted);
        }
        .footer-content {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            gap: 40px;
            align-items: start;
        }
        .footer-col h4 { color: white; margin-bottom: 15px; font-size: 1.1rem; }
        .footer-contact p { margin-bottom: 8px; display: flex; align-items: center; gap: 10px; }
        .social-links { display: flex; gap: 15px; margin-top: 15px; }
        .social-links a { color: var(--text-muted); transition: 0.3s; }
        .social-links a:hover { color: var(--primary); }
        .footer-legal { text-align: right; }
        .footer-legal a { color: var(--text-muted); text-decoration: none; margin-left: 15px; display: inline-block; }
        
        /* --- RESPONSIVE --- */
        @media (max-width: 768px) {
            h1 { font-size: 2.5rem; }
            .hamburger { display: block; z-index: 1001; }
            .nav-links {
                position: fixed;
                top: 0; right: -100%;
                width: 80%; height: 100vh;
                background: rgba(0, 8, 57, 0.98);
                flex-direction: column;
                justify-content: center;
                align-items: center;
                transition: 0.3s ease;
                border-left: 1px solid var(--border-glass);
            }
            .nav-links.active { right: 0; }
            .timeline { flex-direction: column; }
            .timeline::before { top: 0; bottom: 0; left: 25px; width: 2px; height: 100%; }
            .step { display: flex; text-align: left; align-items: flex-start; gap: 20px; padding-left: 0; }
            .step-circle { margin: 0; min-width: 50px; }
            .footer-content { grid-template-columns: 1fr; text-align: center; }
            .footer-legal { text-align: center; margin-top: 20px; }
            .footer-legal a { margin: 0 10px; }
            .social-links { justify-content: center; }
            .footer-contact p { justify-content: center; }
        }

        /* --- ANIMATIONS --- */
        .reveal { opacity: 0; transform: translateY(30px); transition: all 0.8s var(--ease-out); }
        .reveal.active { opacity: 1; transform: translateY(0); }
    </style>
</head>
<body>

    <!-- HEADER -->
    <header class="header">
        <div class="container nav-container">
            <a href="#" class="logo">
                <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg">
                    <path d="M24 8c-1.5-2-4-3-7-3-6 0-11 4.5-11 11s5 11 11 11c3 0 5.5-1 7-3" stroke="currentColor" fill="none" />
                    <path d="M12 16h8" stroke="currentColor" />
                </svg>
                Everon
            </a>
            
            <button class="hamburger" aria-label="Menú">
                <span></span><span></span><span></span>
            </button>

            <ul class="nav-links">
                <li><a href="#servicios" class="nav-link">Servicios</a></li>
                <li><a href="#metodologia" class="nav-link">Metodología</a></li>
                <li><a href="#ai-demo" class="nav-link" style="color: var(--primary-glow);">Demo IA ✨</a></li>
                <li><a href="#casos" class="nav-link">Resultados</a></li>
                <li><a href="#blog" class="nav-link">Blog</a></li>
                <li><a href="#contacto" class="btn btn-primary">Agenda una llamada</a></li>
            </ul>
        </div>
    </header>

    <!-- HERO -->
    <section class="hero">
        <div class="wave-bg">
            <svg class="wave-svg" viewBox="0 0 1440 600" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
                <defs>
                    <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%">
                        <stop offset="0%" style="stop-color:#000839;stop-opacity:0" />
                        <stop offset="50%" style="stop-color:#2556d6;stop-opacity:0.3" />
                        <stop offset="100%" style="stop-color:#1a3c8a;stop-opacity:0" />
                    </linearGradient>
                    <filter id="glow">
                        <feGaussianBlur stdDeviation="10" result="coloredBlur"/>
                        <feMerge><feMergeNode in="coloredBlur"/><feMergeNode in="SourceGraphic"/></feMerge>
                    </filter>
                </defs>
                <path d="M0,300 C320,100 640,100 960,300 C1280,500 1600,500 1920,300 L1920,600 L0,600 Z" fill="url(#grad1)" filter="url(#glow)" />
            </svg>
            <svg class="wave-svg secondary" viewBox="0 0 1440 600" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M0,400 C320,500 640,500 960,400 C1280,200 1600,200 1920,400 L1920,600 L0,600 Z" fill="url(#grad1)" />
            </svg>
        </div>

        <div class="container hero-content reveal active">
            <h1>Estrategia Data-Driven para <br><span class="text-gradient">Liderar el Mercado</span></h1>
            <p style="font-size: 1.25rem; max-width: 600px;">
                Consultoría estratégica integral que une visión de negocio, tecnología y creatividad para transformar incertidumbre en crecimiento exponencial.
            </p>
            
            <div class="cta-group">
                <a href="#ai-demo" class="btn btn-primary">Probar Consultor IA ✨</a>
                <a href="#casos" class="btn btn-outline">Ver Resultados</a>
            </div>

            <div class="trust-bullets">
                <div class="bullet-item">
                    <svg class="bullet-icon" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3"><polyline points="20 6 9 17 4 12"></polyline></svg>
                    +10 Años de Experiencia
                </div>
                <div class="bullet-item">
                    <svg class="bullet-icon" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3"><polyline points="20 6 9 17 4 12"></polyline></svg>
                    Enfoque Data-Driven
                </div>
                <div class="bullet-item">
                    <svg class="bullet-icon" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3"><polyline points="20 6 9 17 4 12"></polyline></svg>
                    Acompañamiento End-to-End
                </div>
            </div>
        </div>
    </section>

    <!-- SERVICES -->
    <section id="servicios" class="section-padding">
        <div class="container">
            <div class="text-center reveal">
                <h2>Servicios de <span class="text-gradient">Alto Impacto</span></h2>
                <p>Diseñamos soluciones escalables para retos complejos.</p>
            </div>

            <div class="services-grid">
                <article class="card reveal">
                    <div class="card-icon">
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M2 20h20M4 16l6-8 5 5 5-5"/></svg>
                    </div>
                    <h3>Estrategia Corporativa</h3>
                    <p>Redefinimos modelos de negocio para la era digital, asegurando sostenibilidad y ventaja competitiva.</p>
                    <ul class="card-list">
                        <li>Visión 360º & Roadmaps</li>
                        <li>Digital Transformation</li>
                        <li>Innovación de Modelos</li>
                    </ul>
                </article>
                <article class="card reveal">
                    <div class="card-icon">
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M22 12h-4M6 12H2M12 6V2M12 22v-4"/></svg>
                    </div>
                    <h3>Go-to-Market</h3>
                    <p>Lanzamos productos y servicios con precisión quirúrgica, minimizando riesgos y acelerando la adopción.</p>
                    <ul class="card-list">
                        <li>Product-Market Fit</li>
                        <li>Lanzamiento Ágil</li>
                        <li>Expansión Internacional</li>
                    </ul>
                </article>
                <article class="card reveal">
                    <div class="card-icon">
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/></svg>
                    </div>
                    <h3>Branding & Posicionamiento</h3>
                    <p>Construimos narrativas poderosas que conectan emocionalmente y elevan el valor percibido de la marca.</p>
                    <ul class="card-list">
                        <li>Identidad Líquida</li>
                        <li>Storytelling Corporativo</li>
                        <li>Arquitectura de Marca</li>
                    </ul>
                </article>
                <article class="card reveal">
                    <div class="card-icon">
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M23 6l-9.5 9.5-5-5L1 18"/><path d="M17 6h6v6"/></svg>
                    </div>
                    <h3>Performance Marketing</h3>
                    <p>Maximización del ROAS mediante atribución avanzada y optimización continua de canales.</p>
                    <ul class="card-list">
                        <li>Analítica Predictiva</li>
                        <li>Full-Funnel Growth</li>
                        <li>CRO & Testing</li>
                    </ul>
                </article>
            </div>
        </div>
    </section>

    <!-- METHODOLOGY -->
    <section id="metodologia" class="section-padding" style="background: rgba(255,255,255,0.02);">
        <div class="container">
            <div class="text-center reveal">
                <h2>Metodología <span class="text-gradient">Everon</span></h2>
                <p>Un proceso estructurado para garantizar resultados predecibles.</p>
            </div>

            <div class="timeline reveal">
                <div class="step">
                    <div class="step-circle">01</div>
                    <div><h3>Diagnóstico</h3><p>Auditoría profunda de datos y mercado.</p></div>
                </div>
                <div class="step">
                    <div class="step-circle">02</div>
                    <div><h3>Estrategia</h3><p>Co-creación de un plan de acción a medida.</p></div>
                </div>
                <div class="step">
                    <div class="step-circle">03</div>
                    <div><h3>Ejecución</h3><p>Implementación ágil mediante sprints.</p></div>
                </div>
                <div class="step">
                    <div class="step-circle">04</div>
                    <div><h3>Optimización</h3><p>Monitorización y refinamiento constante.</p></div>
                </div>
            </div>
        </div>
    </section>

    <!-- GEMINI AI DEMO -->
    <section id="ai-demo" class="section-padding">
        <div class="container">
            <div class="text-center reveal">
                <h2>Everon AI <span class="text-gradient">Insight ✨</span></h2>
                <p>Experimenta el poder de nuestra inteligencia estratégica.</p>
            </div>

            <div class="ai-interface reveal">
                <div class="ai-input-panel">
                    <h3 style="margin-bottom: 20px;">Consulta tu negocio</h3>
                    <div class="form-group">
                        <label for="ai-industry" class="form-label">Industria / Sector</label>
                        <input type="text" id="ai-industry" class="form-input" placeholder="Ej. Logística, FinTech...">
                    </div>
                    <div class="form-group">
                        <label for="ai-challenge" class="form-label">Principal Reto de Negocio</label>
                        <textarea id="ai-challenge" rows="4" class="form-textarea" placeholder="Ej. Necesitamos reducir el coste de adquisición de clientes B2B sin perder calidad..."></textarea>
                    </div>
                    
                    <!-- NEW EMAIL GATING FIELD -->
                    <div class="form-group">
                        <label for="ai-email" class="form-label">Email Corporativo (para recibir el informe)</label>
                        <input type="email" id="ai-email" class="form-input" placeholder="tu@empresa.com">
                    </div>

                    <button id="ai-btn" class="btn btn-primary" style="width: 100%; display: flex; gap: 10px;">
                        <span>Generar y Enviar a mi Correo ✨</span>
                    </button>
                    <!-- Eliminado texto de Gemini -->
                </div>

                <div class="ai-output-panel">
                    <div id="ai-placeholder" style="position: absolute; top:50%; left:50%; transform:translate(-50%, -50%); text-align: center; width: 80%; opacity: 0.5;">
                        <svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" style="margin-bottom: 10px;"><path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"></path><polyline points="3.27 6.96 12 12.01 20.73 6.96"></polyline><line x1="12" y1="22.08" x2="12" y2="12"></line></svg>
                        <p>Los insights generados se enviarán a tu correo.</p>
                    </div>
                    
                    <div id="ai-loading" class="ai-loading">
                        <div class="spinner"></div>
                        <span>Generando y enviando informe...</span>
                    </div>

                    <div id="ai-result" class="ai-output-content"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- CASES -->
    <section id="casos" class="section-padding">
        <div class="container">
            <h2 class="text-center reveal">Resultados que <span class="text-gradient">Hablan</span></h2>
            <div class="cases-grid">
                <article class="card reveal">
                    <span class="case-tag">FinTech SaaS</span>
                    <h4>Escalado B2B Internacional</h4>
                    <p>Rediseño de la estrategia de captación y onboarding.</p>
                    <span class="case-stat text-gradient">+240%</span>
                    <p style="margin:0; font-size:0.9rem;">Incremento en MRR</p>
                </article>
                <article class="card reveal">
                    <span class="case-tag">Retail E-commerce</span>
                    <h4>Omnicanalidad Integrada</h4>
                    <p>Unificación de datos offline/online.</p>
                    <span class="case-stat text-gradient">3.5x</span>
                    <p style="margin:0; font-size:0.9rem;">Retorno ROAS</p>
                </article>
                <article class="card reveal">
                    <span class="case-tag">Industria 4.0</span>
                    <h4>Digitalización de Ventas</h4>
                    <p>Implementación de CRM y automatización.</p>
                    <span class="case-stat text-gradient">-45%</span>
                    <p style="margin:0; font-size:0.9rem;">Reducción ciclo venta</p>
                </article>
            </div>
        </div>
    </section>

    <!-- NEW BLOG SECTION -->
    <section id="blog" class="section-padding" style="background: rgba(255,255,255,0.02);">
        <div class="container">
            <h2 class="text-center reveal">Everon <span class="text-gradient">Insights</span></h2>
            <p class="text-center">Tendencias y análisis para líderes visionarios.</p>
            
            <div class="services-grid">
                <!-- Blog Post 1 -->
                <article class="card reveal">
                    <span class="blog-meta">Estrategia</span>
                    <h3>El fin del Growth Hacking: Por qué el crecimiento sostenible gana.</h3>
                    <p>Analizamos el cambio de paradigma hacia la retención y el CLV a largo plazo.</p>
                    <a href="blog/fin-del-growth-hacking.html" class="blog-link">Leer Artículo <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></a>
                </article>
                <!-- Blog Post 2 -->
                <article class="card reveal">
                    <span class="blog-meta">Tecnología</span>
                    <h3>IA Generativa en B2B: Más allá del Hype.</h3>
                    <p>Casos de uso reales para optimizar la cadena de valor sin perder el toque humano.</p>
                    <a href="blog/ia-generativa-b2b.html" class="blog-link">Leer Artículo <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></a>
                </article>
                <!-- Blog Post 3 -->
                <article class="card reveal">
                    <span class="blog-meta">Liderazgo</span>
                    <h3>Navegando la Incertidumbre Económica en 2025.</h3>
                    <p>Claves para directivos que buscan blindar sus operaciones ante la volatilidad.</p>
                    <a href="blog/incertidumbre-economica-2025.html" class="blog-link">Leer Artículo <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></a>
                </article>
            </div>
        </div>
    </section>

    <!-- TESTIMONIALS -->
    <section class="section-padding">
        <div class="container">
            <h2 class="text-center reveal">Confianza <span class="text-gradient">Ejecutiva</span></h2>
            <div class="testimonials-grid">
                <div class="card reveal" style="background: transparent; border: none;">
                    <div class="quote-icon">“</div>
                    <p style="color: white; font-size: 1.1rem;">"Everon no es solo una consultora, son socios estratégicos."</p>
                    <div class="client-info">
                        <div class="client-avatar">CR</div>
                        <div><strong>Carlos Ruiz</strong><br><span style="font-size:0.8rem; color:var(--text-muted);">CEO, TechNova</span></div>
                    </div>
                </div>
                <div class="card reveal" style="background: transparent; border: none;">
                    <div class="quote-icon">“</div>
                    <p style="color: white; font-size: 1.1rem;">"Resultados tangibles desde el primer trimestre."</p>
                    <div class="client-info">
                        <div class="client-avatar">AM</div>
                        <div><strong>Ana Martínez</strong><br><span style="font-size:0.8rem; color:var(--text-muted);">CMO, GreenEnergy</span></div>
                    </div>
                </div>
                <div class="card reveal" style="background: transparent; border: none;">
                    <div class="quote-icon">“</div>
                    <p style="color: white; font-size: 1.1rem;">"Sofisticación y pragmatismo puros."</p>
                    <div class="client-info">
                        <div class="client-avatar">JL</div>
                        <div><strong>Javier López</strong><br><span style="font-size:0.8rem; color:var(--text-muted);">Director, LogiTrans</span></div>
                    </div>
                </div>
            </div>
            
            <!-- Generic Logos -->
            <div style="display:flex; justify-content:center; gap:40px; margin-top:50px; opacity:0.4; flex-wrap:wrap;">
               <svg width="100" height="30" viewBox="0 0 100 30" fill="currentColor"><rect x="0" y="5" width="20" height="20" rx="2"/><rect x="25" y="10" width="70" height="10" rx="2"/></svg>
               <svg width="100" height="30" viewBox="0 0 100 30" fill="currentColor"><circle cx="15" cy="15" r="10"/><rect x="35" y="10" width="60" height="10" rx="2"/></svg>
               <svg width="100" height="30" viewBox="0 0 100 30" fill="currentColor"><path d="M10 5L20 25H0L10 5Z"/><rect x="25" y="10" width="70" height="10" rx="2"/></svg>
            </div>
        </div>
    </section>

    <!-- CONTACT CTA -->
    <section id="contacto" class="section-padding cta-section">
        <div class="wave-bg" style="transform: scaleY(-1); bottom:0; top:auto;">
             <svg class="wave-svg" viewBox="0 0 1440 600" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M0,300 C320,100 640,100 960,300 C1280,500 1600,500 1920,300 L1920,600 L0,600 Z" fill="url(#grad1)" filter="url(#glow)" />
            </svg>
        </div>
        <div class="container reveal">
            <h2>¿Listo para <span class="text-gradient">Escalar?</span></h2>
            <p style="max-width:500px; margin: 0 auto 30px;">Déjanos tus datos y agendaremos una sesión estratégica.</p>
            <div class="form-container">
                <form id="contactForm" novalidate>
                    <div class="form-group"><label for="name" class="form-label">Nombre</label><input type="text" id="name" class="form-input" required></div>
                    <div class="form-group"><label for="email" class="form-label">Email</label><input type="email" id="email" class="form-input" required></div>
                    <div class="form-group"><label for="message" class="form-label">Reto principal</label><textarea id="message" rows="3" class="form-textarea"></textarea></div>
                    <div class="form-checkbox-group"><input type="checkbox" id="privacy" required><label for="privacy">Acepto la política de privacidad.</label></div>
                    <button type="submit" class="btn btn-primary" style="width: 100%;">Solicitar Diagnóstico</button>
                </form>
                <div id="successMessage" class="success-overlay">
                    <h3>¡Solicitud Recibida!</h3><p>Contactaremos contigo pronto.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="footer">
        <div class="container footer-content">
            <!-- Col 1: Branding -->
            <div class="footer-col">
                <a href="#" class="logo" style="font-size: 1.2rem; margin-bottom: 10px;">Everon.</a>
                <p style="margin:0; font-size:0.85rem;">Transformando incertidumbre en crecimiento.</p>
            </div>

            <!-- Col 2: Contact Info (NEW) -->
            <div class="footer-col footer-contact">
                <h4>Contacto</h4>
                <p><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg> Paseo de la Castellana 100, Madrid</p>
                <p><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/></svg> +34 912 345 678</p>
                <p><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg> hola@everon.com</p>
            </div>
            
            <!-- Col 3: Social & Legal -->
            <div class="footer-col" style="text-align: right;">
                 <div class="social-links" style="justify-content: flex-end;">
                    <a href="#" aria-label="LinkedIn"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg></a>
                    <!-- INSTAGRAM ICON (Replaced Twitter) -->
                    <a href="#" aria-label="Instagram"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg></a>
                </div>
                <div class="footer-legal">
                    <a href="#">Aviso Legal</a>
                    <a href="#">Privacidad</a>
                    <div style="margin-top:5px; opacity:0.6;">© 2024 Everon Strategy</div>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const hamburger = document.querySelector('.hamburger');
            const navLinks = document.querySelector('.nav-links');
            const links = document.querySelectorAll('.nav-link, .btn-primary');

            hamburger.addEventListener('click', () => {
                navLinks.classList.toggle('active');
            });
            links.forEach(link => {
                link.addEventListener('click', () => { navLinks.classList.remove('active'); });
            });

            // Scroll Spy & Reveal
            const sections = document.querySelectorAll('section');
            const navItems = document.querySelectorAll('.nav-link');
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        const id = entry.target.getAttribute('id');
                        navItems.forEach(link => {
                            link.classList.remove('active');
                            if (link.getAttribute('href') === `#${id}`) link.classList.add('active');
                        });
                    }
                });
            }, { threshold: 0.3 });
            sections.forEach(section => observer.observe(section));

            const revealElements = document.querySelectorAll('.reveal');
            const revealObserver = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('active');
                        revealObserver.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.1 });
            revealElements.forEach(el => revealObserver.observe(el));

            // Form
            const form = document.getElementById('contactForm');
            const successMsg = document.getElementById('successMessage');
            form.addEventListener('submit', (e) => {
                e.preventDefault();
                let isValid = true;
                const name = document.getElementById('name');
                const email = document.getElementById('email');
                if(!name.value.trim() || !email.value.includes('@')) isValid = false;
                
                if (isValid) {
                    const btn = form.querySelector('button');
                    btn.textContent = 'Enviando...';
                    btn.disabled = true;
                    setTimeout(() => {
                        successMsg.classList.add('visible');
                        form.reset();
                        btn.textContent = 'Solicitar Diagnóstico';
                        btn.disabled = false;
                    }, 1500);
                }
            });

            // GEMINI AI INTEGRATION
            const aiBtn = document.getElementById('ai-btn');
            const aiLoading = document.getElementById('ai-loading');
            const aiResult = document.getElementById('ai-result');
            const aiPlaceholder = document.getElementById('ai-placeholder');
            const apiKey = ""; 

            async function callGeminiAPI(prompt) {
                const response = await fetch(
                    `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`,
                    {
                        method: 'POST',
                        headers: { 'Content-Type': 'application/json' },
                        body: JSON.stringify({ contents: [{ parts: [{ text: prompt }] }] })
                    }
                );
                return await response.json();
            }

            aiBtn.addEventListener('click', async () => {
                const industry = document.getElementById('ai-industry').value.trim();
                const challenge = document.getElementById('ai-challenge').value.trim();
                const email = document.getElementById('ai-email').value.trim(); // Nuevo campo Email

                if (!industry || !challenge) {
                    alert("Por favor, completa Industria y Reto.");
                    return;
                }
                
                if (!email || !email.includes('@')) {
                    alert("Por favor, introduce un email válido para recibir el informe.");
                    return;
                }

                aiBtn.disabled = true;
                aiBtn.innerHTML = '<span>Generando y Enviando...</span>';
                aiPlaceholder.style.display = 'none';
                aiResult.innerHTML = '';
                aiLoading.style.display = 'flex';

                // PROMPT: Estrategia de Marketing + Transformación Digital
                const prompt = `Actúa como un Estratega Senior de Marketing y Transformación Digital de Everon. El usuario tiene un negocio en la industria: '${industry}' y su reto principal es: '${challenge}'. 
                
                Dame 3 estrategias accionables priorizando el marketing de contenidos, la narrativa de marca y la captación digital.
                IMPORTANTE: Asegúrate de conectar estas acciones con la transformación digital y la optimización de procesos como palancas clave para escalar los resultados.
                
                Usa un tono profesional, creativo y orientado a resultados.
                Formato de salida: solo devuelve un código HTML <ul> con 3 <li>. No uses markdown, ni intro, ni outro. 
                Cada <li> debe tener un <strong>título corto</strong> seguido de la explicación.`;

                try {
                    const data = await callGeminiAPI(prompt);
                    const generatedText = data.candidates[0].content.parts[0].text;
                    const cleanHtml = generatedText.replace(/```html/g, '').replace(/```/g, '');
                    
                    // Simulación de envío de email
                    console.log("Enviando correo a:", email);
                    console.log("Contenido:", cleanHtml);

                    // Retardo artificial para simular el envío SMTP
                    await new Promise(resolve => setTimeout(resolve, 1500));

                    // Renderizar éxito + vista previa "template de email"
                    aiResult.innerHTML = `
                        <div class="email-success-badge">
                            <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3"><polyline points="20 6 9 17 4 12"></polyline></svg>
                            Informe enviado correctamente a ${email}
                        </div>
                        <div class="email-preview-header">
                            <strong>Asunto:</strong> Tu Estrategia Personalizada Everon 🚀<br>
                            <strong>Para:</strong> ${email}
                        </div>
                        ${cleanHtml}
                        <p style="font-size:0.8rem; margin-top:20px; opacity:0.7; border-top:1px solid rgba(255,255,255,0.1); padding-top:10px;">
                            ¿Quieres profundizar en este plan? <a href="#contacto" style="color:var(--primary-glow)">Agenda una llamada</a> con nuestro equipo.
                        </p>
                    `;
                } catch (error) {
                    console.error(error);
                    aiResult.innerHTML = '<p style="color:#ef4444; text-align:center;">Error de conexión. Inténtalo de nuevo.</p>';
                } finally {
                    aiLoading.style.display = 'none';
                    aiBtn.disabled = false;
                    aiBtn.innerHTML = '<span>Generar y Enviar a mi Correo ✨</span>';
                }
            });
        });
    </script>
</body>
</html>
