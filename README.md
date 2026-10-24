<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AlgoCore Technology — Digital Product Studio & Software Agency</title>
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts: Plus Jakarta Sans & Outfit -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;500;600;700;800&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        canvasBg: '#f8fafc',
                        cardBg: '#ffffff',
                        indigoPrimary: '#4f46e5',
                        indigoHover: '#4338ca',
                        violetAccent: '#7c3aed',
                        cyanAccent: '#0891b2',
                        emeraldAccent: '#059669',
                        slateDark: '#0f172a',
                        slateMuted: '#64748b',
                        lightBorder: '#e2e8f0'
                    },
                    fontFamily: {
                        heading: ['Outfit', 'sans-serif'],
                        body: ['Plus Jakarta Sans', 'sans-serif']
                    },
                    boxShadow: {
                        'soft': '0 4px 20px -2px rgba(15, 23, 42, 0.05)',
                        'hover-card': '0 12px 30px -4px rgba(79, 70, 229, 0.12)',
                        'indigo-glow': '0 10px 25px -5px rgba(79, 70, 229, 0.3)'
                    }
                }
            }
        }
    </script>

    <style>
        body {
            background-color: #f8fafc;
            font-family: 'Plus Jakarta Sans', sans-serif;
            color: #0f172a;
            overflow-x: hidden;
        }

        h1, h2, h3, h4, h5, h6, .font-heading {
            font-family: 'Outfit', sans-serif;
        }

        /* Modern Light Glass & Card Styling */
        .light-glass {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(226, 232, 240, 0.8);
        }

        .light-card {
            background: #ffffff;
            border: 1px solid #e2e8f0;
            transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .light-card:hover {
            border-color: #c7d2fe;
            transform: translateY(-3px);
            box-shadow: 0 12px 30px -4px rgba(79, 70, 229, 0.12);
        }

        /* Gradient Text */
        .gradient-text-indigo {
            background: linear-gradient(135deg, #4f46e5 0%, #7c3aed 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .gradient-text-emerald {
            background: linear-gradient(135deg, #059669 0%, #0284c7 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f5f9;
        }
        ::-webkit-scrollbar-thumb {
            background: #cbd5e1;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #94a3b8;
        }

        /* Checkbox Option Style */
        .option-card-checkbox:checked + label {
            border-color: #4f46e5;
            background: #f0fdf4;
            background: linear-gradient(135deg, #eef2ff 0%, #f5f3ff 100%);
            box-shadow: 0 0 0 2px #4f46e5;
        }
        
        .option-card-radio:checked + label {
            border-color: #059669;
            background: #ecfdf5;
            box-shadow: 0 0 0 2px #059669;
        }

        /* Subtle Background Gradient Accents */
        .bg-blob-1 {
            position: absolute;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, rgba(99, 102, 241, 0.08) 0%, rgba(255,255,255,0) 70%);
            top: -150px;
            right: -100px;
            z-index: -1;
            pointer-events: none;
        }

        .bg-blob-2 {
            position: absolute;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(16, 185, 129, 0.06) 0%, rgba(255,255,255,0) 70%);
            top: 35%;
            left: -200px;
            z-index: -1;
            pointer-events: none;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col justify-between selection:bg-indigo-500 selection:text-white">

    <!-- Ambient Subtle Light Blobs -->
    <div class="bg-blob-1"></div>
    <div class="bg-blob-2"></div>

    <!-- Sticky Navigation Bar -->
    <nav class="sticky top-0 z-50 light-glass border-b border-slate-200 px-4 py-3 transition-all duration-300">
        <div class="max-w-5xl mx-auto flex items-center justify-between">
            <a href="#" class="flex items-center space-x-2.5">
                <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-indigo-600 via-violet-600 to-emerald-500 flex items-center justify-center font-heading font-black text-white text-xl shadow-md shadow-indigo-200">
                    AC
                </div>
                <div class="flex flex-col">
                    <span class="font-heading font-extrabold text-lg tracking-tight leading-none text-slate-900">AlgoCore<span class="text-indigo-600">.tech</span></span>
                    <span class="text-[10px] text-slate-500 font-semibold tracking-wider uppercase">Digital Product Studio</span>
                </div>
            </a>

            <!-- Desktop Navigation Links -->
            <div class="hidden md:flex items-center space-x-6 text-sm font-semibold text-slate-600">
                <a href="#services" class="hover:text-indigo-600 transition-colors">Services</a>
                <a href="#work" class="hover:text-indigo-600 transition-colors">Portfolio</a>
                <a href="#estimate" class="hover:text-indigo-600 transition-colors">Estimate Scope</a>
                <a href="#links" class="hover:text-indigo-600 transition-colors">Quick Links</a>
            </div>

            <!-- Header Quick Action Buttons -->
            <div class="flex items-center space-x-2.5">
                <button onclick="copyEmailToClipboard()" class="hidden sm:inline-flex items-center space-x-1.5 text-xs font-semibold px-3 py-2 rounded-xl bg-slate-100 hover:bg-slate-200 text-slate-700 transition-colors border border-slate-200">
                    <i class="fa-regular fa-copy text-indigo-600"></i>
                    <span id="copyEmailText">Copy Email</span>
                </button>
                <a href="#estimate" class="inline-flex items-center space-x-1.5 px-4 py-2 rounded-xl bg-indigo-600 hover:bg-indigo-700 text-white text-xs font-bold shadow-md shadow-indigo-200 transition-all transform hover:-translate-y-0.5">
                    <i class="fa-solid fa-bolt text-yellow-300"></i>
                    <span>Start Project</span>
                </a>
            </div>
        </div>
    </nav>

    <!-- Main Container -->
    <main class="max-w-5xl mx-auto px-4 sm:px-6 pt-6 pb-16 space-y-16">

        <!-- HERO SECTION / IG BIO HEADER -->
        <header class="text-center pt-4 pb-2 relative">
            
            <!-- Availability Badge & Profile -->
            <div class="relative inline-block mb-4">
                <div class="w-24 h-24 sm:w-28 sm:h-28 rounded-3xl p-1 bg-gradient-to-tr from-indigo-500 via-violet-500 to-emerald-400 shadow-xl shadow-indigo-100 mx-auto">
                    <div class="w-full h-full bg-white rounded-[22px] flex flex-col items-center justify-center p-2 relative overflow-hidden border border-slate-100">
                        <i class="fa-solid fa-microchip text-4xl text-indigo-600 mb-1"></i>
                        <span class="text-[10px] font-extrabold tracking-widest text-slate-800 uppercase">ALGOCORE</span>
                    </div>
                </div>
                <!-- Availability Status Badge -->
                <div class="absolute -bottom-2 left-1/2 -translate-x-1/2 bg-white border border-emerald-300 rounded-full px-3 py-0.5 flex items-center space-x-1.5 shadow-sm whitespace-nowrap">
                    <span class="relative flex h-2 w-2">
                      <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
                      <span class="relative inline-flex rounded-full h-2 w-2 bg-emerald-500"></span>
                    </span>
                    <span class="text-[11px] font-bold text-emerald-700">Accepting Q4 Projects</span>
                </div>
            </div>

            <!-- Main Title Headlines -->
            <h1 class="text-3xl sm:text-5xl font-black tracking-tight text-slate-900 mb-3 max-w-3xl mx-auto leading-tight">
                We Build Intelligent Web Apps & MVPs, <span class="gradient-text-indigo">Fast.</span>
            </h1>
            
            <p class="text-base sm:text-lg text-slate-600 max-w-xl mx-auto font-medium leading-relaxed mb-6">
                Turn your product idea into a high-converting digital experience. We create modern web apps, AI integrations, and rapid startup MVPs.
            </p>

            <!-- IG Link-In-Bio Primary Action Buttons -->
            <div class="flex flex-col sm:flex-row items-center justify-center gap-3 max-w-md mx-auto">
                <a href="#estimate" class="w-full sm:w-auto px-6 py-3.5 rounded-xl bg-indigo-600 hover:bg-indigo-700 text-white font-bold shadow-lg shadow-indigo-200 flex items-center justify-center space-x-2 transition-all transform hover:-translate-y-0.5">
                    <i class="fa-solid fa-calculator text-indigo-200"></i>
                    <span>Calculate Project Scope</span>
                </a>
                <a href="mailto:algocoretechnology@gmail.com" class="w-full sm:w-auto px-6 py-3.5 rounded-xl bg-white hover:bg-slate-50 text-slate-800 font-semibold border border-slate-300 shadow-sm flex items-center justify-center space-x-2 transition-all">
                    <i class="fa-regular fa-envelope text-indigo-600"></i>
                    <span>Email Us Direct</span>
                </a>
            </div>

            <!-- Trust Metrics Bar -->
            <div class="grid grid-cols-3 gap-3 max-w-xl mx-auto mt-10 p-3.5 rounded-2xl bg-white border border-slate-200 shadow-soft">
                <div class="text-center p-1">
                    <div class="text-xl sm:text-2xl font-black font-heading text-indigo-600">7-14 Days</div>
                    <div class="text-[11px] sm:text-xs text-slate-500 font-semibold mt-0.5">Average MVP Delivery</div>
                </div>
                <div class="text-center p-1 border-x border-slate-100">
                    <div class="text-xl sm:text-2xl font-black font-heading text-emerald-600">100%</div>
                    <div class="text-[11px] sm:text-xs text-slate-500 font-semibold mt-0.5">Custom Production Code</div>
                </div>
                <div class="text-center p-1">
                    <div class="text-xl sm:text-2xl font-black font-heading text-violet-600">25+</div>
                    <div class="text-[11px] sm:text-xs text-slate-500 font-semibold mt-0.5">Products Launched</div>
                </div>
            </div>
        </header>

        <!-- DIRECT CONTACT & LINK-IN-BIO DIRECTORY -->
        <section id="links" class="scroll-mt-20">
            <div class="text-center mb-5">
                <span class="text-xs font-bold uppercase tracking-widest text-indigo-600">Quick Connect Hub</span>
                <h2 class="text-xl font-extrabold text-slate-900 mt-0.5">One-Tap Direct Links</h2>
            </div>

            <!-- Highlighted Official Contact Email Card -->
            <div class="mb-4 bg-gradient-to-r from-indigo-500 via-purple-600 to-indigo-700 rounded-2xl p-4 sm:p-5 text-white shadow-lg flex flex-col sm:flex-row items-center justify-between gap-4">
                <div class="flex items-center space-x-3 text-center sm:text-left">
                    <div class="w-12 h-12 rounded-xl bg-white/20 backdrop-blur-md flex items-center justify-center text-xl text-white shrink-0">
                        <i class="fa-solid fa-at"></i>
                    </div>
                    <div>
                        <div class="text-xs text-indigo-100 font-medium">Official Company Email</div>
                        <div class="text-base sm:text-lg font-mono font-bold tracking-tight text-white select-all">
                            algocoretechnology@gmail.com
                        </div>
                    </div>
                </div>
                <div class="flex items-center space-x-2 w-full sm:w-auto">
                    <a href="mailto:algocoretechnology@gmail.com" class="flex-1 sm:flex-none px-4 py-2.5 bg-white text-indigo-700 font-bold rounded-xl text-xs hover:bg-slate-100 transition-colors text-center shadow-sm">
                        <i class="fa-solid fa-paper-plane mr-1"></i> Send Mail
                    </a>
                    <button onclick="copyEmailToClipboard()" class="px-3 py-2.5 bg-indigo-900/40 hover:bg-indigo-900/60 text-white font-semibold rounded-xl text-xs transition-colors border border-white/20 whitespace-nowrap">
                        <i class="fa-regular fa-copy mr-1"></i> <span id="copyBtnMsg">Copy</span>
                    </button>
                </div>
            </div>

            <!-- 4 Grid Direct Action Links -->
            <div class="grid grid-cols-2 sm:grid-cols-4 gap-3">
                
                <a href="mailto:algocoretechnology@gmail.com?subject=Project%20Inquiry%20from%20Website" class="light-card p-3.5 rounded-2xl flex items-center space-x-3 hover:border-indigo-400 group">
                    <div class="w-10 h-10 rounded-xl bg-indigo-50 text-indigo-600 flex items-center justify-center text-lg group-hover:bg-indigo-600 group-hover:text-white transition-all">
                        <i class="fa-regular fa-envelope"></i>
                    </div>
                    <div class="text-left overflow-hidden">
                        <div class="text-[11px] text-slate-400 font-semibold">Direct Email</div>
                        <div class="text-xs font-bold text-slate-800 truncate">Email AlgoCore</div>
                    </div>
                </a>

                <a href="https://wa.me/?text=Hi%20AlgoCore%20Technology!%20I%20visited%20your%20website%20and%20want%20to%20discuss%20a%20project." target="_blank" class="light-card p-3.5 rounded-2xl flex items-center space-x-3 hover:border-emerald-400 group">
                    <div class="w-10 h-10 rounded-xl bg-emerald-50 text-emerald-600 flex items-center justify-center text-lg group-hover:bg-emerald-600 group-hover:text-white transition-all">
                        <i class="fa-brands fa-whatsapp"></i>
                    </div>
                    <div class="text-left overflow-hidden">
                        <div class="text-[11px] text-slate-400 font-semibold">Instant Chat</div>
                        <div class="text-xs font-bold text-slate-800 truncate">WhatsApp DM</div>
                    </div>
                </a>

                <button onclick="openBookingModal()" class="light-card p-3.5 rounded-2xl flex items-center space-x-3 hover:border-violet-400 group text-left w-full">
                    <div class="w-10 h-10 rounded-xl bg-violet-50 text-violet-600 flex items-center justify-center text-lg group-hover:bg-violet-600 group-hover:text-white transition-all">
                        <i class="fa-regular fa-calendar-check"></i>
                    </div>
                    <div class="text-left overflow-hidden">
                        <div class="text-[11px] text-slate-400 font-semibold">15-Min Intro</div>
                        <div class="text-xs font-bold text-slate-800 truncate">Book Meeting</div>
                    </div>
                </button>

                <a href="https://instagram.com" target="_blank" class="light-card p-3.5 rounded-2xl flex items-center space-x-3 hover:border-pink-400 group">
                    <div class="w-10 h-10 rounded-xl bg-pink-50 text-pink-600 flex items-center justify-center text-lg group-hover:bg-pink-600 group-hover:text-white transition-all">
                        <i class="fa-brands fa-instagram"></i>
                    </div>
                    <div class="text-left overflow-hidden">
                        <div class="text-[11px] text-slate-400 font-semibold">Social Bio</div>
                        <div class="text-xs font-bold text-slate-800 truncate">Instagram</div>
                    </div>
                </a>

            </div>
        </section>

        <!-- SERVICES SECTION ("What Help We Provide") -->
        <section id="services" class="scroll-mt-20 space-y-6">
            <div class="flex flex-col md:flex-row md:items-end justify-between border-b border-slate-200 pb-4">
                <div>
                    <span class="text-xs font-bold tracking-widest text-indigo-600 uppercase">Core Capabilities</span>
                    <h2 class="text-2xl sm:text-3xl font-extrabold text-slate-900 mt-1">What We Build For You</h2>
                </div>
                <p class="text-sm text-slate-500 max-w-md mt-2 md:mt-0 font-medium">
                    End-to-end engineering and design to convert your vision into market-ready software solutions.
                </p>
            </div>

            <!-- 4 Service Cards -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-5">
                
                <!-- Service 1 -->
                <div class="light-card p-6 rounded-2xl relative overflow-hidden group">
                    <div class="flex items-center justify-between mb-4">
                        <div class="w-12 h-12 rounded-xl bg-indigo-50 border border-indigo-100 text-indigo-600 flex items-center justify-center text-xl">
                            <i class="fa-solid fa-rocket"></i>
                        </div>
                        <span class="text-[11px] font-bold bg-indigo-50 text-indigo-700 border border-indigo-200 px-3 py-1 rounded-full">Full Development</span>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 mb-2 group-hover:text-indigo-600 transition-colors">Full-Stack MVPs & Web Apps</h3>
                    <p class="text-sm text-slate-600 mb-4 leading-relaxed">
                        Custom web applications built with production-grade tech stacks. Authentication, database models, Stripe payments, and scalable backend logic.
                    </p>
                    <ul class="space-y-2 mb-5 text-xs text-slate-700 font-medium">
                        <li class="flex items-center space-x-2">
                            <i class="fa-solid fa-circle-check text-emerald-500 text-sm"></i>
                            <span>React, Next.js & Node.js scalable architecture</span>
                        </li>
                        <li class="flex items-center space-x-2">
                            <i class="fa-solid fa-circle-check text-emerald-500 text-sm"></i>
                            <span>Secure authentication & user management</span>
                        </li>
                        <li class="flex items-center space-x-2">
                            <i class="fa-solid fa-circle-check text-emerald-500 text-sm"></i>
                            <span>Payment gateway & subscriptions setup</span>
                        </li>
                    </ul>
                    <div class="flex flex-wrap gap-1.5 pt-3 border-t border-slate-100">
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">Next.js</span>
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">Node.js</span>
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">PostgreSQL</span>
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">Tailwind</span>
                    </div>
                </div>

                <!-- Service 2 -->
                <div class="light-card p-6 rounded-2xl relative overflow-hidden group">
                    <div class="flex items-center justify-between mb-4">
                        <div class="w-12 h-12 rounded-xl bg-purple-50 border border-purple-100 text-purple-600 flex items-center justify-center text-xl">
                            <i class="fa-solid fa-brain"></i>
                        </div>
                        <span class="text-[11px] font-bold bg-purple-50 text-purple-700 border border-purple-200 px-3 py-1 rounded-full">AI & Automation</span>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 mb-2 group-hover:text-purple-600 transition-colors">AI Integration & Smart Workflows</h3>
                    <p class="text-sm text-slate-600 mb-4 leading-relaxed">
                        Embed custom AI capabilities into your product. OpenAI/Claude pipelines, autonomous customer bots, and custom RAG knowledge bases.
                    </p>
                    <ul class="space-y-2 mb-5 text-xs text-slate-700 font-medium">
                        <li class="flex items-center space-x-2">
                            <i class="fa-solid fa-circle-check text-emerald-500 text-sm"></i>
                            <span>Custom LLM prompt engineering & API integration</span>
                        </li>
                        <li class="flex items-center space-x-2">
                            <i class="fa-solid fa-circle-check text-emerald-500 text-sm"></i>
                            <span>Smart data scrapers & automated workflows</span>
                        </li>
                        <li class="flex items-center space-x-2">
                            <i class="fa-solid fa-circle-check text-emerald-500 text-sm"></i>
                            <span>Vector Database & Chat with PDF capabilities</span>
                        </li>
                    </ul>
                    <div class="flex flex-wrap gap-1.5 pt-3 border-t border-slate-100">
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">OpenAI API</span>
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">Claude SDK</span>
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">Pinecone</span>
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">LangChain</span>
                    </div>
                </div>

                <!-- Service 3 -->
                <div class="light-card p-6 rounded-2xl relative overflow-hidden group">
                    <div class="flex items-center justify-between mb-4">
                        <div class="w-12 h-12 rounded-xl bg-emerald-50 border border-emerald-100 text-emerald-600 flex items-center justify-center text-xl">
                            <i class="fa-solid fa-laptop-code"></i>
                        </div>
                        <span class="text-[11px] font-bold bg-emerald-50 text-emerald-700 border border-emerald-200 px-3 py-1 rounded-full">High Converting</span>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 mb-2 group-hover:text-emerald-600 transition-colors">Landing Pages & Studio UI</h3>
                    <p class="text-sm text-slate-600 mb-4 leading-relaxed">
                        Sleek, lightning-fast landing pages crafted to captivate visitors and convert organic traffic into subscribers and sales.
                    </p>
                    <ul class="space-y-2 mb-5 text-xs text-slate-700 font-medium">
                        <li class="flex items-center space-x-2">
                            <i class="fa-solid fa-circle-check text-emerald-500 text-sm"></i>
                            <span>Clean modern UI with interactive micro-animations</span>
                        </li>
                        <li class="flex items-center space-x-2">
                            <i class="fa-solid fa-circle-check text-emerald-500 text-sm"></i>
                            <span>98+ PageSpeed optimization & mobile responsiveness</span>
                        </li>
                        <li class="flex items-center space-x-2">
                            <i class="fa-solid fa-circle-check text-emerald-500 text-sm"></i>
                            <span>Lead capture forms, calendar booking & analytics</span>
                        </li>
                    </ul>
                    <div class="flex flex-wrap gap-1.5 pt-3 border-t border-slate-100">
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">HTML5 / JS</span>
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">TailwindCSS</span>
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">SEO Optimized</span>
                    </div>
                </div>

                <!-- Service 4 -->
                <div class="light-card p-6 rounded-2xl relative overflow-hidden group">
                    <div class="flex items-center justify-between mb-4">
                        <div class="w-12 h-12 rounded-xl bg-cyan-50 border border-cyan-100 text-cyan-600 flex items-center justify-center text-xl">
                            <i class="fa-solid fa-wand-magic-sparkles"></i>
                        </div>
                        <span class="text-[11px] font-bold bg-cyan-50 text-cyan-700 border border-cyan-200 px-3 py-1 rounded-full">UI/UX & Demos</span>
                    </div>
                    <h3 class="text-xl font-bold text-slate-900 mb-2 group-hover:text-cyan-600 transition-colors">Clickable Prototypes & Pitch Demos</h3>
                    <p class="text-sm text-slate-600 mb-4 leading-relaxed">
                        High-fidelity dynamic prototypes designed to present to angel investors, pitch decks, or pre-launch waitlists.
                    </p>
                    <ul class="space-y-2 mb-5 text-xs text-slate-700 font-medium">
                        <li class="flex items-center space-x-2">
                            <i class="fa-solid fa-circle-check text-emerald-500 text-sm"></i>
                            <span>Realistic mock user data & dynamic UI elements</span>
                        </li>
                        <li class="flex items-center space-x-2">
                            <i class="fa-solid fa-circle-check text-emerald-500 text-sm"></i>
                            <span>Rapid 3 to 5-day turnaround for pitch demos</span>
                        </li>
                        <li class="flex items-center space-x-2">
                            <i class="fa-solid fa-circle-check text-emerald-500 text-sm"></i>
                            <span>Directly upgradable to full production code</span>
                        </li>
                    </ul>
                    <div class="flex flex-wrap gap-1.5 pt-3 border-t border-slate-100">
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">Figma to Code</span>
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">UI Animation</span>
                        <span class="px-2.5 py-1 rounded-lg bg-slate-100 text-[11px] font-semibold text-slate-600">Micro-UX</span>
                    </div>
                </div>

            </div>
        </section>

        <!-- INTERACTIVE PROJECT SCOPE & CALCULATOR FORM -->
        <section id="estimate" class="scroll-mt-20">
            <div class="bg-white p-6 sm:p-8 rounded-3xl border border-slate-200 shadow-xl relative overflow-hidden">
                
                <div class="max-w-2xl mx-auto text-center mb-8">
                    <span class="text-xs font-bold tracking-widest text-indigo-600 uppercase">Interactive Configurator</span>
                    <h2 class="text-2xl sm:text-4xl font-extrabold text-slate-900 mt-1">Project Scope & Quote Calculator</h2>
                    <p class="text-sm text-slate-500 mt-2 font-medium">
                        Configure your project requirements below to calculate an estimated budget and timeline instantly.
                    </p>
                </div>

                <form id="projectForm" onsubmit="handleFormSubmit(event)" class="space-y-8">
                    
                    <!-- STEP 1: Services Needed -->
                    <div>
                        <div class="flex items-center justify-between mb-3">
                            <label class="text-sm font-bold text-slate-900">
                                1. What help do you need? <span class="text-slate-400 font-normal">(Select all that apply)</span>
                            </label>
                            <span class="text-xs font-bold text-indigo-600 bg-indigo-50 px-2.5 py-1 rounded-full border border-indigo-100" id="selectedServicesCount">0 selected</span>
                        </div>

                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                            <div>
                                <input type="checkbox" id="srv-mvp" value="Full MVP App" class="hidden option-card-checkbox" onchange="calculateEstimate()">
                                <label for="srv-mvp" class="flex items-start p-3.5 rounded-2xl bg-white border border-slate-200 cursor-pointer hover:border-indigo-300 transition-all select-none">
                                    <div class="text-indigo-600 text-lg mr-3 mt-0.5"><i class="fa-solid fa-cubes"></i></div>
                                    <div>
                                        <div class="text-sm font-bold text-slate-900">Full Web Application / MVP</div>
                                        <div class="text-xs text-slate-500">Database, Auth, Admin & Stripe</div>
                                    </div>
                                </label>
                            </div>

                            <div>
                                <input type="checkbox" id="srv-ai" value="AI Agent Integration" class="hidden option-card-checkbox" onchange="calculateEstimate()">
                                <label for="srv-ai" class="flex items-start p-3.5 rounded-2xl bg-white border border-slate-200 cursor-pointer hover:border-indigo-300 transition-all select-none">
                                    <div class="text-purple-600 text-lg mr-3 mt-0.5"><i class="fa-solid fa-robot"></i></div>
                                    <div>
                                        <div class="text-sm font-bold text-slate-900">AI / LLM Integration</div>
                                        <div class="text-xs text-slate-500">OpenAI, Claude, RAG, Bot</div>
                                    </div>
                                </label>
                            </div>

                            <div>
                                <input type="checkbox" id="srv-landing" value="Landing Page" class="hidden option-card-checkbox" onchange="calculateEstimate()">
                                <label for="srv-landing" class="flex items-start p-3.5 rounded-2xl bg-white border border-slate-200 cursor-pointer hover:border-indigo-300 transition-all select-none">
                                    <div class="text-emerald-600 text-lg mr-3 mt-0.5"><i class="fa-solid fa-laptop-code"></i></div>
                                    <div>
                                        <div class="text-sm font-bold text-slate-900">High-Converting Website</div>
                                        <div class="text-xs text-slate-500">Sleek, fast, lead-optimized</div>
                                    </div>
                                </label>
                            </div>

                            <div>
                                <input type="checkbox" id="srv-proto" value="Interactive Prototype" class="hidden option-card-checkbox" onchange="calculateEstimate()">
                                <label for="srv-proto" class="flex items-start p-3.5 rounded-2xl bg-white border border-slate-200 cursor-pointer hover:border-indigo-300 transition-all select-none">
                                    <div class="text-cyan-600 text-lg mr-3 mt-0.5"><i class="fa-solid fa-vial"></i></div>
                                    <div>
                                        <div class="text-sm font-bold text-slate-900">Pitch Prototype / Demo</div>
                                        <div class="text-xs text-slate-500">Interactive UI for investors</div>
                                    </div>
                                </label>
                            </div>
                        </div>
                    </div>

                    <!-- STEP 2: Budget Range -->
                    <div>
                        <label class="block text-sm font-bold text-slate-900 mb-3">
                            2. Estimated Budget Range
                        </label>
                        <div class="grid grid-cols-1 sm:grid-cols-3 gap-3">
                            <div>
                                <input type="radio" name="budget" id="b-tier1" value="$500–$1,500" class="hidden option-card-radio" checked onchange="calculateEstimate()">
                                <label for="b-tier1" class="block p-3 text-center rounded-2xl bg-white border border-slate-200 cursor-pointer transition-all select-none">
                                    <div class="text-[11px] text-slate-400 font-bold uppercase mb-0.5">Starter MVP</div>
                                    <div class="text-base font-extrabold text-slate-900">$500 – $1,500</div>
                                </label>
                            </div>
                            <div>
                                <input type="radio" name="budget" id="b-tier2" value="$1,500–$4,000" class="hidden option-card-radio" onchange="calculateEstimate()">
                                <label for="b-tier2" class="block p-3 text-center rounded-2xl bg-white border border-slate-200 cursor-pointer transition-all select-none">
                                    <div class="text-[11px] text-slate-400 font-bold uppercase mb-0.5">Growth SaaS</div>
                                    <div class="text-base font-extrabold text-slate-900">$1,500 – $4,000</div>
                                </label>
                            </div>
                            <div>
                                <input type="radio" name="budget" id="b-tier3" value="$4,000+" class="hidden option-card-radio" onchange="calculateEstimate()">
                                <label for="b-tier3" class="block p-3 text-center rounded-2xl bg-white border border-slate-200 cursor-pointer transition-all select-none">
                                    <div class="text-[11px] text-slate-400 font-bold uppercase mb-0.5">Enterprise Scale</div>
                                    <div class="text-base font-extrabold text-slate-900">$4,000+</div>
                                </label>
                            </div>
                        </div>
                    </div>

                    <!-- STEP 3: Timeline -->
                    <div>
                        <label class="block text-sm font-bold text-slate-900 mb-3">
                            3. Desired Launch Speed
                        </label>
                        <div class="grid grid-cols-3 gap-3">
                            <div>
                                <input type="radio" name="timeline" id="t-urgent" value="Urgent (< 1 Wk)" class="hidden option-card-radio" checked onchange="calculateEstimate()">
                                <label for="t-urgent" class="block p-3 text-center rounded-2xl bg-white border border-slate-200 cursor-pointer transition-all select-none">
                                    <div class="text-xs text-emerald-600 font-bold mb-0.5"><i class="fa-solid fa-bolt"></i> Fast-Track</div>
                                    <div class="text-xs font-extrabold text-slate-800">&lt; 1 Week</div>
                                </label>
                            </div>
                            <div>
                                <input type="radio" name="timeline" id="t-standard" value="2-3 Weeks" class="hidden option-card-radio" onchange="calculateEstimate()">
                                <label for="t-standard" class="block p-3 text-center rounded-2xl bg-white border border-slate-200 cursor-pointer transition-all select-none">
                                    <div class="text-xs text-indigo-600 font-bold mb-0.5"><i class="fa-regular fa-clock"></i> Standard</div>
                                    <div class="text-xs font-extrabold text-slate-800">2 - 3 Weeks</div>
                                </label>
                            </div>
                            <div>
                                <input type="radio" name="timeline" id="t-flexible" value="Flexible" class="hidden option-card-radio" onchange="calculateEstimate()">
                                <label for="t-flexible" class="block p-3 text-center rounded-2xl bg-white border border-slate-200 cursor-pointer transition-all select-none">
                                    <div class="text-xs text-purple-600 font-bold mb-0.5"><i class="fa-regular fa-calendar"></i> Flexible</div>
                                    <div class="text-xs font-extrabold text-slate-800">3+ Weeks</div>
                                </label>
                            </div>
                        </div>
                    </div>

                    <!-- STEP 4: Requirement Details & Contact Info -->
                    <div class="space-y-4 pt-2">
                        <div>
                            <label for="projectDetails" class="block text-sm font-bold text-slate-900 mb-1">
                                4. Describe your project requirements or paste website links
                            </label>
                            <textarea id="projectDetails" rows="3" required placeholder="E.g., I need a full-stack platform where users can log in, upload PDF documents, and summarize them using AI. Send details to my email..." class="w-full bg-slate-50 border border-slate-300 focus:border-indigo-600 rounded-xl p-3 text-sm text-slate-900 placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-indigo-100 transition-all"></textarea>
                        </div>

                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                            <div>
                                <label for="clientName" class="block text-xs font-bold text-slate-700 mb-1">Your Name *</label>
                                <input type="text" id="clientName" required placeholder="Alex Morgan" class="w-full bg-slate-50 border border-slate-300 focus:border-indigo-600 rounded-xl p-3 text-sm text-slate-900 placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-indigo-100 transition-all">
                            </div>

                            <div>
                                <label for="clientEmail" class="block text-xs font-bold text-slate-700 mb-1">Your Email Address *</label>
                                <input type="email" id="clientEmail" required placeholder="alex@company.com" class="w-full bg-slate-50 border border-slate-300 focus:border-indigo-600 rounded-xl p-3 text-sm text-slate-900 placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-indigo-100 transition-all">
                            </div>
                        </div>

                        <div>
                            <label for="clientContact" class="block text-xs font-bold text-slate-700 mb-1">Phone / WhatsApp or Social Handle</label>
                            <input type="text" id="clientContact" placeholder="+1 (555) 234-5678 or @alex_tech" class="w-full bg-slate-50 border border-slate-300 focus:border-indigo-600 rounded-xl p-3 text-sm text-slate-900 placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-indigo-100 transition-all">
                        </div>
                    </div>

                    <!-- CALCULATED SUMMARY & SUBMIT BUTTON BAR -->
                    <div class="bg-slate-900 rounded-2xl p-4 text-white flex flex-col sm:flex-row items-center justify-between gap-4 shadow-xl">
                        <div class="text-left w-full sm:w-auto">
                            <div class="text-xs text-slate-400 font-medium">Calculated Estimate:</div>
                            <div class="text-base sm:text-lg font-bold text-emerald-400 font-heading" id="estimatedQuoteText">Select options above</div>
                        </div>
                        <button type="submit" class="w-full sm:w-auto px-8 py-3.5 bg-gradient-to-r from-indigo-500 via-purple-500 to-emerald-400 hover:from-indigo-600 hover:to-emerald-500 text-white font-extrabold rounded-xl shadow-md flex items-center justify-center space-x-2 transition-all transform hover:scale-[1.02]">
                            <span>Send Requirements</span>
                            <i class="fa-solid fa-paper-plane text-xs"></i>
                        </button>
                    </div>

                </form>
            </div>
        </section>

        <!-- FEATURED PORTFOLIO showcase -->
        <section id="work" class="scroll-mt-20 space-y-6">
            <div class="flex flex-col sm:flex-row sm:items-end justify-between border-b border-slate-200 pb-4">
                <div>
                    <span class="text-xs font-bold tracking-widest text-purple-600 uppercase">Proof of Work</span>
                    <h2 class="text-2xl sm:text-3xl font-extrabold text-slate-900 mt-1">Featured Products Built</h2>
                </div>
                <div class="mt-2 sm:mt-0 flex space-x-2 text-xs">
                    <button onclick="filterPortfolio('all')" class="portfolio-filter-btn px-3 py-1.5 rounded-lg bg-indigo-600 text-white font-bold" data-filter="all">All</button>
                    <button onclick="filterPortfolio('mvp')" class="portfolio-filter-btn px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-600 font-semibold hover:bg-slate-50" data-filter="mvp">MVPs</button>
                    <button onclick="filterPortfolio('ai')" class="portfolio-filter-btn px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-600 font-semibold hover:bg-slate-50" data-filter="ai">AI Tools</button>
                </div>
            </div>

            <!-- Portfolio Grid -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-5" id="portfolioGrid">

                <!-- Card 1 -->
                <div class="portfolio-card light-card rounded-2xl overflow-hidden group flex flex-col justify-between" data-category="mvp">
                    <div>
                        <div class="h-44 bg-slate-100 relative overflow-hidden flex items-center justify-center p-4 border-b border-slate-200">
                            <div class="absolute inset-0 bg-gradient-to-tr from-indigo-500/10 to-purple-500/10"></div>
                            <div class="relative w-full h-full bg-white rounded-xl border border-slate-200 p-2.5 shadow-md flex flex-col justify-between">
                                <div class="flex items-center justify-between border-b border-slate-100 pb-1">
                                    <div class="flex space-x-1">
                                        <div class="w-2 h-2 rounded-full bg-slate-300"></div>
                                        <div class="w-2 h-2 rounded-full bg-slate-300"></div>
                                    </div>
                                    <span class="text-[9px] text-indigo-600 font-mono font-bold">pitchid.app</span>
                                </div>
                                <div class="space-y-1.5 my-1">
                                    <div class="h-2 w-3/4 bg-indigo-100 rounded"></div>
                                    <div class="h-2 w-1/2 bg-purple-100 rounded"></div>
                                </div>
                                <div class="flex justify-end">
                                    <span class="px-2 py-0.5 rounded bg-indigo-600 text-[8px] text-white font-bold">Record Pitch</span>
                                </div>
                            </div>
                        </div>
                        <div class="p-5">
                            <span class="text-[10px] font-bold text-indigo-600 uppercase tracking-wider">Video SaaS MVP</span>
                            <h3 class="text-lg font-bold text-slate-900 mt-0.5 group-hover:text-indigo-600 transition-colors">PitchID — Founder Video Deck</h3>
                            <p class="text-xs text-slate-500 mt-2 leading-relaxed font-medium">
                                Full-stack platform built in 8 days. Enables founders to submit 60-second video elevator pitches to venture investors.
                            </p>
                        </div>
                    </div>
                    <div class="px-5 pb-4 pt-2 flex items-center justify-between text-xs border-t border-slate-100">
                        <span class="text-emerald-600 font-bold"><i class="fa-solid fa-circle-check text-xs mr-1"></i> Live Software</span>
                        <span class="font-mono text-[11px] text-slate-400">8 Days Delivery</span>
                    </div>
                </div>

                <!-- Card 2 -->
                <div class="portfolio-card light-card rounded-2xl overflow-hidden group flex flex-col justify-between" data-category="ai">
                    <div>
                        <div class="h-44 bg-slate-100 relative overflow-hidden flex items-center justify-center p-4 border-b border-slate-200">
                            <div class="absolute inset-0 bg-gradient-to-tr from-purple-500/10 to-emerald-500/10"></div>
                            <div class="relative w-full h-full bg-white rounded-xl border border-slate-200 p-2.5 shadow-md flex flex-col justify-between">
                                <div class="flex items-center justify-between border-b border-slate-100 pb-1">
                                    <div class="flex space-x-1">
                                        <div class="w-2 h-2 rounded-full bg-slate-300"></div>
                                        <div class="w-2 h-2 rounded-full bg-slate-300"></div>
                                    </div>
                                    <span class="text-[9px] text-purple-600 font-mono font-bold">supportbot.ai</span>
                                </div>
                                <div class="flex items-center space-x-2 my-2">
                                    <div class="w-5 h-5 rounded-full bg-purple-100 text-purple-600 flex items-center justify-center text-[10px]"><i class="fa-solid fa-robot"></i></div>
                                    <div class="bg-slate-100 text-[9px] text-slate-700 p-1.5 rounded-lg font-medium">AI Agent answering query...</div>
                                </div>
                                <div class="h-1.5 w-full bg-slate-100 rounded overflow-hidden">
                                    <div class="h-full bg-purple-500 w-3/4"></div>
                                </div>
                            </div>
                        </div>
                        <div class="p-5">
                            <span class="text-[10px] font-bold text-purple-600 uppercase tracking-wider">AI Integration</span>
                            <h3 class="text-lg font-bold text-slate-900 mt-0.5 group-hover:text-purple-600 transition-colors">SupportPilot AI Agent</h3>
                            <p class="text-xs text-slate-500 mt-2 leading-relaxed font-medium">
                                Autonomous Claude-powered customer support bot trained on product documentation, handling over 70% of tickets.
                            </p>
                        </div>
                    </div>
                    <div class="px-5 pb-4 pt-2 flex items-center justify-between text-xs border-t border-slate-100">
                        <span class="text-emerald-600 font-bold"><i class="fa-solid fa-circle-check text-xs mr-1"></i> Active Agent</span>
                        <span class="font-mono text-[11px] text-slate-400">10 Days Delivery</span>
                    </div>
                </div>

                <!-- Card 3 -->
                <div class="portfolio-card light-card rounded-2xl overflow-hidden group flex flex-col justify-between" data-category="mvp">
                    <div>
                        <div class="h-44 bg-slate-100 relative overflow-hidden flex items-center justify-center p-4 border-b border-slate-200">
                            <div class="absolute inset-0 bg-gradient-to-tr from-emerald-500/10 to-cyan-500/10"></div>
                            <div class="relative w-full h-full bg-white rounded-xl border border-slate-200 p-2.5 shadow-md flex flex-col justify-between">
                                <div class="flex items-center justify-between border-b border-slate-100 pb-1">
                                    <div class="flex space-x-1">
                                        <div class="w-2 h-2 rounded-full bg-slate-300"></div>
                                        <div class="w-2 h-2 rounded-full bg-slate-300"></div>
                                    </div>
                                    <span class="text-[9px] text-emerald-600 font-mono font-bold">metricspulse.io</span>
                                </div>
                                <div class="grid grid-cols-2 gap-1.5 my-1">
                                    <div class="bg-slate-50 p-1 rounded border border-slate-200">
                                        <div class="text-[8px] text-slate-400 font-bold">MRR</div>
                                        <div class="text-[10px] font-bold text-emerald-600">$18,400</div>
                                    </div>
                                    <div class="bg-slate-50 p-1 rounded border border-slate-200">
                                        <div class="text-[8px] text-slate-400 font-bold">Users</div>
                                        <div class="text-[10px] font-bold text-indigo-600">890</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="p-5">
                            <span class="text-[10px] font-bold text-emerald-600 uppercase tracking-wider">Analytics Web App</span>
                            <h3 class="text-lg font-bold text-slate-900 mt-0.5 group-hover:text-emerald-600 transition-colors">MetricsPulse Dashboard</h3>
                            <p class="text-xs text-slate-500 mt-2 leading-relaxed font-medium">
                                Live Stripe revenue analytics dashboard built for online micro-SaaS founders with real-time automated reports.
                            </p>
                        </div>
                    </div>
                    <div class="px-5 pb-4 pt-2 flex items-center justify-between text-xs border-t border-slate-100">
                        <span class="text-emerald-600 font-bold"><i class="fa-solid fa-circle-check text-xs mr-1"></i> Production Web App</span>
                        <span class="font-mono text-[11px] text-slate-400">12 Days Delivery</span>
                    </div>
                </div>

            </div>
        </section>

        <!-- TESTIMONIALS SECTION -->
        <section class="bg-white p-6 sm:p-8 rounded-3xl border border-slate-200 text-center relative overflow-hidden shadow-soft">
            <div class="max-w-xl mx-auto space-y-4">
                <div class="flex justify-center space-x-1 text-amber-400 text-sm">
                    <i class="fa-solid fa-star"></i>
                    <i class="fa-solid fa-star"></i>
                    <i class="fa-solid fa-star"></i>
                    <i class="fa-solid fa-star"></i>
                    <i class="fa-solid fa-star"></i>
                </div>
                <p class="text-base sm:text-lg text-slate-800 font-medium italic leading-relaxed">
                    "AlgoCore Technology converted our wireframes into a fully working software application in less than two weeks. Communication was seamless and execution was top notch!"
                </p>
                <div>
                    <div class="text-sm font-bold text-slate-900">David K.</div>
                    <div class="text-xs text-slate-500 font-semibold">Founder @ VentureTech</div>
                </div>
            </div>
        </section>

    </main>

    <!-- FLOATING QUICK EMAIL / CONTACT BUTTON (MOBILE & DESKTOP) -->
    <div class="fixed bottom-5 right-5 z-40">
        <a href="mailto:algocoretechnology@gmail.com" class="px-4 py-3 bg-indigo-600 hover:bg-indigo-700 text-white rounded-full shadow-lg shadow-indigo-300 flex items-center space-x-2 text-xs font-bold transition-all transform hover:scale-105">
            <i class="fa-regular fa-paper-plane text-sm"></i>
            <span>Email Us</span>
        </a>
    </div>

    <!-- FOOTER -->
    <footer class="border-t border-slate-200 bg-white py-10 px-4 text-center">
        <div class="max-w-5xl mx-auto space-y-4">
            <div class="flex items-center justify-center space-x-2.5">
                <div class="w-8 h-8 rounded-lg bg-gradient-to-tr from-indigo-600 to-emerald-500 flex items-center justify-center font-heading font-black text-white text-xs shadow-sm">
                    AC
                </div>
                <span class="font-heading font-extrabold text-slate-900 text-base">AlgoCore Technology</span>
            </div>
            
            <p class="text-xs text-slate-500 max-w-sm mx-auto font-medium">
                High-performance digital product studio specializing in web apps, AI integrations, and rapid startup MVPs.
            </p>

            <div class="text-xs font-mono font-semibold text-slate-700 py-1">
                <a href="mailto:algocoretechnology@gmail.com" class="hover:text-indigo-600 transition-colors">
                    algocoretechnology@gmail.com
                </a>
            </div>

            <div class="flex justify-center space-x-5 text-slate-400 text-sm">
                <a href="mailto:algocoretechnology@gmail.com" class="hover:text-indigo-600 transition-colors" title="Email"><i class="fa-regular fa-envelope"></i></a>
                <a href="https://instagram.com" target="_blank" class="hover:text-pink-600 transition-colors" title="Instagram"><i class="fa-brands fa-instagram"></i></a>
                <a href="https://wa.me/?text=Hi%20AlgoCore" target="_blank" class="hover:text-emerald-600 transition-colors" title="WhatsApp"><i class="fa-brands fa-whatsapp"></i></a>
                <a href="https://github.com" target="_blank" class="hover:text-slate-900 transition-colors" title="GitHub"><i class="fa-brands fa-github"></i></a>
            </div>

            <div class="text-[11px] text-slate-400 font-medium pt-2">
                &copy; <span id="year"></span> AlgoCore Technology. All rights reserved.
            </div>
        </div>
    </footer>

    <!-- MODAL 1: SUBMISSION CONFIRMATION MODAL -->
    <div id="confirmationModal" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-slate-900/60 backdrop-blur-sm hidden">
        <div class="bg-white border border-slate-200 rounded-3xl max-w-md w-full p-6 text-center shadow-2xl relative">
            <button onclick="closeConfirmationModal()" class="absolute top-4 right-4 text-slate-400 hover:text-slate-700">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>

            <div class="w-16 h-16 rounded-full bg-emerald-100 text-emerald-600 flex items-center justify-center text-3xl mx-auto mb-4">
                <i class="fa-solid fa-circle-check"></i>
            </div>

            <h3 class="text-2xl font-bold text-slate-900 mb-1">Requirement Logged!</h3>
            <p class="text-xs text-slate-600 mb-6 font-medium">
                Thank you, <span id="modalClientName" class="font-bold text-slate-900"></span>. We have saved your project scope and sent a copy to <span class="font-semibold text-indigo-600">algocoretechnology@gmail.com</span>.
            </p>

            <!-- Summary Receipt -->
            <div class="bg-slate-50 rounded-2xl p-4 text-left border border-slate-200 space-y-2 mb-6 font-mono text-xs">
                <div class="flex justify-between border-b border-slate-200 pb-2">
                    <span class="text-slate-400">Ref ID:</span>
                    <span class="text-slate-700 font-bold" id="modalRef">#AC-9823</span>
                </div>
                <div class="flex justify-between">
                    <span class="text-slate-400">Services:</span>
                    <span class="text-slate-800 font-sans font-semibold text-right max-w-[180px] truncate" id="modalServices">MVP Dev</span>
                </div>
                <div class="flex justify-between">
                    <span class="text-slate-400">Est. Budget:</span>
                    <span class="text-emerald-600 font-bold" id="modalBudget">$1,500 - $4,000</span>
                </div>
                <div class="flex justify-between">
                    <span class="text-slate-400">Timeline:</span>
                    <span class="text-indigo-600 font-bold" id="modalTimeline">Fast-Track (&lt; 1 wk)</span>
                </div>
            </div>

            <div class="space-y-2">
                <a id="modalMailtoLink" href="#" class="w-full py-3 bg-indigo-600 hover:bg-indigo-700 text-white font-bold rounded-xl flex items-center justify-center space-x-2 text-xs transition-colors shadow-md">
                    <i class="fa-solid fa-envelope text-sm"></i>
                    <span>Open Email App to Send Directly</span>
                </a>
                <button onclick="closeConfirmationModal()" class="w-full py-2.5 bg-slate-100 text-slate-700 text-xs font-semibold rounded-xl hover:bg-slate-200">
                    Close Window
                </button>
            </div>
        </div>
    </div>

    <!-- MODAL 2: BOOKING CALL SIMULATION MODAL -->
    <div id="bookingModal" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-slate-900/60 backdrop-blur-sm hidden">
        <div class="bg-white border border-slate-200 rounded-3xl max-w-md w-full p-6 text-center shadow-2xl relative">
            <button onclick="closeBookingModal()" class="absolute top-4 right-4 text-slate-400 hover:text-slate-700">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>

            <div class="w-12 h-12 rounded-2xl bg-indigo-50 text-indigo-600 flex items-center justify-center text-2xl mx-auto mb-3">
                <i class="fa-regular fa-calendar-days"></i>
            </div>

            <h3 class="text-xl font-bold text-slate-900 mb-1">Book 15-Min Intro Call</h3>
            <p class="text-xs text-slate-500 mb-4 font-medium">Select a slot to speak with the AlgoCore team.</p>

            <div class="space-y-3 text-left">
                <div>
                    <label class="block text-xs font-bold text-slate-700 mb-1">Select Date</label>
                    <input type="date" class="w-full bg-slate-50 border border-slate-300 rounded-xl p-2.5 text-xs text-slate-900 focus:outline-none focus:border-indigo-600">
                </div>
                <div>
                    <label class="block text-xs font-bold text-slate-700 mb-1">Select Time Slot</label>
                    <select class="w-full bg-slate-50 border border-slate-300 rounded-xl p-2.5 text-xs text-slate-900 focus:outline-none focus:border-indigo-600">
                        <option>10:00 AM EST (Available)</option>
                        <option>02:30 PM EST (Available)</option>
                        <option>05:00 PM EST (Available)</option>
                    </select>
                </div>
            </div>

            <button onclick="confirmBooking()" class="w-full mt-5 py-3 bg-indigo-600 hover:bg-indigo-700 text-white font-bold rounded-xl text-xs transition-colors shadow-md">
                Confirm Slot Reservation
            </button>
        </div>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        const OFFICIAL_EMAIL = "algocoretechnology@gmail.com";

        // Set dynamic year in footer
        document.getElementById('year').textContent = new Date().getFullYear();

        // Copy Email to Clipboard Function
        function copyEmailToClipboard() {
            // Using standard clipboard copy exec
            const tempInput = document.createElement('input');
            tempInput.value = OFFICIAL_EMAIL;
            document.body.appendChild(tempInput);
            tempInput.select();
            document.execCommand('copy');
            document.body.removeChild(tempInput);

            // UI Feedback
            const copyTextNav = document.getElementById('copyEmailText');
            const copyBtnMsg = document.getElementById('copyBtnMsg');
            
            if (copyTextNav) copyTextNav.textContent = "Copied!";
            if (copyBtnMsg) copyBtnMsg.textContent = "Copied!";

            setTimeout(() => {
                if (copyTextNav) copyTextNav.textContent = "Copy Email";
                if (copyBtnMsg) copyBtnMsg.textContent = "Copy";
            }, 2500);
        }

        // Calculate Project Estimate dynamically
        function calculateEstimate() {
            const checkboxes = document.querySelectorAll('.option-card-checkbox:checked');
            const selectedCount = checkboxes.length;
            
            document.getElementById('selectedServicesCount').textContent = `${selectedCount} selected`;

            const budgetRadio = document.querySelector('input[name="budget"]:checked');
            const timelineRadio = document.querySelector('input[name="timeline"]:checked');

            const budgetVal = budgetRadio ? budgetRadio.value : '$500–$1,500';
            const timelineVal = timelineRadio ? timelineRadio.value : '2-3 Weeks';

            const summaryText = document.getElementById('estimatedQuoteText');

            if (selectedCount === 0) {
                summaryText.textContent = `Select services above • ${budgetVal}`;
            } else {
                summaryText.textContent = `${selectedCount} Service(s) • Est ${budgetVal} (${timelineVal})`;
            }
        }

        // Handle Form Submission
        function handleFormSubmit(event) {
            event.preventDefault();

            const name = document.getElementById('clientName').value;
            const email = document.getElementById('clientEmail').value;
            const contact = document.getElementById('clientContact').value;
            const details = document.getElementById('projectDetails').value;

            // Get selected services
            const selectedServices = [];
            document.querySelectorAll('.option-card-checkbox:checked').forEach(cb => {
                selectedServices.push(cb.value);
            });

            const budget = document.querySelector('input[name="budget"]:checked').value;
            const timeline = document.querySelector('input[name="timeline"]:checked').value;

            // Generate unique lead ID
            const leadId = 'AC-' + Math.floor(1000 + Math.random() * 9000);

            // Populate Modal
            document.getElementById('modalClientName').textContent = name;
            document.getElementById('modalRef').textContent = `#${leadId}`;
            document.getElementById('modalServices').textContent = selectedServices.length > 0 ? selectedServices.join(', ') : 'General Custom App';
            document.getElementById('modalBudget').textContent = budget;
            document.getElementById('modalTimeline').textContent = timeline;

            // Prepare pre-filled mailto URL for direct client mailing
            const emailSubject = encodeURIComponent(`Project Inquiry [${leadId}] - ${name}`);
            const emailBody = encodeURIComponent(
                `Hello AlgoCore Technology,\n\nI filled out your website configurator with the following project requirements:\n\n` +
                `- Name: ${name}\n` +
                `- Client Email: ${email}\n` +
                `- Phone/Social: ${contact}\n` +
                `- Selected Services: ${selectedServices.join(', ')}\n` +
                `- Budget Range: ${budget}\n` +
                `- Timeline: ${timeline}\n\n` +
                `Project Brief:\n${details}\n\n` +
                `Looking forward to hearing from you!`
            );

            document.getElementById('modalMailtoLink').href = `mailto:${OFFICIAL_EMAIL}?subject=${emailSubject}&body=${emailBody}`;

            // Show Confirmation Modal
            document.getElementById('confirmationModal').classList.remove('hidden');
        }

        function closeConfirmationModal() {
            document.getElementById('confirmationModal').classList.add('hidden');
            document.getElementById('projectForm').reset();
            calculateEstimate();
        }

        // Booking Modal Logic
        function openBookingModal() {
            document.getElementById('bookingModal').classList.remove('hidden');
        }

        function closeBookingModal() {
            document.getElementById('bookingModal').classList.add('hidden');
        }

        function confirmBooking() {
            alert('Slot Reserved! We will send a calendar invite to your email shortly.');
            closeBookingModal();
        }

        // Portfolio Filter Logic
        function filterPortfolio(category) {
            const cards = document.querySelectorAll('.portfolio-card');
            const buttons = document.querySelectorAll('.portfolio-filter-btn');

            buttons.forEach(btn => {
                if (btn.getAttribute('data-filter') === category) {
                    btn.className = 'portfolio-filter-btn px-3 py-1.5 rounded-lg bg-indigo-600 text-white font-bold';
                } else {
                    btn.className = 'portfolio-filter-btn px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-600 font-semibold hover:bg-slate-50';
                }
            });

            cards.forEach(card => {
                const cardCat = card.getAttribute('data-category');
                if (category === 'all' || cardCat === category) {
                    card.style.display = 'flex';
                } else {
                    card.style.display = 'none';
                }
            });
        }

        // Initial trigger on page load
        calculateEstimate();
    </script>
</body>
</html>
