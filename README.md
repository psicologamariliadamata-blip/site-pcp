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

        /* --- Grid Cards (Princípios e Contexto) --- */
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
            position: relative;
            overflow: hidden;
        }

        .card:hover { transform: translateY(-5px); }

        .card-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary-dark);
        }

        /* --- O que fazer / Não Fazer --- */
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

        .list-box ul {
            list-style: none;
        }

        .list-box li {
            margin-bottom: 1rem;
            padding-left: 1.5rem;
            position: relative;
        }

        .list-box.do li::before {
            content: '✓';
            color: var(--success);
            position: absolute;
            left: 0;
            font-weight: bold;
        }

        .list-box.dont li::before {
            content: '✕';
            color: var(--danger);
            position: absolute;
            left: 0;
            font-weight: bold;
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

        .group-card h4 {
            color: var(--primary-dark);
            margin-bottom: 0.5rem;
            font-size: 1.2rem;
        }

        /* --- Mitos e Verdades (Accordion) --- */
        details {
            background: var(--white);
            margin-bottom: 1rem;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            overflow: hidden;
            border: 1px solid #e2e8f0;
        }

        summary {
            padding: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            list-style: none;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: var(--primary-dark);
        }

        summary::-webkit-details-marker { display: none; }
        
        summary::after {
            content: '+';
            font-size: 1.5rem;
            color: var(--primary);
        }

        details[open] summary::after { content: '-'; }

        .details-content {
            padding: 0 1.2rem 1.2rem;
            color: var(--text-muted);
        }

        /* --- Autocuidado e Ajuda --- */
        .alert-box {
            background-color: #fffaf0;
            border-left: 5px solid var(--warning);
            padding: 2rem;
            border-radius: 8px;
            margin-bottom: 3rem;
        }

        .alert-box h3 { color: #c05621; margin-bottom: 1rem; }

        .emergency-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .emergency-card {
            background: #fff5f5;
            padding: 1.5rem;
            border-radius: 8px;
            border: 1px solid #fed7d7;
            text-align: center;
        }

        .emergency-card h4 { color: var(--danger); font-size: 1.5rem; margin-bottom: 0.5rem; }

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
                text-align: center;
                gap: 0;
                transition: 0.3s ease-in-out;
                box-shadow: 0 10px 10px rgba(0,0,0,0.1);
            }

            .nav-links.active { left: 0; }

            .nav-links li { padding: 1.5rem 0; border-top: 1px solid var(--bg-light); }

            .menu-toggle { display: flex; }

            header h1 { font-size: 2rem; }
            .section-title { font-size: 1.8rem; }
        }
    </style>
</head>
<body>

    <!-- Navegação -->
    <nav>
        <div class="nav-container">
            <a href="#" class="logo">💙 ApoioPsi</a>
            <div class="menu-toggle" id="mobile-menu">
                <span></span>
                <span></span>
                <span></span>
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

    <!-- Cabeçalho -->
    <header id="inicio">
        <h1>Primeiros Cuidados Psicológicos (PCP)</h1>
        <p>Apoio humano, solidário e prático a pessoas que vivenciaram uma situação de crise ou sofrimento intenso. Você não precisa ser psicólogo para ajudar a salvar uma vida.</p>
        <a href="#principios" class="btn">Conhecer o Método da OMS</a>
    </header>

    <!-- O que, Quem, Quando, Onde -->
    <section id="sobre">
        <div class="section-content">
            <h2 class="section-title">O Básico sobre os PCP</h2>
            <div class="grid-3">
                <div class="card">
                    <div class="card-icon">👥</div>
                    <h3>Quem pode aplicar?</h3>
                    <p>Qualquer pessoa orientada pode aplicar. Os PCP não são aconselhamento profissional nem psicoterapia. Trata-se de oferecer conforto e escuta segura.</p>
                </div>
                <div class="card">
                    <div class="card-icon">⏱️</div>
                    <h3>Quando aplicar?</h3>
                    <p>Idealmente durante ou logo após o evento estressante/traumático. Contudo, em alguns casos, as pessoas podem precisar de apoio semanas após o evento.</p>
                </div>
                <div class="card">
                    <div class="card-icon">📍</div>
                    <h3>Onde aplicar?</h3>
                    <p>Em qualquer local que seja seguro o suficiente. Idealmente, deve-se buscar um local onde haja privacidade e proteção contra o clima e a exposição pública.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Princípios Básicos -->
    <section id="principios">
        <div class="section-content">
            <h2 class="section-title">Os Princípios de Ação (Método OMS)</h2>
            <div class="grid-3">
                <div class="card" style="border-top: 4px solid var(--warning)">
                    <div class="card-icon">👀</div>
                    <h3>1. Observar</h3>
                    <p>Antes de se aproximar, verifique a segurança do local. Observe se há pessoas com necessidades básicas urgentes (ferimentos) ou que apresentam reações graves de angústia (paralisia, choro extremo).</p>
                </div>
                <div class="card" style="border-top: 4px solid var(--primary)">
                    <div class="card-icon">👂</div>
                    <h3>2. Ouvir</h3>
                    <p>Aproxime-se com calma. Pergunte sobre as necessidades da pessoa. Ouça ativamente, sem interromper ou julgar. Ajude a pessoa a se acalmar respeitando o ritmo dela.</p>
                </div>
                <div class="card" style="border-top: 4px solid var(--success)">
                    <div class="card-icon">🤝</div>
                    <h3>3. Aproximar</h3>
                    <p>Conecte a pessoa aos serviços de ajuda profissional. Ajude-a a resolver necessidades básicas (água, telefone). Facilite o contato dela com familiares e redes de apoio.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- O que fazer / O que não fazer -->
    <section id="dicas">
        <div class="section-content">
            <h2 class="section-title">Diretrizes Práticas de Conduta</h2>
            <div class="dos-donts">
                <div class="list-box do">
                    <h3>O que FAZER e DIZER</h3>
                    <ul>
                        <li>Seja honesto e confiável.</li>
                        <li>Respeite o direito da pessoa de não querer conversar.</li>
                        <li>Diga frases validadoras: "Sinto muito pelo que aconteceu", "Você está seguro agora".</li>
                        <li>Ofereça ajuda prática (um copo d'água, um casaco, um telefone).</li>
                        <li>Mantenha um tom de voz suave e calmo.</li>
                        <li>Reconheça as forças da pessoa e como ela tem se ajudado.</li>
                    </ul>
                </div>
                <div class="list-box dont">
                    <h3>O que NÃO FAZER e NÃO DIZER</h3>
                    <ul>
                        <li>Não force a pessoa a contar sua história ou detalhes do trauma.</li>
                        <li>Não interrompa ou apresse a pessoa enquanto ela fala.</li>
                        <li>Não use frases clichês ("Tudo vai ficar bem", "Poderia ter sido pior").</li>
                        <li>Não julgue o que ela fez ou deixou de fazer para sobreviver.</li>
                        <li>Não prometa coisas que você não pode cumprir.</li>
                        <li>Não compartilhe as informações da pessoa com curiosos.</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Populações Específicas -->
    <section id="grupos">
        <div class="section-content">
            <h2 class="section-title">Atenção a Grupos Vulneráveis</h2>
            <div class="special-groups">
                <div class="group-card">
                    <h4>👶 Crianças e Adolescentes</h4>
                    <p>Abaixe-se na altura dos olhos da criança. Use palavras simples e não separe crianças de seus cuidadores, a menos que seja estritamente necessário para sua segurança.</p>
                </div>
                <div class="group-card">
                    <h4>🧓 Idosos</h4>
                    <p>Fale com clareza (sem gritar). Certifique-se de que estão com seus óculos, aparelhos auditivos ou bengalas. Questione com delicadeza sobre medicamentos de uso contínuo que possam ter perdido.</p>
                </div>
                <div class="group-card">
                    <h4>♿ Pessoas com Deficiência</h4>
                    <p>Pergunte como pode ajudá-los em vez de simplesmente assumir que sabem do que precisam. Garanta que a área de abrigo e os banheiros sejam acessíveis a eles.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Mitos e Verdades -->
    <section id="mitos" style="background-color: var(--white);">
        <div class="section-content">
            <h2 class="section-title">Mitos e Verdades</h2>
            <div style="max-width: 800px; margin: 0 auto;">
                <details>
                    <summary>As pessoas precisam falar sobre o trauma para superá-lo.</summary>
                    <div class="details-content">
                        <strong>Mito.</strong> Forçar alguém a reviver o trauma pode causar re-traumatização. Respeite se a pessoa preferir o silêncio.
                    </div>
                </details>
                <details>
                    <summary>Chorar faz a pessoa piorar, devo pedir para ela se acalmar.</summary>
                    <div class="details-content">
                        <strong>Mito.</strong> O choro é uma forma natural de processar o estresse. Deixe a pessoa chorar, ofereça um lenço e fique presente em silêncio.
                    </div>
                </details>
                <details>
                    <summary>Primeiros Cuidados Psicológicos não são terapia.</summary>
                    <div class="details-content">
                        <strong>Verdade.</strong> O objetivo é fornecer alívio imediato e suporte prático, e não fazer diagnósticos psicológicos ou tratar patologias.
                    </div>
                </details>
            </div>
        </div>
    </section>

    <!-- Autocuidado -->
    <section id="autocuidado">
        <div class="section-content">
            <h2 class="section-title">O Cuidado de Quem Cuida</h2>
            <div class="alert-box">
                <h3>A Regra de Ouro: Proteja-se primeiro</h3>
                <p>Ajudar pessoas em situação de crise pode ser desgastante. Você não pode servir água de um copo vazio.</p>
                <ul style="margin-top: 1rem; margin-left: 1.5rem;">
                    <li><strong>Antes de ajudar:</strong> Avalie se você está física e emocionalmente apto.</li>
                    <li><strong>Durante:</strong> Faça pausas. Peça ajuda a outros voluntários se a situação estiver pesada.</li>
                    <li><strong>Depois:</strong> Converse com alguém de sua confiança sobre o que você viveu. Descanse, coma bem e evite consumir álcool para lidar com o estresse da ajuda.</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Ajuda Profissional -->
    <section id="ajuda">
        <div class="section-content">
            <h2 class="section-title">Contatos de Emergência (Brasil)</h2>
            <p style="text-align: center; margin-bottom: 2rem;">Acione ajuda profissional se a pessoa não conseguir cuidar de si mesma, estiver profundamente desorientada ou em risco de ferir a si mesma ou aos outros.</p>
            
            <div class="emergency-grid">
                <div class="emergency-card">
                    <h4>📞 188</h4>
                    <strong>CVV</strong>
                    <p>Centro de Valorização da Vida. Apoio emocional gratuito, sigiloso e 24h.</p>
                </div>
                <div class="emergency-card">
                    <h4>🚑 192</h4>
                    <strong>SAMU</strong>
                    <p>Emergências médicas urgentes, incluindo surtos psicóticos graves.</p>
                </div>
                <div class="emergency-card">
                    <h4>🚒 193</h4>
                    <strong>Bombeiros</strong>
                    <p>Prevenção de suicídio em andamento e resgate em áreas de risco.</p>
                </div>
                <div class="emergency-card">
                    <h4>🏥 CAPS</h4>
                    <strong>Rede SUS</strong>
                    <p>Centro de Atenção Psicossocial. Busque na sua cidade para tratamento contínuo.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Rodapé -->
    <footer>
        <p><strong>ApoioPsi</strong> - Diretrizes baseadas nos manuais da Organização Mundial da Saúde (OMS) e OPAS.</p>
        <p style="font-size: 0.85rem; margin-top: 1rem; color: #a0aec0;">
            * Isenção de responsabilidade: Este site tem fins estritamente informativos. O treinamento prático é encorajado. Em caso de sofrimento prolongado, busque sempre um profissional de saúde mental (Psicólogo ou Psiquiatra).
        </p>
    </footer>

    <!-- Scripts -->
    <script>
        // Menu Mobile (Hamburguer)
        const menuToggle = document.getElementById('mobile-menu');
        const navLinks = document.getElementById('nav-links');
        const links = document.querySelectorAll('.nav-links a');

        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Fechar menu ao clicar em um link
        links.forEach(link => {
            link.addEventListener('click', () => {
                if (navLinks.classList.contains('active')) {
                    navLinks.classList.remove('active');
                }
            });
        });

        // Rolagem Suave
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if(target) {
                    // Compensa a altura do menu fixo (aprox 70px)
                    const offsetTop = target.offsetTop - 70;
                    window.scrollTo({
                        top: offsetTop,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>

</body>
</html>
