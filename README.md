<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Guia Completo: Primeiros Cuidados Psicológicos</title>
    <style>
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

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            color: var(--text-main);
            line-height: 1.6;
            background-color: var(--bg-light);
            overflow-x: hidden; /* Evita rolagem lateral indesejada */
        }

        /* --- Layout Centralizado --- */
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
            width: 100%;
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
            max-width: 1100px;
            margin: 0 auto;
            padding: 1rem 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.3rem;
            font-weight: 800;
            color: var(--primary);
            text-decoration: none;
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
            font-size: 0.9rem;
            transition: color 0.3s;
        }

        .nav-links a:hover { color: var(--primary); }

        /* Menu Mobile */
        .menu-toggle {
            display: none;
            flex-direction: column;
            gap: 5px;
            cursor: pointer;
        }

        .menu-toggle span {
            width: 25px;
            height: 3px;
            background-color: var(--primary);
        }

        /* --- Hero Section --- */
        header {
            background: linear-gradient(135deg, var(--primary-light) 0%, #c3ddfa 100%);
            padding: 10rem 0 6rem;
            text-align: center;
            border-bottom: 4px solid var(--primary);
        }

        header h1 {
            font-size: clamp(2rem, 5vw, 2.8rem);
            color: var(--primary-dark);
            margin-bottom: 1.5rem;
        }

        header p {
            font-size: 1.1rem;
            max-width: 700px;
            margin: 0 auto 2rem;
            padding: 0 20px;
        }

        /* --- Seções Gerais --- */
        section {
            padding: 5rem 0;
        }

        section:nth-child(even) {
            background-color: var(--white);
        }

        .section-title {
            text-align: center;
            font-size: 2rem;
            color: var(--primary-dark);
            margin-bottom: 3rem;
        }

        .section-title::after {
            content: '';
            width: 50px;
            height: 4px;
            background-color: var(--primary);
            display: block;
            margin: 10px auto 0;
        }

        /* --- Grids e Cards --- */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            justify-content: center;
        }

        .card {
            background: var(--white);
            padding: 2rem;
            border-radius: 12px;
            border: 1px solid #e2e8f0;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
        }

        .card-icon { font-size: 2.5rem; margin-bottom: 1rem; }

        /* --- Listas Do/Don't --- */
        .dos-donts {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .list-box {
            padding: 2rem;
            border-radius: 12px;
            background: var(--bg-light);
        }

        .list-box.do { border-top: 5px solid var(--success); }
        .list-box.dont { border-top: 5px solid var(--danger); }

        .list-box ul { list-style: none; margin-top: 1rem; }
        .list-box li { margin-bottom: 0.8rem; padding-left: 1.5rem; position: relative; }
        .list-box.do li::before { content: '✓'; color: var(--success); position: absolute; left: 0; font-weight: bold; }
        .list-box.dont li::before { content: '✕'; color: var(--danger); position: absolute; left: 0; font-weight: bold; }

        /* --- Rodapé --- */
        footer {
            background-color: var(--text-main);
            color: var(--white);
            padding: 3rem 0;
            text-align: center;
        }

        /* --- Ajustes Responsivos --- */
        @media (max-width: 768px) {
            .menu-toggle { display: flex; }
            .nav-links {
                display: none;
                position: absolute;
                top: 60px;
                left: 0;
                width: 100%;
                background: white;
                flex-direction: column;
                text-align: center;
                padding: 1rem 0;
                box-shadow: 0 5px 10px rgba(0,0,0,0.1);
            }
            .nav-links.active { display: flex; }
            header { padding-top: 7rem; }
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
                <li><a href="#autocuidado">Autocuidado</a></li>
                <li><a href="#ajuda">Pedir Ajuda</a></li>
            </ul>
        </div>
    </nav>

    <header>
        <div class="container">
            <h1>Primeiros Cuidados Psicológicos</h1>
            <p>Um guia prático para oferecer apoio humano e solidário a pessoas em situações de crise.</p>
            <a href="#principios" style="display:inline-block; background:var(--primary); color:white; padding:12px 30px; border-radius:30px; text-decoration:none; font-weight:bold;">Começar Guia</a>
        </div>
    </header>

    <section id="sobre">
        <div class="container">
            <h2 class="section-title">O Básico</h2>
            <div class="grid">
                <div class="card">
                    <div class="card-icon">👥</div>
                    <h3>Qualquer pessoa</h3>
                    <p>Não é necessário ser profissional de saúde mental para aplicar os cuidados básicos.</p>
                </div>
                <div class="card">
                    <div class="card-icon">⏱️</div>
                    <h3>Imediato</h3>
                    <p>Aplicado logo após o evento estressante para reduzir a angústia inicial.</p>
                </div>
                <div class="card">
                    <div class="card-icon">📍</div>
                    <h3>Em qualquer lugar</h3>
                    <p>Desde que o ambiente ofereça segurança e o mínimo de privacidade.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="principios">
        <div class="container">
            <h2 class="section-title">Princípios OMS</h2>
            <div class="grid">
                <div class="card">
                    <h3>1. Observar</h3>
                    <p>Verifique a segurança do local e se há pessoas com reações graves.</p>
                </div>
                <div class="card">
                    <h3>2. Ouvir</h3>
                    <p>Aproxime-se, pergunte o que a pessoa precisa e ouça sem julgar.</p>
                </div>
                <div class="card">
                    <h3>3. Aproximar</h3>
                    <p>Conecte a pessoa com informações e serviços de ajuda prática.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="dicas">
        <div class="container">
            <h2 class="section-title">Como Agir</h2>
            <div class="dos-donts">
                <div class="list-box do">
                    <h3>O que Fazer</h3>
                    <ul>
                        <li>Seja calmo e paciente.</li>
                        <li>Respeite o desejo de silêncio.</li>
                        <li>Ofereça ajuda prática (água, cobertor).</li>
                    </ul>
                </div>
                <div class="list-box dont">
                    <h3>O que Evitar</h3>
                    <ul>
                        <li>Não force a pessoa a falar.</li>
                        <li>Não dê falsas promessas.</li>
                        <li>Não julgue o comportamento dela.</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="ajuda">
        <div class="container" style="text-align: center;">
            <h2 class="section-title">Contatos de Emergência</h2>
            <div class="grid">
                <div class="card" style="border: 2px solid var(--danger);">
                    <h2 style="color:var(--danger)">188</h2>
                    <p><strong>CVV</strong> - Apoio emocional gratuito e 24h.</p>
                </div>
                <div class="card">
                    <h2 style="color:var(--primary)">192</h2>
                    <p><strong>SAMU</strong> - Emergências de saúde.</p>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>© 2026 ApoioPsi - Conteúdo baseado nas diretrizes da OMS.</p>
        </div>
    </footer>

    <script>
        // Menu Mobile Toggle
        const menuToggle = document.getElementById('mobile-menu');
        const navLinks = document.getElementById('nav-links');

        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Fecha o menu ao clicar em um link (mobile)
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });
    </script>
</body>
</html>
