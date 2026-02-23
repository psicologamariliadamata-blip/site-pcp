<!DOCTYPE html>
<html lang="pt-BR" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Apoio - Primeiros Cuidados Psicológicos</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Libre+Baskerville:italic,wght@400;700&display=swap" rel="stylesheet">
    <script src="https://unpkg.com/lucide@latest"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'ui-sans-serif', 'system-ui', 'sans-serif'],
                        serif: ['Libre Baskerville', 'serif'],
                    },
                    colors: {
                        brand: {
                            cream: '#FDFCF8',
                            sage: '#6B705C',
                            clay: '#A5A58D',
                            warm: '#FFE8D6',
                            dark: '#1B1B1B',
                        }
                    }
                }
            }
        }
    </script>
    <style>
        body {
            background-color: #FDFCF8;
            color: #1B1B1B;
        }
        .glass-card {
            background: rgba(255, 255, 255, 0.6);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1);
        }
        .step-number {
            font-family: 'Libre Baskerville', serif;
            font-style: italic;
            font-size: 2.25rem;
            line-height: 2.5rem;
            opacity: 0.2;
            position: absolute;
            top: -1rem;
            left: -0.5rem;
        }
        .accordion-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out, opacity 0.3s ease-out;
            opacity: 0;
        }
        .accordion-item.active .accordion-content {
            max-height: 500px;
            opacity: 1;
        }
        .accordion-item.active .chevron {
            transform: rotate(180deg);
        }
    </style>
</head>
<body class="font-sans antialiased">

    <!-- Navigation -->
    <nav class="fixed top-0 w-full z-50 bg-brand-cream/80 backdrop-blur-md border-b border-brand-dark/5">
        <div class="max-w-7xl mx-auto px-6 h-16 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <i data-lucide="heart" class="text-brand-sage fill-brand-sage w-6 h-6"></i>
                <span class="font-serif font-bold text-lg tracking-tight">Apoio PCP</span>
            </div>
            <div class="hidden md:flex items-center gap-8 text-sm font-medium opacity-70">
                <a href="#o-que-e" class="hover:opacity-100 transition-opacity">O que é?</a>
                <a href="#principios" class="hover:opacity-100 transition-opacity">Princípios</a>
                <a href="#vulneraveis" class="hover:opacity-100 transition-opacity">Grupos</a>
                <a href="#faq" class="hover:opacity-100 transition-opacity">Dúvidas</a>
                <a href="#referencias" class="hover:opacity-100 transition-opacity">Referências</a>
                <a href="#contatos" class="bg-brand-dark text-white px-4 py-2 rounded-full hover:bg-brand-sage transition-colors">Emergência</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="pt-32 pb-20 px-6 text-center max-w-7xl mx-auto">
        <span class="text-xs uppercase tracking-[0.2em] font-semibold text-brand-sage mb-4 block">
            Primeiros Cuidados Psicológicos
        </span>
        <h1 class="text-5xl md:text-7xl mb-6 leading-[1.1] font-serif">
            Presença que <span class="italic">acolhe</span>,<br />
            escuta que <span class="italic text-brand-sage">cura</span>.
        </h1>
        <p class="max-w-2xl mx-auto text-lg opacity-70 mb-10">
            PCP não é terapia. É uma resposta humana e prática para apoiar pessoas em sofrimento agudo após um evento crítico.
        </p>
        <div class="flex flex-wrap justify-center gap-4">
            <a href="#principios" class="px-8 py-4 bg-brand-dark text-white rounded-full font-medium flex items-center gap-2 hover:bg-brand-sage transition-all">
                Aprender os Princípios <i data-lucide="arrow-right" class="w-4 h-4"></i>
            </a>
            <a href="#o-que-e" class="px-8 py-4 border border-brand-dark/20 rounded-full font-medium hover:bg-brand-warm transition-all">
                Saiba mais
            </a>
        </div>
    </header>

    <!-- What is PFA -->
    <section id="o-que-e" class="py-20 px-6 md:px-12 max-w-7xl mx-auto bg-brand-warm/30 rounded-[3rem]">
        <div class="grid md:grid-cols-2 gap-12 items-center">
            <div>
                <h2 class="text-4xl mb-6 font-serif">O que são os Primeiros Cuidados Psicológicos?</h2>
                <p class="text-lg opacity-80 mb-6">
                    Os Primeiros Cuidados Psicológicos (PCP) descrevem uma resposta humana, de apoio, a um ser humano que está sofrendo e que pode precisar de ajuda.
                </p>
                <ul class="space-y-4">
                    <li class="flex items-start gap-3">
                        <i data-lucide="check-circle-2" class="text-brand-sage shrink-0 mt-1 w-5 h-5"></i>
                        <span>Oferecer ajuda e apoio prático, de forma não invasiva.</span>
                    </li>
                    <li class="flex items-start gap-3">
                        <i data-lucide="check-circle-2" class="text-brand-sage shrink-0 mt-1 w-5 h-5"></i>
                        <span>Avaliar as necessidades e preocupações.</span>
                    </li>
                    <li class="flex items-start gap-3">
                        <i data-lucide="check-circle-2" class="text-brand-sage shrink-0 mt-1 w-5 h-5"></i>
                        <span>Ajudar as pessoas a atenderem às necessidades básicas (comida, água, informação).</span>
                    </li>
                    <li class="flex items-start gap-3">
                        <i data-lucide="check-circle-2" class="text-brand-sage shrink-0 mt-1 w-5 h-5"></i>
                        <span>Ouvir as pessoas, mas não pressioná-las a falar.</span>
                    </li>
                    <li class="flex items-start gap-3">
                        <i data-lucide="check-circle-2" class="text-brand-sage shrink-0 mt-1 w-5 h-5"></i>
                        <span>Confortar as pessoas e ajudá-las a se sentirem calmas.</span>
                    </li>
                </ul>
            </div>
            <div class="grid gap-6">
                <div class="glass-card rounded-3xl p-8 relative overflow-hidden bg-white">
                    <i data-lucide="shield-alert" class="text-brand-sage mb-4 w-8 h-8"></i>
                    <h3 class="text-xl mb-2 font-serif italic">O que NÃO é PCP</h3>
                    <p class="text-sm text-brand-dark/70 leading-relaxed">
                        Não é algo que apenas profissionais fazem. Não é aconselhamento profissional. Não é "debriefing" psicológico (pedir para detalhar o trauma).
                    </p>
                </div>
                <div class="rounded-3xl p-8 relative overflow-hidden bg-brand-sage text-white shadow-lg">
                    <i data-lucide="info" class="mb-4 text-brand-warm w-8 h-8"></i>
                    <h3 class="text-xl mb-2 font-serif italic">Quem precisa?</h3>
                    <p class="text-sm opacity-90 leading-relaxed">
                        Pessoas muito angustiadas que foram expostas recentemente a um evento crítico grave. Nem todos que passam por uma crise precisam ou querem PCP.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- The 3 Principles -->
    <section id="principios" class="py-20 px-6 md:px-12 max-w-7xl mx-auto">
        <div class="text-center mb-16">
            <h2 class="text-4xl mb-4 font-serif">Os Três Princípios de Ação</h2>
            <p class="opacity-60">O framework fundamental: Ver, Ouvir e Conectar.</p>
        </div>
        
        <div class="grid md:grid-cols-3 gap-8">
            <!-- VER -->
            <div class="relative group">
                <div class="glass-card rounded-3xl p-8 h-full border-t-4 border-t-brand-sage transition-all duration-300 hover:-translate-y-2">
                    <span class="step-number">01</span>
                    <div class="w-12 h-12 bg-brand-sage/10 rounded-2xl flex items-center justify-center mb-6">
                        <i data-lucide="eye" class="text-brand-sage w-6 h-6"></i>
                    </div>
                    <h3 class="text-2xl mb-4 font-serif">Ver (Look)</h3>
                    <p class="text-sm opacity-70 leading-relaxed">
                        Verifique a segurança. Verifique se há pessoas com necessidades básicas urgentes. Verifique se há pessoas com reações de angústia grave.
                    </p>
                    <ul class="mt-6 space-y-2 text-xs font-medium opacity-60 uppercase tracking-wider">
                        <li>• Segurança do local</li>
                        <li>• Ferimentos visíveis</li>
                        <li>• Estado de choque</li>
                    </ul>
                </div>
            </div>

            <!-- OUVIR -->
            <div class="relative group">
                <div class="glass-card rounded-3xl p-8 h-full border-t-4 border-t-brand-clay transition-all duration-300 hover:-translate-y-2">
                    <span class="step-number">02</span>
                    <div class="w-12 h-12 bg-brand-clay/10 rounded-2xl flex items-center justify-center mb-6">
                        <i data-lucide="ear" class="text-brand-clay w-6 h-6"></i>
                    </div>
                    <h3 class="text-2xl mb-4 font-serif">Ouvir (Listen)</h3>
                    <p class="text-sm opacity-70 leading-relaxed">
                        Aproxime-se das pessoas que podem precisar de apoio. Pergunte sobre as necessidades e preocupações das pessoas. Ouça e ajude-as a se acalmarem.
                    </p>
                    <ul class="mt-6 space-y-2 text-xs font-medium opacity-60 uppercase tracking-wider">
                        <li>• Escuta Ativa</li>
                        <li>• Validar sentimentos</li>
                        <li>• Respeitar o silêncio</li>
                    </ul>
                </div>
            </div>

            <!-- CONECTAR -->
            <div class="relative group">
                <div class="glass-card rounded-3xl p-8 h-full border-t-4 border-t-brand-dark transition-all duration-300 hover:-translate-y-2">
                    <span class="step-number">03</span>
                    <div class="w-12 h-12 bg-brand-dark/10 rounded-2xl flex items-center justify-center mb-6">
                        <i data-lucide="link" class="text-brand-dark w-6 h-6"></i>
                    </div>
                    <h3 class="text-2xl mb-4 font-serif">Conectar (Link)</h3>
                    <p class="text-sm opacity-70 leading-relaxed">
                        Ajude as pessoas a atenderem às necessidades básicas e a acessarem serviços. Ajude as pessoas a lidarem com os problemas. Forneça informações. Conecte com entes queridos.
                    </p>
                    <ul class="mt-6 space-y-2 text-xs font-medium opacity-60 uppercase tracking-wider">
                        <li>• Informação correta</li>
                        <li>• Rede de apoio</li>
                        <li>• Serviços sociais</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Vulnerable Groups -->
    <section id="vulneraveis" class="py-20 px-6 md:px-12 max-w-7xl mx-auto bg-brand-dark text-white rounded-[3rem]">
        <div class="text-center mb-16">
            <h2 class="text-4xl mb-4 font-serif">Grupos Vulneráveis</h2>
            <p class="opacity-60">Pessoas que podem precisar de atenção especial em crises.</p>
        </div>
        <div class="grid md:grid-cols-3 gap-8">
            <div class="space-y-4">
                <div class="w-12 h-12 bg-white/10 rounded-full flex items-center justify-center">
                    <i data-lucide="baby" class="w-6 h-6"></i>
                </div>
                <h3 class="text-xl font-serif italic">Crianças e Adolescentes</h3>
                <p class="text-sm opacity-70">Priorize a reunião com cuidadores. Use linguagem simples e honesta. Mantenha-os protegidos de cenas traumáticas.</p>
            </div>
            <div class="space-y-4">
                <div class="w-12 h-12 bg-white/10 rounded-full flex items-center justify-center">
                    <i data-lucide="user-round" class="w-6 h-6"></i>
                </div>
                <h3 class="text-xl font-serif italic">Idosos</h3>
                <p class="text-sm opacity-70">Verifique necessidades de medicação e mobilidade. Seja paciente com possíveis desorientações causadas pelo estresse.</p>
            </div>
            <div class="space-y-4">
                <div class="w-12 h-12 bg-white/10 rounded-full flex items-center justify-center">
                    <i data-lucide="accessibility" class="w-6 h-6"></i>
                </div>
                <h3 class="text-xl font-serif italic">Pessoas com Deficiência</h3>
                <p class="text-sm opacity-70">Pergunte como pode ajudar antes de agir. Mantenha equipamentos de suporte próximos e garanta acessibilidade.</p>
            </div>
        </div>
    </section>

    <!-- FAQ Section -->
    <section id="faq" class="py-20 px-6 md:px-12 max-w-3xl mx-auto">
        <h2 class="text-4xl mb-12 text-center font-serif">Dúvidas Frequentes</h2>
        <div class="space-y-2">
            <div class="accordion-item border-b border-brand-dark/10">
                <button class="accordion-trigger w-full py-6 flex items-center justify-between text-left hover:text-brand-sage transition-colors">
                    <span class="font-serif text-xl">Preciso ser psicólogo para aplicar o PCP?</span>
                    <i data-lucide="chevron-down" class="chevron transition-transform duration-300 w-5 h-5"></i>
                </button>
                <div class="accordion-content">
                    <p class="pb-6 opacity-70 leading-relaxed">Não. O PCP foi desenhado para ser aplicado por qualquer pessoa instruída, assim como os primeiros socorros físicos. É uma resposta humana e prática, não uma intervenção clínica.</p>
                </div>
            </div>
            <div class="accordion-item border-b border-brand-dark/10">
                <button class="accordion-trigger w-full py-6 flex items-center justify-between text-left hover:text-brand-sage transition-colors">
                    <span class="font-serif text-xl">E se a pessoa chorar incontrolavelmente?</span>
                    <i data-lucide="chevron-down" class="chevron transition-transform duration-300 w-5 h-5"></i>
                </button>
                <div class="accordion-content">
                    <p class="pb-6 opacity-70 leading-relaxed">O choro é uma reação natural. Não tente pará-lo com frases como 'não chore'. Ofereça um lenço, água e permaneça ao lado da pessoa, validando sua dor e garantindo que ela está segura agora.</p>
                </div>
            </div>
            <div class="accordion-item border-b border-brand-dark/10">
                <button class="accordion-trigger w-full py-6 flex items-center justify-between text-left hover:text-brand-sage transition-colors">
                    <span class="font-serif text-xl">Quanto tempo dura a aplicação do PCP?</span>
                    <i data-lucide="chevron-down" class="chevron transition-transform duration-300 w-5 h-5"></i>
                </button>
                <div class="accordion-content">
                    <p class="pb-6 opacity-70 leading-relaxed">Geralmente é uma intervenção de curto prazo, que dura de alguns minutos a algumas horas, focada no momento imediato da crise e na conexão com suportes posteriores.</p>
                </div>
            </div>
            <div class="accordion-item border-b border-brand-dark/10">
                <button class="accordion-trigger w-full py-6 flex items-center justify-between text-left hover:text-brand-sage transition-colors">
                    <span class="font-serif text-xl">O que fazer se eu me sentir sobrecarregado?</span>
                    <i data-lucide="chevron-down" class="chevron transition-transform duration-300 w-5 h-5"></i>
                </button>
                <div class="accordion-content">
                    <p class="pb-6 opacity-70 leading-relaxed">O autocuidado é fundamental. Se você sentir que não tem condições emocionais no momento, peça para outra pessoa assumir. Após ajudar, reserve um tempo para descansar e processar seus próprios sentimentos.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Interactive & Self Care -->
    <section id="auto-cuidado" class="py-20 px-6 md:px-12 max-w-7xl mx-auto grid md:grid-cols-2 gap-8">
        <!-- Breathing Exercise -->
        <div class="rounded-3xl p-8 relative overflow-hidden bg-brand-sage text-white flex flex-col items-center justify-center text-center shadow-xl">
            <h3 class="text-2xl mb-6 font-serif italic">Pausa para Respirar</h3>
            <div class="relative w-48 h-48 flex items-center justify-center">
                <div id="breathing-circle" class="absolute w-32 h-32 bg-white/30 rounded-full blur-xl transition-all duration-[4000ms] ease-in-out"></div>
                <div id="breathing-text" class="z-10 text-2xl font-bold tracking-tight">Começar</div>
            </div>
            <button id="breathing-btn" class="mt-8 px-8 py-3 bg-white text-brand-sage rounded-full font-bold hover:bg-brand-warm transition-all shadow-lg active:scale-95">
                Iniciar Exercício
            </button>
            <p class="mt-6 text-sm font-medium opacity-90">Técnica 4-4-4 para acalmar o sistema nervoso.</p>
        </div>

        <!-- Self Care Card -->
        <div class="rounded-3xl p-8 relative overflow-hidden bg-brand-warm text-brand-dark flex flex-col justify-center shadow-md">
            <h3 class="text-3xl mb-6 font-serif italic">Cuidar de quem cuida</h3>
            <p class="text-brand-dark/80 mb-8 leading-relaxed">
                Ajudar em situações de crise pode ser exaustivo. Para apoiar os outros de forma eficaz, você precisa estar bem.
            </p>
            <div class="space-y-6">
                <div class="flex items-center gap-4">
                    <div class="w-12 h-12 rounded-full bg-white flex items-center justify-center shrink-0 shadow-sm">
                        <i data-lucide="wind" class="text-brand-sage w-6 h-6"></i>
                    </div>
                    <span class="text-sm font-semibold">Reconheça seus limites e peça ajuda se necessário.</span>
                </div>
                <div class="flex items-center gap-4">
                    <div class="w-12 h-12 rounded-full bg-white flex items-center justify-center shrink-0 shadow-sm">
                        <i data-lucide="heart" class="text-brand-sage w-6 h-6"></i>
                    </div>
                    <span class="text-sm font-semibold">Mantenha rotinas básicas de sono e alimentação.</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Professional Contact -->
    <section id="contato-profissional" class="py-20 px-6 md:px-12 max-w-7xl mx-auto pt-0">
        <div class="rounded-3xl p-8 relative overflow-hidden bg-brand-cream border border-brand-sage/20 flex flex-col md:flex-row items-center justify-between gap-8 py-12 shadow-sm">
            <div class="text-center md:text-left">
                <h3 class="text-3xl mb-2 font-serif italic">Dúvidas ou Suporte Profissional?</h3>
                <p class="opacity-70">Entre em contato para orientações especializadas ou parcerias.</p>
            </div>
            <div class="flex flex-wrap justify-center gap-6">
                <a href="https://instagram.com/psicomariliadamata" target="_blank" rel="noopener noreferrer" class="flex items-center gap-3 px-6 py-3 bg-white rounded-2xl shadow-sm hover:shadow-md transition-all group">
                    <div class="w-10 h-10 bg-gradient-to-tr from-yellow-400 via-red-500 to-purple-600 rounded-full flex items-center justify-center text-white">
                        <i data-lucide="instagram" class="w-5 h-5"></i>
                    </div>
                    <span class="font-medium group-hover:text-brand-sage">@psicomariliadamata</span>
                </a>
                <a href="mailto:psicologamariliadamata@gmail.com" class="flex items-center gap-3 px-6 py-3 bg-white rounded-2xl shadow-sm hover:shadow-md transition-all group">
                    <div class="w-10 h-10 bg-brand-sage rounded-full flex items-center justify-center text-white">
                        <i data-lucide="mail" class="w-5 h-5"></i>
                    </div>
                    <span class="font-medium group-hover:text-brand-sage">psicologamariliadamata@gmail.com</span>
                </a>
            </div>
        </div>
    </section>

    <!-- References Section -->
    <section id="referencias" class="py-20 px-6 md:px-12 max-w-7xl mx-auto bg-brand-warm/20 rounded-[3rem] mt-20">
        <div class="max-w-4xl mx-auto">
            <div class="flex items-center gap-4 mb-10">
                <i data-lucide="book-open" class="text-brand-sage w-8 h-8"></i>
                <h2 class="text-4xl font-serif">Referências e Materiais</h2>
            </div>
            <div class="grid gap-6">
                <div class="p-6 bg-white/50 rounded-2xl border border-brand-dark/5 hover:bg-white transition-colors">
                    <h4 class="font-bold mb-2 flex items-center justify-between">
                        OMS - Primeiros Cuidados Psicológicos: Guia para trabalhadores de campo
                        <i data-lucide="external-link" class="opacity-40 w-4 h-4"></i>
                    </h4>
                    <p class="text-sm opacity-70">Organização Mundial da Saúde, Organização Internacional para as Migrações e Visão Mundial Internacional (2011).</p>
                </div>
                <div class="p-6 bg-white/50 rounded-2xl border border-brand-dark/5 hover:bg-white transition-colors">
                    <h4 class="font-bold mb-2 flex items-center justify-between">
                        IFRC - Psychological First Aid (PFA) Guide
                        <i data-lucide="external-link" class="opacity-40 w-4 h-4"></i>
                    </h4>
                    <p class="text-sm opacity-70">International Federation of Red Cross and Red Crescent Societies.</p>
                </div>
                <div class="p-6 bg-white/50 rounded-2xl border border-brand-dark/5 hover:bg-white transition-colors">
                    <h4 class="font-bold mb-2 flex items-center justify-between">
                        Cartilha de Primeiros Cuidados Psicológicos em Desastres
                        <i data-lucide="external-link" class="opacity-40 w-4 h-4"></i>
                    </h4>
                    <p class="text-sm opacity-70">Conselho Federal de Psicologia (CFP) e órgãos regionais.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Emergency Contacts -->
    <section id="contatos" class="py-20 px-6 md:px-12 max-w-7xl mx-auto text-center">
        <div class="bg-brand-dark rounded-[3rem] py-20 px-8 text-white shadow-2xl">
            <i data-lucide="phone-call" class="mx-auto mb-8 text-brand-sage w-14 h-14"></i>
            <h2 class="text-4xl md:text-5xl mb-12 font-serif">Precisa de ajuda agora?</h2>
            <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8 md:gap-12 max-w-6xl mx-auto">
                <div class="flex flex-col items-center">
                    <span class="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">188</span>
                    <p class="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">CVV (Brasil)</p>
                </div>
                <div class="flex flex-col items-center">
                    <span class="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">192</span>
                    <p class="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">SAMU</p>
                </div>
                <div class="flex flex-col items-center">
                    <span class="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">193</span>
                    <p class="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">Bombeiros</p>
                </div>
                <div class="flex flex-col items-center">
                    <span class="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">190</span>
                    <p class="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">Polícia Militar</p>
                </div>
                <div class="flex flex-col items-center">
                    <span class="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">180</span>
                    <p class="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">Mulher</p>
                </div>
                <div class="flex flex-col items-center">
                    <span class="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">100</span>
                    <p class="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">Direitos Humanos</p>
                </div>
                <div class="flex flex-col items-center">
                    <span class="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">199</span>
                    <p class="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">Defesa Civil</p>
                </div>
                <div class="flex flex-col items-center">
                    <span class="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">197</span>
                    <p class="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">Polícia Civil</p>
                </div>
            </div>
            <p class="mt-16 text-sm md:text-base opacity-60 max-w-2xl mx-auto leading-relaxed">
                Este site é informativo. Em caso de emergência médica ou risco imediato à vida, entre em contato com as autoridades locais imediatamente.
            </p>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-12 px-6 border-t border-brand-dark/5 text-center opacity-50 text-xs">
        <div class="max-w-7xl mx-auto flex flex-col md:flex-row items-center justify-between gap-6">
            <p>© <span id="year"></span> Apoio - Primeiros Cuidados Psicológicos.</p>
            <div class="flex items-center gap-6">
                <a href="https://instagram.com/psicomariliadamata" target="_blank" rel="noopener noreferrer" class="hover:text-brand-sage transition-colors">Instagram</a>
                <a href="#referencias" class="hover:text-brand-sage transition-colors">Referências</a>
                <a href="#contatos" class="hover:text-brand-sage transition-colors">Emergência</a>
            </div>
            <p>Conteúdo baseado nos protocolos da OMS e IFRC.</p>
        </div>
    </footer>

    <script>
        // Initialize Lucide Icons
        lucide.createIcons();

        // Footer Year
        document.getElementById('year').textContent = new Date().getFullYear();

        // Accordion Logic
        document.querySelectorAll('.accordion-trigger').forEach(trigger => {
            trigger.addEventListener('click', () => {
                const item = trigger.parentElement;
                const isActive = item.classList.contains('active');
                
                // Close all other items
                document.querySelectorAll('.accordion-item').forEach(i => i.classList.remove('active'));
                
                if (!isActive) {
                    item.classList.add('active');
                }
            });
        });

        // Breathing Exercise Logic
        const breathingBtn = document.getElementById('breathing-btn');
        const breathingCircle = document.getElementById('breathing-circle');
        const breathingText = document.getElementById('breathing-text');
        let breathingInterval;
        let isBreathing = false;
        let phase = 0; // 0: Inspirar, 1: Segurar, 2: Expirar

        const phases = [
            { text: 'Inspirar', scale: 'scale-150' },
            { text: 'Segurar', scale: 'scale-150' },
            { text: 'Expirar', scale: 'scale-100' }
        ];

        function updateBreathing() {
            const currentPhase = phases[phase];
            breathingText.textContent = currentPhase.text;
            
            // Update scale
            breathingCircle.classList.remove('scale-100', 'scale-150');
            breathingCircle.classList.add(currentPhase.scale);
            
            phase = (phase + 1) % 3;
        }

        breathingBtn.addEventListener('click', () => {
            isBreathing = !isBreathing;
            
            if (isBreathing) {
                breathingBtn.textContent = 'Parar';
                phase = 0;
                updateBreathing();
                breathingInterval = setInterval(updateBreathing, 4000);
            } else {
                breathingBtn.textContent = 'Iniciar Exercício';
                breathingText.textContent = 'Começar';
                clearInterval(breathingInterval);
                breathingCircle.classList.remove('scale-150');
                breathingCircle.classList.add('scale-100');
            }
        });
    </script>
</body>
</html>
