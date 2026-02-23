/**
 * @license
 * SPDX-License-Identifier: Apache-2.0
 */

import React, { useState, useEffect } from 'react';
import { 
  Heart, 
  Eye, 
  Ear, 
  Link as LinkIcon, 
  ShieldAlert, 
  Info, 
  ArrowRight,
  Wind,
  CheckCircle2,
  PhoneCall,
  ChevronDown,
  Users,
  Baby,
  UserRound,
  Accessibility,
  Instagram,
  Mail,
  BookOpen,
  ExternalLink
} from 'lucide-react';
import { motion, AnimatePresence } from 'motion/react';
import { cn } from './lib/utils';

const Section = ({ children, className, id }: { children: React.ReactNode; className?: string; id?: string }) => (
  <section id={id} className={cn("py-20 px-6 md:px-12 max-w-7xl mx-auto", className)}>
    {children}
  </section>
);

const Card = ({ children, className, variant = 'glass' }: { children: React.ReactNode; className?: string; variant?: 'glass' | 'solid' | 'none' }) => (
  <div className={cn(
    "rounded-3xl p-8 relative overflow-hidden transition-all duration-300",
    variant === 'glass' && "glass-card",
    variant === 'solid' && "bg-white shadow-sm border border-brand-dark/5",
    className
  )}>
    {children}
  </div>
);

const AccordionItem = ({ question, answer }: { question: string, answer: string }) => {
  const [isOpen, setIsOpen] = useState(false);
  return (
    <div className="border-b border-brand-dark/10">
      <button 
        onClick={() => setIsOpen(!isOpen)}
        className="w-full py-6 flex items-center justify-between text-left hover:text-brand-sage transition-colors"
      >
        <span className="font-serif text-xl">{question}</span>
        <ChevronDown className={cn("transition-transform duration-300", isOpen && "rotate-180")} />
      </button>
      <AnimatePresence>
        {isOpen && (
          <motion.div
            initial={{ height: 0, opacity: 0 }}
            animate={{ height: "auto", opacity: 1 }}
            exit={{ height: 0, opacity: 0 }}
            className="overflow-hidden"
          >
            <p className="pb-6 opacity-70 leading-relaxed">
              {answer}
            </p>
          </motion.div>
        )}
      </AnimatePresence>
    </div>
  );
};

const BreathingExercise = () => {
  const [phase, setPhase] = useState<'Inspirar' | 'Segurar' | 'Expirar'>('Inspirar');
  const [isActive, setIsActive] = useState(false);

  useEffect(() => {
    if (!isActive) return;
    
    const timer = setInterval(() => {
      setPhase(prev => {
        if (prev === 'Inspirar') return 'Segurar';
        if (prev === 'Segurar') return 'Expirar';
        return 'Inspirar';
      });
    }, 4000);

    return () => clearInterval(timer);
  }, [isActive]);

  return (
    <Card variant="none" className="bg-brand-sage text-white flex flex-col items-center justify-center text-center shadow-xl">
      <h3 className="text-2xl mb-6 font-serif italic">Pausa para Respirar</h3>
      <div className="relative w-48 h-48 flex items-center justify-center">
        <AnimatePresence mode="wait">
          <motion.div
            key={phase}
            initial={{ scale: 0.8, opacity: 0 }}
            animate={{ 
              scale: phase === 'Inspirar' ? 1.4 : phase === 'Segurar' ? 1.4 : 0.8,
              opacity: 1 
            }}
            exit={{ opacity: 0 }}
            transition={{ duration: 4, ease: "easeInOut" }}
            className="absolute w-32 h-32 bg-white/30 rounded-full blur-xl"
          />
        </AnimatePresence>
        <motion.div 
          animate={{ scale: isActive ? [1, 1.1, 1] : 1 }}
          transition={{ repeat: Infinity, duration: 2 }}
          className="z-10 text-2xl font-bold tracking-tight"
        >
          {isActive ? phase : "Começar"}
        </motion.div>
      </div>
      <button 
        onClick={() => setIsActive(!isActive)}
        className="mt-8 px-8 py-3 bg-white text-brand-sage rounded-full font-bold hover:bg-brand-warm transition-all shadow-lg active:scale-95"
      >
        {isActive ? "Parar" : "Iniciar Exercício"}
      </button>
      <p className="mt-6 text-sm font-medium opacity-90">Técnica 4-4-4 para acalmar o sistema nervoso.</p>
    </Card>
  );
};

export default function App() {
  return (
    <div className="min-h-screen">
      {/* Navigation */}
      <nav className="fixed top-0 w-full z-50 bg-brand-cream/80 backdrop-blur-md border-b border-brand-dark/5">
        <div className="max-w-7xl mx-auto px-6 h-16 flex items-center justify-between">
          <div className="flex items-center gap-2">
            <Heart className="text-brand-sage fill-brand-sage" size={24} />
            <span className="font-serif font-bold text-lg tracking-tight">Apoio PCP</span>
          </div>
          <div className="hidden md:flex items-center gap-8 text-sm font-medium opacity-70">
            <a href="#o-que-e" className="hover:opacity-100 transition-opacity">O que é?</a>
            <a href="#principios" className="hover:opacity-100 transition-opacity">Princípios</a>
            <a href="#vulneraveis" className="hover:opacity-100 transition-opacity">Grupos</a>
            <a href="#faq" className="hover:opacity-100 transition-opacity">Dúvidas</a>
            <a href="#referencias" className="hover:opacity-100 transition-opacity">Referências</a>
            <a href="#contatos" className="bg-brand-dark text-white px-4 py-2 rounded-full hover:bg-brand-sage transition-colors">Emergência</a>
          </div>
        </div>
      </nav>

      {/* Hero Section */}
      <Section className="pt-32 pb-20 text-center">
        <motion.div
          initial={{ opacity: 0, y: 20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.8 }}
        >
          <span className="text-xs uppercase tracking-[0.2em] font-semibold text-brand-sage mb-4 block">
            Primeiros Cuidados Psicológicos
          </span>
          <h1 className="text-5xl md:text-7xl mb-6 leading-[1.1]">
            Presença que <span className="italic">acolhe</span>,<br />
            escuta que <span className="italic text-brand-sage">cura</span>.
          </h1>
          <p className="max-w-2xl mx-auto text-lg opacity-70 mb-10">
            PCP não é terapia. É uma resposta humana e prática para apoiar pessoas em sofrimento agudo após um evento crítico.
          </p>
          <div className="flex flex-wrap justify-center gap-4">
            <a href="#principios" className="px-8 py-4 bg-brand-dark text-white rounded-full font-medium flex items-center gap-2 hover:bg-brand-sage transition-all">
              Aprender os Princípios <ArrowRight size={18} />
            </a>
            <a href="#o-que-e" className="px-8 py-4 border border-brand-dark/20 rounded-full font-medium hover:bg-brand-warm transition-all">
              Saiba mais
            </a>
          </div>
        </motion.div>
      </Section>

      {/* What is PFA */}
      <Section id="o-que-e" className="bg-brand-warm/30 rounded-[3rem]">
        <div className="grid md:grid-cols-2 gap-12 items-center">
          <div>
            <h2 className="text-4xl mb-6">O que são os Primeiros Cuidados Psicológicos?</h2>
            <p className="text-lg opacity-80 mb-6">
              Os Primeiros Cuidados Psicológicos (PCP) descrevem uma resposta humana, de apoio, a um ser humano que está sofrendo e que pode precisar de ajuda.
            </p>
            <ul className="space-y-4">
              {[
                "Oferecer ajuda e apoio prático, de forma não invasiva.",
                "Avaliar as necessidades e preocupações.",
                "Ajudar as pessoas a atenderem às necessidades básicas (comida, água, informação).",
                "Ouvir as pessoas, mas não pressioná-las a falar.",
                "Confortar as pessoas e ajudá-las a se sentirem calmas."
              ].map((item, i) => (
                <li key={i} className="flex items-start gap-3">
                  <CheckCircle2 className="text-brand-sage shrink-0 mt-1" size={20} />
                  <span>{item}</span>
                </li>
              ))}
            </ul>
          </div>
          <div className="grid gap-6">
            <Card variant="solid">
              <ShieldAlert className="text-brand-sage mb-4" size={32} />
              <h3 className="text-xl mb-2 font-serif italic">O que NÃO é PCP</h3>
              <p className="text-sm text-brand-dark/70 leading-relaxed">
                Não é algo que apenas profissionais fazem. Não é aconselhamento profissional. Não é "debriefing" psicológico (pedir para detalhar o trauma).
              </p>
            </Card>
            <Card variant="none" className="bg-brand-sage text-white shadow-lg">
              <Info className="mb-4 text-brand-warm" size={32} />
              <h3 className="text-xl mb-2 font-serif italic">Quem precisa?</h3>
              <p className="text-sm opacity-90 leading-relaxed">
                Pessoas muito angustiadas que foram expostas recentemente a um evento crítico grave. Nem todos que passam por uma crise precisam ou querem PCP.
              </p>
            </Card>
          </div>
        </div>
      </Section>

      {/* The 3 Principles */}
      <Section id="principios">
        <div className="text-center mb-16">
          <h2 className="text-4xl mb-4">Os Três Princípios de Ação</h2>
          <p className="opacity-60">O framework fundamental: Ver, Ouvir e Conectar.</p>
        </div>
        
        <div className="grid md:grid-cols-3 gap-8">
          {/* VER */}
          <motion.div whileHover={{ y: -10 }} className="relative">
            <Card className="h-full border-t-4 border-t-brand-sage">
              <span className="step-number">01</span>
              <div className="w-12 h-12 bg-brand-sage/10 rounded-2xl flex items-center justify-center mb-6">
                <Eye className="text-brand-sage" size={24} />
              </div>
              <h3 className="text-2xl mb-4">Ver (Look)</h3>
              <p className="text-sm opacity-70 leading-relaxed">
                Verifique a segurança. Verifique se há pessoas com necessidades básicas urgentes. Verifique se há pessoas com reações de angústia grave.
              </p>
              <ul className="mt-6 space-y-2 text-xs font-medium opacity-60 uppercase tracking-wider">
                <li>• Segurança do local</li>
                <li>• Ferimentos visíveis</li>
                <li>• Estado de choque</li>
              </ul>
            </Card>
          </motion.div>

          {/* OUVIR */}
          <motion.div whileHover={{ y: -10 }} className="relative">
            <Card className="h-full border-t-4 border-t-brand-clay">
              <span className="step-number">02</span>
              <div className="w-12 h-12 bg-brand-clay/10 rounded-2xl flex items-center justify-center mb-6">
                <Ear className="text-brand-clay" size={24} />
              </div>
              <h3 className="text-2xl mb-4">Ouvir (Listen)</h3>
              <p className="text-sm opacity-70 leading-relaxed">
                Aproxime-se das pessoas que podem precisar de apoio. Pergunte sobre as necessidades e preocupações das pessoas. Ouça e ajude-as a se acalmarem.
              </p>
              <ul className="mt-6 space-y-2 text-xs font-medium opacity-60 uppercase tracking-wider">
                <li>• Escuta Ativa</li>
                <li>• Validar sentimentos</li>
                <li>• Respeitar o silêncio</li>
              </ul>
            </Card>
          </motion.div>

          {/* CONECTAR */}
          <motion.div whileHover={{ y: -10 }} className="relative">
            <Card className="h-full border-t-4 border-t-brand-dark">
              <span className="step-number">03</span>
              <div className="w-12 h-12 bg-brand-dark/10 rounded-2xl flex items-center justify-center mb-6">
                <LinkIcon className="text-brand-dark" size={24} />
              </div>
              <h3 className="text-2xl mb-4">Conectar (Link)</h3>
              <p className="text-sm opacity-70 leading-relaxed">
                Ajude as pessoas a atenderem às necessidades básicas e a acessarem serviços. Ajude as pessoas a lidarem com os problemas. Forneça informações. Conecte com entes queridos.
              </p>
              <ul className="mt-6 space-y-2 text-xs font-medium opacity-60 uppercase tracking-wider">
                <li>• Informação correta</li>
                <li>• Rede de apoio</li>
                <li>• Serviços sociais</li>
              </ul>
            </Card>
          </motion.div>
        </div>
      </Section>

      {/* Vulnerable Groups */}
      <Section id="vulneraveis" className="bg-brand-dark text-white rounded-[3rem]">
        <div className="text-center mb-16">
          <h2 className="text-4xl mb-4">Grupos Vulneráveis</h2>
          <p className="opacity-60">Pessoas que podem precisar de atenção especial em crises.</p>
        </div>
        <div className="grid md:grid-cols-3 gap-8">
          <div className="space-y-4">
            <div className="w-12 h-12 bg-white/10 rounded-full flex items-center justify-center">
              <Baby size={24} />
            </div>
            <h3 className="text-xl font-serif italic">Crianças e Adolescentes</h3>
            <p className="text-sm opacity-70">Priorize a reunião com cuidadores. Use linguagem simples e honesta. Mantenha-os protegidos de cenas traumáticas.</p>
          </div>
          <div className="space-y-4">
            <div className="w-12 h-12 bg-white/10 rounded-full flex items-center justify-center">
              <UserRound size={24} />
            </div>
            <h3 className="text-xl font-serif italic">Idosos</h3>
            <p className="text-sm opacity-70">Verifique necessidades de medicação e mobilidade. Seja paciente com possíveis desorientações causadas pelo estresse.</p>
          </div>
          <div className="space-y-4">
            <div className="w-12 h-12 bg-white/10 rounded-full flex items-center justify-center">
              <Accessibility size={24} />
            </div>
            <h3 className="text-xl font-serif italic">Pessoas com Deficiência</h3>
            <p className="text-sm opacity-70">Pergunte como pode ajudar antes de agir. Mantenha equipamentos de suporte próximos e garanta acessibilidade.</p>
          </div>
        </div>
      </Section>

      {/* FAQ Section */}
      <Section id="faq">
        <div className="max-w-3xl mx-auto">
          <h2 className="text-4xl mb-12 text-center">Dúvidas Frequentes</h2>
          <div className="space-y-2">
            <AccordionItem 
              question="Preciso ser psicólogo para aplicar o PCP?"
              answer="Não. O PCP foi desenhado para ser aplicado por qualquer pessoa instruída, assim como os primeiros socorros físicos. É uma resposta humana e prática, não uma intervenção clínica."
            />
            <AccordionItem 
              question="E se a pessoa chorar incontrolavelmente?"
              answer="O choro é uma reação natural. Não tente pará-lo com frases como 'não chore'. Ofereça um lenço, água e permaneça ao lado da pessoa, validando sua dor e garantindo que ela está segura agora."
            />
            <AccordionItem 
              question="Quanto tempo dura a aplicação do PCP?"
              answer="Geralmente é uma intervenção de curto prazo, que dura de alguns minutos a algumas horas, focada no momento imediato da crise e na conexão com suportes posteriores."
            />
            <AccordionItem 
              question="O que fazer se eu me sentir sobrecarregado?"
              answer="O autocuidado é fundamental. Se você sentir que não tem condições emocionais no momento, peça para outra pessoa assumir. Após ajudar, reserve um tempo para descansar e processar seus próprios sentimentos."
            />
          </div>
        </div>
      </Section>

      {/* Interactive & Self Care */}
      <Section id="auto-cuidado" className="grid md:grid-cols-2 gap-8">
        <BreathingExercise />
        <Card variant="none" className="bg-brand-warm text-brand-dark flex flex-col justify-center shadow-md">
          <h3 className="text-3xl mb-6 font-serif italic">Cuidar de quem cuida</h3>
          <p className="text-brand-dark/80 mb-8 leading-relaxed">
            Ajudar em situações de crise pode ser exaustivo. Para apoiar os outros de forma eficaz, você precisa estar bem.
          </p>
          <div className="space-y-6">
            <div className="flex items-center gap-4">
              <div className="w-12 h-12 rounded-full bg-white flex items-center justify-center shrink-0 shadow-sm">
                <Wind size={24} className="text-brand-sage" />
              </div>
              <span className="text-sm font-semibold">Reconheça seus limites e peça ajuda se necessário.</span>
            </div>
            <div className="flex items-center gap-4">
              <div className="w-12 h-12 rounded-full bg-white flex items-center justify-center shrink-0 shadow-sm">
                <Heart size={24} className="text-brand-sage" />
              </div>
              <span className="text-sm font-semibold">Mantenha rotinas básicas de sono e alimentação.</span>
            </div>
          </div>
        </Card>
      </Section>

      {/* Professional Contact */}
      <Section id="contato-profissional" className="pt-0">
        <Card variant="solid" className="bg-brand-cream border-brand-sage/20 flex flex-col md:flex-row items-center justify-between gap-8 py-12">
          <div className="text-center md:text-left">
            <h3 className="text-3xl mb-2 font-serif italic">Dúvidas ou Suporte Profissional?</h3>
            <p className="opacity-70">Entre em contato para orientações especializadas ou parcerias.</p>
          </div>
          <div className="flex flex-wrap justify-center gap-6">
            <a 
              href="https://instagram.com/psicomariliadamata" 
              target="_blank" 
              rel="noopener noreferrer"
              className="flex items-center gap-3 px-6 py-3 bg-white rounded-2xl shadow-sm hover:shadow-md transition-all group"
            >
              <div className="w-10 h-10 bg-gradient-to-tr from-yellow-400 via-red-500 to-purple-600 rounded-full flex items-center justify-center text-white">
                <Instagram size={20} />
              </div>
              <span className="font-medium group-hover:text-brand-sage">@psicomariliadamata</span>
            </a>
            <a 
              href="mailto:psicologamariliadamata@gmail.com"
              className="flex items-center gap-3 px-6 py-3 bg-white rounded-2xl shadow-sm hover:shadow-md transition-all group"
            >
              <div className="w-10 h-10 bg-brand-sage rounded-full flex items-center justify-center text-white">
                <Mail size={20} />
              </div>
              <span className="font-medium group-hover:text-brand-sage">psicologamariliadamata@gmail.com</span>
            </a>
          </div>
        </Card>
      </Section>

      {/* References Section */}
      <Section id="referencias" className="bg-brand-warm/20 rounded-[3rem] mt-20">
        <div className="max-w-4xl mx-auto">
          <div className="flex items-center gap-4 mb-10">
            <BookOpen className="text-brand-sage" size={32} />
            <h2 className="text-4xl">Referências e Materiais</h2>
          </div>
          <div className="grid gap-6">
            <div className="p-6 bg-white/50 rounded-2xl border border-brand-dark/5 hover:bg-white transition-colors">
              <h4 className="font-bold mb-2 flex items-center justify-between">
                OMS - Primeiros Cuidados Psicológicos: Guia para trabalhadores de campo
                <ExternalLink size={16} className="opacity-40" />
              </h4>
              <p className="text-sm opacity-70">Organização Mundial da Saúde, Organização Internacional para as Migrações e Visão Mundial Internacional (2011).</p>
            </div>
            <div className="p-6 bg-white/50 rounded-2xl border border-brand-dark/5 hover:bg-white transition-colors">
              <h4 className="font-bold mb-2 flex items-center justify-between">
                IFRC - Psychological First Aid (PFA) Guide
                <ExternalLink size={16} className="opacity-40" />
              </h4>
              <p className="text-sm opacity-70">International Federation of Red Cross and Red Crescent Societies.</p>
            </div>
            <div className="p-6 bg-white/50 rounded-2xl border border-brand-dark/5 hover:bg-white transition-colors">
              <h4 className="font-bold mb-2 flex items-center justify-between">
                Cartilha de Primeiros Cuidados Psicológicos em Desastres
                <ExternalLink size={16} className="opacity-40" />
              </h4>
              <p className="text-sm opacity-70">Conselho Federal de Psicologia (CFP) e órgãos regionais.</p>
            </div>
          </div>
        </div>
      </Section>

      {/* Emergency Contacts */}
      <Section id="contatos" className="text-center">
        <div className="bg-brand-dark rounded-[3rem] py-20 px-8 text-white shadow-2xl">
          <PhoneCall className="mx-auto mb-8 text-brand-sage" size={56} />
          <h2 className="text-4xl md:text-5xl mb-12">Precisa de ajuda agora?</h2>
          <div className="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8 md:gap-12 max-w-6xl mx-auto">
            <div className="flex flex-col items-center">
              <span className="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">188</span>
              <p className="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">CVV (Brasil)</p>
            </div>
            <div className="flex flex-col items-center">
              <span className="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">192</span>
              <p className="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">SAMU</p>
            </div>
            <div className="flex flex-col items-center">
              <span className="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">193</span>
              <p className="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">Bombeiros</p>
            </div>
            <div className="flex flex-col items-center">
              <span className="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">190</span>
              <p className="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">Polícia Militar</p>
            </div>
            <div className="flex flex-col items-center">
              <span className="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">180</span>
              <p className="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">Mulher</p>
            </div>
            <div className="flex flex-col items-center">
              <span className="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">100</span>
              <p className="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">Direitos Humanos</p>
            </div>
            <div className="flex flex-col items-center">
              <span className="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">199</span>
              <p className="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">Defesa Civil</p>
            </div>
            <div className="flex flex-col items-center">
              <span className="text-4xl md:text-5xl font-serif italic text-brand-warm mb-3">197</span>
              <p className="text-xs md:text-sm font-bold uppercase tracking-[0.2em] text-white/90">Polícia Civil</p>
            </div>
          </div>
          <p className="mt-16 text-sm md:text-base opacity-60 max-w-2xl mx-auto leading-relaxed">
            Este site é informativo. Em caso de emergência médica ou risco imediato à vida, entre em contato com as autoridades locais imediatamente.
          </p>
        </div>
      </Section>

      {/* Footer */}
      <footer className="py-12 px-6 border-t border-brand-dark/5 text-center opacity-50 text-xs">
        <div className="max-w-7xl mx-auto flex flex-col md:flex-row items-center justify-between gap-6">
          <p>© {new Date().getFullYear()} Apoio - Primeiros Cuidados Psicológicos.</p>
          <div className="flex items-center gap-6">
            <a href="https://instagram.com/psicomariliadamata" target="_blank" rel="noopener noreferrer" className="hover:text-brand-sage transition-colors">Instagram</a>
            <a href="#referencias" className="hover:text-brand-sage transition-colors">Referências</a>
            <a href="#contatos" className="hover:text-brand-sage transition-colors">Emergência</a>
          </div>
          <p>Conteúdo baseado nos protocolos da OMS e IFRC.</p>
        </div>
      </footer>
    </div>
  );
}
