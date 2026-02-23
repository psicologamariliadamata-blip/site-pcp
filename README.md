<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Primeiros Cuidados Psicológicos | Guia Completo</title>
    <!-- FontAwesome para Ícones -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* Variáveis de Cores e Estilos */
        :root {
            --primary: #2b6cb0; 
            --primary-dark: #1a365d;
            --secondary: #4299e1;
            --bg-light: #f7fafc;
            --text-dark: #2d3748;
            --text-muted: #718096;
            --white: #ffffff;
            --success: #38a169;
            --danger: #e53e3e;
            --warning: #dd6b20;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }

        body {
            color: var(--text-dark);
            line-height: 1.6;
            background-color: var(--bg-light);
            padding-top: 70px;
        }

        /* --- NAVEGAÇÃO --- */
        nav {
            background-color: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
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
            font-weight: bold;
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
            color: var(--text-dark);
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover { color: var(--secondary); }

        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--primary);
        }

        /* --- HERO SECTION --- */
        header {
            background: linear-gradient(135deg, var(--primary-dark) 0%, var(--primary) 100%);
            color: var(--white);
            padding: 6rem 2rem;
            text-align: center;
        }

        header h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            animation: fadeInDown 1s ease;
        }

        header p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
            opacity: 0.9;
        }

        .btn {
            background-color: var(--white);
            color: var(--primary-dark);
            padding: 1rem 2rem;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s;
            display: inline-block;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.15);
        }

        /* --- SEÇÕES GERAIS --- */
        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        section:nth-child(even) { background-color: var(--white); max-width: 100%; }

        .section-inner {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            color: var(--primary-dark);
            margin-bottom: 3rem;
        }

        /* --- GRIDS --- */
        .grid-2, .grid-3 {
            display: grid;
            gap: 2rem;
        }
        .grid-2 { grid-template-columns: 1fr 1fr; }
        .grid-3 { grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); }

        .card {
            background: var(--white);
            padding: 2.5rem 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            text-align: center;
            transition: transform 0.3s;
            border-bottom: 4px solid var(--primary);
        }

        .card:hover { transform: translateY(-5px); }

        .card i {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 1.5rem;
        }

        .card h3 { margin-bottom: 1rem; color: var(--text-dark); }

        /* --- DOS AND DONTS --- */
        .list-box {
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            background: var(--white);
        }

        .list-box.do { border-top: 5px solid var(--success); }
        .list-box.dont { border-top: 5px solid var(--danger); }

        .list-box h3 { margin-bottom: 1.5rem; display: flex; align-items: center; gap: 10px; }
        .list-box.do h3 { color: var(--success); }
        .list-box.dont h3 { color: var(--danger); }

        .list-box ul { list-style: none; }
        .list-box li { margin-bottom: 1rem; display: flex; align-items: flex-start; gap: 10px; }
        .list-box.do li::before { content: "\f00c"; font-family: "Font Awesome 6 Free"; font-weight: 900; color: var(--success); }
        .list-box.dont li::before { content: "\f00d"; font-family: "Font Awesome 6 Free"; font-weight: 900; color: var(--danger); }

        /* --- AUTOCUIDADO --- */
        .self-care {
            background-color: #fffaf0;
            border-left: 5px solid var(--warning);
            padding: 2rem;
            border-radius: 0 10px 10px 0;
            margin-top: 2rem;
        }

        /* --- PESQUISA IA --- */
        .ai-search-container {
            background: linear-gradient(to right, #ffffff, #f0f7ff);
            border: 1px solid #e2e8f0;
            border-radius: 12px;
            padding: 3rem 2rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.08);
            text-align: center;
        }
        
        .ai-search-box {
            display: flex;
            gap: 10px;
            max-width: 700px;
            margin: 0 auto;
            position: relative;
        }
        
        .ai-search-box input {
            flex: 1;
            padding: 1.2rem 1.5rem;
            border: 2px solid #cbd5e0;
            border-radius: 30px;
            font-size: 1rem;
            outline: none;
            transition: all 0.3s ease;
            box-shadow: inset 0 2px 4px rgba(0,0,0,0.02);
        }
        
        .ai-search-box input:focus {
            border-color: var(--secondary);
            box-shadow: 0 0 0 3px rgba(66, 153, 225, 0.2);
        }
        
        .ai-search-box button {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: var(--white);
            border: none;
            padding: 0 2rem;
            border-radius: 30px;
            cursor: pointer;
            font-size: 1.1rem;
            font-weight: bold;
            transition: transform 0.2s, box-shadow 0.2s;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .ai-search-box button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(43, 108, 176, 0.3);
        }

        .ai-result {
            background: var(--white);
            border-left: 5px solid var(--primary);
            padding: 2rem;
            border-radius: 8px;
            text-align: left;
            display: none;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            margin-top: 2rem;
            animation: fadeInDown 0.5s ease;
        }

        .ai-result.loading {
            display: block;
            color: var(--text-muted);
            text-align: center;
            border-left: none;
            background: transparent;
            box-shadow: none;
            font-size: 1.2rem;
        }

        /* --- FAQ (ACCORDION) --- */
        .faq-item {
            background: var(--white);
            margin-bottom: 1rem;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            overflow: hidden;
        }

        .faq-question {
            padding: 1.5rem;
            font-weight: bold;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: var(--primary-dark);
            background: var(--white);
            border: none;
            width: 100%;
            text-align: left;
            font-size: 1.1rem;
        }

        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease;
            background: #fafafa;
        }

        .faq-answer p { padding: 0 1.5rem 1.5rem; }
        .faq-item.active .faq-answer { max-height: 200px; }
        .faq-item.active .faq-question i { transform: rotate(180deg); }

        /* --- EMERGÊNCIA --- */
        .emergency-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .contact-card {
            background: #fff5f5;
            padding: 1.5rem;
            border-radius: 8px;
            border: 1px solid #fed7d7;
            text-align: center;
        }

        .contact-card h4 { color: var(--danger); font-size: 1.5rem; margin: 10px 0; }

        /* --- FOOTER --- */
        footer {
            background-color: var(--primary-dark);
            color: var(--white);
            text-align: center;
            padding: 3rem 2rem;
        }

        footer p { margin-bottom: 1rem; opacity: 0.8; }

        /* --- RESPONSIVIDADE --- */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                background: var(--white);
                padding: 1rem 0;
                box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            }
            .nav-links.active { display: flex; }
            .nav-links li { text-align: center; padding: 10px 0; }
            .menu-toggle { display: block; }
            .grid-2 { grid-template-columns: 1fr; }
            header h1 { font-size: 2rem; }
            .ai-search-box { flex-direction: column; }
            .ai-search-box button { padding: 1rem; justify-content: center; }
        }

        /* Animações */
        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <!-- Navegação -->
    <nav>
        <div class="nav-container">
            <a href="#" class="logo"><i class="fa-solid fa-hand-holding-heart"></i> Guia PCP</a>
            <i class="fa-solid fa-bars menu-toggle" id="mobile-menu-btn"></i>
            <ul class="nav-links" id="nav-links">
                <li><a href="#sobre">O que é?</a></li>
                <li><a href="#principios">Princípios</a></li>
                <li><a href="#vulneraveis">Grupos</a></li>
                <li><a href="#dicas">Como Agir</a></li>
                <li><a href="#ia-search">IA Assistente</a></li> <!-- Link novo -->
                <li><a href="#ajuda">Pedir Ajuda</a></li>
            </ul>
        </div>
    </nav>

    <!-- Cabeçalho -->
    <header id="inicio">
        <h1>Primeiros Cuidados Psicológicos</h1>
        <p>Apoio humano, prático e solidário a pessoas em situação de sofrimento recente. Você não precisa ser um psicólogo para oferecer ajuda e compaixão.</p>
        <a href="#principios" class="btn">Entenda como ajudar</a>
    </header>

    <!-- O que são / Mitos e Verdades -->
    <section id="sobre" style="background-color: var(--white);">
        <div class="section-inner">
            <h2 class="section-title">O que é (e o que não é) o PCP?</h2>
            <div class="grid-2">
                <div>
                    <h3 style="color: var(--primary); margin-bottom: 1rem;"><i class="fa-solid fa-check-circle"></i> O que É:</h3>
                    <p>Envolve oferecer cuidado não intrusivo e prático, avaliar necessidades básicas (como água, abrigo, informações) e ouvir sem pressionar a pessoa a falar. É ajudar a pessoa a se acalmar e conectá-la a redes de apoio.</p>
                </div>
                <div>
                    <h3 style="color: var(--danger); margin-bottom: 1rem;"><i class="fa-solid fa-times-circle"></i> O que NÃO é:</h3>
                    <p>Não é terapia. Não é aconselhamento profissional. Não envolve pedir à pessoa que analise o que aconteceu ou que detalhe cronologicamente os eventos do trauma. Não é julgar os sentimentos do outro.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Princípios Básicos -->
    <section id="principios">
        <div class="section-inner">
            <h2 class="section-title">Os 3 Princípios de Ação (OMS)</h2>
            <p style="text-align: center; margin-bottom: 3rem; color: var(--text-muted);">A Organização Mundial da Saúde define três passos cruciais para a aplicação segura do PCP.</p>
            <div class="grid-3">
                <div class="card">
                    <i class="fa-solid fa-eye"></i>
                    <h3>1. Observar</h3>
                    <p>Verifique a segurança do local. Verifique se há pessoas com necessidades básicas ou ferimentos urgentes. Observe quem apresenta reações graves de angústia antes de se aproximar.</p>
                </div>
                <div class="card">
                    <i class="fa-solid fa-ear-listen"></i>
                    <h3>2. Ouvir</h3>
                    <p>Aproxime-se das pessoas que precisam de apoio. Pergunte sobre suas preocupações, necessidades imediatas e ouça com atenção, ajudando-as a se sentirem seguras e calmas.</p>
                </div>
                <div class="card">
                    <i class="fa-solid fa-link"></i>
                    <h3>3. Aproximar (Conectar)</h3>
                    <p>Ajude as pessoas a resolverem suas necessidades imediatas. Conecte-as a serviços, informações confiáveis e, principalmente, a entes queridos e suporte social.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Grupos Vulneráveis -->
    <section id="vulneraveis" style="background-color: var(--white);">
        <div class="section-inner">
            <h2 class="section-title">Atenção a Grupos Vulneráveis</h2>
            <div class="grid-3">
                <div class="card" style="border-bottom-color: #ed8936;">
                    <i class="fa-solid fa-child-reaching" style="color: #ed8936;"></i>
                    <h3>Crianças e Adolescentes</h3>
                    <p>Reúna-os com seus cuidadores o mais rápido possível. Mantenha o tom de voz calmo. Não minta sobre o que aconteceu, use palavras adequadas à idade.</p>
                </div>
                <div class="card" style="border-bottom-color: #9f7aea;">
                    <i class="fa-solid fa-person-cane" style="color: #9f7aea;"></i>
                    <h3>Idosos</h3>
                    <p>Podem precisar de ajuda para mobilidade ou para encontrar medicações perdidas. Seja paciente. A confusão pode ser apenas desorientação devido ao trauma recente.</p>
                </div>
                <div class="card" style="border-bottom-color: #38b2ac;">
                    <i class="fa-solid fa-wheelchair" style="color: #38b2ac;"></i>
                    <h3>Pessoas com Deficiência</h3>
                    <p>Pergunte como pode ajudar antes de agir. Mantenha equipamentos de mobilidade junto a eles. Assegure-se de que consigam acessar áreas de abrigo ou comunicação.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- O que fazer / O que não fazer e Autocuidado -->
    <section id="dicas">
        <div class="section-inner">
            <h2 class="section-title">Guia Prático de Abordagem</h2>
            <div class="grid-2">
                <div class="list-box do">
                    <h3><i class="fa-solid fa-thumbs-up"></i> O que Fazer e Dizer</h3>
                    <ul>
                        <li>Encontre um lugar tranquilo e seguro para conversar.</li>
                        <li>Diga quem você é e explique que está ali para ajudar.</li>
                        <li>Pergunte o que a pessoa precisa no momento (água, casaco, telefone).</li>
                        <li>Aja de maneira calma e demonstre escuta ativa.</li>
                        <li>Permita o silêncio. Ficar ao lado já é reconfortante.</li>
                        <li>Diga: "Sinto muito por isso", "Entendo que esteja triste".</li>
                    </ul>
                </div>
                <div class="list-box dont">
                    <h3><i class="fa-solid fa-thumbs-down"></i> O que Evitar</h3>
                    <ul>
                        <li>Não pressione a pessoa a contar detalhes do evento.</li>
                        <li>Não faça falsas promessas (ex: "Tudo vai ficar bem amanhã").</li>
                        <li>Não minimize a dor (Evite: "Pelo menos você está vivo", "Você tem que ser forte").</li>
                        <li>Não conte histórias dos seus próprios problemas ou de terceiros.</li>
                        <li>Não julgue as reações da pessoa (se chora, grita ou fica apática).</li>
                    </ul>
                </div>
            </div>

            <!-- Bloco de Autocuidado -->
            <div class="self-care">
                <h3 style="color: var(--warning); margin-bottom: 1rem;"><i class="fa-solid fa-heart-pulse"></i> O Seu Autocuidado</h3>
                <p>Prestar primeiros cuidados psicológicos pode ser exaustivo. <strong>Lembre-se:</strong> você não pode ajudar se o seu "copo estiver vazio". Antes de intervir, avalie se você tem condições emocionais. Depois de ajudar, reserve um tempo para descansar, converse com alguém de confiança sobre como você se sentiu e não hesite em buscar suporte profissional se as imagens ou sentimentos do trauma o acompanharem nos dias seguintes.</p>
            </div>
        </div>
    </section>

    <!-- NOVA SEÇÃO: Assistente IA -->
    <section id="ia-search" style="background-color: var(--white);">
        <div class="section-inner">
            <h2 class="section-title"><i class="fa-solid fa-wand-magic-sparkles" style="color: var(--primary);"></i> Pergunte à IA</h2>
            <div class="ai-search-container">
                <h3 style="margin-bottom: 10px; color: var(--text-dark);">Como posso te orientar agora?</h3>
                <p style="margin-bottom: 2rem; color: var(--text-muted); max-width: 800px; margin-left: auto; margin-right: auto;">
                    Descreva rapidamente a situação de crise que você está presenciando e nossa Inteligência Artificial irá sugerir os melhores passos baseados no protocolo internacional de Primeiros Cuidados Psicológicos.
                </p>
                
                <div class="ai-search-box">
                    <input type="text" id="ai-input" placeholder="Ex: Meu amigo sofreu um acidente de trânsito leve e está em pânico..." autocomplete="off">
                    <button id="ai-btn">Consultar <i class="fa-solid fa-paper-plane"></i></button>
                </div>

                <!-- Área onde a resposta vai aparecer -->
                <div id="ai-response" class="ai-result"></div>
            </div>
        </div>
    </section>

    <!-- FAQ -->
    <section id="faq">
        <div class="section-inner">
            <h2 class="section-title">Perguntas Frequentes (FAQ)</h2>
            <div class="faq-container">
                <div class="faq-item">
                    <button class="faq-question">Eu preciso ser psicólogo para aplicar o PCP? <i class="fa-solid fa-chevron-down"></i></button>
                    <div class="faq-answer"><p>Não. Os Primeiros Cuidados Psicológicos foram desenhados para que qualquer pessoa bem-intencionada e instruída possa aplicá-los, assim como os primeiros socorros físicos (fazer um curativo, por exemplo).</p></div>
                </div>
                <div class="faq-item">
                    <button class="faq-question">E se a pessoa chorar incontrolavelmente? <i class="fa-solid fa-chevron-down"></i></button>
                    <div class="faq-answer"><p>O choro é uma reação natural ao estresse e ao trauma. Não tente parar o choro da pessoa dizendo "não chore". Ofereça um lenço, água e permaneça ao lado dela em silêncio ou afirmando que ela está segura agora.</p></div>
                </div>
                <div class="faq-item">
                    <button class="faq-question">Quanto tempo dura a aplicação do PCP? <i class="fa-solid fa-chevron-down"></i></button>
                    <div class="faq-answer"><p>Pode durar de alguns minutos a algumas horas, dependendo do contexto. É uma intervenção imediata, focada apenas no momento da crise. Depois, a pessoa deve ser encaminhada a redes de apoio contínuas, se necessário.</p></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Ajuda Profissional / Contatos -->
    <section id="ajuda" style="background-color: var(--white);">
        <div class="section-inner">
            <h2 class="section-title">Quando e Onde Buscar Ajuda Especializada?</h2>
            <p style="text-align: center; max-width: 800px; margin: 0 auto;">Se a pessoa apresentar <strong>risco iminente contra a própria vida ou a de terceiros</strong>, incapacidade de cuidar de funções básicas (como não comer, não beber) ou confusão extrema (não saber quem é ou onde está), o suporte médico imediato é necessário.</p>

            <div class="emergency-grid">
                <div class="contact-card">
                    <i class="fa-solid fa-phone-volume fa-2x" style="color: var(--danger);"></i>
                    <h4>Ligue 188</h4>
                    <p><strong>CVV</strong></p>
                    <p style="font-size: 0.9rem;">Centro de Valorização da Vida. Atendimento 24h, gratuito e sob total sigilo.</p>
                </div>
                <div class="contact-card">
                    <i class="fa-solid fa-ambulance fa-2x" style="color: var(--danger);"></i>
                    <h4>Ligue 192</h4>
                    <p><strong>SAMU</strong></p>
                    <p style="font-size: 0.9rem;">Para urgências de saúde, surtos psicóticos ou tentativas de suicídio em andamento.</p>
                </div>
                <div class="contact-card">
                    <i class="fa-solid fa-fire-extinguisher fa-2x" style="color: var(--danger);"></i>
                    <h4>Ligue 193</h4>
                    <p><strong>Bombeiros</strong></p>
                    <p style="font-size: 0.9rem;">Resgate imediato em situações de desastres, acidentes e risco de vida.</p>
                </div>
                <div class="contact-card">
                    <i class="fa-solid fa-hospital fa-2x" style="color: var(--primary);"></i>
                    <h4>CAPS / UPA</h4>
                    <p><strong>Rede Pública</strong></p>
                    <p style="font-size: 0.9rem;">Procure o Centro de Atenção Psicossocial ou a UPA mais próxima de você.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Rodapé -->
    <footer>
        <div class="section-inner">
            <p><i class="fa-solid fa-heart"></i> Feito para promover a empatia e o cuidado em nossa sociedade.</p>
            <p style="font-size: 0.9rem; margin-top: 1rem;">Conteúdo baseado no guia de "Primeiros Cuidados Psicológicos: Guia para trabalhadores de campo" da Organização Mundial da Saúde (OMS).</p>
            <p style="font-size: 0.8rem; color: #a0aec0; margin-top: 2rem;">Aviso: O conteúdo deste site é puramente informativo e educacional. Não substitui diagnóstico, tratamento psiquiátrico ou terapia psicológica.</p>
        </div>
    </footer>

    <!-- Scripts da Página -->
    <script>
        // Menu Mobile Toggle
        const menuBtn = document.getElementById('mobile-menu-btn');
        const navLinks = document.getElementById('nav-links');

        menuBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Fechar menu mobile ao clicar em um link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });

        // FAQ Accordion
        const faqItems = document.querySelectorAll('.faq-item');
        
        faqItems.forEach(item => {
            const question = item.querySelector('.faq-question');
            question.addEventListener('click', () => {
                faqItems.forEach(otherItem => {
                    if (otherItem !== item) {
                        otherItem.classList.remove('active');
                    }
                });
                item.classList.toggle('active');
            });
        });

        // Rolagem Suave (Smooth Scroll)
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    window.scrollTo({
                        top: target.offsetTop - 70, 
                        behavior: 'smooth'
                    });
                }
            });
        });

        // --- SISTEMA DE SIMULAÇÃO DA IA ---
        const aiInput = document.getElementById('ai-input');
        const aiBtn = document.getElementById('ai-btn');
        const aiResponse = document.getElementById('ai-response');

        function realizarPesquisaIA() {
            const query = aiInput.value.trim();
            
            // Não faz nada se o campo estiver vazio
            if (!query) return;

            // 1. Mostrar estado de carregamento
            aiResponse.className = 'ai-result loading';
            aiResponse.innerHTML = '<i class="fa-solid fa-circle-notch fa-spin"></i> A IA está analisando a sua situação...';
            
            // 2. Simular o delay de uma requisição real de API (2 segundos)
            setTimeout(() => {
                aiResponse.className = 'ai-result';
                
                // Texto de resposta padrão para fins de simulação
                aiResponse.innerHTML = `
                    <h4 style="color: var(--primary-dark); margin-bottom: 12px; font-size: 1.2rem;">
                        <i class="fa-solid fa-clipboard-check"></i> Orientação Recomendada
                    </h4>
                    <p style="margin-bottom: 10px;"><strong>Situação relatada:</strong> "${query}"</p>
                    <p style="margin-bottom: 10px;">
                        <strong>Como proceder:</strong> Mantenha a calma. Aproxime-se lentamente, respeitando o espaço pessoal. 
                        Apresente-se e pergunte: "Posso ajudar em algo agora?". Foque nas necessidades básicas da pessoa (água, um lugar para sentar longe de aglomeração). 
                        Escute sem interromper ou julgar. Se a pessoa apresentar risco à própria vida ou extrema confusão, acione o resgate (192) imediatamente.
                    </p>
                    <div style="margin-top: 15px; padding-top: 15px; border-top: 1px solid #e2e8f0; font-size: 0.85rem; color: var(--danger);">
                        <em><i class="fa-solid fa-triangle-exclamation"></i> Nota: Esta é uma simulação para fins demonstrativos. Em casos graves, busque a rede pública de saúde.</em>
                    </div>
                `;
            }, 2000);
        }

        // Acionar a IA ao clicar no botão
        aiBtn.addEventListener('click', realizarPesquisaIA);

        // Acionar a IA ao apertar a tecla "Enter"
        aiInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                realizarPesquisaIA();
            }
        });
    </script>

</body>
</html>
