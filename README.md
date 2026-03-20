<!DOCTYPE html>

<html class="dark" lang="fr"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
      tailwind.config = {
        darkMode: "class",
        theme: {
          extend: {
            colors: {
              "tertiary": "#75d1ff",
              "on-surface": "#d8e2ff",
              "on-primary-fixed-variant": "#004e5f",
              "background": "#001233",
              "on-tertiary-container": "#004057",
              "surface-tint": "#4cd6fb",
              "error-container": "#93000a",
              "primary-container": "#00b4d8",
              "surface-dim": "#001233",
              "on-tertiary": "#003548",
              "tertiary-fixed-dim": "#75d1ff",
              "on-tertiary-fixed-variant": "#004d67",
              "on-secondary-fixed-variant": "#5900c6",
              "secondary-fixed-dim": "#d2bbff",
              "surface-bright": "#28395b",
              "primary": "#4cd6fb",
              "surface-variant": "#243456",
              "on-primary-fixed": "#001f27",
              "primary-fixed-dim": "#4cd6fb",
              "outline-variant": "#3d494d",
              "secondary": "#d2bbff",
              "on-background": "#d8e2ff",
              "surface-container": "#0d1f40",
              "on-primary": "#003642",
              "on-primary-container": "#00414f",
              "secondary-container": "#6800e4",
              "outline": "#869398",
              "surface-container-highest": "#243456",
              "on-error": "#690005",
              "inverse-primary": "#00677d",
              "on-secondary-fixed": "#25005a",
              "primary-fixed": "#b3ebff",
              "on-secondary": "#3e008e",
              "inverse-surface": "#d8e2ff",
              "surface-container-high": "#18294b",
              "on-tertiary-fixed": "#001e2b",
              "on-error-container": "#ffdad6",
              "surface-container-low": "#081a3b",
              "surface": "#001233",
              "error": "#ffb4ab",
              "on-secondary-container": "#d2bbff",
              "on-surface-variant": "#bcc9ce",
              "inverse-on-surface": "#1f3051",
              "tertiary-fixed": "#c2e8ff",
              "surface-container-lowest": "#000d29",
              "tertiary-container": "#36b1e4",
              "secondary-fixed": "#eaddff"
            },
            fontFamily: {
              "headline": ["Inter"],
              "body": ["Inter"],
              "label": ["Inter"]
            },
            borderRadius: {"DEFAULT": "0.25rem", "lg": "0.5rem", "xl": "0.75rem", "2xl": "1.5rem", "full": "9999px"},
          },
        },
      }
    </script>
<style>
        .material-symbols-outlined {
            font-variation-settings: 'FILL' 0, 'wght' 400, 'GRAD' 0, 'opsz' 24;
        }
        .signature-gradient {
            background: linear-gradient(135deg, #00B4D8 0%, #7B2FF7 100%);
        }
        .ghost-border {
            border: 1px solid rgba(255, 255, 255, 0.07);
        }
        .ia-text { color: #00B4D8; font-weight: 700; }
        .glass-panel {
            background: rgba(13, 31, 64, 0.6);
            backdrop-filter: blur(20px);
        }
    </style>

<style>
    /* Mobile Menu */
    .mobile-menu-overlay {
        display: none;
        position: fixed;
        inset: 0;
        background: rgba(0, 13, 41, 0.95);
        backdrop-filter: blur(20px);
        z-index: 100;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        gap: 2rem;
    }
    .mobile-menu-overlay.active { display: flex; }
    .mobile-menu-overlay a {
        color: #d8e2ff;
        font-size: 1.25rem;
        font-weight: 600;
        text-decoration: none;
        padding: 0.5rem 1rem;
        transition: color 0.2s;
    }
    .mobile-menu-overlay a:hover,
    .mobile-menu-overlay a.active-link { color: #00B4D8; }
    .mobile-menu-close {
        position: absolute;
        top: 1.5rem;
        right: 1.5rem;
        color: white;
        font-size: 2rem;
        background: none;
        border: none;
        cursor: pointer;
    }
    .hamburger-btn {
        display: none;
        background: none;
        border: none;
        cursor: pointer;
        color: white;
        font-size: 1.5rem;
        padding: 0.25rem;
    }
    @media (max-width: 768px) {
        .hamburger-btn { display: flex; align-items: center; }
        .nav-contact-btn { font-size: 0.75rem; padding: 0.4rem 1rem !important; }
        /* Fix hero text sizes for mobile */
        .mobile-hero-fix { font-size: 2.5rem !important; }
        /* Fix padding on mobile */
        .px-12 { padding-left: 1.5rem !important; padding-right: 1.5rem !important; }
        .px-8 { padding-left: 1rem !important; padding-right: 1rem !important; }
        /* Fix footer grid on mobile */
        footer .grid { gap: 2rem !important; padding: 3rem 1.5rem !important; }
    }
    @media (max-width: 480px) {
        .mobile-hero-fix { font-size: 2rem !important; }
    }
</style>
</head>
<body class="bg-surface text-on-surface font-body selection:bg-primary/30">

<!-- Mobile Menu Overlay -->
<div class="mobile-menu-overlay" id="mobileMenu">
    <button class="mobile-menu-close" onclick="document.getElementById('mobileMenu').classList.remove('active')">&times;</button>
    <a href="index.html">Accueil</a>
    <a href="a-propos.html">À propos</a>
    <a href="services.html">Services</a>
    <a href="fonctionnalites.html">Fonctionnalités</a>
    <a href="tarifs.html">Tarifs</a>
    <a href="blog.html">Blog</a>
    <a href="contact.html" class="signature-gradient px-6 py-2 rounded-full font-bold text-white" style="margin-top:1rem">Contact</a>
</div>

<!-- TopNavBar -->
<nav class="fixed top-0 w-full z-50 bg-[#0D1F40] font-['Inter'] antialiased text-sm tracking-wide shadow-2xl shadow-black/20">
<div class="flex justify-between items-center px-8 py-4 max-w-screen-2xl mx-auto">
<div class="text-2xl font-bold tracking-tighter text-white">
                Falconid<span class="ia-text">IA</span>
</div>
<div class="hidden md:flex space-x-8">
<a class="text-slate-300 hover:text-white transition-colors" href="index.html">Accueil</a>
<a class="text-slate-300 hover:text-white transition-colors" href="a-propos.html">À propos</a>
<a class="text-slate-300 hover:text-white transition-colors" href="services.html">Services</a>
<a class="text-[#00B4D8] font-semibold border-b-2 border-[#00B4D8] pb-1" href="fonctionnalites.html">Fonctionnalités</a>
<a class="text-slate-300 hover:text-white transition-colors" href="tarifs.html">Tarifs</a>
<a class="text-slate-300 hover:text-white transition-colors" href="blog.html">Blog</a>
</div>
<button class="hamburger-btn" onclick="document.getElementById('mobileMenu').classList.add('active')"><span class="material-symbols-outlined">menu</span></button>
<a href="contact.html" class="signature-gradient px-6 py-2 rounded-full font-bold text-white transition-transform scale-95 active:scale-90 hover:shadow-[0_0_20px_rgba(123,47,247,0.3)] inline-block">Contact</a>
</div>
</nav>
<main class="pt-24">
<!-- Hero Section -->
<section class="relative overflow-hidden px-8 py-20 lg:py-32">
<div class="max-w-7xl mx-auto relative z-10">
<div class="max-w-4xl">
<h1 class="text-5xl lg:text-7xl font-bold tracking-tighter mb-6 leading-tight">
                        Voir plus loin.<br/>
                        Décider plus vite.
                    </h1>
<p class="text-xl text-on-surface-variant max-w-2xl mb-10 leading-relaxed">
                        Exploitez la puissance de la Kinetic Intelligence pour transformer des signaux faibles en opportunités business concrètes. Notre <span class="ia-text">IA</span> travaille 24h/24 et 7j/7 pour votre croissance.
                    </p>
<div class="flex flex-wrap gap-4">
<button class="signature-gradient px-8 py-4 rounded-xl font-bold text-white flex items-center gap-2">
                            Démarrer l'analyse
                            <span class="material-symbols-outlined">arrow_forward</span>
</button>
<button class="border-2 border-primary text-primary px-8 py-4 rounded-xl font-bold hover:bg-primary/10 transition-colors">
                            Voir la démo
                        </button>
</div>
</div>
</div>
<!-- Decorative Background Element -->
<div class="absolute top-0 right-0 -translate-y-1/4 translate-x-1/4 w-[800px] h-[800px] bg-secondary/10 rounded-full blur-[120px]"></div>
</section>
<!-- Tech Explanation: Scan, Analyze, Detect, Automate -->
<section class="px-8 py-20 bg-surface-container-low">
<div class="max-w-7xl mx-auto">
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
<!-- Tech Card 1 -->
<div class="glass-panel ghost-border p-8 rounded-2xl group hover:bg-surface-container-highest transition-all duration-300">
<div class="w-12 h-12 rounded-lg bg-primary/10 flex items-center justify-center mb-6">
<span class="material-symbols-outlined text-primary text-3xl">radar</span>
</div>
<h3 class="text-xl font-semibold mb-4 text-white">Scan</h3>
<p class="text-on-surface-variant text-sm leading-relaxed">Exploration exhaustive de milliards de points de données en temps réel pour identifier les vecteurs de croissance.</p>
</div>
<!-- Tech Card 2 -->
<div class="glass-panel ghost-border p-8 rounded-2xl group hover:bg-surface-container-highest transition-all duration-300">
<div class="w-12 h-12 rounded-lg bg-primary/10 flex items-center justify-center mb-6">
<span class="material-symbols-outlined text-primary text-3xl">psychology</span>
</div>
<h3 class="text-xl font-semibold mb-4 text-white">Analyze</h3>
<p class="text-on-surface-variant text-sm leading-relaxed">Modélisation prédictive par notre moteur <span class="ia-text">IA</span> pour filtrer le bruit et ne garder que l'essentiel.</p>
</div>
<!-- Tech Card 3 -->
<div class="glass-panel ghost-border p-8 rounded-2xl group hover:bg-surface-container-highest transition-all duration-300">
<div class="w-12 h-12 rounded-lg bg-primary/10 flex items-center justify-center mb-6">
<span class="material-symbols-outlined text-primary text-3xl">target</span>
</div>
<h3 class="text-xl font-semibold mb-4 text-white">Detect</h3>
<p class="text-on-surface-variant text-sm leading-relaxed">Isolement précis des signaux d'achat et des décideurs clés avant même qu'ils n'expriment leur besoin.</p>
</div>
<!-- Tech Card 4 -->
<div class="glass-panel ghost-border p-8 rounded-2xl group hover:bg-surface-container-highest transition-all duration-300">
<div class="w-12 h-12 rounded-lg bg-primary/10 flex items-center justify-center mb-6">
<span class="material-symbols-outlined text-primary text-3xl">auto_mode</span>
</div>
<h3 class="text-xl font-semibold mb-4 text-white">Automate</h3>
<p class="text-on-surface-variant text-sm leading-relaxed">Exécution autonome des premières étapes de mise en relation pour maximiser votre taux de conversion.</p>
</div>
</div>
</div>
</section>
<!-- 4-Step Flow Visualization -->
<section class="px-8 py-32 overflow-hidden">
<div class="max-w-7xl mx-auto">
<div class="mb-20 text-center">
<h2 class="text-4xl font-bold tracking-tight text-white mb-4">Le Pipeline de l'Intelligence</h2>
<p class="text-on-surface-variant">Un flux continu optimisé pour la performance pure.</p>
</div>
<div class="relative flex flex-col md:flex-row items-center justify-between gap-8">
<!-- Background Flow Line -->
<div class="absolute top-1/2 left-0 w-full h-px signature-gradient opacity-20 hidden md:block"></div>
<!-- Step 1 -->
<div class="relative z-10 w-full md:w-1/4">
<div class="glass-panel ghost-border p-6 rounded-2xl text-center group">
<div class="mb-4 inline-flex items-center justify-center w-16 h-16 rounded-full signature-gradient text-white font-black text-xl shadow-lg shadow-primary/20">01</div>
<h4 class="text-lg font-bold text-white mb-2">Détection du signal</h4>
<div class="text-xs text-on-surface-variant uppercase tracking-widest font-bold mb-4">Input Stage</div>
<div class="h-1 w-full bg-surface-container rounded-full overflow-hidden">
<div class="h-full signature-gradient w-1/4 group-hover:w-full transition-all duration-1000"></div>
</div>
</div>
</div>
<!-- Flow Icon -->
<span class="material-symbols-outlined text-primary rotate-90 md:rotate-0 text-3xl opacity-50">chevron_right</span>
<!-- Step 2 -->
<div class="relative z-10 w-full md:w-1/4">
<div class="glass-panel ghost-border p-6 rounded-2xl text-center group">
<div class="mb-4 inline-flex items-center justify-center w-16 h-16 rounded-full signature-gradient text-white font-black text-xl shadow-lg shadow-primary/20">02</div>
<h4 class="text-lg font-bold text-white mb-2">Analyse du prospect</h4>
<div class="text-xs text-on-surface-variant uppercase tracking-widest font-bold mb-4">Processing</div>
<div class="h-1 w-full bg-surface-container rounded-full overflow-hidden">
<div class="h-full signature-gradient w-1/2 group-hover:w-full transition-all duration-1000"></div>
</div>
</div>
</div>
<!-- Flow Icon -->
<span class="material-symbols-outlined text-primary rotate-90 md:rotate-0 text-3xl opacity-50">chevron_right</span>
<!-- Step 3 -->
<div class="relative z-10 w-full md:w-1/4">
<div class="glass-panel ghost-border p-6 rounded-2xl text-center group">
<div class="mb-4 inline-flex items-center justify-center w-16 h-16 rounded-full signature-gradient text-white font-black text-xl shadow-lg shadow-primary/20">03</div>
<h4 class="text-lg font-bold text-white mb-2">Contact personnalisé</h4>
<div class="text-xs text-on-surface-variant uppercase tracking-widest font-bold mb-4">Engagement</div>
<div class="h-1 w-full bg-surface-container rounded-full overflow-hidden">
<div class="h-full signature-gradient w-3/4 group-hover:w-full transition-all duration-1000"></div>
</div>
</div>
</div>
<!-- Flow Icon -->
<span class="material-symbols-outlined text-primary rotate-90 md:rotate-0 text-3xl opacity-50">chevron_right</span>
<!-- Step 4 -->
<div class="relative z-10 w-full md:w-1/4">
<div class="glass-panel ghost-border p-6 rounded-2xl text-center group">
<div class="mb-4 inline-flex items-center justify-center w-16 h-16 rounded-full signature-gradient text-white font-black text-xl shadow-lg shadow-primary/20">04</div>
<h4 class="text-lg font-bold text-white mb-2">RDV qualifié</h4>
<div class="text-xs text-on-surface-variant uppercase tracking-widest font-bold mb-4">Outcome</div>
<div class="h-1 w-full bg-surface-container rounded-full overflow-hidden">
<div class="h-full signature-gradient w-full"></div>
</div>
</div>
</div>
</div>
</div>
</section>
<!-- Bento Grid Features -->
<section class="px-8 py-20 bg-surface-container-lowest">
<div class="max-w-7xl mx-auto">
<div class="grid grid-cols-1 md:grid-cols-6 grid-rows-2 gap-6 h-auto md:h-[600px]">
<!-- Large Bento Card -->
<div class="md:col-span-3 md:row-span-2 glass-panel ghost-border rounded-2xl p-10 flex flex-col justify-between overflow-hidden relative group">
<div class="relative z-10">
<span class="text-primary font-bold tracking-widest text-xs uppercase mb-4 block">Performance Temps Réel</span>
<h3 class="text-3xl font-bold text-white mb-6">Tableau de bord de Kinetic Intelligence</h3>
<p class="text-on-surface-variant max-w-sm">Visualisez l'impact de l'<span class="ia-text">IA</span> sur votre pipeline commercial avec une précision chirurgicale.</p>
</div>
<div class="mt-8 flex items-end gap-2 h-40">
<div class="flex-1 bg-primary/20 rounded-t-lg group-hover:h-32 transition-all duration-500" style="height: 60%"></div>
<div class="flex-1 bg-primary/40 rounded-t-lg group-hover:h-36 transition-all duration-500" style="height: 40%"></div>
<div class="flex-1 signature-gradient rounded-t-lg group-hover:h-40 transition-all duration-500" style="height: 80%"></div>
<div class="flex-1 bg-primary/30 rounded-t-lg group-hover:h-28 transition-all duration-500" style="height: 50%"></div>
<div class="flex-1 bg-primary/50 rounded-t-lg group-hover:h-36 transition-all duration-500" style="height: 70%"></div>
</div>
<div class="absolute -bottom-20 -right-20 w-64 h-64 bg-primary/5 rounded-full blur-3xl"></div>
</div>
<!-- Medium Bento Card -->
<div class="md:col-span-3 glass-panel ghost-border rounded-2xl p-8 flex items-center gap-8 group">
<div class="flex-1">
<h4 class="text-xl font-bold text-white mb-2">Surveillance 24/7</h4>
<p class="text-sm text-on-surface-variant">Notre <span class="ia-text">IA</span> ne dort jamais. Elle scanne les opportunités pendant que vous dormez.</p>
</div>
<div class="w-32 h-32 relative">
<div class="absolute inset-0 border-4 border-primary/20 rounded-full"></div>
<div class="absolute inset-0 border-4 border-t-primary rounded-full animate-spin" style="animation-duration: 3s"></div>
<div class="absolute inset-0 flex items-center justify-center">
<span class="material-symbols-outlined text-primary text-4xl">bedtime_off</span>
</div>
</div>
</div>
<!-- Small Bento Card 1 -->
<div class="md:col-span-1.5 glass-panel ghost-border rounded-2xl p-6 flex flex-col justify-center items-center text-center group">
<div class="text-4xl font-black text-primary mb-2">+240%</div>
<div class="text-xs font-bold uppercase tracking-tight text-white">Taux d'engagement</div>
</div>
<!-- Small Bento Card 2 -->
<div class="md:col-span-1.5 glass-panel ghost-border rounded-2xl p-6 flex flex-col justify-center items-center text-center group">
<div class="text-4xl font-black text-secondary mb-2">-65%</div>
<div class="text-xs font-bold uppercase tracking-tight text-white">Temps de prospection</div>
</div>
</div>
</div>
</section>
<!-- CTA Section -->
<section class="px-8 py-32">
<div class="max-w-5xl mx-auto glass-panel ghost-border rounded-[2.5rem] p-12 lg:p-20 text-center relative overflow-hidden">
<div class="relative z-10">
<h2 class="text-4xl lg:text-6xl font-bold text-white mb-8 tracking-tighter">
                        Prêt à passer à l'échelle ?
                    </h2>
<p class="text-xl text-on-surface-variant mb-12 max-w-2xl mx-auto">
                        Rejoignez les leaders qui utilisent Falconid<span class="ia-text">IA</span> pour dominer leur marché grâce à la data.
                    </p>
<button class="signature-gradient px-12 py-5 rounded-2xl font-black text-xl text-white shadow-2xl hover:scale-105 transition-transform">
                        Réserver un Diagnostic <span class="ia-text">IA</span>
</button>
</div>
<!-- Ambient glow -->
<div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-full h-full bg-primary/5 blur-3xl rounded-full"></div>
</div>
</section>
</main>
<!-- Footer -->
<footer class="bg-[#060F1E] w-full rounded-t-[24px] mt-20">
<div class="grid grid-cols-1 md:grid-cols-4 gap-12 px-12 py-20 max-w-7xl mx-auto font-['Inter'] text-sm leading-relaxed">
<div class="col-span-1">
<div class="text-xl font-black text-white mb-4">Falconid<span class="ia-text">IA</span></div>
<p class="text-slate-400">© 2024 FalconidIA. Voir plus loin. Décider plus vite. Notre <span class="ia-text">IA</span> travaille pour vous 24h/24, 7j/7.</p>
</div>
<div class="col-span-1">
<h5 class="text-white font-bold mb-6">Produit</h5>
<ul class="space-y-4">
<li><a class="text-slate-400 hover:text-[#4FC3F7] hover:translate-x-1 transition-transform inline-block" href="fonctionnalites.html">Fonctionnalités</a></li>
<li><a class="text-slate-400 hover:text-[#4FC3F7] hover:translate-x-1 transition-transform inline-block" href="tarifs.html">Tarifs</a></li>
<li><a class="text-slate-400 hover:text-[#4FC3F7] hover:translate-x-1 transition-transform inline-block" href="#">Sécurité</a></li>
</ul>
</div>
<div class="col-span-1">
<h5 class="text-white font-bold mb-6">Ressources</h5>
<ul class="space-y-4">
<li><a class="text-slate-400 hover:text-[#4FC3F7] hover:translate-x-1 transition-transform inline-block" href="blog.html">Blog</a></li>
<li><a class="text-slate-400 hover:text-[#4FC3F7] hover:translate-x-1 transition-transform inline-block" href="#">Études de cas</a></li>
<li><a class="text-slate-400 hover:text-[#4FC3F7] hover:translate-x-1 transition-transform inline-block" href="#">Documentation</a></li>
</ul>
</div>
<div class="col-span-1">
<h5 class="text-white font-bold mb-6">Suivez-nous</h5>
<div class="flex gap-4">
<a class="text-slate-400 hover:text-primary transition-colors" href="#"><span class="material-symbols-outlined">share</span> LinkedIn</a>
<a class="text-slate-400 hover:text-primary transition-colors" href="#"><span class="material-symbols-outlined">groups</span> Communauté</a>
</div>
</div>
</div>
</footer>

<script>
// Fonctionnalités page - static content, CMS extensible
</script>
</body></html>