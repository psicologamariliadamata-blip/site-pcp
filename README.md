<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Guia Completo: Primeiros Cuidados Psicológicos</title>
    <style>
        /* Variáveis de Cores e Tema */
        :root {
            --primary: #2b6cb0;
            --primary-light: #ebf8ff;
            --primary-dark: #2c5282;
            --text-main: #2d3748;
            --text-muted: #718096;
            --bg-light: #f7fafc;
            --white: #ffffff;
            --success: #38a169;
            --danger: #e53e3e;
            --warning: #dd6b20;
        }

        /* Reset e Configurações Base */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            color: var(--text-main);
            line-height: 1.6;
            background-color: var(--bg-light);
        }

        /* --- Navegação --- */
        nav {
            background-color: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--primary);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav-links {
            list-style: none;
            display: flex;
            gap: 1.5rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-main);
            font-weight: 500;
            transition: color 0.3s;
            font-size: 0.95rem;
        }

        .nav-links a:hover { color: var(--primary); }

        /* Menu Mobile Toggle */
        .menu-toggle {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 5px;
        }

        .menu-toggle span {
            width: 25px;
            height: 3px;
            background-color: var(--primary);
            transition: 0.3s;
        }

        /* --- Cabeçalho (Hero) --- */
        header {
            background: linear-gradient(135deg, var(--primary-light) 0%, #c3ddfa 100%);
            padding: 8rem 2rem 5rem;
            text-align: center;
            border-bottom: 4px solid var(--primary);
        }

        header h1 {
            font-size: 2.8rem;
            color: var(--primary-dark);
            margin-bottom: 1.5rem;
            max-width: 800px;
            margin-inline: auto;
        }

        header p {
            font-size: 1.2rem;
            color: var(--text-main);
            max-width: 700px;
            margin: 0 auto 2rem;
        }

        .btn {
            background-color: var(--primary);
            color: var(--white);
            padding: 0.8rem 2rem;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            transition: all 0.3s ease;
            display: inline-block;
            box-shadow: 0 4px 6px rgba(43, 108, 176, 0.2);
        }

        .btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
        }

        /* --- Estrutura de Seções --- */
        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        section:nth-child(even) {
            background-color: var(--white);
            max-width: 100%;
        }

        .section-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            color: var(--primary-dark);
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            width: 60px;
            height: 4px;
            background-color: var(--primary);
            display: block;
            margin: 10px auto 0;
            border-radius: 2px;
        }

        /* --- Grid Cards --- */
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .card {
            background-color: var(--white);
            padding: 2.5rem 2rem;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            text-align: center;
            transition: transform 0.3s;
            border: 1px solid #e2e8f0;
        }

        .card:hover { transform: translateY(-5px); }

        .card-icon { font-size: 3rem; margin-bottom: 1rem; }

        .card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary-dark);
        }

        /* --- Dos and Donts --- */
        .dos-donts {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .list-box {
            background: var(--bg-light);
            padding: 2.5rem;
            border-radius: 12px;
        }

        .list-box.do { border-top: 5px solid var(--success); }
        .list-box.dont { border-top: 5px solid var(--danger); }

        .list-box h3 { margin-bottom: 1.5rem; font-size: 1.4rem; }
        .list-box.do h3 { color: var(--success); }
        .list-box.dont h3 { color: var(--danger); }

        .list-box ul { list-style: none; }

        .list-box li {
            margin-bottom: 1rem;
            padding-left: 1.5rem;
            position: relative;
        }

        .list-box.do li::before {
            content: '✓'; color: var(--success); position: absolute; left: 0; font-weight: bold;
        }

        .list-box.dont li::before {
            content: '✕'; color: var(--danger); position: absolute; left: 0; font-weight: bold;
        }

        /* --- Populações Específicas --- */
        .special-groups {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }

        .group-card {
            background: var(--primary-light);
            padding: 2rem;
            border-radius: 8px;
            border-left: 4px solid var(--primary);
        }

        /* --- Mitos e Verdades --- */
        details {
            background: var(--white);
            margin-bottom: 1rem;
            border-radius: 8px;
            border: 1px solid #e2e8f0;
        }

        summary {
            padding: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: var(--primary-dark);
        }

        .details-content { padding: 0 1.2rem 1.2rem; color: var(--text-muted); }

        /* --- Autocuidado e Ajuda --- */
        .alert-box {
            background-color: #fffaf0;
            border-left: 5px solid var(--warning);
            padding: 2rem;
            border-radius: 8px;
            margin-bottom: 3rem;
        }

        .emergency-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 1.5rem;
        }

        .emergency-card {
            background: #fff5f5;
            padding: 1.5rem;
            border-radius: 8px;
            border: 1px solid #fed7d7;
            text-align: center;
        }

        .emergency-card h4 { color: var(--danger); font-size: 1.5rem; }

        /* --- Footer --- */
        footer {
            background-color: var(--text-main);
            color: var(--white);
            text-align: center;
            padding: 3rem 2rem;
        }

        /* --- Responsividade --- */
        @media (max-width: 768px) {
            .nav-links {
                position: absolute;
                top: 70px;
                left: -100%;
                width: 100%;
                background-color: var(--white);
                flex-direction: column;
                transition: 0.3s;
                box-shadow: 0 10px 10px rgba(0,0,0,0.1);
            }
            .nav-links.active { left: 0; }
            .nav-links li { padding: 1.5rem; border-top: 1px solid var(--bg-light); }
            .menu-toggle { display: flex; }
            header h1 { font-size: 2rem; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="nav-container">
            <a href="#" class="logo">💙 ApoioPsi</a>
            <div class="menu-toggle" id="mobile-menu">
                <span></span><span></span><span></span>
            </div>
            <ul class="nav-links" id="nav-links">
                <li><a href="#sobre">O que são?</a></li>
                <li><a href="#principios">Os 3 Princípios</a></li>
                <li><a href="#dicas">Como Agir</a></li>
                <li><a href="#grupos">Casos Específicos</a></li>
                <li><a href="#autocuidado">Autocuidado</a></li>
                <li><a href="#ajuda">Pedir Ajuda</a></li>
            </ul>
        </div>
    </nav>

    <header id="inicio">
        <h1>Primeiros Cuidados Psicológicos (PCP)</h1>
        <p>Apoio humano, solidário e prático a pessoas que vivenciaram uma situação de crise. Você não precisa ser psicólogo para oferecer conforto e segurança.</p>
        <a href="#principios" class="btn">Conhecer o Método da OMS</a>
    </header>

    <section id="sobre">
        <div class="section-content">
            <h2 class="section-title">O Básico sobre os PCP</h2>
            <div class="grid-3">
                <div class="card">
                    <div class="card-icon">👥</div>
                    <h3>Quem pode aplicar?</h3>
                    <p>Qualquer pessoa orientada. Não é psicoterapia, é suporte prático e escuta empática.</p>
                </div>
                <div class="card">
                    <div class="card-icon">⏱️</div>
                    <h3>Quando aplicar?</h3>
                    <p>Logo após o evento traumático ou enquanto as reações agudas de estresse persistirem.</p>
                </div>
                <div class="card">
                    <div class="card-icon">📍</div>
                    <h3>Onde aplicar?</h3>
                    <p>Em locais seguros, que ofereçam o máximo de privacidade possível.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="principios">
        <div class="section-content">
            <h2 class="section-title">Os Princípios de Ação</h2>
            <div class="grid-3">
                <div class="card" style="border-top: 4px solid var(--warning)">
                    <div class="card-icon">👀</div>
                    <h3>1. Observar</h3>
                    <p>Verifique a segurança e identifique pessoas com necessidades urgentes ou reações graves.</p>
                </div>
                <div class="card" style="border-top: 4px solid var(--primary)">
                    <div class="card-icon">👂</div>
                    <h3>2. Ouvir</h3>
                    <p>Aproxime-se, pergunte as necessidades e ouça ativamente para ajudar a pessoa a se acalmar.</p>
                </div>
                <div class="card" style="border-top: 4px solid var(--success)">
                    <div class="card-icon">🤝</div>
                    <h3>3. Aproximar</h3>
                    <p>Ajude a resolver necessidades básicas e conecte a pessoa aos seus entes queridos e serviços.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="dicas">
        <div class="section-content">
            <h2 class="section-title">Diretrizes de Conduta</h2>
            <div class="dos-donts">
                <div class="list-box do">
                    <h3>O que FAZER</h3>
                    <ul>
                        <li>Seja honesto e respeite o silêncio.</li>
                        <li>Valide os sentimentos da pessoa.</li>
                        <li>Ofereça ajuda prática (água, telefone).</li>
                    </ul>
                </div>
                <div class="list-box dont">
                    <h3>O que NÃO FAZER</h3>
                    <ul>
                        <li>Não force a pessoa a falar.</li>
                        <li>Não use clichês ("vai ficar tudo bem").</li>
                        <li>Não faça promessas que não pode cumprir.</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="grupos">
        <div class="section-content">
            <h2 class="section-title">Grupos Vulneráveis</h2>
            <div class="special-groups">
                <div class="group-card">
                    <h4>👶 Crianças</h4>
                    <p>Mantenha-as perto dos cuidadores e use linguagem simples.</p>
                </div>
                <div class="group-card">
                    <h4>🧓 Idosos</h4>
                    <p>Garanta que tenham seus óculos ou aparelhos auditivos por perto.</p>
                </div>
                <div class="group-card">
                    <h4>♿ Pessoas com Deficiência</h4>
                    <p>Pergunte como ajudar antes de tomar qualquer iniciativa.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="autocuidado">
        <div class="section-content">
            <h2 class="section-title">Cuidar de Quem Ajuda</h2>
            <div class="alert-box">
                <h3>A Regra de Ouro: Proteja-se primeiro</h3>
                <p>Avalie sua disposição emocional antes de ajudar. Faça pausas e converse sobre sua experiência com alguém de confiança após o atendimento.</p>
            </div>
        </div>
    </section>

    <section id="ajuda">
        <div
