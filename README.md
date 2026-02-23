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
            /* Garante que o conteúdo nunca "cole" nas bordas e esteja sempre ao centro */
            display: flex;
            flex-direction: column;
            align-items: center;
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
            opacity: 0.1;
            position: absolute;
            top: 0.5rem;
            left: 0.5rem;
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
        /* Ajuste para seções ocuparem 100% da largura mas manterem o conteúdo centralizado */
        section, header, footer, nav {
            width: 100%;
            display: flex;
            justify-content: center;
        }
        .inner-container {
            width: 100%;
            max-width: 1100px;
            margin: 0 auto;
        }
    </style>
</head>
<body class="font-sans antialiased">

    <nav class="fixed top-0 z-50 bg-brand-cream/80 backdrop-blur-md border-b border-brand-dark/5">
        <div class="inner-container px-6 h-16 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <i data-lucide="heart" class="text-brand-sage fill-brand-sage w-6 h-6"></i>
                <span class="font-serif font-bold text-lg tracking-tight">Apoio PCP</span>
            </div>
            <div class="hidden md:flex items-center gap-6 text-sm font-medium opacity-70">
                <a href="#o-que-e" class="hover:opacity-100 transition-opacity">O que é?</a>
                <a href="#principios" class="hover:opacity-100 transition-opacity">Princípios</a>
                <a href="#vulneraveis" class="hover:opacity-100 transition-opacity">Grupos</a>
                <a href="#contatos" class="bg-brand-dark text-white px-4 py-2 rounded-full hover:bg-brand-sage transition-colors">Emergência</a>
            </div>
            <div class="md:hidden">
                 <a href="#contatos" class="text-xs bg-brand-dark text-white px-3 py-1.5 rounded-full">Emergência</a>
            </div>
        </div>
    </nav>

    <header class="pt-32 pb-20 px-6 text-center">
        <div class="inner-container">
            <span class="text-xs uppercase tracking-[0.2em] font-semibold text-brand-sage mb-4 block">
                Primeiros Cuidados Psicológicos
            </span>
            <h1 class="text-4xl md:text-7xl mb-6 leading-[1.1] font-serif">
                Presença que <span class="italic">acolhe</span>,<br />
                escuta que <span class="italic text-brand-sage">cura</span>.
            </h1>
            <p class="max-w-2xl mx-auto text-base md:text-lg opacity-70 mb-10 px-4">
                PCP não é terapia. É uma resposta humana e prática para apoiar pessoas em sofrimento agudo após um evento crítico.
            </p>
            <div class="flex flex-col md:flex-row justify-center gap-4 px-6">
                <a href="#principios" class="px-8 py-4 bg-brand-dark text-white rounded-full font-medium flex items-center justify-center gap-2 hover:bg-brand-sage transition-all">
                    Aprender os Princípios <i data-lucide="arrow-right" class="w-4 h-4"></i>
                </a>
                <a href="#o-que-e" class="px-8 py-4 border border-brand-dark/20 rounded-full font-medium hover:bg-brand-warm transition-all">
                    Saiba mais
                </a>
            </div>
        </div>
    </header>

    <section id="o-que-e" class="py-16 px-6">
        <div class="inner-container bg-brand-warm/30 rounded-[2.5rem] p-8 md:p-16">
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div>
                    <h2 class="text-3xl md:text-4xl mb-6 font-serif">O que são os PCP?</h2>
                    <p class="text-lg opacity-80 mb-6">
                        Uma resposta de apoio a um ser humano que está sofrendo e precisa de ajuda imediata.
                    </p>
                    <ul class="space-y-4">
                        <li class="flex items-start gap-3">
                            <i data-lucide="check-circle-2" class="text-brand-sage shrink-0 mt-1 w-5 h-5"></i>
                            <span class="text-sm md:text-base">Ajuda prática e não invasiva.</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <i data-lucide="check-circle-2" class="text-brand-sage shrink-0 mt-1 w-5 h-5"></i>
                            <span class="text-sm md:text-base">Avaliar necessidades e preocupações.</span>
                        </li>
                        <li class="flex items-start gap-3">
                            <i data-lucide="check-circle-2" class="text-brand-sage shrink-0 mt-1 w-5 h-5"></i>
                            <span class="text-sm md:text-base">Ouvir sem pressionar a fala.</span>
                        </li>
                    </ul>
                </div>
                <div class="grid gap-6">
                    <div class="glass-card rounded-3xl p-6 bg-white">
                        <h3 class="text-lg mb-2 font-serif italic text-brand-sage">O que NÃO é PCP</h3>
                        <p class="text-sm text-brand-dark/70">Não é aconselhamento profissional, nem "debriefing" psicológico ou terapia.</p>
                    </div>
                    <div class="rounded-3xl p-6 bg-brand-sage text-white shadow-lg">
                        <h3 class="text-lg mb-2 font-serif italic">Quem precisa?</h3>
                        <p class="text-sm opacity-90">Pessoas angustiadas expostas recentemente a um evento crítico grave.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="principios" class="py-20 px-6">
        <div class="inner-container">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl mb-4 font-serif">Os Três Princípios de Ação</h2>
                <p class="opacity-60 text-sm md:text-base">Framework fundamental: Ver, Ouvir e Conectar.</p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-8">
                <div class="glass-card rounded-3xl p-8 h-full border-t-4 border-t-brand-sage relative">
                    <span class="step-number">01</span>
                    <div class="w-12 h-12 bg-brand-sage/10 rounded-2xl flex items-center justify-center mb-6">
                        <i data-lucide="eye" class="text-brand-sage w-6 h-6"></i>
                    </div>
                    <h3 class="text-xl mb-3 font-serif">Ver (Look)</h3>
                    <p class="text-sm opacity-70 leading-relaxed">Verifique a segurança, ferimentos e necessidades básicas urgentes no local.</p>
                </div>

                <div class="glass-card rounded-3xl p-8 h-full border-t-4 border-t-brand-clay relative">
                    <span class="step-number">02</span>
                    <div class="w-12 h-12 bg-brand-clay/10 rounded-2xl flex items-center justify-center mb-6">
                        <i data-lucide="ear" class="text-brand-clay w-6 h-6"></i>
                    </div>
                    <h3 class="text-xl mb-3 font-serif">Ouvir (Listen)</h3>
                    <p class="text-sm opacity-70 leading-relaxed">Aproxime-se, pergunte as necessidades e ouça para ajudar a pessoa a se acalmar.</p>
                </div>

                <div class="glass-card rounded-3xl p-8 h-full border-t-4 border-t-brand-dark relative">
                    <span class="step-number">03</span>
                    <div class="w-12 h-12 bg-brand-dark/10 rounded-2xl flex items-center justify-center mb-6">
                        <i data-lucide="link" class="text-brand-dark w-6 h-6"></i>
                    </div>
                    <h3 class="text-xl mb-3 font-serif">Conectar (Link)</h3>
                    <p class="text-sm opacity-70 leading-relaxed">Conecte com entes queridos e serviços de apoio ou informações corretas.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="vulneraveis" class="py-16 px-6">
        <div class="inner-container bg-brand-dark text-white rounded-[2.5rem] p-8 md:p-16">
            <h2 class="text-3xl font-serif mb-12 text-center md:text-left">Grupos Vulneráveis</h2>
            <div class="grid md:grid-cols-3 gap-10">
                <div class="space-y-4">
                    <i data-lucide="baby" class="w-8 h-8 text-brand-warm"></i>
                    <h3 class="text-xl font-serif italic">Crianças</h3>
                    <p class="text-sm opacity-70">Priorize a reunião com cuidadores e use linguagem simples.</p>
                </div>
                <div class="space-y-4">
                    <i data-lucide="user-round" class="w-8 h-8 text-brand-warm"></i>
                    <h3 class="text-xl font-serif italic">Idosos</h3>
                    <p class="text-sm opacity-70">Verifique medicação, mobilidade e forneça paciência extra.</p>
                </div>
                <div class="space-y-4">
                    <i data-lucide="accessibility" class="w-8 h-8 text-brand-warm"></i>
                    <h3 class="text-xl font-serif italic">PCDs</h3>
                    <p class="text-sm opacity-70">Pergunte como ajudar antes de agir e garanta acessibilidade.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="py-12 px-6">
        <div class="inner-container">
            <div class="rounded-3xl p-8 bg-brand-sage text-white flex flex-col items-center text-center shadow-xl">
                <h3 class="text-2xl mb-6 font-serif italic">Pausa para Respirar (4-4-4)</h3>
                <div class="relative w-32 h-32 md:w-40 md:h-40 flex items-center justify-center">
                    <div id="breathing-circle" class="absolute w-24 h-24 bg-white/20 rounded-full blur-xl transition-all duration-[4000ms] ease-in-out"></div>
                    <div id="breathing-text" class="z-10 text-xl font-bold">Começar</div>
                </div>
                <button id="breathing-btn" class="mt-8 px-8 py-3 bg-white text-brand-sage rounded-full font-bold shadow-lg">
                    Iniciar Exercício
                </button>
            </div>
        </div>
    </section>

    <section id="contatos" class="py-20 px-6">
        <div class="inner-container bg-brand-dark rounded-[2.5rem] p-8 md:p-16 text-white text-center">
            <h2 class="text-3xl md:text-5xl mb-12 font-serif">Precisa de ajuda agora?</h2>
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6 md:gap-8">
                <div class="p-4 border border-white/10 rounded-2xl">
                    <span class="text-3xl font-serif italic text-brand-warm block">188</span>
                    <p class="text-[10px] uppercase tracking-widest opacity-60">CVV</p>
                </div>
                <div class="p-4 border border-white/10 rounded-2xl">
                    <span class="text-3xl font-serif italic text-brand-warm block">192</span>
                    <p class="text-[10px] uppercase tracking-widest opacity-60">SAMU</p>
                </div>
                <div class="p-4 border border-white/10 rounded-2xl">
                    <span class="text-3xl font-serif italic text-brand-warm block">193</span>
                    <p class="text-[10px] uppercase tracking-widest opacity-60">Bombeiros</p>
                </div>
                <div class="p-4 border border-white/10 rounded-2xl">
                    <span class="text-3xl font-serif italic text-brand-warm block">190</span>
                    <p class="text-[10px] uppercase tracking-widest opacity-60">Polícia</p>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-12 border-t border-brand-dark/5 px-6">
        <div class="inner-container flex flex-col md:flex-row items-center justify-between gap-6 opacity-50 text-[10px] uppercase tracking-widest">
            <p>© <span id="year"></span> Apoio PCP</p>
            <p>Protocolos baseados na OMS e IFRC</p>
            <div class="flex gap-4">
                <a href="https://instagram.com/psicomariliadamata" target="_blank">Instagram</a>
            </div>
        </div>
    </footer>

    <script>
        lucide.createIcons();
        document.getElementById('year').textContent = new Date().getFullYear();

        // Breathing Exercise
        const breathingBtn = document.getElementById('breathing-btn');
        const breathingCircle = document.getElementById('breathing-circle');
        const breathingText = document.getElementById('breathing-text');
        let breathingInterval;
        let isBreathing = false;
        let phase = 0;
        const phases = [
            { text: 'Inspirar', scale: 'scale-150' },
            { text: 'Segurar', scale: 'scale-150' },
            { text: 'Expirar', scale: 'scale-100' }
        ];

        function updateBreathing() {
            const currentPhase = phases[phase];
            breathingText.textContent = currentPhase.text;
            breathingCircle.classList.remove('scale-100', 'scale-150');
            breathingCircle.classList.add(currentPhase.scale);
            phase = (phase + 1) % 3;
        }

        breathingBtn.addEventListener('click', () => {
            isBreathing = !isBreathing;
            if (isBreathing) {
                breathingBtn.textContent = 'Parar';
                updateBreathing();
                breathingInterval = setInterval(updateBreathing, 4000);
            } else {
                breathingBtn.textContent = 'Iniciar Exercício';
                breathingText.textContent = 'Começar';
                clearInterval(breathingInterval);
                breathingCircle.classList.replace('scale-150', 'scale-100');
            }
        });
    </script>
</body>
</html>
